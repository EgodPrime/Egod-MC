### 2. 创建一个方块：熊猫矿石（不包含在世界上生成）

这一章将会创造一个拥有熊猫贴图的方块，类似于游戏中的岩石方块，泥土方块

你将会增加使用如下工具
```
1. Phtoshop
2. 百度/搜狗
```
首先确定要建立的`.java`文件名为`PandaRock.java`，我把它叫作熊猫岩石。这个类继承了`net.minecraft.block`中的`Block`类，继承，往往是我们
代码简单的源头。
```
public class PandaRock extends Block{
    public PandaRock(){}
}
```
现在它还什么都没有，接下来完善它的构造函数
```
// 为熊猫岩石设置一个静态属性——它的名字，并且会在下面用到
private static final String name = "panda_rock";

public PandaRock() {

  // 使用ROCK类材料的构造函数
  super(Material.ROCK); 
  
  // 将name作为熊猫岩石的注册名
  setRegistryName(name); 
  
  // 将"panda_mod:panda_rock_item"作为 Unlocalized Name
  setUnlocalizedName(INFO.MODID+":"+name+"_item"); 
  
  // 这一步照着做就行
  setCreativeTab(CreativeTabs.BUILDING_BLOCKS); 
  
  // 发光程度(0~1)
  setLightLevel(0.5f); 
  
  // 硬度
  setHardness(1.5f); 
  
  // 对爆炸的抵抗力
  setResistance(10.0f); 
  
  // 设置为只能用开采等级为1的 十字镐 进行挖掘
  setHarvestLevel("pickaxe", 1); 
  
  设置它的声音像 石头 
  setSoundType(SoundType.STONE); // 
}
```



上一章：[1.让一个MOD运行起来的基本框架](../CPT1/CPT-1.md)

下一章：[3.创建一个金属锭：熊猫锭](../CPT3/CPT-3.md)
