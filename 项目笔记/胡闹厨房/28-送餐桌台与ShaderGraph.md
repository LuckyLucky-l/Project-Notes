# 28.送餐桌台与ShaderGraph

![f1e2152674c31f3e1c78aca0c572a00e.png](image/f1e2152674c31f3e1c78aca0c572a00e.png)

1.创建好送餐桌台

![524486218b91c7d5ce0c9072a21079b5.png](image/524486218b91c7d5ce0c9072a21079b5.png)

2.写好脚本，交互的时候把玩家的物品进行销毁，注：要在盘子上

![7ccef593dd35a9ef8822d676bf2b3848.png](image/7ccef593dd35a9ef8822d676bf2b3848.png)

3.**ShaderGraph--着色器**

一：创建一个文件夹专门用来装着色器

![5d0c849462f934fa2fd017654187e6ae.png](image/5d0c849462f934fa2fd017654187e6ae.png)

二：创建一个最基础的着色器

Lit就是会受到光照影响

Unlit不受光照影响

![a3492f4b5a995a2190f72efda494b752.png](image/a3492f4b5a995a2190f72efda494b752.png)

![a8065b87618d167d5de94330b95c6744.png](image/a8065b87618d167d5de94330b95c6744.png)

![48c1db6187ecc75870892b95b9929ff6.png](image/48c1db6187ecc75870892b95b9929ff6.png)

可以右键预览窗口更换显示模型

![deeb3bb7327d2649a6686301eb92204f.png](image/deeb3bb7327d2649a6686301eb92204f.png)

![04da77d09622a6ee4fad9b579c6d695d.png](image/04da77d09622a6ee4fad9b579c6d695d.png)

注意：在Shader里面的换图片不会影响外面编译好的材质球，重新新建一个材质球才会不一样

![4d1aafcf7d7e8a61c4ecf2d58bca1a20.png](image/4d1aafcf7d7e8a61c4ecf2d58bca1a20.png)

![bb0b37c7536656165530bcc5665349c5.png](image/bb0b37c7536656165530bcc5665349c5.png)

为什么还是白茫茫一片？--还没有调颜色通道

![525aee19cc4a132785685f078aa042ea.png](image/525aee19cc4a132785685f078aa042ea.png)

![da50e2f1420a42c3e913ca13ab56166d.png](image/da50e2f1420a42c3e913ca13ab56166d.png)

怎么让图片动起来？--不停的移到UV值就可以了

UV坐标决定了纹理如何贴在模型表面上，通常范围是 `(0,0)` 到 `(1,1)`。通过改变UV坐标（如偏移`U`或`V`的值），可以使纹理在物体表面滑动，从而产生图片移动的效果。

![bec158abea399bcf5cd0c968294f21ec.png](image/bec158abea399bcf5cd0c968294f21ec.png)

---

![e335cbd06d18b2d4a80d7752db21f10b.png](image/e335cbd06d18b2d4a80d7752db21f10b.png)

---

![95e31460597a037fa5d1b5111373064d.png](image/95e31460597a037fa5d1b5111373064d.png)

---

![ccc6d678e82b9ee3b1f3ff892f0261c5.png](image/ccc6d678e82b9ee3b1f3ff892f0261c5.png)

![e12ff18eb5114a5abdeb0b1ece66687d.png](image/e12ff18eb5114a5abdeb0b1ece66687d.png)

---

---

![a652661292484946314a3f23d6821624.png](image/a652661292484946314a3f23d6821624.png)

![95d5b34530ab7cf68df51d53a61cd018.png](image/95d5b34530ab7cf68df51d53a61cd018.png)

注意：加入的图片要是Repeat才行

![31b61abc2a37222433ca0e2bd0e19335.png](image/31b61abc2a37222433ca0e2bd0e19335.png)
