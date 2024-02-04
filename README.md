# Pam-s-Food-Crafting-Repices
## Pam's HarvestCraft 2 Mod running on Bukkit Server by using ItemsAdder
## 用ItemsAdder插件在Bukkit服务器上实现类似潘马斯2模组的IA拓展包
## Original source coding by zibuu(User on https://polymart.org/team/zibuu.222)
## 原始代码来自zibbu
## 目前进度：
### 潘马斯2——食物核心包：100%
### 潘马斯2——作物包：100%
### 潘马斯2——果树包：100%
### 潘马斯2——食物扩展包：20%
## 如何完善本项目：
### 1、熟悉基本的Bukkit服务端 
### 2、了解ItemsAdder插件是如何添加与管理合成 
### 3、根据原Mod内或Wiki中的合成表对相关的yaml文件进行编辑
### PS:目前应该只用编辑pam_foodsextended_recipes.yml
## 一些注意事项
### 1、由于ItemsAdder的局限性，目前无法实现矿物辞典功能
### 2、合成里有需要用到重复材料的，就不能用无序合成（需要把shapeless处改为false）
#### 有序合成的例子（代码来自pam_foodsextended_recipes.yml的mcpam）：
    mcpam:
      enabled: true
      pattern:
      - ABC
      - DEF
      - EXX
      ingredients:
        A: pam:skilletitem
        B: pam:onionitem
        C: pam:groundbeefitem
        D: pam:lettuceitem
        E: pam:relishitem
        F: BREAD
      result:
        amount: 1
        item: pam:mcpamitem
      return_item:
        decrement_durability:
          skillet:
              item: pam:skilletitem
              amount: 0
      shapeless: false
  #### 3、若游戏中用到矿物辞典的合成，请务必对应到具体物品
  #### 4、若调用Minecraft的原版物品参与合成，请使用大写（如BREAD）
  #### 例子：
      cantaloupejellysandwich:
      enabled: true
      ingredients:
        A: pam:cuttingboarditem
        B: pam:cantaloupejellyitem
        C: BREAD #原版物品（面包）
        D: pam:chestnutbutteritem
      result:
        amount: 1
        item: pam:cantaloupejellysandwichitem
      return_item:
        decrement_durability:
          roller:
            item: pam:rolleritem
            amount: 0
      shapeless: true
