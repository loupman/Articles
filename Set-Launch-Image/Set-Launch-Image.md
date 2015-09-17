###缘由
在项目中默认使用的·LaunchScreen.xib·作为启动界面，你可以在上面添加一个·UIImageView· 也可以添加一个启动时也有图片，但是现在iPhone出现了4inch，4.7inch, 5.5inch的不同屏幕，分辨率也不一样，会导致显示的图片效果不行。5.5inch需要3倍图,导致图片被拉升或压缩的变形。
所以可以直接使用一组有不同分辨率的图片，让iPhone自己去适应，选择能达到最佳效果的图。
###如何不使用·LaunchScreen.xib· 就可以使用图片适配手机。需要做如下几步：
  * 准备如下4张不同分辨率的图片，为了适配不同尺寸的手机。
      * 640*960   (命名为：xxx@2x.png - xxx的适配4s的2倍图) 
      * 640*1136  (命名为：xxx-568h@2x.png - xxx的适配5及5s的2倍图)
      * 740*1334 （命名为：xxx-667h@2x.png - xxx的适配6及6s的2倍图）
      * 1242*2208 (命名为：xxx-736h@3x.png - xxx的适配6 plus 及 6s plus的3倍图）
  * 选中项目文件, 选中 “General” -> "App Icons and Launch Images" -> “Launch Images Source”中新建一个ImageAsset为·LaunchImage·。如下图
  ![](https://github.com/loupman/Articles/blob/master/Set-Launch-Image/select-launch-image.jpeg "在General中选择图集")
  * 在项目资源·Images.xcassets· 中新建一个图库命名为‘LaunchImage’ 同时按项目需求选择所需要方向和iOS版本。如下图
  ![](https://github.com/loupman/Articles/blob/master/Set-Launch-Image/new-image-set.png "新建LaunchImage图集")

  * 最重要的一点是：在‘在General中选择图集’ 图片中必须把 "Launch Screen File" 的值置空。
