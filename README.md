# V1.1 #

# 先上个效果图 #

![效果图](https://github.com/manitozhang/CircleProgress/blob/master/circleprogress/src/main/res/drawable/show.png)


This is a CircleProgress Dependency library. I'm a Chinese, my English is not very well. So I'll speak Chinese next.

这是一个圆形进度条依赖库,带波浪效果的,里面的属性都可以自定义.

## 使用方法: ##

添加  

        maven { url 'https://jitpack.io' }
        
        
到你的工程下的build.gradle ---> allprojects ---> repositories 的标签下


添加

    implementation 'com.github.manitozhang:CircleProgress:1.0'

到你的 moudle 下的 dependencies 标签下

配置就已经完成了

## 调用方法: ##

在布局里直接加载这个自定义View
例如:   

      <com.manitozhang.CircleProgress
        android:id="@+id/circleProgress"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />
        
        
## 开启方法: ##
        //获取布局文件里该自定义View的Id:
        CircleProgress circleProgress = findViewById(R.id.circleProgress);
        ---
        调用自定义View里面的方法:
        第一个参数为进度的最大值,第二个参数为到达最大值所需要使用的时间,以毫秒为单位
        circleProgress.setProgress(100,5000);
        
## 对进度的监听: ##

        circleProgress.setOnCircleProgressListener();
        返回的int值即进度
       
       
       
## 高级进阶用法,设置圆形进度条的各个参数: ##

     wavePaint;     //波动画笔
     textPaint;     //百分比字画笔
     circlePaint;   //圆形画笔
     cycle;         //sin曲线的长度：一个周期长度
     waveHeight;    //sin曲线振幅的高度
     progress;      //出事波浪的进度
     waveSpeech;    //当前波浪的速度
     
 ## 改变画笔颜色: ##
 例如:  
 
        //获取需要改变颜色的画笔
        Paint circlePaint = circleProgress.getCirclePaint();
        
        //改变颜色
        circlePaint.setColor(Color.parseColor("#000000"));
        
  其他改变属性的方法亦是如此! 
 
 # 后续会持续进行更新 #
        
        
