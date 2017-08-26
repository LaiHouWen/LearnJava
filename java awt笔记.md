
# AWT入门

  图形用户界面AWT中的容器是一种特殊的组件，他可以包含其他组件，即可以把组件方法容器中。
  Container类是用来存放其他组件的Component类的子类，Frame类又是Component的子类。
  Frame类用于创建具有标题栏和边界的窗口。这里通过继承Frame类来建立自己的界面  
# 布局管理器
  图形界面在布局管理上采用容器和布局管理相分离的方案，也就是说容器只是把组件放进来，但它不管怎样放置。至于如何放置需要用到布局管理器。
  Java中有几种布局管理器，分别是：FlowLayout , BorderLayout, GridLayout和GardLayout。

# 组件和监听接口
 1)、按钮和ActionListener  
 ActionListener是由处理ActionEvent事件的监听器对象实现的。当单击按钮、在文本区域中按回车键、选择菜单项、双击列表项都会触发监听器
 
 2)、运用WindowListener
  WindowListener是处理WindowEvent事件的对象实现的。这个监听器确定了窗口设么时候被打开、关闭、激活、不激活、最小化和最大化。该接口中的方法有：
       >public voidwindowActivated(WindowEvent e)
       >public voidwindowClosed(WindowEvent e)
       >public voidwindowClosing(WindowEvent e)
       >public voidwindowDeactivated(WindowEvent e)
       >public voidwindowDeiconfied(WindowEvent e)
       >public void windowIconified(WindowEvente)
       >public voidwindowOpened(WindowEvent e)
       
 3)、文本组件和TextListener
  文本组件就像把窗口空白处看成记事本一样，它是一个用来写内容的组件。TextListener用来确定何时文本值改变。
  
  
