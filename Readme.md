
## 动物背包系统
### 添加动物的时，玩家能够通过选择“是否立即放置”。

该脚本绑定到游戏场景中的物品下：
`public class AddInventory : MonoBehaviour`
给物品注册该物品是哪一类的物品
`public Item thisItem`
玩家背包
`public InventoryBag thisBag`

遍历背包，如果为null的话就设置成该物品，因为我们直接给装备栏添加了18个物品，只是初始化都是null
`if (!thisBag.bagList.Contains(thisItem))`
如果存在该物品，就将数量+1；
`thisItem.itemHeld += 1`
更新背包的数据
`InventoryMannage.RestItem()`

牛、羊物体身上有触发器体，人物身上有碰撞体，当二者发生碰撞时，触发存放物品的事件。若要新增加物体，物体上挂载AddInventory脚本即可，并将碰撞器改为触发器。

***
***
# 备注
## 


