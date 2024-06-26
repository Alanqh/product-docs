# 物理连接

::: tip **阅读本文预计 10 分钟**
**本文概述了编辑器中物理连接的相关定义及使用方法。**
:::


## 什么是物理连接
> 物理连接可以将两个对象进行约束,使其进行有关联的物理模拟运动.



## 物理连接对象属性

### 连接属性设置

| 属性     | 说明                                                 |
| -------- | ---------------------------------------------------- |
| 约束对象1 | 被约束对象1,当前可约束类型为模型、角色、NPC、载具等具有物理模拟特性的对象,其他对象约束无效. |
| 约束对象2 | 被约束对象2,当前可约束类型为模型、角色、NPC、载具等具有物理模拟特性的对象,其他对象约束无效.  |
| 当前距离 | 自动计算出两个被约束对象的间隔距离 |
| 自动启用 | 在运行时自动启用约束效果 |
| 连接线 | 显示约束对象的连接线 |
| 软连接 | 开启软连接后，约束变为“绳子”的效果 |


### 软连接设置

| 属性   | 说明                   |
| ------ | ---------------------- |
| 最大约束距离 | 设置两个被约束对象可无离的最大间隔距离,当被约束对象当前距离超过设置的最大约束距离时,会自动收缩物理连接，将两个被约束对象拉近. |


## 如何物理连接约束对象

在本地资源库中搜索[物理连接],找到功能对象,拖入到场景中即可完成创建.

![](https://cdn.233xyx.com/online/jAicpYIRYxqs1709269580817.png)

通过属性面板绑定想要被约束的对象,完成约束。

![](https://cdn.233xyx.com/online/gorIZftGvWc01709269589773.png)


普通连接效果
<video controls src="https://cdn.233xyx.com/athena/online/fdef770208c4414aaf53ebaa7e7b2446.mp4"></video>

软连接效果
<video controls src="https://cdn.233xyx.com/athena/online/9767e43b2bad4a76b590355bfd43d11e.mp4"></video>


### 绞盘设置

| 属性   | 说明                         |
| ------ | ---------------------------- |
| 启用绞盘 | 开启软连接后可以启用绞盘功能. |
| 绞盘力 | 设置绞盘的拉力,拉动目标质量越大,所需要的拉力越大. |
| 绞盘速度 | 设置绞盘运动速度(cm/s) |
| 绞盘目标距离 | 设置绞盘运动的目标距离,当被约束的两个对象间隔距离达到绞盘目标时,停止绞盘运动. |



## 绞盘使用方法

1.在空中放置一个方块,做为固定约束点.在下方放置一个球，并开启物理模拟，做为可被拉动的约束对象.
2.创建一个物理连接逻辑对象，分别将两个约束对象约束到方块和球模型上.
3.物理连接逻辑对象开启[自动启用],[软连接],[设置最大约束距离].
4.物理连接逻辑对象开启[启用绞盘],设置[绞盘力]和[绞盘速度],同时设置一个[绞盘目标距离]

![](https://cdn.233xyx.com/online/Pdh6wEkldRpq1709514494240.png)

##