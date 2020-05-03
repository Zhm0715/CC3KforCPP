// Author: ZHM 18011485
// Date: 19/10/22 - 19/10/26
// 本程序需在C++11环境下编译
// 本程序需UTF-8编码
// 设计思路:
    1 采用一个二维字符数组Map[x][y]存储地图上所有点 并用x指代行，用y指代列，定义string Action为英雄每步操作，定义Gold、Enemies数组。
    2 定义Player、Enemies、Door、Gold、Potion类，主要属性有：各个角色的x、y坐标、属性值(Player、Enemies、Potion、Gold).主要函数有：位置变换函数、攻击函数、判定死亡/被使用函数(Player、Enemies、Potion、Gold)。
    3 遍历Enemies数组 对其中每个元素的坐标(x、y)值进行随机的+-1的改变。
    4 读取玩家命令，并根据命令进行更新PC位置、攻击周围目标等操作。
    4 定义map型变量DireList以及结构体DireMap对英雄周围的位置进行遍历，并对Enemies、Potion、Gold进行遍历，判定位置是否与英雄周围位置相等，若相等，则进行对英雄的操作(攻击、更新Action等)。
    5 当角色死亡时设置其坐标为-100，-100 使其不出现在Map上，并在位置变换过程中不对其进行变换。
    6 将所有改变(坐标变化等)读取至Map数组中并刷新屏幕，再将新的Map输出至屏幕上。