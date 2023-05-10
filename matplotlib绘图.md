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
    可以创建多个ax对象，设置不同的宽度，以此来实现同一张画布上多张图
    调用ax对象
    ax.plot(x,y)
    
  3.axes类
  ------
    ax.legend(线型，图例名称，图例位置)
    ax.set_xlabel()
    ax.set_ylabel()
    ax.plot(x,y,'ys-') #x,y为数组或者函数表达式,''中为字母缩写线性、图例名、位置缩写：
    '-'	实线
    '--'	虚线
    '-.'	点划线
    ':'	虚线
    'H'	六角标记
    
    '.'	点标记
    'o'	圆圈标记
    'x'	'X'标记
    'D'	钻石标记
    'H'	六角标记
    's'	正方形标记
    '+'	加号标记
    
    
    'b'	蓝色
    'g'	绿色
    'r'	红色
    'c'	青色
    'm'	品红色
    'y'	黄色
    'k'	黑色
    'w'	白色
    
  4.分割绘图区域
  ------
    示例：
    plt.subplot(221)表示将画布分割为二行二列区域，在1位置绘图
    或：
    fig,axes = ply.subplot((x,y),figsize = ?)指定图片尺寸
    然后：
    axes[x][y].plot(......)
   
  5.设置网格格式
  ------
    grid(color = '颜色缩写',ls = '网格线样式缩写',lw = 宽度)
    
  6.坐标轴格式
  -----
    示例：
    fig, axes = plt.subplots(1, 2, figsize=(10,4))
    axes[0]plot(......)
    axes.set_xlabel("......")
    axes[0].set_ylabel("......")
  7.坐标轴范围
  ------
    ax.set_xlim(a,b)
    ax.set_ylim(a,b)
    ax.set_zlim(a,b)
    
  8.设置坐标轴刻度
  ------
    ax.set_xticks(a,b,,...,n) #设置x轴刻度为a,b,...,n
    ax.set_xticklabels(......) #刻度设置名称，与数字一一对应
  
二、各种格式图
=========
  
  1.双轴图
  ------
    示例：
    fig = plt.figure()
    a1  = fig.add_axes([0,0,1,1])
    a1.plot(...)
    a2  = a1.twinx()
    a2.plot(...)
    
  2.柱状图
  ------
    ax.bar(x坐标，高度，可选参数柱状图宽度，可选参数柱底部y坐标，可选x值位于柱的位置)
    #x坐标和高度可为一一对应的列表数组
    #宽度默认0.8，y坐标默认None，位置可选"center","edge"，默认center
    
  3.直方图
  ------
    
  
三、3d绘图规范：
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
