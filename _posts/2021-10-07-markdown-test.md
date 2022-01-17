---
layout:     post
title: Markdown Test
date:       2021-10-07 12:00:00
author:     "LPZhang"
catalog: false
header-style: text
tags: 
  - test
---

Ramerzhang's Blog
======
Content
---------
# Ramerzhang's Blog
#### Ramerzhang's Blog

欢迎使用 **{小书匠}(xiaoshujiang)编辑器**，您可以通过 `小书匠主按钮>模板` 里的模板管理来改变新建文章的内容。&#x1F605;<br/>

> 引用

###### 超链接
[github](https://github.com/Ramer42/Ramer42.github.io)

###### 图片
![](https://github.com/Ramer42/Ramer42.github.io/blob/master/img/404-bg.jpg?raw=true)

<img src="https://github.com/Ramer42/Ramer42.github.io/blob/master/img/404-bg.jpg?raw=true" width = "100%" align=center />

###### 动图
![](https://github.com/Ramer42/Ramer42.github.io/blob/master/img/shishi.gif?raw=true)

<div  align="center">    
<img src="https://github.com/Ramer42/Ramer42.github.io/blob/master/img/shishi.gif?raw=true" width="50%">
</div>


###### 视频
[![](https://res.cloudinary.com/marcomontalbano/image/upload/v1633664414/video_to_markdown/images/youtube--kMndV7Fy-zw-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

**这是加粗**
*这是斜体*
~~这是划掉~~

- 项目1
  - 子项目1.1
  - 子项目1.2
    - 子项目1.2.1
- 项目2
- 项目3

1. First
2. Second
3. Serve the website (`localhost:4000` by default):

```java
public class OomageTestUtility {
    public static boolean haveNiceHashCodeSpread(List<Oomage> oomages, int M) {
        int[] bucketList = new int[M];
        for (Oomage o : oomages) {
            int bucketNum = (o.hashCode() & 0x7FFFFFFF) % M;
            bucketList[bucketNum] = bucketList[bucketNum] + 1;
        }
        for (int j : bucketList) {
            if ((j < oomages.size() / 50) || (j > oomages.size() / 2.5)) {
                return false;
            }
        }
        return true;
    }
}
```

From the `hashCode` of `ComplexOomage`, we can calculate the hashcode given length of list $N$ and each argument $s$ from the function below:

$${s_1} \times {256^{N - 1}} + {s_2} \times {256^{N - 2}} + {s_3} \times {256^{N - 3}} +  \ldots  \ldots  + {s_{N - 1}} \times {256^0}$$

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=34341360&auto=0&height=66"></iframe><br/>
<audio id="audio" controls="" preload="none">
      <source id="mp3" src="http://music.163.com/song/media/outer/url?id=1382359170.mp3"></audio>

<iframe width="560" height="315" src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
