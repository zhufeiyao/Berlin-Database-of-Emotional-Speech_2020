

# Berlin-Database-of-Emotional-Speech
柏林情感言论数据库分析

项目介绍参考URL:http://emodb.bilderbar.info/

数据库背景：As a part of the DFG funded research project SE462/3-1 in 1997 and 1999 we recorded a database of emotional utterances spoken by actors. The recordings took place in the anechoic chamber of the Technical University Berlin, department of Technical Acoustics. Director of the project was Prof. Dr. W. Sendlmeier, Technical University of Berlin, Institute of Speech and Communication, department of communication science. Members of the project were mainly Felix Burkhardt, Miriam Kienast, Astrid Paeschke and Benjamin Weiss.

信息表：
1.列: 连续数字
2-6.列: 感知测试结果:
  ·正确识别情绪的百分比
  ·认为表现出的情感表现合理的人的百分比
  ·感知实验中每个参与者的情感识别
  ·情绪强度（1=非常弱，7=非常强）
  ·上述值的标准偏差
7.列: 一个包含原始F0-和持续时间值的pho-文件，使用MBROLA合成词文件。
#注：F0-:基本频率（或简称 基频、fundamental frequency），当发声体由于振动而发出声音时，声音一般可以分解为许多单纯的正弦波，也就是说所有的自然声音基本都是由许多频率不同的正弦波组成的，其中频率最低的正弦波即为基音，而其他频率较高的正弦波则为泛音。MBROLA 是一个TTS 引擎，旨在尽可能的提供各种语言的语音合成器
8.列：字母P-L-A-Y：
  ·（P）原始声音
  ·（L）MBROLA重新合成的版本（具有原始的F0轮廓）
  ·（A）根据D'Alessandro＆Mertens的造型算法，使用MBROLA重新合成具有程式化F0轮廓的版本
  ·（Y）根据Sascha Fagel编写的算法，另一个具有程式化F0轮廓的重新合成的音频文件
9.列：查看话语图形

#第9列用于配置图形显示的选项：
  ·Scaling缩放比例：
      real=所有话语的时间尺度都是相同的
      perc性能=缩放时间轴，使整个话语适合窗口大小
  ·Label标签：
      none =不显示标签文件
      |||| =仅显示音节之间的边界
      |a|b|c| =显示边框和音节标签
      a，b，c =边框仅在音节标签之间显示，而不是在整个窗口高度上显示
  ·Stress强调：
      黄色条表示每个音节的重音水平（感知测试的平均值）；
      单位为0到3（根据无压力，正常压力，强烈压力和强调压力）
      深红色细线构成的标线，其值分别为1（最低），2（中）和3（最高）
  ·F0：
      normal正常= F0值显示为测量值（清音部分无值）
      interpolated插值= F0值显示为中间值（通过线性插值计算）
   ·Stylization程式化：
      none =不显示F0样式
      spline样条=将显示带有样条函数的F0风格化（由Sascha Fagel编程）
      linear线性=将显示线性F0风格化（D'Alessandro＆Mertens开发的风格化方法）
   ·gliss. threshold欢乐.阈：
      差分glissando阈值是D'Alessandro和Mertens用于样式化算法的参数），较高的值将导致较少的块，较低的值将产生更详细的样式，因此将更多的块
   ·diff. gliss. threshold:差异.欢乐.阈：
      差分glissando阈值（D'Alessandro＆Mertens用于样式化算法的另一个参数），较低的值=更多的块
   ·Trend趋势：
      线性全局趋势（=回归线）及其斜率将显示
   ·Histograms直方图：
      话语的F0直方图将显示
      如果您对直方图特别感兴趣，可以在“"results-histograms结果-直方图”下获得更好的视图（带有标记的单位）
   ·Energy能源：
      显示了代表测量的能量值的深蓝色曲线
   ·Loudness响度：
      显示了代表所计算的响度值的蓝色曲线，Zwicker已开发了用于响度计算的算法（请参见Zwicker，Fastl（1990）：“ Psychoacoustics”）
   ·Rhythm Events节奏事件：
      如果选择字母A-H红色点之一（通常在响度曲线的最大值上），则表示计算出的节奏事件
      用于计算节奏事件的算法也基于Zwicker开发的方法
      字母A到H代表计算所需的响度最大值的不同参考值
      A-参考值等于每个单个发声的最大响度
      B-参考值等于特定文字和特定情感的响度最大值（所有讲话者）
      C-参考值等于相应文本（所有讲话者，所有情感）的最大响度
      D-参考值等于相应情感（所有文本，所有讲话者）的最大响度
      E-参考值等于所有讲话的最大响度（整个数据库的最大响度）
      F-参考值等于特定文字和特定说话者的最大音量（所有情绪）
      G-参考值等于相应说话者的最大响度（所有文本，所有情感）
      H-参考值等于特定情绪和特定说话者的最大响度（所有文字）
      
      
每种说话都按照相同的方案命名：
    位置1-2：演讲者编号
    位置3-5：文案代码
    位置6：情感
    位置7：如果有两个以上的版本，则编号为a，b，c...。
    例如：03a01Fa.wav是来自扬声器03的语音文件，语音文本为a01，带有情感“ Freude”（幸福）。

演讲者编号的信息
    03-男，31岁
    08-女，34岁
    09-女，21岁
    10-男，32岁
    11-男，26岁
    12-男，30岁
    13-女，32岁
    14-女，35岁
    15-男，25岁
    16-女，31岁

文案代码
    a01 抹布在冰箱上。
    a02 她想在周三递交。
    a04 我今晚可以告诉他。
    a05 黑色的纸放在那块木头旁边。
    a07 七小时后就可以完成了。
    b01 桌子下面的那些袋子是什么？
    b02 他们刚把它搬上楼，现在又下楼了。
    b03 每到周末我总是回家看艾格妮丝。
    b09 我要把这个拿走，和卡尔喝一杯。
    b10 它会放在我们经常放的地方。
    
情绪代号（德版）
W 愤怒
L 无聊
E 厌恶
A 焦虑
F 幸福
T 悲伤
N 中性
