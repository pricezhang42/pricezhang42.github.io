---
layout:     post
title:  Java Swing - English Number Listening Trainer - Notes
date:       2022-08-08 12:00:00
author:     "LPZhang"
catalog: false
header-style: text
tags: 
  - Java
  - Swing
---


Since Swing is a pretty old GUI widget toolkit for Java, I find it's **extremely** hard to use. First of all is the layout, the default layout is almost totally useless. So I use `MigLayout` instead. (But I heard that the development tools by JetBrains such as Pycharm and IntelliJ IDEA are developed on Swing????)

**File Structure:**
```
├─listener
│      ButtonListener.java
│      CheckBoxListener.java
│      MyDocumentListener.java
│      MyTextListener.java
│      NumberPanelListener.java
│      
├─panel
│  │  ControlPanel.java
│  │  SettingPanel.java
│  │  ShowPanel.java
│  │  SpeedPanel.java
│  │  
│  └─panelOfSetting
│          DatePanel.java
│          ExtraNumberPanel.java
│          ExtraPanel.java
│          GeneratedNumPanel.java
│          NumberPanel.java
│          PhonePanel.java
│          TextPanel.java
│          
├─run
│      mainFrame.java
│      
└─util
        ColorUtil.java
        NumberClass.java
        SpeakUtil.java
```

For the speech part of the program, I use Jacob to call Microsotf SAPI built in Windows to synthesize speech. 
```java
import com.jacob.activeX.ActiveXComponent;
import com.jacob.com.Dispatch;
import com.jacob.com.Variant;

public static void speak(String str) {
    try {
        sap.setProperty("Volume", new Variant(100));
        sap.setProperty("Rate", new Variant(0));
        sap.setProperty("SynchronousSpeakTimeout", new Variant(1000000));

        Dispatch.call(sapo, "Speak", new Variant("<speak version=\"1.0\"\n" +
                "xmlns=\"http://www.w3.org/2001/10/synthesis\"\n" +
                "xml:lang=\"en-US\">\n" +
                "<voice xml:lang=\"en-US\" gender=\"female\">\n" +
                str + " </voice>\n" +
                "</speak>"), new Variant(0));

    } catch (Exception e) {
        e.printStackTrace();
    }
}
```

I planned to implement more functions such as **pause** and **resume** buttons, speed control and Franch version. But because Jacob cannot directly operate SAPI, bugs keep coming. So I cut off some additional functions, and I'm planning to realize them in Android app or website in the future.

But at least through this project I learnt a lot of points in front-end development.
**Multi-threading**:
Speech can take a long time. If don't implement by multi-threading, the interface will stand still and we can't do anything during the time. Here we use `SwingWorker`to create new thread of speech process.
```java
public static void createWorkerAndSpeak() {
    sw = new SwingWorker() {

        @Override
        protected Object doInBackground() {
            SpeakUtil.speak();
            return null;
        }

        @Override
        protected void done() {
            System.out.println("finished");
            isFinished = true;
        }
    };
    sw.execute();
}
```
**Debounce**:
Debounce is a very important part of front-end performance optimization, it can be used to reduce the number of page requests. 
When clicking, trigger and disable the button, wait certain time then enable the button.
```java
Timer timer = new Timer();
TimerTask task = new TimerTask(){
    @Override
    public void run() {
        createWorkerAndSpeak();
        ControlPanel.instance.bPlay.setEnabled(true);
    }
};
if (sw != null) {
    ControlPanel.instance.bPlay.setEnabled(false);
    SpeakUtil.stop();
    timer.schedule(task, 1000);  // wait 1000ms
} else {
    createWorkerAndSpeak();
}
```