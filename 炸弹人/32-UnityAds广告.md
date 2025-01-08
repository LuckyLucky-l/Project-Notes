# 32.UnityAds广告

1.添加广告播放键和脚本

![27446fa358cadd410c5326467e4fbce4.png](image/27446fa358cadd410c5326467e4fbce4.png)

![11e9509d144eccf063884a86160c93e3.png](image/11e9509d144eccf063884a86160c93e3.png)

2.写逻辑

![160f586bf3d838ae765279da0769cdb7.png](image/160f586bf3d838ae765279da0769cdb7.png)

3.条件编译语句，灰色代表切换到安卓平台时才会被执行

![58bd052e04970253d1cd49e7df28ac6c.png](image/58bd052e04970253d1cd49e7df28ac6c.png)

![f20f0ba075afd87a5d5725d6d371bd5d.png](image/f20f0ba075afd87a5d5725d6d371bd5d.png)

4.按下按钮显示广告

![0a171058a94d1ff0b3adf1bc6e2c6773.png](image/0a171058a94d1ff0b3adf1bc6e2c6773.png)

5.广告初始化

![36a4c4190716235f80bd185477db2298.png](image/36a4c4190716235f80bd185477db2298.png)

测试：广告准备好的时候输出：“广告准备好了”

![17a7daf147b76f5710337faa01e3b0e1.png](image/17a7daf147b76f5710337faa01e3b0e1.png)

5.完成播放完广告的逻辑

![58a0cf52ccaf906c3454a0e2b36a3b5c.png](image/58a0cf52ccaf906c3454a0e2b36a3b5c.png)

小问题：

死亡后，观看广告的按钮不能按

——广告按钮一开始是失活状态，广告就不会准备好，所以就不能播放

————解决方法：删掉广告是否准备好的判断条件

![053d8b0aa664e726fce379f4d3a48cc2.png](image/053d8b0aa664e726fce379f4d3a48cc2.png)

![9fb417efe996da09c45242d81d45bb81.png](image/9fb417efe996da09c45242d81d45bb81.png)

![4366656730e4c693c814c2bbfbf5c359.png](image/4366656730e4c693c814c2bbfbf5c359.png)

6.广告播放完给奖励

![050c29ab7ff81cf1a9ea4fcac0bc785e.png](image/050c29ab7ff81cf1a9ea4fcac0bc785e.png)

由于是在Unity编辑器中，所以现在看不到广告

![a0aa9d6bfe612d7aba99a4ddfc685331.png](image/a0aa9d6bfe612d7aba99a4ddfc685331.png)

小问题：

可以移动但是出错了

![c945ce16243c5baf719f886e2a7a4223.png](image/c945ce16243c5baf719f886e2a7a4223.png)

解决办法：

为玩家添加死亡到Idel状态的切换

![40521ff760cd0f4681e7bf6742b7f38f.png](image/40521ff760cd0f4681e7bf6742b7f38f.png)

![263c9e8e422b922ab1658cf858e44538.png](image/263c9e8e422b922ab1658cf858e44538.png)

7.

![183699e11f7ffdbd46e3299447bd826e.png](image/183699e11f7ffdbd46e3299447bd826e.png)

小补充:

![9f0666364d9ab164c4622fd78b4d3589.png](image/9f0666364d9ab164c4622fd78b4d3589.png)

![c8a1767bc0cf2f8bc954571e024a4e9b.png](image/c8a1767bc0cf2f8bc954571e024a4e9b.png)
