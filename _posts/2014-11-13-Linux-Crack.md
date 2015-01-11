---
layout: post
title:  "linux小程序"
date:   2014-11-14 19:27:00
categories: jekyll update
---

#linux小程序

**用linux命令解决：**

打开运行程序：

![Alt text](http://ww2.sinaimg.cn/large/e1050ff2tw1emaokgrq1nj20hh09ndgl.jpg)


排序：

![Alt text](http://ww3.sinaimg.cn/large/e1050ff2tw1emaokipv1vj20gs07zaar.jpg)


输出6250行：

![Alt text](http://ww4.sinaimg.cn/large/e1050ff2tw1emaokjmbuij20d301xdfx.jpg)



用Python脚本解决：
注：lin2.txt  是程序运行输出的乱序数字。


    f = open('lin2.txt')
    array =[]
    for linea in f.readlines():
         array.append(linea.strip('\n'))
    
    *print len(array)
    *print array
    
    def bubble_sort(array):
         flag = 1
         tail = len(array)-1
         while(flag):
              flag=0
              for i in range(tail):
                   if array[i]>array[i + 1]:
                        t = array[i]
                        array[i]  = array[i + 1]
                        array[i + 1] = t
                        flag = 1
                        pass
                   pass
              tail-=1
              pass
         return array
        
    bubble_sort(array)
    print array[6250]
    f.close()

