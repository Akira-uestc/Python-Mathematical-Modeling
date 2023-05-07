一、一般绘图
========

  1.图标
  ------
    plt.xlabel("x轴名称")
    plt.ylabel("y轴名称")
    plt.title('标题')
  
  2.绘图
  -----
    #颜色(pyplot库)
    b(蓝色)，g(绿色)，r(红色)，c(青色)，m(品红)，y(黄色)，k(黑色)，w(白色)
    plt.plot(x,y,'颜色')
    
    #创建图形对象
    fig = plt.figure()
    add_axes() 的参数值是一个序列，序列中的 4 个数字分别对应图形的左侧，底部，宽度，和高度，且每个数字必须介于 0 到 1 之间
    ax=fig.add_axes([0,0,1,1])
    调用ax对象
    ax.plot(x,y)
    
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
