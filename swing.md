
# Swing界面编程
   随着Java的发展，AWT已经渐渐被淘汰，它已经不能适应发展的需要，不能满足开发功能强大的用户界面的需要。
   这时Swing出现了，它是建立在AWT之上的组件集，在不同的平台上都能保持组件的界面样式，因此得到了非常广泛的应用
   
# 1.Swing组件库
  常用到的只有javax.swing.*和javax.swing.event.*这两个包;
   1)、JFC结构
       JFC包含了图形用户界面构建中需要用到的顶级容器(Applet、Dialog、Frame)、普通容器(面板、滚动面板、拆分窗格组件、选项卡插U能给个和工具条等)、
       特殊容器(InternalFrame、Layeredpane、root pane)、基本组件(button , combo box , list , menu , slider , spinner和textfild)等  
   2)、与AWT的区别
      最大的区别在于Swing组件的实现与本地实现无关。Swing组件比AWT组件具有更多的功能。
      例如在Swing中添加了按钮组件和标签组件，通过继承来更改Swing组件的行为和外观，访问技术等;
      
# 2.Jfram窗口容器
    它定义了一个UI程序的框架，是图形程序不可缺少的一部分。它与java.awt.Frame类很类似，它是RootPaneContainer的一种，是顶层的Swing容器。
    通过继承jframe，所构建的容器就有一些最基本的组件。例如和关闭按钮相对应的容器有一个setDefaultCloseOperation(int operation)方法，
    这是每个Swing程序都有的，它有四个参数：
       >DO_NOTHING_ON_CLOSE(单击后不管用)
       >HIDE_ON_CLOSE(单击后窗口隐藏)
       >DISPOSE_ON_CLOSE(单击后窗口释放)
       >EXIT_ON_CLOSE(单击后退出)
       
  # 3.通过Icon接口进行图像操作
     Icon接口用于显示图像。在Icon接口中定义了许多方法，这些方法都是图像应用方面必不可少的。
     在Swing组件中支持图像显示。ImageIcon类用来描述图像。创建Icon对象的方法有3种：
       >new ImageIcon(Image i)
       >new ImageIcon(Stringfilename)(参数为图像文件的名称)
       >new ImageIcon(URL u)(参数为网络地址)
       实现Icon接口的方法也有3种：
       >PaintIcon(Graphics)
       >getIconWidth()(设置图像宽度)
       >getIconHeight()(设置图像长度)
       JLable是一种既可以包含文本又可以包含图像的控件，该控件不能响应用户的动作。创建一个JLable的方法如下：
       Jlabel j1 = new JLable(“a”);
       this.add(j1);
      
 # 4.按钮
     JButton类用来定义按钮。JButton类的常用方法如下：
       >addActionListener()：注册点击事件监听器；
       >setText()：设置按钮文字；
       >setIcon()：设置按钮图标。
       通过组建的setMnemonic()方法可以设置组件Mnemonic助记符。通过组件的setTipText可以设置组建的ToolTip提示信息。
       在Swing中，JButton是有AbstractButton类派生的。AbstractButton类派生了两个组件：JButton和JtoggleButton组件。
       JButton是Swing的按钮，而ToggleButton组件是单选按钮和复选框的基类;
      
# 5、复选框  
  JcheckBox提供选中/未选中两种状态，当用户单击复选框时改变复选框原来设置的状态;
  
# 6、弹出式菜单
    JPopupMenu是一种Menu的组件，因此在使用JPopupMenu时都需要一个Container来放置JPopupMenu。
       通过JpopupMenu类可以定义弹出式菜单，其重要方法有：
       >add(JmenuItem e)：(往菜单中增加菜单项)
       >show()：(显示菜单)
       通过JMenuItem类来定义菜单项，通过addActionListener()为菜单项增加事件处理。
       JpopupMenu是一个可弹出并显示一系列选项的小窗口，可用于用户在菜单栏上选择选项时显示菜单，
       还可以用于当用户选择菜单项并激活时显示“右拉式(pull-right)“菜单；
       
# 7、单选按钮
    单选按钮的实质就是在一组按钮中一次只能有一个按钮被选中。单选按钮的外观类似复选框，但是复选框没有对可以选择的选项数目进行限制。
    对于每一组的单选按钮，必须创建一个ButtonGroup对象实例并且将每一个单选按钮添加到该ButtonGroup对象中；

# 8、下拉列表框
    下拉列表框可以让人感觉到整个界面很简洁，在大的网页中都能感觉到这一点。列表可以有许多选项，所以它们通常被放置在一个滚动窗格中。
     组合框与下拉列表框相似，区别在于使用组合框时用户可以不从列表中选择项目，还可以选择一个项目。在某些版本的组合框中，
    还可以输入自己的选择，如浏览器的地址栏。
       JComboBox方法很多，它们主要用来管理列表中的数据：
       >addItem()：添加一个项目到JComboBox
       >get/setSelectedIndex()：获取/设置JComboBox中选中项目的索引
       >get/setSelectedItem()：获取/设置选中的对象
       >removeAllItems()：从JComboBox删除所有对象
       >remoteItem()：从JComboBox删除特定对象

# 9、选项卡
    使用JTabbedPane类可以把几个组件放在一个组件中，如面板。用户可以通过选择对应于目标组件的选项卡来选择要查看的组件。要创建一个选项卡窗格，
    只要实例化一个JTabbedPane对象
    
# 10、滑杆 
  JSlider类定义了滑杆组件，它的重要方法有：
       >setMaxorTickSpacing()：设置主刻度
       >setMinorTickSpacing()：设置次刻度
       >setPaintTicks()：设置是否绘制刻度
       >setPaintLabels()：设置是否绘制标签
       >addChangeListener()：刻度变化事件处理
       >getValue()：获取当前滑块位置值
       >setValue()：设置滑块初始位置

# 11、滚动条
    JscrollPane的方法如下：
       >getHorizontalScrollBar()：返回水平的JscrollBar组件
       >getVerticalScrollBar()：返回垂直的JscrollBar组件
       >get/setHorizontalScrollBarPolicy()：Always、Never或As Needed
       >get/setVerticalScrollBarPolicy()：与水平函数相同
       
# 12、列表框
  JList是一个有用的组件，其类似于一组复选框或一组单选按钮。通过设置，允许对列表框中的项目进行多项选择。JList的方法如下：
       >getSelectedIndex()：获取选中的第一个索引
       >getSelectionMode()：设置单项选择还是多项选择
       >getListData()：设置在列表框中使用数据的模型
       >getSelectedValue()：获取选中的第一个值
      
# 13、菜单     
    JMenuItem和JMenu：
       >get/setAccelerator()：获取/设置快捷键
       >get/setText()：获取/设置菜单的文本
       >get/setIcon()：获取/设置菜单使用的图片
       JMenu专用：
       >add()：将JMenu或JMenuItem添加到JMenuBar或JMenu中。
       
      
