README
===========================
封装android开发中常用的Utils。可直接依赖使用，喜欢的话不妨star一下吧。
****
### Author:赵文贇
### E-mail:dev_zwy@aliyun.com
****
## 目录
* [日志输出](#日志输出)
* [引导页集成](#引导页集成)
* [集成该库](#集成该库)


### 日志输出
-----------
- [x] 优雅的日志输出
- [x] 突破系统日志打印长度的限制
- [x] 自动校验Json串输出格式
- [x] 打印异常输出位置（精确到行）
- [x] 日志一目了然  

 使用:
```diff
+ 在application中初始化操作（注意：不初始化直接调用Log输出日志会有空指针异常抛出）：
 
 Log.init(TAG, true);//开启日志打印
  
+ 调用和系统Log调用一样
  private String json = "{\"key_a\":999,\"key_b\":\"这是b的值\"}";
  private String text = "这是一条测试日志";
    Log.d(json);
    Log.e(json);
    Log.w(json);  
    Log.d(text);
    Log.e(text);
    Log.w(text);

```
 输出效果图  
 ![baidu](https://github.com/devzwy/KUtils/raw/master/images/loginfo.png)  
### 引导页集成
-----------
- [x] 引导界面导航效果
- [x] 支持根据服务端返回的数据动态设置广告条的总页数
- [x] 支持大于等于1页时的无限循环自动轮播、手指按下暂停轮播、抬起手指开始轮播
- [x] 支持自定义指示器位置和广告文案位置
- [x] 支持图片指示器和数字指示器
- [x] 支持 ViewPager 各种切换动画
- [x] 支持选中特定页面
- [x] 支持监听 item 点击事件
- [x] 加载网络数据时支持占位图设置，避免出现整个广告条空白的情况
- [x] 多个 ViewPager 跟随滚动



















### 集成该库
-----------
```diff
+ 方式1   预留jcenter仓库方式  
    预留
+ 方式2   clone项目到本地，将kutils库直接依赖到项目。
    compile project(':kutils')
+ 方式3   在项目根目录下新建aars文件夹，将kutils目录build/outputs下的kutils-1.2.0.aar文件copy进aars文件夹  在app的build.gradle 最外层节点加入
    repositories { flatDir { dirs '../aars' } }
         在dependencies节点下加入对aar的依赖
    compile(name: 'kutils-1.2.0', ext: 'aar')
 ```
 ****
 集成过程出现问题可联系本人QQ：3648415(注明来自github)