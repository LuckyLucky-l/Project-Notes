# 13.可编程厨房物品ScriptableObject

1.创建一个西红柿并做好视觉逻辑分层

![400a560d194402883b428e82e21fabd9.png](image/400a560d194402883b428e82e21fabd9.png) 

做好预设体的整理

![7cdb3ebf98d637cc808bc416c8519bbc.png](image/7cdb3ebf98d637cc808bc416c8519bbc.png) 

![0d6e144633bdf5fc359bdf32296241d3.png](image/0d6e144633bdf5fc359bdf32296241d3.png)

![a5ab479d82616394d21ca911f15e89c8.png](image/a5ab479d82616394d21ca911f15e89c8.png)

2.除了生成西红柿，想生成其他的怎么办？

一：创建脚本生成各自的文件

![7d43b94a2b1b28d31d9571de94c3f73d.png](image/7d43b94a2b1b28d31d9571de94c3f73d.png)

问题：桌台怎么知道想生成谁（目前是自己拽上去的）

![6495eb5ad3d81bcb1f2199af100d76ee.png](image/6495eb5ad3d81bcb1f2199af100d76ee.png)

![9da587b07b7884d430fcae35fb86cd83.png](image/9da587b07b7884d430fcae35fb86cd83.png)

![fa87fb0f54d649321b205a7f76ce9092.png](image/fa87fb0f54d649321b205a7f76ce9092.png)

```c#
在Unity中，`ScriptableObject` 是一种特殊的类，允许你存储和管理数据，而不需要创建和运行场景中的游戏对象。这里的关键概念是“**无需实例化场景对象**”。
### 传统对象 vs. ScriptableObject
通常在Unity中，你会创建**场景对象**（GameObjects），它们有各种组件（如`Transform`、`Rigidbody`等），并存在于场景中。比如，角色、敌人、道具都是场景对象。这些对象只有在场景中实例化时，才能被管理和操作。

而`ScriptableObject`则不同，它并不依赖于场景中的对象。它可以独立于场景存在，作为一种纯粹的数据容器。你可以把它看作是“游戏数据的配置文件”，比如存储物品属性、技能数据、关卡设定等，而不需要在场景中创建一个可见的对象。

### ScriptableObject的作用
1. **节省内存**：`ScriptableObject`在使用时只会加载一次，并可以被多个场景或对象共享，减少了重复实例化的内存占用。
2. **便于编辑和管理**：通过`CreateAssetMenu`，你可以在Unity编辑器中直接创建这些资产，并且在Inspector面板中轻松编辑。
3. **保持场景独立性**：因为它们不依赖场景对象，`ScriptableObject`可以存储跨场景的数据或全局配置，而不会随着场景的销毁而丢失。

### 举例：
假设你在做一个烹饪游戏，你需要定义各种厨房道具（比如锅、碗、菜刀）。你不需要每次在场景中实例化这些对象，而是可以使用 `ScriptableObject` 来创建一个数据资产文件，保存这些厨房道具的属性（例如图片、预制体等），并且在需要时读取这个数据。这样，数据是独立存储的，与你的场景或游戏对象分离，方便管理。

例如：

```csharp
[CreateAssetMenu(menuName = "Kitchen Object")]
public class KitchenObjectSO : ScriptableObject {
    public Transform prefab;
    public Sprite sprite;
    public string objectName;
}
```

你可以在Unity中右键创建这个资产，然后为它设置各种数据（比如图片、预制体等），而不需要创建实际的物体实例。

### 总结：
`ScriptableObject`是一种优化和简化数据管理的方法，允许你在Unity中存储资产和配置，而无需在场景中创建实际的游戏对象。这使得它非常适合保存跨场景共享的静态数据或配置文件。

二：设置各自的文件

![934b473c64da300d947f315478094199.png](assets/934b473c64da300d947f315478094199.png)

三：改脚本代码，将直接得到预设体的代码改成得到对应的SO文件

![afae3746b122c7022ca89e4c2e1eb683.png](assets/afae3746b122c7022ca89e4c2e1eb683.png)

![c75221a40abd04f0ef1354220b3be632.png](assets/c75221a40abd04f0ef1354220b3be632.png)

四：

![ee952e38d579c49becacf4b2971bc458.png](assets/ee952e38d579c49becacf4b2971bc458.png)

![03df032fb60d51861aca0e81409dc08d.png](assets/03df032fb60d51861aca0e81409dc08d.png)

![4fd7710fbd870ce75c4a133d6ea965f8.png](assets/4fd7710fbd870ce75c4a133d6ea965f8.png)

![fd86d94dda60bd693a37f95362bcb32f.png](assets/fd86d94dda60bd693a37f95362bcb32f.png)

总结：

SO=在面板中可以编辑的一个类
