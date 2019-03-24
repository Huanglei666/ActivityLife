# 实验一ActivityLife                                    
>                                                                               软工（1）班 黄磊 123012016005
## 1.实验内容
验证 Activity 的生命周期

## 2.相关概念
Activity 是一个应用组件，用户可与其提供的屏幕进行交互，以执行拨打电话、拍摄照片、发送电子邮件或查看地图等操作。 
每个 Activity 都会获得一个用于绘制其用户界面的窗口。窗口通常会充满屏幕，但也可小于屏幕并浮动在其他窗口之上。<br>
一个应用通常由多个彼此松散联系的 Activity 组成。 一般会指定应用中的某个 Activity 为“主”Activity，即首次启动
应用时呈现给用户的那个 Activity。 而且每个 Activity 均可启动另一个 Activity，以便执行不同的操作。因为在切换 
Activity 的过程中状态会不断发生变化，因此这些状态便组成了 Activity 的生命周期。<br>
Activity 的生命周期包括：创建onCreate()、暂停onPause()、停止onStop()、恢复onResume()、销毁onResume()。

![Activity 生命周期](https://developer.android.google.cn/images/activity_lifecycle.png)
              
**图1 Activity 生命周期**

## 3.实验关键/核心代码
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.i("MainActivityLife","调用onCreate()");
    }

    @Override
    protected void onStart() {
        super.onStart();
        Log.i("MainActivityLife","调用onStart()");
    }
    @Override
    protected void onResume() {
        super.onResume();
        Log.i("MainActivityLife","调用onResume()");
    }
    @Override
    protected void onPause() {
        super.onPause();
        Log.i("MainActivityLife","调用onPause()");
    }
    @Override
    protected void onStop() {
        super.onStop();
        Log.i("MainActivityLife","调用onStop()");
    }
    @Override
    protected void onDestroy() {
        super.onDestroy();
        Log.i("MainActivityLife","调用onDestroy()");
    }
    
## 4.实验运行截图

![运行截图(1)](https://github.com/Huanglei666/ActivityLife/blob/master/%E5%AE%9E%E9%AA%8C%E4%B8%80%E6%88%AA%E5%9B%BE(1).png)

**图2 实验截图(1)**
                         
![运行截图(2)](https://github.com/Huanglei666/ActivityLife/blob/master/%E5%AE%9E%E9%AA%8C%E4%B8%80%E6%88%AA%E5%9B%BE(2).png)
                          
**图3 实验截图(2)**
