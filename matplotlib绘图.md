一、一般绘图
========

  1.图标
  ------
  plt.xlabel("x轴名称")
  plt.ylabel("y轴名称")
  plt.title('标题')
  
  2.绘图
  -----
  
二、3d绘图规范：
==========

  1.导入matplotlib和mpl_toolkits:
  ------
    import matplotlib.pyplot as plt
    from mpl_toolkits import mplt3d
    ax = plt.axes(projection = '3d')
    
  2.创建表达式：
  ------
    z = 函数表达式
    y = 函数表达式
    z = 函数表达式
    
  3.绘图：
  ------
    ax.plot3D(x,y,z,'color')
    ax.set_title('标题')
    plt.show()
