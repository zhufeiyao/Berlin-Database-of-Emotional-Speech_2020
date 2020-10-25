

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






http://emodb.bilderbar.info/download/
【核心代码】
download
├── erkennung.txt
├── erklaerung.txt
├── lablaut
│   ├── 03a01Faxx.lablaut
│   ├── 03a01Ncxx.lablaut
│   ├── 03a01Waxx.lablaut
│   ├── 03a02Fcxx.lablaut
│   ├── 03a02Ncxx.lablaut
│   ├── 03a02Taxx.lablaut
│   ├── 03a02Wbxx.lablaut
│   ├── 03a02Wcxx.lablaut
│   ├── 03a04Adxx.lablaut
│   ├── 03a04Fdxx.lablaut
│   ├── 03a04Lcxx.lablaut
│   ├── 03a04Ncxx.lablaut
│   ├── 03a04Taxx.lablaut
│   ├── 03a04Waxx.lablaut
│   ├── 03a04Wcxx.lablaut
│   ├── 03a05Aaxx.lablaut
│   ├── 03a05Fcxx.lablaut
│   ├── 03a05Ndxx.lablaut
│   ├── 03a05Tcxx.lablaut
│   ├── 03a05Waxx.lablaut
│   ├── 03a05Wbxx.lablaut
│   ├── 03a07Faxx.lablaut
│   ├── 03a07Fbxx.lablaut
│   ├── 03a07Laxx.lablaut
│   ├── 03a07Ncxx.lablaut
│   ├── 03a07Wcxx.lablaut
│   ├── 03b01Faxx.lablaut
│   ├── 03b01Lbxx.lablaut
│   ├── 03b01Nbxx.lablaut
│   ├── 03b01Tdxx.lablaut
│   ├── 03b01Waxx.lablaut
│   ├── 03b01Wcxx.lablaut
│   ├── 03b02Aaxx.lablaut
│   ├── 03b02Laxx.lablaut
│   ├── 03b02Naxx.lablaut
│   ├── 03b02Tbxx.lablaut
│   ├── 03b02Wbxx.lablaut
│   ├── 03b03Nbxx.lablaut
│   ├── 03b03Tcxx.lablaut
│   ├── 03b03Wcxx.lablaut
│   ├── 03b09Laxx.lablaut
│   ├── 03b09Ncxx.lablaut
│   ├── 03b09Tcxx.lablaut
│   ├── 03b09Waxx.lablaut
│   ├── 03b10Abxx.lablaut
│   ├── 03b10Ecxx.lablaut
│   ├── 03b10Naxx.lablaut
│   ├── 03b10Ncxx.lablaut
│   ├── 03b10Wbxx.lablaut
│   ├── 03b10Wcxx.lablaut
│   ├── 08a01Abxx.lablaut
│   ├── 08a01Fdxx.lablaut
│   ├── 08a01Lcxx.lablaut
│   ├── 08a01Naxx.lablaut
│   ├── 08a01Waxx.lablaut
│   ├── 08a01Wcxx.lablaut
│   ├── 08a02Abxx.lablaut
│   ├── 08a02Acxx.lablaut
│   ├── 08a02Fexx.lablaut
│   ├── 08a02Laxx.lablaut
│   ├── 08a02Naxx.lablaut
│   ├── 08a02Tbxx.lablaut
│   ├── 08a02Wcxx.lablaut
│   ├── 08a04Ffxx.lablaut
│   ├── 08a04Laxx.lablaut
│   ├── 08a04Ncxx.lablaut
│   ├── 08a04Tbxx.lablaut
│   ├── 08a04Wcxx.lablaut
│   ├── 08a05Fexx.lablaut
│   ├── 08a05Lcxx.lablaut
│   ├── 08a05Nbxx.lablaut
│   ├── 08a05Taxx.lablaut
│   ├── 08a05Waxx.lablaut
│   ├── 08a07Fdxx.lablaut
│   ├── 08a07Laxx.lablaut
│   ├── 08a07Naxx.lablaut
│   ├── 08a07Taxx.lablaut
│   ├── 08a07Tbxx.lablaut
│   ├── 08a07Wcxx.lablaut
│   ├── 08b01Aaxx.lablaut
│   ├── 08b01Fdxx.lablaut
│   ├── 08b01Fexx.lablaut
│   ├── 08b01Lbxx.lablaut
│   ├── 08b01Naxx.lablaut
│   ├── 08b01Waxx.lablaut
│   ├── 08b02Ffxx.lablaut
│   ├── 08b02Laxx.lablaut
│   ├── 08b02Nbxx.lablaut
│   ├── 08b02Tcxx.lablaut
│   ├── 08b02Wdxx.lablaut
│   ├── 08b03Fexx.lablaut
│   ├── 08b03Lcxx.lablaut
│   ├── 08b03Nbxx.lablaut
│   ├── 08b03Tcxx.lablaut
│   ├── 08b03Wdxx.lablaut
│   ├── 08b09Abxx.lablaut
│   ├── 08b09Fdxx.lablaut
│   ├── 08b09Lcxx.lablaut
│   ├── 08b09Nbxx.lablaut
│   ├── 08b09Tbxx.lablaut
│   ├── 08b09Waxx.lablaut
│   ├── 08b09Wcxx.lablaut
│   ├── 08b10Aaxx.lablaut
│   ├── 08b10Fdxx.lablaut
│   ├── 08b10Laxx.lablaut
│   ├── 08b10Ncxx.lablaut
│   ├── 08b10Tcxx.lablaut
│   ├── 08b10Waxx.lablaut
│   ├── 09a01Eaxx.lablaut
│   ├── 09a01Faxx.lablaut
│   ├── 09a01Nbxx.lablaut
│   ├── 09a01Wbxx.lablaut
│   ├── 09a02Eaxx.lablaut
│   ├── 09a02Ebxx.lablaut
│   ├── 09a02Laxx.lablaut
│   ├── 09a02Wbxx.lablaut
│   ├── 09a04Fdxx.lablaut
│   ├── 09a04Laxx.lablaut
│   ├── 09a04Nbxx.lablaut
│   ├── 09a04Waxx.lablaut
│   ├── 09a05Edxx.lablaut
│   ├── 09a05Lcxx.lablaut
│   ├── 09a05Nbxx.lablaut
│   ├── 09a05Tbxx.lablaut
│   ├── 09a05Wbxx.lablaut
│   ├── 09a05Wcxx.lablaut
│   ├── 09a07Ebxx.lablaut
│   ├── 09a07Naxx.lablaut
│   ├── 09a07Taxx.lablaut
│   ├── 09a07Wbxx.lablaut
│   ├── 09a07Wdxx.lablaut
│   ├── 09b01Eaxx.lablaut
│   ├── 09b01Naxx.lablaut
│   ├── 09b01Wbxx.lablaut
│   ├── 09b02Naxx.lablaut
│   ├── 09b02Tbxx.lablaut
│   ├── 09b02Wcxx.lablaut
│   ├── 09b02Wdxx.lablaut
│   ├── 09b03Edxx.lablaut
│   ├── 09b03Faxx.lablaut
│   ├── 09b03Fdxx.lablaut
│   ├── 09b03Lbxx.lablaut
│   ├── 09b03Nbxx.lablaut
│   ├── 09b03Taxx.lablaut
│   ├── 09b03Wbxx.lablaut
│   ├── 09b09Eaxx.lablaut
│   ├── 09b09Ndxx.lablaut
│   ├── 09b09Waxx.lablaut
│   ├── 09b10Aaxx.lablaut
│   ├── 09b10Ndxx.lablaut
│   ├── 09b10Waxx.lablaut
│   ├── 10a01Acxx.lablaut
│   ├── 10a01Nbxx.lablaut
│   ├── 10a01Waxx.lablaut
│   ├── 10a02Abxx.lablaut
│   ├── 10a02Faxx.lablaut
│   ├── 10a02Lbxx.lablaut
│   ├── 10a02Naxx.lablaut
│   ├── 10a02Waxx.lablaut
│   ├── 10a04Fdxx.lablaut
│   ├── 10a04Nbxx.lablaut
│   ├── 10a04Waxx.lablaut
│   ├── 10a04Wbxx.lablaut
│   ├── 10a05Aaxx.lablaut
│   ├── 10a05Ldxx.lablaut
│   ├── 10a05Tbxx.lablaut
│   ├── 10a05Wbxx.lablaut
│   ├── 10a07Aaxx.lablaut
│   ├── 10a07Adxx.lablaut
│   ├── 10a07Laxx.lablaut
│   ├── 10a07Taxx.lablaut
│   ├── 10a07Wbxx.lablaut
│   ├── 10b01Aaxx.lablaut
│   ├── 10b01Eaxx.lablaut
│   ├── 10b01Faxx.lablaut
│   ├── 10b01Lbxx.lablaut
│   ├── 10b02Aaxx.lablaut
│   ├── 10b02Laxx.lablaut
│   ├── 10b02Naxx.lablaut
│   ├── 10b02Wbxx.lablaut
│   ├── 10b03Laxx.lablaut
│   ├── 10b03Tbxx.lablaut
│   ├── 10b03Wbxx.lablaut
│   ├── 10b09Adxx.lablaut
│   ├── 10b09Lbxx.lablaut
│   ├── 10b09Wbxx.lablaut
│   ├── 10b10Fcxx.lablaut
│   ├── 10b10Lcxx.lablaut
│   ├── 10b10Waxx.lablaut
│   ├── 11a01Aaxx.lablaut
│   ├── 11a01Abxx.lablaut
│   ├── 11a01Ldxx.lablaut
│   ├── 11a01Ndxx.lablaut
│   ├── 11a01Wcxx.lablaut
│   ├── 11a02Ecxx.lablaut
│   ├── 11a02Fbxx.lablaut
│   ├── 11a02Ldxx.lablaut
│   ├── 11a02Ncxx.lablaut
│   ├── 11a02Tcxx.lablaut
│   ├── 11a02Wcxx.lablaut
│   ├── 11a04Acxx.lablaut
│   ├── 11a04Fdxx.lablaut
│   ├── 11a04Ndxx.lablaut
│   ├── 11a04Wcxx.lablaut
│   ├── 11a05Adxx.lablaut
│   ├── 11a05Fbxx.lablaut
│   ├── 11a05Fcxx.lablaut
│   ├── 11a05Lcxx.lablaut
│   ├── 11a05Naxx.lablaut
│   ├── 11a05Tdxx.lablaut
│   ├── 11a05Wdxx.lablaut
│   ├── 11a07Acxx.lablaut
│   ├── 11a07Ldxx.lablaut
│   ├── 11a07Taxx.lablaut
│   ├── 11a07Wcxx.lablaut
│   ├── 11b01Abxx.lablaut
│   ├── 11b01Ebxx.lablaut
│   ├── 11b01Fcxx.lablaut
│   ├── 11b01Lbxx.lablaut
│   ├── 11b01Ncxx.lablaut
│   ├── 11b01Wdxx.lablaut
│   ├── 11b02Abxx.lablaut
│   ├── 11b02Fdxx.lablaut
│   ├── 11b02Naxx.lablaut
│   ├── 11b02Tdxx.lablaut
│   ├── 11b02Wbxx.lablaut
│   ├── 11b03Fcxx.lablaut
│   ├── 11b03Lcxx.lablaut
│   ├── 11b03Nbxx.lablaut
│   ├── 11b03Tdxx.lablaut
│   ├── 11b03Waxx.lablaut
│   ├── 11b03Wbxx.lablaut
│   ├── 11b09Adxx.lablaut
│   ├── 11b09Fdxx.lablaut
│   ├── 11b09Ldxx.lablaut
│   ├── 11b09Naxx.lablaut
│   ├── 11b09Tdxx.lablaut
│   ├── 11b09Waxx.lablaut
│   ├── 11b10Adxx.lablaut
│   ├── 11b10Aexx.lablaut
│   ├── 11b10Ldxx.lablaut
│   ├── 11b10Ncxx.lablaut
│   ├── 11b10Tdxx.lablaut
│   ├── 11b10Waxx.lablaut
│   ├── 12a01Fbxx.lablaut
│   ├── 12a01Lbxx.lablaut
│   ├── 12a01Nbxx.lablaut
│   ├── 12a01Wcxx.lablaut
│   ├── 12a02Acxx.lablaut
│   ├── 12a02Ecxx.lablaut
│   ├── 12a02Nbxx.lablaut
│   ├── 12a02Taxx.lablaut
│   ├── 12a02Waxx.lablaut
│   ├── 12a02Wcxx.lablaut
│   ├── 12a04Wcxx.lablaut
│   ├── 12a05Abxx.lablaut
│   ├── 12a05Lbxx.lablaut
│   ├── 12a05Ndxx.lablaut
│   ├── 12a05Taxx.lablaut
│   ├── 12a05Wbxx.lablaut
│   ├── 12a07Acxx.lablaut
│   ├── 12a07Laxx.lablaut
│   ├── 12a07Waxx.lablaut
│   ├── 12b01Taxx.lablaut
│   ├── 12b01Waxx.lablaut
│   ├── 12b02Adxx.lablaut
│   ├── 12b02Eaxx.lablaut
│   ├── 12b02Fbxx.lablaut
│   ├── 12b02Naxx.lablaut
│   ├── 12b02Waxx.lablaut
│   ├── 12b02Wbxx.lablaut
│   ├── 12b02Wdxx.lablaut
│   ├── 12b03Laxx.lablaut
│   ├── 12b03Taxx.lablaut
│   ├── 12b09Acxx.lablaut
│   ├── 12b09Tdxx.lablaut
│   ├── 12b09Wcxx.lablaut
│   ├── 12b10Acxx.lablaut
│   ├── 12b10Ldxx.lablaut
│   ├── 12b10Waxx.lablaut
│   ├── 13a01Acxx.lablaut
│   ├── 13a01Eaxx.lablaut
│   ├── 13a01Ecxx.lablaut
│   ├── 13a01Fdxx.lablaut
│   ├── 13a01Lbxx.lablaut
│   ├── 13a01Nbxx.lablaut
│   ├── 13a01Wbxx.lablaut
│   ├── 13a02Adxx.lablaut
│   ├── 13a02Ecxx.lablaut
│   ├── 13a02Faxx.lablaut
│   ├── 13a02Lcxx.lablaut
│   ├── 13a02Ncxx.lablaut
│   ├── 13a02Taxx.lablaut
│   ├── 13a02Waxx.lablaut
│   ├── 13a04Acxx.lablaut
│   ├── 13a04Fcxx.lablaut
│   ├── 13a04Lbxx.lablaut
│   ├── 13a04Taxx.lablaut
│   ├── 13a04Wcxx.lablaut
│   ├── 13a05Aaxx.lablaut
│   ├── 13a05Eaxx.lablaut
│   ├── 13a05Lcxx.lablaut
│   ├── 13a05Nbxx.lablaut
│   ├── 13a05Tcxx.lablaut
│   ├── 13a05Waxx.lablaut
│   ├── 13a05Wcxx.lablaut
│   ├── 13a07Fdxx.lablaut
│   ├── 13a07Lbxx.lablaut
│   ├── 13a07Naxx.lablaut
│   ├── 13a07Tcxx.lablaut
│   ├── 13a07Wbxx.lablaut
│   ├── 13b01Abxx.lablaut
│   ├── 13b01Ecxx.lablaut
│   ├── 13b01Fcxx.lablaut
│   ├── 13b01Ldxx.lablaut
│   ├── 13b01Ncxx.lablaut
│   ├── 13b01Waxx.lablaut
│   ├── 13b02Fbxx.lablaut
│   ├── 13b02Lcxx.lablaut
│   ├── 13b02Nbxx.lablaut
│   ├── 13b02Waxx.lablaut
│   ├── 13b03Acxx.lablaut
│   ├── 13b03Edxx.lablaut
│   ├── 13b03Fdxx.lablaut
│   ├── 13b03Lbxx.lablaut
│   ├── 13b03Naxx.lablaut
│   ├── 13b03Tdxx.lablaut
│   ├── 13b03Wcxx.lablaut
│   ├── 13b09Abxx.lablaut
│   ├── 13b09Ecxx.lablaut
│   ├── 13b09Fbxx.lablaut
│   ├── 13b09Fcxx.lablaut
│   ├── 13b09Laxx.lablaut
│   ├── 13b09Naxx.lablaut
│   ├── 13b09Waxx.lablaut
│   ├── 13b10Ecxx.lablaut
│   ├── 13b10Faxx.lablaut
│   ├── 13b10Laxx.lablaut
│   ├── 13b10Ncxx.lablaut
│   ├── 13b10Waxx.lablaut
│   ├── 13b10Wcxx.lablaut
│   ├── 14a01Aaxx.lablaut
│   ├── 14a01Acxx.lablaut
│   ├── 14a01Eaxx.lablaut
│   ├── 14a01Naxx.lablaut
│   ├── 14a01Waxx.lablaut
│   ├── 14a01Wcxx.lablaut
│   ├── 14a02Abxx.lablaut
│   ├── 14a02Eaxx.lablaut
│   ├── 14a02Fdxx.lablaut
│   ├── 14a02Laxx.lablaut
│   ├── 14a02Ncxx.lablaut
│   ├── 14a02Tbxx.lablaut
│   ├── 14a02Waxx.lablaut
│   ├── 14a02Wcxx.lablaut
│   ├── 14a04Aaxx.lablaut
│   ├── 14a04Edxx.lablaut
│   ├── 14a04Lbxx.lablaut
│   ├── 14a04Tbxx.lablaut
│   ├── 14a04Tcxx.lablaut
│   ├── 14a04Wbxx.lablaut
│   ├── 14a04Wcxx.lablaut
│   ├── 14a05Aaxx.lablaut
│   ├── 14a05Acxx.lablaut
│   ├── 14a05Faxx.lablaut
│   ├── 14a05Fbxx.lablaut
│   ├── 14a05Lbxx.lablaut
│   ├── 14a05Naxx.lablaut
│   ├── 14a05Taxx.lablaut
│   ├── 14a05Tcxx.lablaut
│   ├── 14a05Waxx.lablaut
│   ├── 14a05Wbxx.lablaut
│   ├── 14a07Aaxx.lablaut
│   ├── 14a07Ebxx.lablaut
│   ├── 14a07Fdxx.lablaut
│   ├── 14a07Lcxx.lablaut
│   ├── 14a07Ldxx.lablaut
│   ├── 14a07Naxx.lablaut
│   ├── 14a07Tcxx.lablaut
│   ├── 14a07Wcxx.lablaut
│   ├── 14b01Acxx.lablaut
│   ├── 14b01Ebxx.lablaut
│   ├── 14b01Faxx.lablaut
│   ├── 14b01Fcxx.lablaut
│   ├── 14b01Naxx.lablaut
│   ├── 14b01Wcxx.lablaut
│   ├── 14b02Aaxx.lablaut
│   ├── 14b02Fbxx.lablaut
│   ├── 14b02Naxx.lablaut
│   ├── 14b02Tcxx.lablaut
│   ├── 14b02Wbxx.lablaut
│   ├── 14b02Wdxx.lablaut
│   ├── 14b03Adxx.lablaut
│   ├── 14b03Edxx.lablaut
│   ├── 14b03Lbxx.lablaut
│   ├── 14b03Taxx.lablaut
│   ├── 14b03Wbxx.lablaut
│   ├── 14b09Acxx.lablaut
│   ├── 14b09Ea.lablaut
│   ├── 14b09Eaxx.lablaut
│   ├── 14b09Fcxx.lablaut
│   ├── 14b09Lbxx.lablaut
│   ├── 14b09Tdxx.lablaut
│   ├── 14b09Waxx.lablaut
│   ├── 14b09Wcxx.lablaut
│   ├── 14b10Adxx.lablaut
│   ├── 14b10Ebxx.lablaut
│   ├── 14b10Lbxx.lablaut
│   ├── 14b10Nbxx.lablaut
│   ├── 14b10Tcxx.lablaut
│   ├── 14b10Wcxx.lablaut
│   ├── 15a01Eaxx.lablaut
│   ├── 15a01Fbxx.lablaut
│   ├── 15a01Laxx.lablaut
│   ├── 15a01Nbxx.lablaut
│   ├── 15a01Waxx.lablaut
│   ├── 15a02Acxx.lablaut
│   ├── 15a02Eaxx.lablaut
│   ├── 15a02Laxx.lablaut
│   ├── 15a02Naxx.lablaut
│   ├── 15a02Taxx.lablaut
│   ├── 15a02Wbxx.lablaut
│   ├── 15a02Wdxx.lablaut
│   ├── 15a04Abxx.lablaut
│   ├── 15a04Acxx.lablaut
│   ├── 15a04Fdxx.lablaut
│   ├── 15a04Ncxx.lablaut
│   ├── 15a04Waxx.lablaut
│   ├── 15a04Wbxx.lablaut
│   ├── 15a05Ebxx.lablaut
│   ├── 15a05Fbxx.lablaut
│   ├── 15a05Lbxx.lablaut
│   ├── 15a05Naxx.lablaut
│   ├── 15a05Waxx.lablaut
│   ├── 15a07Acxx.lablaut
│   ├── 15a07Ebxx.lablaut
│   ├── 15a07Faxx.lablaut
│   ├── 15a07Fbxx.lablaut
│   ├── 15a07Ldxx.lablaut
│   ├── 15a07Ncxx.lablaut
│   ├── 15b01Ecxx.lablaut
│   ├── 15b01Lbxx.lablaut
│   ├── 15b01Naxx.lablaut
│   ├── 15b01Wcxx.lablaut
│   ├── 15b02Aaxx.lablaut
│   ├── 15b02Lbxx.lablaut
│   ├── 15b02Ndxx.lablaut
│   ├── 15b02Tcxx.lablaut
│   ├── 15b02Waxx.lablaut
│   ├── 15b02Wcxx.lablaut
│   ├── 15b03Aaxx.lablaut
│   ├── 15b03Lcxx.lablaut
│   ├── 15b03Nbxx.lablaut
│   ├── 15b03Tcxx.lablaut
│   ├── 15b03Waxx.lablaut
│   ├── 15b03Wbxx.lablaut
│   ├── 15b09Acxx.lablaut
│   ├── 15b09Faxx.lablaut
│   ├── 15b09Laxx.lablaut
│   ├── 15b09Nbxx.lablaut
│   ├── 15b09Taxx.lablaut
│   ├── 15b09Wbxx.lablaut
│   ├── 15b10Acxx.lablaut
│   ├── 15b10Lcxx.lablaut
│   ├── 15b10Nbxx.lablaut
│   ├── 15b10Ncxx.lablaut
│   ├── 15b10Waxx.lablaut
│   ├── 16a01Ecxx.lablaut
│   ├── 16a01Fcxx.lablaut
│   ├── 16a01Lbxx.lablaut
│   ├── 16a01Ncxx.lablaut
│   ├── 16a01Tbxx.lablaut
│   ├── 16a01Wbxx.lablaut
│   ├── 16a02Eaxx.lablaut
│   ├── 16a02Ecxx.lablaut
│   ├── 16a02Lbxx.lablaut
│   ├── 16a02Nbxx.lablaut
│   ├── 16a02Tcxx.lablaut
│   ├── 16a02Wbxx.lablaut
│   ├── 16a04Abxx.lablaut
│   ├── 16a04Eaxx.lablaut
│   ├── 16a04Faxx.lablaut
│   ├── 16a04Laxx.lablaut
│   ├── 16a04Lcxx.lablaut
│   ├── 16a04Ncxx.lablaut
│   ├── 16a04Tcxx.lablaut
│   ├── 16a04Wbxx.lablaut
│   ├── 16a04Wcxx.lablaut
│   ├── 16a05Abxx.lablaut
│   ├── 16a05Eaxx.lablaut
│   ├── 16a05Fcxx.lablaut
│   ├── 16a05Laxx.lablaut
│   ├── 16a05Tbxx.lablaut
│   ├── 16a05Wbxx.lablaut
│   ├── 16a05Wcxx.lablaut
│   ├── 16a07Eaxx.lablaut
│   ├── 16a07Faxx.lablaut
│   ├── 16a07Fbxx.lablaut
│   ├── 16a07Laxx.lablaut
│   ├── 16a07Lbxx.lablaut
│   ├── 16a07Nbxx.lablaut
│   ├── 16a07Tdxx.lablaut
│   ├── 16a07Waxx.lablaut
│   ├── 16b01Aaxx.lablaut
│   ├── 16b01Ebxx.lablaut
│   ├── 16b01Faxx.lablaut
│   ├── 16b01Laxx.lablaut
│   ├── 16b01Lcxx.lablaut
│   ├── 16b01Tbxx.lablaut
│   ├── 16b01Waxx.lablaut
│   ├── 16b01Wbxx.lablaut
│   ├── 16b02Aaxx.lablaut
│   ├── 16b02Ebxx.lablaut
│   ├── 16b02Fdxx.lablaut
│   ├── 16b02Lbxx.lablaut
│   ├── 16b02Wbxx.lablaut
│   ├── 16b03Adxx.lablaut
│   ├── 16b03Eaxx.lablaut
│   ├── 16b03Faxx.lablaut
│   ├── 16b03Fdxx.lablaut
│   ├── 16b03Laxx.lablaut
│   ├── 16b03Nbxx.lablaut
│   ├── 16b03Taxx.lablaut
│   ├── 16b03Wbxx.lablaut
│   ├── 16b09Abxx.lablaut
│   ├── 16b09Ebxx.lablaut
│   ├── 16b09Fbxx.lablaut
│   ├── 16b09Laxx.lablaut
│   ├── 16b09Lbxx.lablaut
│   ├── 16b09Wbxx.lablaut
│   ├── 16b10Aaxx.lablaut
│   ├── 16b10Ebxx.lablaut
│   ├── 16b10Fbxx.lablaut
│   ├── 16b10Lbxx.lablaut
│   ├── 16b10Tbxx.lablaut
│   ├── 16b10Tdxx.lablaut
│   ├── 16b10Waxx.lablaut
│   └── 16b10Wbxx.lablaut
├── labsilb
│   ├── 03a01Fa.labsilb
│   ├── 03a01Nc.labsilb
│   ├── 03a01Wa.labsilb
│   ├── 03a02Fc.labsilb
│   ├── 03a02Nc.labsilb
│   ├── 03a02Ta.labsilb
│   ├── 03a02Wb.labsilb
│   ├── 03a02Wc.labsilb
│   ├── 03a04Ad.labsilb
│   ├── 03a04Fd.labsilb
│   ├── 03a04Lc.labsilb
│   ├── 03a04Nc.labsilb
│   ├── 03a04Ta.labsilb
│   ├── 03a04Wc.labsilb
│   ├── 03a05Fc.labsilb
│   ├── 03a05Nd.labsilb
│   ├── 03a05Wa.labsilb
│   ├── 03a05Wb.labsilb
│   ├── 03a07Fa.labsilb
│   ├── 03a07Fb.labsilb
│   ├── 03a07La.labsilb
│   ├── 03a07Nc.labsilb
│   ├── 03a07Wc.labsilb
│   ├── 03b01Fa.labsilb
│   ├── 03b01Lb.labsilb
│   ├── 03b01Nb.labsilb
│   ├── 03b01Wa.labsilb
│   ├── 03b01Wc.labsilb
│   ├── 03b02Aa.labsilb
│   ├── 03b02La.labsilb
│   ├── 03b02Na.labsilb
│   ├── 03b02Wb.labsilb
│   ├── 03b03Nb.labsilb
│   ├── 03b03Tc.labsilb
│   ├── 03b03Wc.labsilb
│   ├── 03b09La.labsilb
│   ├── 03b09Nc.labsilb
│   ├── 03b09Tc.labsilb
│   ├── 03b09Wa.labsilb
│   ├── 03b10Ab.labsilb
│   ├── 03b10Na.labsilb
│   ├── 03b10Nc.labsilb
│   ├── 03b10Wb.labsilb
│   ├── 03b10Wc.labsilb
│   ├── 08a01Lc.labsilb
│   ├── 08a01Na.labsilb
│   ├── 08a01Wa.labsilb
│   ├── 08a01Wc.labsilb
│   ├── 08a02Ab.labsilb
│   ├── 08a02Fe.labsilb
│   ├── 08a02La.labsilb
│   ├── 08a02Na.labsilb
│   ├── 08a02Tb.labsilb
│   ├── 08a02Wc.labsilb
│   ├── 08a04Ff.labsilb
│   ├── 08a04La.labsilb
│   ├── 08a04Nc.labsilb
│   ├── 08a04Tb.labsilb
│   ├── 08a04Wc.labsilb
│   ├── 08a05Fe.labsilb
│   ├── 08a05Lc.labsilb
│   ├── 08a05Nb.labsilb
│   ├── 08a05Ta.labsilb
│   ├── 08a05Wa.labsilb
│   ├── 08a07Fd.labsilb
│   ├── 08a07La.labsilb
│   ├── 08a07Na.labsilb
│   ├── 08a07Ta.labsilb
│   ├── 08a07Tb.labsilb
│   ├── 08a07Wc.labsilb
│   ├── 08b01Aa.labsilb
│   ├── 08b01Fd.labsilb
│   ├── 08b01Fe.labsilb
│   ├── 08b01Lb.labsilb
│   ├── 08b01Na.labsilb
│   ├── 08b01Wa.labsilb
│   ├── 08b02Ff.labsilb
│   ├── 08b02La.labsilb
│   ├── 08b02Nb.labsilb
│   ├── 08b02Tc.labsilb
│   ├── 08b02Wd.labsilb
│   ├── 08b03Fe.labsilb
│   ├── 08b03Lc.labsilb
│   ├── 08b03Nb.labsilb
│   ├── 08b03Tc.labsilb
│   ├── 08b03Wd.labsilb
│   ├── 08b09Ab.labsilb
│   ├── 08b09Fd.labsilb
│   ├── 08b09Lc.labsilb
│   ├── 08b09Nb.labsilb
│   ├── 08b09Tb.labsilb
│   ├── 08b09Wa.labsilb
│   ├── 08b09Wc.labsilb
│   ├── 08b10Aa.labsilb
│   ├── 08b10Fd.labsilb
│   ├── 08b10La.labsilb
│   ├── 08b10Nc.labsilb
│   ├── 08b10Tc.labsilb
│   ├── 08b10Wa.labsilb
│   ├── 09a01Ea.labsilb
│   ├── 09a01Fa.labsilb
│   ├── 09a01Nb.labsilb
│   ├── 09a01Wb.labsilb
│   ├── 09a02Ea.labsilb
│   ├── 09a02La.labsilb
│   ├── 09a02Wb.labsilb
│   ├── 09a04Fd.labsilb
│   ├── 09a04La.labsilb
│   ├── 09a04Nb.labsilb
│   ├── 09a04Wa.labsilb
│   ├── 09a05Ed.labsilb
│   ├── 09a05Lc.labsilb
│   ├── 09a05Nb.labsilb
│   ├── 09a05Wb.labsilb
│   ├── 09a05Wc.labsilb
│   ├── 09a07Eb.labsilb
│   ├── 09a07Na.labsilb
│   ├── 09a07Ta.labsilb
│   ├── 09a07Wb.labsilb
│   ├── 09a07Wd.labsilb
│   ├── 09b01Ea.labsilb
│   ├── 09b01Na.labsilb
│   ├── 09b01Wb.labsilb
│   ├── 09b02Na.labsilb
│   ├── 09b02Wc.labsilb
│   ├── 09b02Wd.labsilb
│   ├── 09b03Ed.labsilb
│   ├── 09b03Fa.labsilb
│   ├── 09b03Lb.labsilb
│   ├── 09b03Nb.labsilb
│   ├── 09b03Ta.labsilb
│   ├── 09b03Wb.labsilb
│   ├── 09b09Ea.labsilb
│   ├── 09b09Nd.labsilb
│   ├── 09b09Wa.labsilb
│   ├── 09b10Aa.labsilb
│   ├── 09b10Nd.labsilb
│   ├── 09b10Wa.labsilb
│   ├── 10a01Nb.labsilb
│   ├── 10a01Wa.labsilb
│   ├── 10a02Ab.labsilb
│   ├── 10a02Lb.labsilb
│   ├── 10a02Na.labsilb
│   ├── 10a02Wa.labsilb
│   ├── 10a04Nb.labsilb
│   ├── 10a04Wa.labsilb
│   ├── 10a04Wb.labsilb
│   ├── 10a05Ld.labsilb
│   ├── 10a05Wb.labsilb
│   ├── 10a07Aa.labsilb
│   ├── 10a07La.labsilb
│   ├── 10a07Ta.labsilb
│   ├── 10a07Wb.labsilb
│   ├── 10b01Aa.labsilb
│   ├── 10b01Ea.labsilb
│   ├── 10b01Fa.labsilb
│   ├── 10b01Lb.labsilb
│   ├── 10b02Aa.labsilb
│   ├── 10b02La.labsilb
│   ├── 10b02Na.labsilb
│   ├── 10b02Wb.labsilb
│   ├── 10b03La.labsilb
│   ├── 10b03Tb.labsilb
│   ├── 10b03Wb.labsilb
│   ├── 10b09Ad.labsilb
│   ├── 10b09Lb.labsilb
│   ├── 10b09Wb.labsilb
│   ├── 10b10Fc.labsilb
│   ├── 10b10Lc.labsilb
│   ├── 10b10Wa.labsilb
│   ├── 11a01Ab.labsilb
│   ├── 11a01Ld.labsilb
│   ├── 11a01Nd.labsilb
│   ├── 11a01Wc.labsilb
│   ├── 11a02Ec.labsilb
│   ├── 11a02Ld.labsilb
│   ├── 11a02Nc.labsilb
│   ├── 11a02Tc.labsilb
│   ├── 11a02Wc.labsilb
│   ├── 11a04Ac.labsilb
│   ├── 11a04Fd.labsilb
│   ├── 11a04Wc.labsilb
│   ├── 11a05Ad.labsilb
│   ├── 11a05Fb.labsilb
│   ├── 11a05Fc.labsilb
│   ├── 11a05Lc.labsilb
│   ├── 11a05Na.labsilb
│   ├── 11a05Td.labsilb
│   ├── 11a05Wd.labsilb
│   ├── 11a07Ac.labsilb
│   ├── 11a07Ld.labsilb
│   ├── 11a07Ta.labsilb
│   ├── 11a07Wc.labsilb
│   ├── 11b01Ab.labsilb
│   ├── 11b01Fc.labsilb
│   ├── 11b01Nc.labsilb
│   ├── 11b01Wd.labsilb
│   ├── 11b02Ab.labsilb
│   ├── 11b02Fd.labsilb
│   ├── 11b02Na.labsilb
│   ├── 11b02Td.labsilb
│   ├── 11b02Wb.labsilb
│   ├── 11b03Fc.labsilb
│   ├── 11b03Lc.labsilb
│   ├── 11b03Nb.labsilb
│   ├── 11b03Td.labsilb
│   ├── 11b03Wa.labsilb
│   ├── 11b03Wb.labsilb
│   ├── 11b09Ad.labsilb
│   ├── 11b09Fd.labsilb
│   ├── 11b09Ld.labsilb
│   ├── 11b09Na.labsilb
│   ├── 11b09Td.labsilb
│   ├── 11b09Wa.labsilb
│   ├── 11b10Ad.labsilb
│   ├── 11b10Ae.labsilb
│   ├── 11b10Ld.labsilb
│   ├── 11b10Nc.labsilb
│   ├── 11b10Td.labsilb
│   ├── 11b10Wa.labsilb
│   ├── 12a01Fb.labsilb
│   ├── 12a01Lb.labsilb
│   ├── 12a01Nb.labsilb
│   ├── 12a01Wc.labsilb
│   ├── 12a02Ac.labsilb
│   ├── 12a02Ec.labsilb
│   ├── 12a02Nb.labsilb
│   ├── 12a02Wa.labsilb
│   ├── 12a02Wc.labsilb
│   ├── 12a04Wc.labsilb
│   ├── 12a05Lb.labsilb
│   ├── 12a05Nd.labsilb
│   ├── 12a05Wb.labsilb
│   ├── 12a07Ac.labsilb
│   ├── 12a07La.labsilb
│   ├── 12a07Wa.labsilb
│   ├── 12b01Ta.labsilb
│   ├── 12b01Wa.labsilb
│   ├── 12b02Ad.labsilb
│   ├── 12b02Fb.labsilb
│   ├── 12b02Na.labsilb
│   ├── 12b02Wa.labsilb
│   ├── 12b02Wb.labsilb
│   ├── 12b02Wd.labsilb
│   ├── 12b03La.labsilb
│   ├── 12b09Wc.labsilb
│   ├── 12b10Ld.labsilb
│   ├── 12b10Wa.labsilb
│   ├── 13a01Ac.labsilb
│   ├── 13a01Ea.labsilb
│   ├── 13a01Ec.labsilb
│   ├── 13a01Fd.labsilb
│   ├── 13a01Lb.labsilb
│   ├── 13a01Nb.labsilb
│   ├── 13a01Wb.labsilb
│   ├── 13a02Ad.labsilb
│   ├── 13a02Ec.labsilb
│   ├── 13a02Fa.labsilb
│   ├── 13a02Lc.labsilb
│   ├── 13a02Nc.labsilb
│   ├── 13a02Ta.labsilb
│   ├── 13a02Wa.labsilb
│   ├── 13a04Ac.labsilb
│   ├── 13a04Fc.labsilb
│   ├── 13a04Lb.labsilb
│   ├── 13a04Ta.labsilb
│   ├── 13a04Wc.labsilb
│   ├── 13a05Aa.labsilb
│   ├── 13a05Ea.labsilb
│   ├── 13a05Lc.labsilb
│   ├── 13a05Nb.labsilb
│   ├── 13a05Tc.labsilb
│   ├── 13a05Wa.labsilb
│   ├── 13a05Wc.labsilb
│   ├── 13a07Fd.labsilb
│   ├── 13a07Lb.labsilb
│   ├── 13a07Na.labsilb
│   ├── 13a07Tc.labsilb
│   ├── 13a07Wb.labsilb
│   ├── 13b01Ab.labsilb
│   ├── 13b01Ec.labsilb
│   ├── 13b01Fc.labsilb
│   ├── 13b01Ld.labsilb
│   ├── 13b01Nc.labsilb
│   ├── 13b01Wa.labsilb
│   ├── 13b02Fb.labsilb
│   ├── 13b02Lc.labsilb
│   ├── 13b02Nb.labsilb
│   ├── 13b02Wa.labsilb
│   ├── 13b03Ac.labsilb
│   ├── 13b03Ed.labsilb
│   ├── 13b03Fd.labsilb
│   ├── 13b03Lb.labsilb
│   ├── 13b03Na.labsilb
│   ├── 13b03Td.labsilb
│   ├── 13b03Wc.labsilb
│   ├── 13b09Ab.labsilb
│   ├── 13b09Fb.labsilb
│   ├── 13b09Fc.labsilb
│   ├── 13b09La.labsilb
│   ├── 13b09Na.labsilb
│   ├── 13b09Wa.labsilb
│   ├── 13b10Ec.labsilb
│   ├── 13b10Fa.labsilb
│   ├── 13b10La.labsilb
│   ├── 13b10Nc.labsilb
│   ├── 13b10Wa.labsilb
│   ├── 13b10Wc.labsilb
│   ├── 14a01Aa.labsilb
│   ├── 14a01Ac.labsilb
│   ├── 14a01Na.labsilb
│   ├── 14a01Wa.labsilb
│   ├── 14a01Wc.labsilb
│   ├── 14a02Ab.labsilb
│   ├── 14a02Ea.labsilb
│   ├── 14a02Fd.labsilb
│   ├── 14a02Nc.labsilb
│   ├── 14a02Tb.labsilb
│   ├── 14a02Wa.labsilb
│   ├── 14a02Wc.labsilb
│   ├── 14a04Aa.labsilb
│   ├── 14a04Lb.labsilb
│   ├── 14a04Tb.labsilb
│   ├── 14a04Tc.labsilb
│   ├── 14a04Wb.labsilb
│   ├── 14a04Wc.labsilb
│   ├── 14a05Aa.labsilb
│   ├── 14a05Ac.labsilb
│   ├── 14a05Fa.labsilb
│   ├── 14a05Fb.labsilb
│   ├── 14a05Lb.labsilb
│   ├── 14a05Na.labsilb
│   ├── 14a05Ta.labsilb
│   ├── 14a05Tc.labsilb
│   ├── 14a05Wa.labsilb
│   ├── 14a05Wb.labsilb
│   ├── 14a07Aa.labsilb
│   ├── 14a07Eb.labsilb
│   ├── 14a07Fd.labsilb
│   ├── 14a07Lc.labsilb
│   ├── 14a07Ld.labsilb
│   ├── 14a07Na.labsilb
│   ├── 14a07Tc.labsilb
│   ├── 14a07Wc.labsilb
│   ├── 14b01Ac.labsilb
│   ├── 14b01Eb.labsilb
│   ├── 14b01Fa.labsilb
│   ├── 14b01Fc.labsilb
│   ├── 14b01Na.labsilb
│   ├── 14b01Wc.labsilb
│   ├── 14b02Aa.labsilb
│   ├── 14b02Fb.labsilb
│   ├── 14b02Na.labsilb
│   ├── 14b02Tc.labsilb
│   ├── 14b02Wb.labsilb
│   ├── 14b02Wd.labsilb
│   ├── 14b03Ad.labsilb
│   ├── 14b03Ed.labsilb
│   ├── 14b03Lb.labsilb
│   ├── 14b03Ta.labsilb
│   ├── 14b03Wb.labsilb
│   ├── 14b09Ac.labsilb
│   ├── 14b09Ea.labsilb
│   ├── 14b09Fc.labsilb
│   ├── 14b09Lb.labsilb
│   ├── 14b09Td.labsilb
│   ├── 14b09Wa.labsilb
│   ├── 14b09Wc.labsilb
│   ├── 14b10Ad.labsilb
│   ├── 14b10Eb.labsilb
│   ├── 14b10Lb.labsilb
│   ├── 14b10Nb.labsilb
│   ├── 14b10Tc.labsilb
│   ├── 14b10Wc.labsilb
│   ├── 15a01Ea.labsilb
│   ├── 15a01Fb.labsilb
│   ├── 15a01La.labsilb
│   ├── 15a01Nb.labsilb
│   ├── 15a01Wa.labsilb
│   ├── 15a02Ac.labsilb
│   ├── 15a02Ea.labsilb
│   ├── 15a02La.labsilb
│   ├── 15a02Na.labsilb
│   ├── 15a02Ta.labsilb
│   ├── 15a02Wb.labsilb
│   ├── 15a02Wd.labsilb
│   ├── 15a04Ab.labsilb
│   ├── 15a04Fd.labsilb
│   ├── 15a04Nc.labsilb
│   ├── 15a04Wa.labsilb
│   ├── 15a04Wb.labsilb
│   ├── 15a05Eb.labsilb
│   ├── 15a05Fb.labsilb
│   ├── 15a05Lb.labsilb
│   ├── 15a05Na.labsilb
│   ├── 15a05Wa.labsilb
│   ├── 15a07Ac.labsilb
│   ├── 15a07Eb.labsilb
│   ├── 15a07Fa.labsilb
│   ├── 15a07Fb.labsilb
│   ├── 15a07Ld.labsilb
│   ├── 15a07Nc.labsilb
│   ├── 15b01Ec.labsilb
│   ├── 15b01Lb.labsilb
│   ├── 15b01Na.labsilb
│   ├── 15b01Wc.labsilb
│   ├── 15b02Lb.labsilb
│   ├── 15b02Nd.labsilb
│   ├── 15b02Wa.labsilb
│   ├── 15b02Wc.labsilb
│   ├── 15b03Aa.labsilb
│   ├── 15b03Lc.labsilb
│   ├── 15b03Nb.labsilb
│   ├── 15b03Tc.labsilb
│   ├── 15b03Wa.labsilb
│   ├── 15b03Wb.labsilb
│   ├── 15b09Ac.labsilb
│   ├── 15b09Fa.labsilb
│   ├── 15b09La.labsilb
│   ├── 15b09Nb.labsilb
│   ├── 15b09Ta.labsilb
│   ├── 15b09Wb.labsilb
│   ├── 15b10Ac.labsilb
│   ├── 15b10Lc.labsilb
│   ├── 15b10Nb.labsilb
│   ├── 15b10Nc.labsilb
│   ├── 15b10Wa.labsilb
│   ├── 16a01Ec.labsilb
│   ├── 16a01Fc.labsilb
│   ├── 16a01Lb.labsilb
│   ├── 16a01Nc.labsilb
│   ├── 16a01Tb.labsilb
│   ├── 16a01Wb.labsilb
│   ├── 16a02Ea.labsilb
│   ├── 16a02Ec.labsilb
│   ├── 16a02Lb.labsilb
│   ├── 16a02Nb.labsilb
│   ├── 16a02Tc.labsilb
│   ├── 16a02Wb.labsilb
│   ├── 16a04Ea.labsilb
│   ├── 16a04Fa.labsilb
│   ├── 16a04La.labsilb
│   ├── 16a04Lc.labsilb
│   ├── 16a04Nc.labsilb
│   ├── 16a04Tc.labsilb
│   ├── 16a04Wb.labsilb
│   ├── 16a04Wc.labsilb
│   ├── 16a05Ab.labsilb
│   ├── 16a05Ea.labsilb
│   ├── 16a05La.labsilb
│   ├── 16a05Tb.labsilb
│   ├── 16a05Wb.labsilb
│   ├── 16a05Wc.labsilb
│   ├── 16a07Ea.labsilb
│   ├── 16a07Fb.labsilb
│   ├── 16a07La.labsilb
│   ├── 16a07Lb.labsilb
│   ├── 16a07Nb.labsilb
│   ├── 16a07Td.labsilb
│   ├── 16a07Wa.labsilb
│   ├── 16b01Aa.labsilb
│   ├── 16b01Eb.labsilb
│   ├── 16b01Fa.labsilb
│   ├── 16b01La.labsilb
│   ├── 16b01Lc.labsilb
│   ├── 16b01Tb.labsilb
│   ├── 16b01Wa.labsilb
│   ├── 16b01Wb.labsilb
│   ├── 16b02Aa.labsilb
│   ├── 16b02Eb.labsilb
│   ├── 16b02Fd.labsilb
│   ├── 16b02Lb.labsilb
│   ├── 16b02Wb.labsilb
│   ├── 16b03Ad.labsilb
│   ├── 16b03Ea.labsilb
│   ├── 16b03Fa.labsilb
│   ├── 16b03Fd.labsilb
│   ├── 16b03La.labsilb
│   ├── 16b03Nb.labsilb
│   ├── 16b03Ta.labsilb
│   ├── 16b03Wb.labsilb
│   ├── 16b09Eb.labsilb
│   ├── 16b09Fb.labsilb
│   ├── 16b09La.labsilb
│   ├── 16b09Lb.labsilb
│   ├── 16b09Wb.labsilb
│   ├── 16b10Aa.labsilb
│   ├── 16b10Fb.labsilb
│   ├── 16b10Lb.labsilb
│   ├── 16b10Tb.labsilb
│   ├── 16b10Td.labsilb
│   ├── 16b10Wa.labsilb
│   └── 16b10Wb.labsilb
├── silb
│   ├── 03a01Fa.silb
│   ├── 03a01Nc.silb
│   ├── 03a01Wa.silb
│   ├── 03a02Fc.silb
│   ├── 03a02Nc.silb
│   ├── 03a02Ta.silb
│   ├── 03a02Wb.silb
│   ├── 03a02Wc.silb
│   ├── 03a04Ad.silb
│   ├── 03a04Fd.silb
│   ├── 03a04Lc.silb
│   ├── 03a04Nc.silb
│   ├── 03a04Ta.silb
│   ├── 03a04Wc.silb
│   ├── 03a05Aa.silb
│   ├── 03a05Fc.silb
│   ├── 03a05Nd.silb
│   ├── 03a05Tc.silb
│   ├── 03a05Wa.silb
│   ├── 03a05Wb.silb
│   ├── 03a07Fa.silb
│   ├── 03a07Fb.silb
│   ├── 03a07La.silb
│   ├── 03a07Nc.silb
│   ├── 03a07Wc.silb
│   ├── 03b01Fa.silb
│   ├── 03b01Lb.silb
│   ├── 03b01Nb.silb
│   ├── 03b01Td.silb
│   ├── 03b01Wa.silb
│   ├── 03b01Wc.silb
│   ├── 03b02Aa.silb
│   ├── 03b02La.silb
│   ├── 03b02Na.silb
│   ├── 03b02Tb.silb
│   ├── 03b02Wb.silb
│   ├── 03b03Nb.silb
│   ├── 03b03Tc.silb
│   ├── 03b03Wc.silb
│   ├── 03b09La.silb
│   ├── 03b09Nc.silb
│   ├── 03b09Tc.silb
│   ├── 03b09Wa.silb
│   ├── 03b10Ab.silb
│   ├── 03b10Ec.silb
│   ├── 03b10Na.silb
│   ├── 03b10Nc.silb
│   ├── 03b10Wb.silb
│   ├── 03b10Wc.silb
│   ├── 08a01Ab.silb
│   ├── 08a01Fd.silb
│   ├── 08a01Lc.silb
│   ├── 08a01Na.silb
│   ├── 08a01Wa.silb
│   ├── 08a01Wc.silb
│   ├── 08a02Ab.silb
│   ├── 08a02Ac.silb
│   ├── 08a02Fe.silb
│   ├── 08a02La.silb
│   ├── 08a02Na.silb
│   ├── 08a02Tb.silb
│   ├── 08a02Wc.silb
│   ├── 08a04Ff.silb
│   ├── 08a04La.silb
│   ├── 08a04Nc.silb
│   ├── 08a04Tb.silb
│   ├── 08a04Wc.silb
│   ├── 08a05Fe.silb
│   ├── 08a05Lc.silb
│   ├── 08a05Nb.silb
│   ├── 08a05Ta.silb
│   ├── 08a05Wa.silb
│   ├── 08a07Fd.silb
│   ├── 08a07La.silb
│   ├── 08a07Na.silb
│   ├── 08a07Ta.silb
│   ├── 08a07Tb.silb
│   ├── 08a07Wc.silb
│   ├── 08b01Aa.silb
│   ├── 08b01Fd.silb
│   ├── 08b01Fe.silb
│   ├── 08b01Lb.silb
│   ├── 08b01Na.silb
│   ├── 08b01Wa.silb
│   ├── 08b02Ff.silb
│   ├── 08b02La.silb
│   ├── 08b02Nb.silb
│   ├── 08b02Tc.silb
│   ├── 08b02Wd.silb
│   ├── 08b03Fe.silb
│   ├── 08b03Lc.silb
│   ├── 08b03Nb.silb
│   ├── 08b03Tc.silb
│   ├── 08b03Wd.silb
│   ├── 08b09Ab.silb
│   ├── 08b09Fd.silb
│   ├── 08b09Lc.silb
│   ├── 08b09Nb.silb
│   ├── 08b09Tb.silb
│   ├── 08b09Wa.silb
│   ├── 08b09Wc.silb
│   ├── 08b10Aa.silb
│   ├── 08b10Fd.silb
│   ├── 08b10La.silb
│   ├── 08b10Nc.silb
│   ├── 08b10Tc.silb
│   ├── 08b10Wa.silb
│   ├── 09a01Ea.silb
│   ├── 09a01Fa.silb
│   ├── 09a01Nb.silb
│   ├── 09a01Wb.silb
│   ├── 09a02Ea.silb
│   ├── 09a02Eb.silb
│   ├── 09a02La.silb
│   ├── 09a02Wb.silb
│   ├── 09a04Fd.silb
│   ├── 09a04La.silb
│   ├── 09a04Nb.silb
│   ├── 09a04Wa.silb
│   ├── 09a05Ed.silb
│   ├── 09a05Lc.silb
│   ├── 09a05Nb.silb
│   ├── 09a05Tb.silb
│   ├── 09a05Wb.silb
│   ├── 09a05Wc.silb
│   ├── 09a07Eb.silb
│   ├── 09a07Na.silb
│   ├── 09a07Ta.silb
│   ├── 09a07Wb.silb
│   ├── 09a07Wd.silb
│   ├── 09b01Ea.silb
│   ├── 09b01Na.silb
│   ├── 09b01Wb.silb
│   ├── 09b02Na.silb
│   ├── 09b02Tb.silb
│   ├── 09b02Wc.silb
│   ├── 09b02Wd.silb
│   ├── 09b03Ed.silb
│   ├── 09b03Fa.silb
│   ├── 09b03Fd.silb
│   ├── 09b03Lb.silb
│   ├── 09b03Nb.silb
│   ├── 09b03Ta.silb
│   ├── 09b03Wb.silb
│   ├── 09b09Ea.silb
│   ├── 09b09Nd.silb
│   ├── 09b09Wa.silb
│   ├── 09b10Aa.silb
│   ├── 09b10Nd.silb
│   ├── 09b10Wa.silb
│   ├── 10a01Ac.silb
│   ├── 10a01Nb.silb
│   ├── 10a01Wa.silb
│   ├── 10a02Ab.silb
│   ├── 10a02Fa.silb
│   ├── 10a02Lb.silb
│   ├── 10a02Na.silb
│   ├── 10a02Wa.silb
│   ├── 10a04Fd.silb
│   ├── 10a04Nb.silb
│   ├── 10a04Wa.silb
│   ├── 10a04Wb.silb
│   ├── 10a05Aa.silb
│   ├── 10a05Ld.silb
│   ├── 10a05Tb.silb
│   ├── 10a05Wb.silb
│   ├── 10a07Aa.silb
│   ├── 10a07Ad.silb
│   ├── 10a07La.silb
│   ├── 10a07Ta.silb
│   ├── 10a07Wb.silb
│   ├── 10b01Aa.silb
│   ├── 10b01Ea.silb
│   ├── 10b01Fa.silb
│   ├── 10b01Lb.silb
│   ├── 10b02Aa.silb
│   ├── 10b02La.silb
│   ├── 10b02Na.silb
│   ├── 10b02Wb.silb
│   ├── 10b03La.silb
│   ├── 10b03Tb.silb
│   ├── 10b03Wb.silb
│   ├── 10b09Ad.silb
│   ├── 10b09Lb.silb
│   ├── 10b09Wb.silb
│   ├── 10b10Fc.silb
│   ├── 10b10Lc.silb
│   ├── 10b10Wa.silb
│   ├── 11a01Aa.silb
│   ├── 11a01Ab.silb
│   ├── 11a01Ld.silb
│   ├── 11a01Nd.silb
│   ├── 11a01Wc.silb
│   ├── 11a02Ec.silb
│   ├── 11a02Fb.silb
│   ├── 11a02Ld.silb
│   ├── 11a02Nc.silb
│   ├── 11a02Tc.silb
│   ├── 11a02Wc.silb
│   ├── 11a04Ac.silb
│   ├── 11a04Fd.silb
│   ├── 11a04Nd.silb
│   ├── 11a04Wc.silb
│   ├── 11a05Ad.silb
│   ├── 11a05Fb.silb
│   ├── 11a05Fc.silb
│   ├── 11a05Lc.silb
│   ├── 11a05Na.silb
│   ├── 11a05Td.silb
│   ├── 11a05Wd.silb
│   ├── 11a07Ac.silb
│   ├── 11a07Ld.silb
│   ├── 11a07Ta.silb
│   ├── 11a07Wc.silb
│   ├── 11b01Ab.silb
│   ├── 11b01Eb.silb
│   ├── 11b01Fc.silb
│   ├── 11b01Lb.silb
│   ├── 11b01Nc.silb
│   ├── 11b01Wd.silb
│   ├── 11b02Ab.silb
│   ├── 11b02Fd.silb
│   ├── 11b02Na.silb
│   ├── 11b02Td.silb
│   ├── 11b02Wb.silb
│   ├── 11b03Fc.silb
│   ├── 11b03Lc.silb
│   ├── 11b03Nb.silb
│   ├── 11b03Td.silb
│   ├── 11b03Wa.silb
│   ├── 11b03Wb.silb
│   ├── 11b09Ad.silb
│   ├── 11b09Fd.silb
│   ├── 11b09Ld.silb
│   ├── 11b09Na.silb
│   ├── 11b09Td.silb
│   ├── 11b09Wa.silb
│   ├── 11b10Ad.silb
│   ├── 11b10Ae.silb
│   ├── 11b10Ld.silb
│   ├── 11b10Nc.silb
│   ├── 11b10Td.silb
│   ├── 11b10Wa.silb
│   ├── 12a01Fb.silb
│   ├── 12a01Lb.silb
│   ├── 12a01Nb.silb
│   ├── 12a01Wc.silb
│   ├── 12a02Ac.silb
│   ├── 12a02Ec.silb
│   ├── 12a02Nb.silb
│   ├── 12a02Wa.silb
│   ├── 12a02Wc.silb
│   ├── 12a04Wc.silb
│   ├── 12a05Ab.silb
│   ├── 12a05Lb.silb
│   ├── 12a05Nd.silb
│   ├── 12a05Ta.silb
│   ├── 12a05Wb.silb
│   ├── 12a07Ac.silb
│   ├── 12a07La.silb
│   ├── 12a07Wa.silb
│   ├── 12b01Ta.silb
│   ├── 12b01Wa.silb
│   ├── 12b02Ad.silb
│   ├── 12b02Ea.silb
│   ├── 12b02Fb.silb
│   ├── 12b02Na.silb
│   ├── 12b02Wa.silb
│   ├── 12b02Wb.silb
│   ├── 12b02Wd.silb
│   ├── 12b03La.silb
│   ├── 12b03Ta.silb
│   ├── 12b09Ac.silb
│   ├── 12b09Td.silb
│   ├── 12b09Wc.silb
│   ├── 12b10Ac.silb
│   ├── 12b10Ld.silb
│   ├── 12b10Wa.silb
│   ├── 13a01Ac.silb
│   ├── 13a01Ea.silb
│   ├── 13a01Ec.silb
│   ├── 13a01Fd.silb
│   ├── 13a01Lb.silb
│   ├── 13a01Nb.silb
│   ├── 13a01Wb.silb
│   ├── 13a02Ad.silb
│   ├── 13a02Ec.silb
│   ├── 13a02Fa.silb
│   ├── 13a02Lc.silb
│   ├── 13a02Nc.silb
│   ├── 13a02Ta.silb
│   ├── 13a02Wa.silb
│   ├── 13a04Ac.silb
│   ├── 13a04Fc.silb
│   ├── 13a04Lb.silb
│   ├── 13a04Ta.silb
│   ├── 13a04Wc.silb
│   ├── 13a05Aa.silb
│   ├── 13a05Ea.silb
│   ├── 13a05Lc.silb
│   ├── 13a05Nb.silb
│   ├── 13a05Tc.silb
│   ├── 13a05Wa.silb
│   ├── 13a05Wc.silb
│   ├── 13a07Fd.silb
│   ├── 13a07Lb.silb
│   ├── 13a07Na.silb
│   ├── 13a07Tc.silb
│   ├── 13a07Wb.silb
│   ├── 13b01Ab.silb
│   ├── 13b01Ec.silb
│   ├── 13b01Fc.silb
│   ├── 13b01Ld.silb
│   ├── 13b01Nc.silb
│   ├── 13b01Wa.silb
│   ├── 13b02Fb.silb
│   ├── 13b02Lc.silb
│   ├── 13b02Nb.silb
│   ├── 13b02Wa.silb
│   ├── 13b03Ac.silb
│   ├── 13b03Ed.silb
│   ├── 13b03Fd.silb
│   ├── 13b03Lb.silb
│   ├── 13b03Na.silb
│   ├── 13b03Td.silb
│   ├── 13b03Wc.silb
│   ├── 13b09Ab.silb
│   ├── 13b09Ec.silb
│   ├── 13b09Fb.silb
│   ├── 13b09Fc.silb
│   ├── 13b09La.silb
│   ├── 13b09Na.silb
│   ├── 13b09Wa.silb
│   ├── 13b10Ec.silb
│   ├── 13b10Fa.silb
│   ├── 13b10La.silb
│   ├── 13b10Nc.silb
│   ├── 13b10Wa.silb
│   ├── 13b10Wc.silb
│   ├── 14a01Aa.silb
│   ├── 14a01Ac.silb
│   ├── 14a01Ea.silb
│   ├── 14a01Na.silb
│   ├── 14a01Wa.silb
│   ├── 14a01Wc.silb
│   ├── 14a02Ab.silb
│   ├── 14a02Ea.silb
│   ├── 14a02Fd.silb
│   ├── 14a02La.silb
│   ├── 14a02Nc.silb
│   ├── 14a02Tb.silb
│   ├── 14a02Wa.silb
│   ├── 14a02Wc.silb
│   ├── 14a04Aa.silb
│   ├── 14a04Ed.silb
│   ├── 14a04Lb.silb
│   ├── 14a04Tb.silb
│   ├── 14a04Tc.silb
│   ├── 14a04Wb.silb
│   ├── 14a04Wc.silb
│   ├── 14a05Aa.silb
│   ├── 14a05Ac.silb
│   ├── 14a05Fa.silb
│   ├── 14a05Fb.silb
│   ├── 14a05Lb.silb
│   ├── 14a05Na.silb
│   ├── 14a05Ta.silb
│   ├── 14a05Tc.silb
│   ├── 14a05Wa.silb
│   ├── 14a05Wb.silb
│   ├── 14a07Aa.silb
│   ├── 14a07Eb.silb
│   ├── 14a07Fd.silb
│   ├── 14a07Lc.silb
│   ├── 14a07Ld.silb
│   ├── 14a07Na.silb
│   ├── 14a07Tc.silb
│   ├── 14a07Wc.silb
│   ├── 14b01Ac.silb
│   ├── 14b01Eb.silb
│   ├── 14b01Fa.silb
│   ├── 14b01Fc.silb
│   ├── 14b01Na.silb
│   ├── 14b01Wc.silb
│   ├── 14b02Aa.silb
│   ├── 14b02Fb.silb
│   ├── 14b02Na.silb
│   ├── 14b02Tc.silb
│   ├── 14b02Wb.silb
│   ├── 14b02Wd.silb
│   ├── 14b03Ad.silb
│   ├── 14b03Ed.silb
│   ├── 14b03Lb.silb
│   ├── 14b03Ta.silb
│   ├── 14b03Wb.silb
│   ├── 14b09Ac.silb
│   ├── 14b09Ea.silb
│   ├── 14b09Fc.silb
│   ├── 14b09Lb.silb
│   ├── 14b09Td.silb
│   ├── 14b09Wa.silb
│   ├── 14b09Wc.silb
│   ├── 14b10Ad.silb
│   ├── 14b10Eb.silb
│   ├── 14b10Lb.silb
│   ├── 14b10Nb.silb
│   ├── 14b10Tc.silb
│   ├── 14b10Wc.silb
│   ├── 15a01Ea.silb
│   ├── 15a01Fb.silb
│   ├── 15a01La.silb
│   ├── 15a01Nb.silb
│   ├── 15a01Wa.silb
│   ├── 15a02Ac.silb
│   ├── 15a02Ea.silb
│   ├── 15a02La.silb
│   ├── 15a02Na.silb
│   ├── 15a02Ta.silb
│   ├── 15a02Wb.silb
│   ├── 15a02Wd.silb
│   ├── 15a04Ab.silb
│   ├── 15a04Ac.silb
│   ├── 15a04Fd.silb
│   ├── 15a04Nc.silb
│   ├── 15a04Wa.silb
│   ├── 15a04Wb.silb
│   ├── 15a05Eb.silb
│   ├── 15a05Fb.silb
│   ├── 15a05Lb.silb
│   ├── 15a05Na.silb
│   ├── 15a05Wa.silb
│   ├── 15a07Ac.silb
│   ├── 15a07Eb.silb
│   ├── 15a07Fa.silb
│   ├── 15a07Fb.silb
│   ├── 15a07Ld.silb
│   ├── 15a07Nc.silb
│   ├── 15b01Ec.silb
│   ├── 15b01Lb.silb
│   ├── 15b01Na.silb
│   ├── 15b01Wc.silb
│   ├── 15b02Aa.silb
│   ├── 15b02Lb.silb
│   ├── 15b02Nd.silb
│   ├── 15b02Tc.silb
│   ├── 15b02Wa.silb
│   ├── 15b02Wc.silb
│   ├── 15b03Aa.silb
│   ├── 15b03Lc.silb
│   ├── 15b03Nb.silb
│   ├── 15b03Tc.silb
│   ├── 15b03Wa.silb
│   ├── 15b03Wb.silb
│   ├── 15b09Ac.silb
│   ├── 15b09Fa.silb
│   ├── 15b09La.silb
│   ├── 15b09Nb.silb
│   ├── 15b09Ta.silb
│   ├── 15b09Wb.silb
│   ├── 15b10Ac.silb
│   ├── 15b10Lc.silb
│   ├── 15b10Nb.silb
│   ├── 15b10Nc.silb
│   ├── 15b10Wa.silb
│   ├── 16a01Ec.silb
│   ├── 16a01Fc.silb
│   ├── 16a01Lb.silb
│   ├── 16a01Nc.silb
│   ├── 16a01Tb.silb
│   ├── 16a01Wb.silb
│   ├── 16a02Ea.silb
│   ├── 16a02Ec.silb
│   ├── 16a02Lb.silb
│   ├── 16a02Nb.silb
│   ├── 16a02Tc.silb
│   ├── 16a02Wb.silb
│   ├── 16a04Ab.silb
│   ├── 16a04Ea.silb
│   ├── 16a04Fa.silb
│   ├── 16a04La.silb
│   ├── 16a04Lc.silb
│   ├── 16a04Nc.silb
│   ├── 16a04Tc.silb
│   ├── 16a04Wb.silb
│   ├── 16a04Wc.silb
│   ├── 16a05Ab.silb
│   ├── 16a05Ea.silb
│   ├── 16a05Fc.silb
│   ├── 16a05La.silb
│   ├── 16a05Tb.silb
│   ├── 16a05Wb.silb
│   ├── 16a05Wc.silb
│   ├── 16a07Ea.silb
│   ├── 16a07Fa.silb
│   ├── 16a07Fb.silb
│   ├── 16a07La.silb
│   ├── 16a07Lb.silb
│   ├── 16a07Nb.silb
│   ├── 16a07Td.silb
│   ├── 16a07Wa.silb
│   ├── 16b01Aa.silb
│   ├── 16b01Eb.silb
│   ├── 16b01Fa.silb
│   ├── 16b01La.silb
│   ├── 16b01Lc.silb
│   ├── 16b01Tb.silb
│   ├── 16b01Wa.silb
│   ├── 16b01Wb.silb
│   ├── 16b02Aa.silb
│   ├── 16b02Eb.silb
│   ├── 16b02Fd.silb
│   ├── 16b02Lb.silb
│   ├── 16b02Wb.silb
│   ├── 16b03Ad.silb
│   ├── 16b03Ea.silb
│   ├── 16b03Fa.silb
│   ├── 16b03Fd.silb
│   ├── 16b03La.silb
│   ├── 16b03Nb.silb
│   ├── 16b03Ta.silb
│   ├── 16b03Wb.silb
│   ├── 16b09Ab.silb
│   ├── 16b09Eb.silb
│   ├── 16b09Fb.silb
│   ├── 16b09La.silb
│   ├── 16b09Lb.silb
│   ├── 16b09Wb.silb
│   ├── 16b10Aa.silb
│   ├── 16b10Eb.silb
│   ├── 16b10Fb.silb
│   ├── 16b10Lb.silb
│   ├── 16b10Tb.silb
│   ├── 16b10Td.silb
│   ├── 16b10Wa.silb
│   └── 16b10Wb.silb
└── wav
├── 03a01Fa.wav
├── 03a01Nc.wav
├── 03a01Wa.wav
├── 03a02Fc.wav
├── 03a02Nc.wav
├── 03a02Ta.wav
├── 03a02Wb.wav
├── 03a02Wc.wav
├── 03a04Ad.wav
├── 03a04Fd.wav
├── 03a04Lc.wav
├── 03a04Nc.wav
├── 03a04Ta.wav
├── 03a04Wc.wav
├── 03a05Aa.wav
├── 03a05Fc.wav
├── 03a05Nd.wav
├── 03a05Tc.wav
├── 03a05Wa.wav
├── 03a05Wb.wav
├── 03a07Fa.wav
├── 03a07Fb.wav
├── 03a07La.wav
├── 03a07Nc.wav
├── 03a07Wc.wav
├── 03b01Fa.wav
├── 03b01Lb.wav
├── 03b01Nb.wav
├── 03b01Td.wav
├── 03b01Wa.wav
├── 03b01Wc.wav
├── 03b02Aa.wav
├── 03b02La.wav
├── 03b02Na.wav
├── 03b02Tb.wav
├── 03b02Wb.wav
├── 03b03Nb.wav
├── 03b03Tc.wav
├── 03b03Wc.wav
├── 03b09La.wav
├── 03b09Nc.wav
├── 03b09Tc.wav
├── 03b09Wa.wav
├── 03b10Ab.wav
├── 03b10Ec.wav
├── 03b10Na.wav
├── 03b10Nc.wav
├── 03b10Wb.wav
├── 03b10Wc.wav
├── 08a01Ab.wav
├── 08a01Fd.wav
├── 08a01Lc.wav
├── 08a01Na.wav
├── 08a01Wa.wav
├── 08a01Wc.wav
├── 08a02Ab.wav
├── 08a02Ac.wav
├── 08a02Fe.wav
├── 08a02La.wav
├── 08a02Na.wav
├── 08a02Tb.wav
├── 08a02Wc.wav
├── 08a04Ff.wav
├── 08a04La.wav
├── 08a04Nc.wav
├── 08a04Tb.wav
├── 08a04Wc.wav
├── 08a05Fe.wav
├── 08a05Lc.wav
├── 08a05Nb.wav
├── 08a05Ta.wav
├── 08a05Wa.wav
├── 08a07Fd.wav
├── 08a07La.wav
├── 08a07Na.wav
├── 08a07Ta.wav
├── 08a07Tb.wav
├── 08a07Wc.wav
├── 08b01Aa.wav
├── 08b01Fd.wav
├── 08b01Fe.wav
├── 08b01Lb.wav
├── 08b01Na.wav
├── 08b01Wa.wav
├── 08b02Ff.wav
├── 08b02La.wav
├── 08b02Nb.wav
├── 08b02Tc.wav
├── 08b02Wd.wav
├── 08b03Fe.wav
├── 08b03Lc.wav
├── 08b03Nb.wav
├── 08b03Tc.wav
├── 08b03Wd.wav
├── 08b09Ab.wav
├── 08b09Fd.wav
├── 08b09Lc.wav
├── 08b09Nb.wav
├── 08b09Tb.wav
├── 08b09Wa.wav
├── 08b09Wc.wav
├── 08b10Aa.wav
├── 08b10Fd.wav
├── 08b10La.wav
├── 08b10Nc.wav
├── 08b10Tc.wav
├── 08b10Wa.wav
├── 09a01Ea.wav
├── 09a01Fa.wav
├── 09a01Nb.wav
├── 09a01Wb.wav
├── 09a02Ea.wav
├── 09a02Eb.wav
├── 09a02La.wav
├── 09a02Wb.wav
├── 09a04Fd.wav
├── 09a04La.wav
├── 09a04Nb.wav
├── 09a04Wa.wav
├── 09a05Ed.wav
├── 09a05Lc.wav
├── 09a05Nb.wav
├── 09a05Tb.wav
├── 09a05Wb.wav
├── 09a05Wc.wav
├── 09a07Eb.wav
├── 09a07Na.wav
├── 09a07Ta.wav
├── 09a07Wb.wav
├── 09a07Wd.wav
├── 09b01Ea.wav
├── 09b01Na.wav
├── 09b01Wb.wav
├── 09b02Na.wav
├── 09b02Tb.wav
├── 09b02Wc.wav
├── 09b02Wd.wav
├── 09b03Ed.wav
├── 09b03Fa.wav
├── 09b03Fd.wav
├── 09b03Lb.wav
├── 09b03Nb.wav
├── 09b03Ta.wav
├── 09b03Wb.wav
├── 09b09Ea.wav
├── 09b09Nd.wav
├── 09b09Wa.wav
├── 09b10Aa.wav
├── 09b10Nd.wav
├── 09b10Wa.wav
├── 10a01Ac.wav
├── 10a01Nb.wav
├── 10a01Wa.wav
├── 10a02Ab.wav
├── 10a02Fa.wav
├── 10a02Lb.wav
├── 10a02Na.wav
├── 10a02Wa.wav
├── 10a04Fd.wav
├── 10a04Nb.wav
├── 10a04Wa.wav
├── 10a04Wb.wav
├── 10a05Aa.wav
├── 10a05Ld.wav
├── 10a05Tb.wav
├── 10a05Wb.wav
├── 10a07Aa.wav
├── 10a07Ad.wav
├── 10a07La.wav
├── 10a07Ta.wav
├── 10a07Wb.wav
├── 10b01Aa.wav
├── 10b01Ea.wav
├── 10b01Fa.wav
├── 10b01Lb.wav
├── 10b02Aa.wav
├── 10b02La.wav
├── 10b02Na.wav
├── 10b02Wb.wav
├── 10b03La.wav
├── 10b03Tb.wav
├── 10b03Wb.wav
├── 10b09Ad.wav
├── 10b09Lb.wav
├── 10b09Wb.wav
├── 10b10Fc.wav
├── 10b10Lc.wav
├── 10b10Wa.wav
├── 11a01Aa.wav
├── 11a01Ab.wav
├── 11a01Ld.wav
├── 11a01Nd.wav
├── 11a01Wc.wav
├── 11a02Ec.wav
├── 11a02Fb.wav
├── 11a02Ld.wav
├── 11a02Nc.wav
├── 11a02Tc.wav
├── 11a02Wc.wav
├── 11a04Ac.wav
├── 11a04Fd.wav
├── 11a04Nd.wav
├── 11a04Wc.wav
├── 11a05Ad.wav
├── 11a05Fb.wav
├── 11a05Fc.wav
├── 11a05Lc.wav
├── 11a05Na.wav
├── 11a05Td.wav
├── 11a05Wd.wav
├── 11a07Ac.wav
├── 11a07Ld.wav
├── 11a07Ta.wav
├── 11a07Wc.wav
├── 11b01Ab.wav
├── 11b01Eb.wav
├── 11b01Fc.wav
├── 11b01Lb.wav
├── 11b01Nc.wav
├── 11b01Wd.wav
├── 11b02Ab.wav
├── 11b02Fd.wav
├── 11b02Na.wav
├── 11b02Td.wav
├── 11b02Wb.wav
├── 11b03Fc.wav
├── 11b03Lc.wav
├── 11b03Nb.wav
├── 11b03Td.wav
├── 11b03Wa.wav
├── 11b03Wb.wav
├── 11b09Ad.wav
├── 11b09Fd.wav
├── 11b09Ld.wav
├── 11b09Na.wav
├── 11b09Td.wav
├── 11b09Wa.wav
├── 11b10Ad.wav
├── 11b10Ae.wav
├── 11b10Ld.wav
├── 11b10Nc.wav
├── 11b10Td.wav
├── 11b10Wa.wav
├── 12a01Fb.wav
├── 12a01Lb.wav
├── 12a01Nb.wav
├── 12a01Wc.wav
├── 12a02Ac.wav
├── 12a02Ec.wav
├── 12a02Nb.wav
├── 12a02Wa.wav
├── 12a02Wc.wav
├── 12a04Wc.wav
├── 12a05Ab.wav
├── 12a05Lb.wav
├── 12a05Nd.wav
├── 12a05Ta.wav
├── 12a05Wb.wav
├── 12a07Ac.wav
├── 12a07La.wav
├── 12a07Wa.wav
├── 12b01Ta.wav
├── 12b01Wa.wav
├── 12b02Ad.wav
├── 12b02Ea.wav
├── 12b02Fb.wav
├── 12b02Na.wav
├── 12b02Wa.wav
├── 12b02Wb.wav
├── 12b02Wd.wav
├── 12b03La.wav
├── 12b03Ta.wav
├── 12b09Ac.wav
├── 12b09Td.wav
├── 12b09Wc.wav
├── 12b10Ac.wav
├── 12b10Ld.wav
├── 12b10Wa.wav
├── 13a01Ac.wav
├── 13a01Ea.wav
├── 13a01Ec.wav
├── 13a01Fd.wav
├── 13a01Lb.wav
├── 13a01Nb.wav
├── 13a01Wb.wav
├── 13a02Ad.wav
├── 13a02Ec.wav
├── 13a02Fa.wav
├── 13a02Lc.wav
├── 13a02Nc.wav
├── 13a02Ta.wav
├── 13a02Wa.wav
├── 13a04Ac.wav
├── 13a04Fc.wav
├── 13a04Lb.wav
├── 13a04Ta.wav
├── 13a04Wc.wav
├── 13a05Aa.wav
├── 13a05Ea.wav
├── 13a05Lc.wav
├── 13a05Nb.wav
├── 13a05Tc.wav
├── 13a05Wa.wav
├── 13a05Wc.wav
├── 13a07Fd.wav
├── 13a07Lb.wav
├── 13a07Na.wav
├── 13a07Tc.wav
├── 13a07Wb.wav
├── 13b01Ab.wav
├── 13b01Ec.wav
├── 13b01Fc.wav
├── 13b01Ld.wav
├── 13b01Nc.wav
├── 13b01Wa.wav
├── 13b02Fb.wav
├── 13b02Lc.wav
├── 13b02Nb.wav
├── 13b02Wa.wav
├── 13b03Ac.wav
├── 13b03Ed.wav
├── 13b03Fd.wav
├── 13b03Lb.wav
├── 13b03Na.wav
├── 13b03Td.wav
├── 13b03Wc.wav
├── 13b09Ab.wav
├── 13b09Ec.wav
├── 13b09Fb.wav
├── 13b09Fc.wav
├── 13b09La.wav
├── 13b09Na.wav
├── 13b09Wa.wav
├── 13b10Ec.wav
├── 13b10Fa.wav
├── 13b10La.wav
├── 13b10Nc.wav
├── 13b10Wa.wav
├── 13b10Wc.wav
├── 14a01Aa.wav
├── 14a01Ac.wav
├── 14a01Ea.wav
├── 14a01Na.wav
├── 14a01Wa.wav
├── 14a01Wc.wav
├── 14a02Ab.wav
├── 14a02Ea.wav
├── 14a02Fd.wav
├── 14a02La.wav
├── 14a02Nc.wav
├── 14a02Tb.wav
├── 14a02Wa.wav
├── 14a02Wc.wav
├── 14a04Aa.wav
├── 14a04Ed.wav
├── 14a04Lb.wav
├── 14a04Tb.wav
├── 14a04Tc.wav
├── 14a04Wb.wav
├── 14a04Wc.wav
├── 14a05Aa.wav
├── 14a05Ac.wav
├── 14a05Fa.wav
├── 14a05Fb.wav
├── 14a05Lb.wav
├── 14a05Na.wav
├── 14a05Ta.wav
├── 14a05Tc.wav
├── 14a05Wa.wav
├── 14a05Wb.wav
├── 14a07Aa.wav
├── 14a07Eb.wav
├── 14a07Fd.wav
├── 14a07Lc.wav
├── 14a07Ld.wav
├── 14a07Na.wav
├── 14a07Tc.wav
├── 14a07Wc.wav
├── 14b01Ac.wav
├── 14b01Eb.wav
├── 14b01Fa.wav
├── 14b01Fc.wav
├── 14b01Na.wav
├── 14b01Wc.wav
├── 14b02Aa.wav
├── 14b02Fb.wav
├── 14b02Na.wav
├── 14b02Tc.wav
├── 14b02Wb.wav
├── 14b02Wd.wav
├── 14b03Ad.wav
├── 14b03Ed.wav
├── 14b03Lb.wav
├── 14b03Ta.wav
├── 14b03Wb.wav
├── 14b09Ac.wav
├── 14b09Ea.wav
├── 14b09Fc.wav
├── 14b09Lb.wav
├── 14b09Td.wav
├── 14b09Wa.wav
├── 14b09Wc.wav
├── 14b10Ad.wav
├── 14b10Eb.wav
├── 14b10Lb.wav
├── 14b10Nb.wav
├── 14b10Tc.wav
├── 14b10Wc.wav
├── 15a01Ea.wav
├── 15a01Fb.wav
├── 15a01La.wav
├── 15a01Nb.wav
├── 15a01Wa.wav
├── 15a02Ac.wav
├── 15a02Ea.wav
├── 15a02La.wav
├── 15a02Na.wav
├── 15a02Ta.wav
├── 15a02Wb.wav
├── 15a02Wd.wav
├── 15a04Ab.wav
├── 15a04Ac.wav
├── 15a04Fd.wav
├── 15a04Nc.wav
├── 15a04Wa.wav
├── 15a04Wb.wav
├── 15a05Eb.wav
├── 15a05Fb.wav
├── 15a05Lb.wav
├── 15a05Na.wav
├── 15a05Wa.wav
├── 15a07Ac.wav
├── 15a07Eb.wav
├── 15a07Fa.wav
├── 15a07Fb.wav
├── 15a07Ld.wav
├── 15a07Nc.wav
├── 15b01Ec.wav
├── 15b01Lb.wav
├── 15b01Na.wav
├── 15b01Wc.wav
├── 15b02Aa.wav
├── 15b02Lb.wav
├── 15b02Nd.wav
├── 15b02Tc.wav
├── 15b02Wa.wav
├── 15b02Wc.wav
├── 15b03Aa.wav
├── 15b03Lc.wav
├── 15b03Nb.wav
├── 15b03Tc.wav
├── 15b03Wa.wav
├── 15b03Wb.wav
├── 15b09Ac.wav
├── 15b09Fa.wav
├── 15b09La.wav
├── 15b09Nb.wav
├── 15b09Ta.wav
├── 15b09Wb.wav
├── 15b10Ac.wav
├── 15b10Lc.wav
├── 15b10Nb.wav
├── 15b10Nc.wav
├── 15b10Wa.wav
├── 16a01Ec.wav
├── 16a01Fc.wav
├── 16a01Lb.wav
├── 16a01Nc.wav
├── 16a01Tb.wav
├── 16a01Wb.wav
├── 16a02Ea.wav
├── 16a02Ec.wav
├── 16a02Lb.wav
├── 16a02Nb.wav
├── 16a02Tc.wav
├── 16a02Wb.wav
├── 16a04Ab.wav
├── 16a04Ea.wav
├── 16a04Fa.wav
├── 16a04La.wav
├── 16a04Lc.wav
├── 16a04Nc.wav
├── 16a04Tc.wav
├── 16a04Wb.wav
├── 16a04Wc.wav
├── 16a05Ab.wav
├── 16a05Ea.wav
├── 16a05Fc.wav
├── 16a05La.wav
├── 16a05Tb.wav
├── 16a05Wb.wav
├── 16a05Wc.wav
├── 16a07Ea.wav
├── 16a07Fa.wav
├── 16a07Fb.wav
├── 16a07La.wav
├── 16a07Lb.wav
├── 16a07Nb.wav
├── 16a07Td.wav
├── 16a07Wa.wav
├── 16b01Aa.wav
├── 16b01Eb.wav
├── 16b01Fa.wav
├── 16b01La.wav
├── 16b01Lc.wav
├── 16b01Tb.wav
├── 16b01Wa.wav
├── 16b01Wb.wav
├── 16b02Aa.wav
├── 16b02Eb.wav
├── 16b02Fd.wav
├── 16b02Lb.wav
├── 16b02Wb.wav
├── 16b03Ad.wav
├── 16b03Ea.wav
├── 16b03Fa.wav
├── 16b03Fd.wav
├── 16b03La.wav
├── 16b03Nb.wav
├── 16b03Ta.wav
├── 16b03Wb.wav
├── 16b09Ab.wav
├── 16b09Eb.wav
├── 16b09Fb.wav
├── 16b09La.wav
├── 16b09Lb.wav
├── 16b09Wb.wav
├── 16b10Aa.wav
├── 16b10Eb.wav
├── 16b10Fb.wav
├── 16b10Lb.wav
├── 16b10Tb.wav
├── 16b10Td.wav
├── 16b10Wa.wav
└── 16b10Wb.wav

4 directories, 2103 files
