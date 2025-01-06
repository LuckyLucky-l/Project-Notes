# 7.全新InputSystem

首先重构输入代码，将输入代码从PlayerControl剥离出去

![77663ec7bf35ff0c38f67a1005ba45db.png](image/77663ec7bf35ff0c38f67a1005ba45db.png)

![b0c8dfa8fd03ead2abf8bbecf24378a8.png](image/b0c8dfa8fd03ead2abf8bbecf24378a8.png)

![cf2ee72ef68ffaff721e7e78eaee7f04.png](image/cf2ee72ef68ffaff721e7e78eaee7f04.png)

安装新的input

![eb0c91681f08fb380a925f3f22e5e30f.png](image/eb0c91681f08fb380a925f3f22e5e30f.png)

![1efa11666be3b8315baf219108971f37.png](image/1efa11666be3b8315baf219108971f37.png)

![74be81927861a3566915840916b53c99.png](image/74be81927861a3566915840916b53c99.png)

方法一：

![b600a6f272e6739e3623af866f95115d.png](image/b600a6f272e6739e3623af866f95115d.png)

![1bb172a80223c4fa8686df4402134400.png](image/1bb172a80223c4fa8686df4402134400.png)

![382d9c660f1eac6b3a9e06a03c7e9428.png](image/382d9c660f1eac6b3a9e06a03c7e9428.png)

![98176fa2ee817e4db3ea54cd330aa760.png](image/98176fa2ee817e4db3ea54cd330aa760.png)

方法二：创建一个.inputactions文件来定义游戏控制的映射（如按键、触摸、手柄）

![5b7220468ea4a9859a044b242b68fd29.png](image/5b7220468ea4a9859a044b242b68fd29.png)

![737532a910a806db8e9bab9d760b542e.png](image/737532a910a806db8e9bab9d760b542e.png)

![e6b54589ef210865cef715d28306450a.png](image/e6b54589ef210865cef715d28306450a.png)

![4d28e3a46880af2ceb8d462adc2b558a.png](image/4d28e3a46880af2ceb8d462adc2b558a.png)

1. **添加绑定（Add Binding）**：用于添加一个简单的输入绑定。你可以将某个按键或输入设备的操作绑定到一个特定的动作上。
2. **添加正/负绑定（Add Positive/Negative Binding）**：用于添加一个输入绑定，可以处理正负两种输入。例如，处理摇杆的左右移动或按键的按下和释放。
3. **添加一个修饰符的绑定（Add Binding With One Modifier）**：用于添加一个带有一个修饰符的输入绑定。修饰符通常是指需要同时按下的另一个按键，例如Ctrl、Shift或Alt。
4. **添加两个修饰符的绑定（Add Binding With Two Modifiers）**：用于添加一个带有两个修饰符的输入绑定。例如，需要同时按下Ctrl和Shift再按下某个按键才能触发的操作。

1. **绑定（Binding）**：
    - 点击“绑定”旁边的加号（+）按钮，添加一个新的绑定。
    - 选择你想要绑定的输入设备和按键。例如，可以选择键盘上的某个按键或游戏手柄上的按钮。
2. **交互（Interactions）**：
    - 点击“交互”旁边的加号（+）按钮，添加一个交互类型。
    - 交互类型可以是“按下”、“长按”等，这些选项可以帮助你定义输入的具体行为。例如，选择“按下”可以设置按键被按下时触发的动作。
3. **处理器（Processors）**：
    - 点击“处理器”旁边的加号（+）按钮，添加一个处理器。
    - 处理器用于修改输入值，例如，可以添加一个“归一化”处理器来将输入值标准化。

生成一个按键控制的类

![357a91bfb8accacaa80bd868ab9fc855.png](image/357a91bfb8accacaa80bd868ab9fc855.png)

![5449f98897075b558f30f1f031b0c290.png](image/5449f98897075b558f30f1f031b0c290.png)
