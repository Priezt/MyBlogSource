Title: 用AutoHotKey实现星际2操作偷懒
Date: 2013-04-03 15:55
Tags: game, ahk
Category: Game
Slug: starcraft2-shortcut-hack
Author: Priezt
Summary: 用AutoHotKey实现星际2操作偷懒

一直喜欢打RTS，但是手真的是很慢。星际2的虫心刚出不久，马上入手开始玩，说实话这个版本的操作已经很人性化了，（F2可以选中所有部队，这个和C&C的q一样，相当实用）。但还是不能满足我这种慢手，所以用了些小技巧，实现操作上更进一步的偷懒。

# 罗技G600 MMO
![G600 MMO](/blog/static/images/g600.jpg)

这个鼠标是去年打Diablo3时买的，当时女儿很喜欢看我打，还要我抱着，那我只能腾出一只手来打，怎么放技能。所以买了这个神器，真心好用，20个自定义按键。

[官网地址](http://www.logitech.com/zh-tw/product/g600-mmo-gaming-mouse)

# AutoHotKey
这个就不说了，[地球人都知道](http://www.autohotkey.com/)

# 直接上脚本
```
#IfWinActive ahk_class StarCraft II
Numpad4::Send {Control Down}9{Control Up}1sdddddddddd9
Numpad5::Send {Control Down}9{Control Up}1szzzzzzzzzz9
Numpad6::Send {Control Down}9{Control Up}1srrrrrrrrrr9
Numpad8::Send {Control Down}9{Control Up}1shhhhhhhhhh9
NumpadDot::Send {F10}
Numpad2::Send {Control Down}9{Control Up}1sv9
#IfWinActive
```

我把G600的按键都映射到小键盘，因为小键盘从来不用。

然后举例来说这一行
```
Numpad4::Send {Control Down}9{Control Up}1sdddddddddd9
```
这行脚本把一个按键映射成如下一系列操作：
```
{Control Down}9{Control Up}
```
Ctrl-9，把当前选中的对象编队为9
```
1s
```
我用虫族，一般把所有老家编队成1，1s是选中所有老家里的小虫
```
dddddddddd
```
连按10下d，造10个农民
```
9
```
因为刚才编队了最后选中的对象为9，现在再选会那些对象，恢复之前的操作状态

其他的几条也是一样的道理。

通过这些映射，我在控制前线作战的时候，只要按下鼠标上的一个键，就能快速造单位，而且不影响当前的选中状态，非常实用。

如果没有G600这样的神器也没关系，映射成其他的键盘快捷键就行了

# 心得
尽管有了这个小窍门，上BN韩服，还是被棒子草割了......
