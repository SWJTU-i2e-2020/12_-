# 基于传感器的智慧农业检测

## 项目名称和作者

## 目录

## 小组每个人的贡献

## 问题定义
水稻是草本稻属的一种，也是稻属中作为粮食的最主要最悠久的一种。原产中国，七千年前长江流域就种植水稻，广义水稻区别于旱稻；狭义水稻指淡水稻，区别于海水稻等，按稻谷类型，水稻可以分为籼稻和粳稻、早稻和中晚稻，糯稻和非糯稻，还有其它分类，水稻一般栽培于水田，无土栽培的是水上稻。水稻一般没有一米高，2米左右的为新培育的巨型稻，我国科学家袁隆平对杂交水稻的研究做出了巨大贡献，被誉为"杂交水稻之父"，水稻所结子实即稻谷，稻谷脱去颖壳后称糙米，糙米碾去米糠层即可得到大米，世界上近一半人口，都以大米为食。水稻除可食用外，还可以酿酒、制糖做工业原料，稻壳、稻秆，可以作为饲料，我国水稻主产区主要是东北地区、长江流域、珠江流域，属于直接经济作物。还是世界上三分之一人类的主食。也是北方人民的主要有机食品。
水位的管理在整个生产过程中最为重要,应根据水稻不同生长期和鳖、虾、鱼对水位的要求,控制好稻田水位。3月份,稻田水位控制在30厘米左右。4月中旬以后,水温稳定在20℃C以上时,应将水位逐渐提高至60厘米以上,这样有利于小龙虾的生长。6-9月份根据水稻不同生长期对水位的要求,控制好稻田水位。6月份插秧后,前期做到薄水返青、浅水分渠、够苗晒田;晒田复水后保持20厘米水层;高温期要求适当提高水位,保持田面水位20-25厘米。小龙虾越冬前(即10-11月份)的稻田水位应控制在30厘米左右,这样可使稻莞露出水面10厘米左右,既可使部分稻苑再生,又可避免因稻苑全部淹没水下,导致稻田水质过肥缺氧,而影响小龙虾的生长。12月至翌年2月份小龙虾在越冬期间,应提高稻田水位,控制在60厘米以上。所以我们想要设计一个微系统来监测水位。

## 问题的背景：

自古以来我国就是农业大国，种植作物，种植类型，种植方式数不胜数。其中种植面积最大的就是水稻。

智慧农业 ：将物联网技术运用到传统农业中去，运用传感器和软件通过移动平台或者电脑平台对农业生产进行控制，使传统农业更具有“智慧”。除了精准感知、控制与决策管理外，从广泛意义上讲，智慧农业还包括农业电子
商务、食品溯源防伪、农业休闲旅游、农业信息服务等方面的内容。

## 需求介绍：
经过我们小组对于市场的分析，对于农户的调查，得出对于设备有以下要求：

1.希望能够检测出水位。

2.希望能够通过明显的方式提示种植者当前水位情况。

3.希望能够在提高水稻产量上起到指导性作用，而并非直接作用。

4.希望能够包装完善，方便使用

5.希望能够在保证安全性的情况下提高精度

## 概念设计
1.可替换的概念

（1）.通过压强传感器，对水田底部的压强进行测量再通过计算机计算出不同压强对应的不同水位，再将计算值与标准值进行比较，将大小结果传输到LCD显示屏上。指示农户进行改变操作。

（2）.通过温湿度传感器，对于临近水平面处进行测量，将测量值与标准值进行比较，若大于标准值则输出信号到LED灯和蜂鸣器上指示农户进行相应操作来改变现状。

（3）.直接通过水位传感器，放置于标准水平面处将水位高度传输到芯片再与标准值进行比较，将大小结果传输到蜂鸣器和LED灯上，指示农户进行操作。
2.概念评估
	通过比较三种传感器的价格以及测量精度得到如下表格
	
	             价格          	测量精度
		     
压强传感器   	较贵（8元）		   较高

温湿度传感器	       贵（8.8元）	 	   一般

水位传感器	        便宜（5.9元）	   较高

3.概念选择
通过横向比较三种方案的成本与精度，由于我们是学生资金有限，决定还是选择成本最低的方案，而且第三种方案不仅成本最低而且精度也是最高的，当然从各个方面都应选择第三种方案，不仅如此，在实际代码编写中第三种方案也会更加简单，因为前两种方案还需将数据传入芯片并进行计算，第三种方案直接将结果传入并显示出来，综上第三种方案为最佳方案，也是我们选择的方案

## 详细设计：
一、工作过程
三种颜色LED分别指示低(红色),中(黄色),高(绿色)水位,低水位抽水或者高水位抽水可以用开关切换，当功能切换开关按弹起时（也就是未按下），低水位时继电器吸合（外接水泵工作），开始加水，水位升高到高水位时继电器断开（水泵停止工作），待水位再次降到低水位时继电器再次吸合，上述过程循环。此功能应用在自动加水设备中，可让水位维持在低水位和高水位之间。当功能切换开关按下时，高水位时继电器吸合（外接电磁阀工作），开始排水，水位降到低水位时继电器断开（电磁阀停止工作），待水位再次升高到高水位时继电器再次吸合，上述过程循环。此功能应用在自动排水设备中，可让水位维持在低水位和高水位之间。
二、工作原理
整个系统由震荡电路、LED指示电路、继电器驱动电路、基准电压、电源电路及传感器电路构成。
1.震荡电路:U1A及外围元件组成一个多谐振动器，工作在放大器比较状态。R1和R12对5V进行分压，R3为反馈电阻，共同作为同相输入3脚的基准电压V+，反相输入端2脚V-取自R2、C1组成积分电路C1两端。V+与V-进行比较决定输出SIG电压的高低，由于C1不断在正反两个方向充电和放电，使V-的电压不断打印V+和小于V+，输出的SIG电压也就不断在高低电平间翻转，这样就产生了系统所需的震荡信号SIG。

2.LED指示灯电路:此电路包括整流滤波和电压比较两部分。C2为耦合电容，D1、D2整流，C4滤波，在R4上形成整流滤波后的电压作为U1B反相输入端电压。同相输入端电压由基准电压VREF提供，同相输入端电压和反相输入端电压进行比较，若同相输入端电压大于反相输入端电压则输出高电平；反之输出低电平。J1和J2外接水位传感器。相当于是由水位控制的两个开关，低水位时J1和J2均为开路状态，R4和R13上无电压。此时U1的7脚和8脚均输出高电平，故只有红色D6（低水位指示）发光。中水位时，水位传感器使J1短路，SIG信号经C8耦合、经液体到C7耦合、D4和D5整流、C9滤波在R13上形成电压作为U1C反相输入端电压；此电压大于U1C同相输入端电压，所以8脚输出低电平，红色D6（低水位指示灯）熄灭，D7黄色（中水位指示灯）发光。高水位时，水位传感器使J2也短路，SIG信号经过C3耦合、经液体到C2耦合，D1和D2整流、C4滤波再R4上形成电压作为U1B反相输入端电压；此电压大于U1B同相输入端电压，所以7脚输出低电平，红色D7（中水位指示灯）熄灭，D3绿色（高水位指示灯）发光。

3.继电器驱动电路:LED指示电路中的两个输出端7脚和8脚经过R8和R16分压后得到VIN7电压作为U1D电压比较器的反相输入端电压；同相输入端电压由基准电压VREF提供，VREF大于VIN时，14脚输出高电平，反之输出低电平。S1为功能切换开关，以14脚输出低电平为例来说明功能切换开关的工作原因，功能1（原理图上开关弹起）低电平经过R21限流到Q2的基极，Q2截止，继电器不工作。功能2（原理图上的开关按下去）低电平经R2限流到Q1的基极，Q1截止，5V电压(高电平）经R22再经开关到Q2的基极，Q2导通，继电器工作。

4.基准电压:由R10与R11串联分压获得基准电压，C10起到进一步稳定基准电压的作用。电阻分压计算公式为VREF=5*R11/(R10+R11)

5.电源电路:J3外接5V电源，C5、C6滤波。

6.传感器电路:由2组镀锡走线构成，较长一组为中水位感应线，较短的一组为高水位感应线。

## 性能评估
一.预期：
根据水位高低的变化通过继电器控制自动浇水，并且将水位传递给网关组以实现水位警报功能
二.测试结果：
测试结果基本满足预期，并总结出产品的优点与不足
产品有以下优点：
（1）能够实现灵敏的继电器的控制，
（2）水位检测灵敏并且现象明显，将水位分成了三个等级，低水位，适中水位以及高水位，分别通过红灯，黄灯，绿灯来表示。
（3）产品小巧便于安放，适用于任何环境
产品也有一定不足：
（1）.指示灯显示不正常，原因是传感器模块入水太深影响了内部电路，
（2）.电路只能使用6至9v电源，如果电源电压过高会烧坏电路，电源电压过低指示灯的显示不正常。

## 全生命周期成本和产品报价

## 环境影响


本次我们制作的是一个水位检测自动抽水控制模块，以下的有关环境影响的分析分为三个部分，分别分析在制作中、投入生产后的影响以及所用主要元件在使用后的回收问题。
在我们制作的过程时，我们将所购买的原材料进行焊接和组装，在此过程中，除了焊接时排放的烟气对环境有一定的影响和之外，我们使用的传统的制作方法对环境影响极小。若实现大工厂生产，我们可以考虑采用更高效的焊接方法，使用激光在一个封闭的仪器中进行焊接，这样既提高了生产效率，又通过封闭系统的烟气排放处理系统将产生的废气集中净化处理，可尽量减少对大气环境的影响。
在投入生产后，我们计划将水位仪放入水稻田中进行使用，所以我们需要考虑的就是此模块对水和水稻的影响。在水下工作时，最容易发生便是水导致电路部分短路烧坏的情况，在使用过程中，我们只需要将传感器插入水稻田即可，在排除特大洪灾的情况下，传感器不会一般不会对水环境和水稻产生不良影响。 
关于水位检测自动抽水控制模块中所使用的主要元件的妥善处理和回收问题，我们接下来对所使用到的元件进行逐一分析：
1、首先我们使用的电源为5V的无汞电池，无任何排放，除了在电池耗尽之时，现国际上通行的废旧电池处理方式大致有三种：固化深埋、存放于废矿井、回收利用。但考虑到前两者的处理方法在一定程度上都会对大环境产生影响，我们可考虑将电池经过特殊处理来进行循环利用。另外，需要特别注意的是，由于电池中的汞对环境有害，为了保护环境，在购买时应选用商标上标有无汞字样的电池。
2、对于所使用的控制主板PCB，在已经损坏的情况下，我们可以将PCB板进行脱漆、破碎和分选的工序，分选出来的物质，就可以再利用。其中，由于PCB表面涂有保护金属，脱漆剂有有机脱漆剂和碱性脱漆剂，有机脱漆剂毒性大，对人体和环境危害大，应使用氢氧化钠、缓蚀剂等加热溶解。关于继电器的处理方法，经过浏览器检索，可考虑将大量继电器交给专业的二手回收公司进行回收；
3、在此模块中，我们使用到了四种电容，分别为：104瓷片电容、223独石电容、25V100UF电解电容和25V100UF电容，一种废旧电解电容器的处理与资源化回收方法,首先将废旧铝电解电容器置于热处理装置中进行非金属组分的热解，热解温度为400～600摄氏度，热解时间为0.5~2小时，热处理气氛为空气;然后对得到的热解残留物破碎至金属组分与非金属组分完全解离;之后用0.1～0.3mm的筛网对破碎后的混合颗粒进行筛分处理,分别得到非金属热解残渣粉末和铝铁金属混合颗粒;最后对铝铁金属混合颗粒进行磁选处理,将铁金属颗粒与铝金属颗粒完全分离回收。本发明实现铝和铁的高回收率、高纯度回收,且处理过程清洁,不向环境中排放任何有毒有害物质,具有操作简便、流程短、高效、环保、资源化程度高的特点,适合大规模工业化应用。各项目标均达国度规范。

## 社会影响 

近年社会影响评价得到了越来越广泛的重视，应重视社会影响分析在项目决策中的作用在工程项目的咨询工作中，在我们的项目中我们主要从以下三个方面评估项目对社会的影响：社会影响效果、社会适应性分析、社会风险以应对策略。

### 一、社会影响效果

  项目对所在地居民收入的影响：项目的使用可以提高当地居民水稻的生产效率，减少劳动成本，提高居民收入。
  
  项目对所在地居民就业的影响：该项目的投入使用分为两种情况：一是应用于大型种植工厂中，该项目的投入使用在一定程度上将会减少对工厂对工人的需求，也就是说，居民面临就业岗位将会变少，就业压力变大的情况。二是应用于小型传统的个体户种植中，该项目的使用将会为居民减少劳动时间，可以将多余的时间用于其他劳动生产中，使居民自己的就业情况改善。

  项目对所在地居民的生活水平和生活质量的影响：居民种植农作物的生产效率变高，居民平均收入将会提升.居民的生活水平和生活质量也会相应提升。
  
  项目对所在地不同利益相关者的影响：项目对所在地区教育、文化、卫生的影响：当地经济的提升将会带动当地教育的发展、文化、卫生的发展。
  
  项目对当地基础设施、社会服务容量的影响：经济发展带动当地基础设施的发展，当地社会服务容量加大。

### 二、社会适应性分析

a.分析预测项目直接相关的不同直接利益相关者对项目建设和运营的态度及参与程度:态度积极、参与度高

b.分析预测项目所在地各类组织对项目建设和运营的态度：态度积极、参与度高

c.分析预测项目所在地现有社会环境、人文条件能否适应项目建设和发展需要：适合


### 三、社会风险及应对策略
  在社会影响效果分析和社会适应性分析基础上，在社会影响效果分析和社会适应性分析基础上，针对项目的不利影响，是否会遭到反对，进而针对项目的不利影响，是否会遭到反对，进而引发社会矛盾，提出征地拆迁、移民安置、补引发社会矛盾，提出征地拆迁、移民安置、补偿标准、环境保护等方案可能存在或应注意的偿标准、环境保护等方案可能存在或应注意的问题以及可能出现的社会风险因素。问题以及可能出现的社会风险因素.针对可能出现的重要风险因素，提出规避风险针对可能出现的重要风险因素，提出规避风险的对策措施。

## 学习收获


在工程概论这门课上，我们的课程主要以中期为分界线分为前后两个部分，前半期我们通过分组翻译《Exploring Engineering》这本书学习了在一个工程中作为一个工程师的角色需要了解的各个方面，从理论到实践，以及涉及到的各个领域的专业知识。
作为一名工程师，不仅需要强大的理论知识，还需要极强的实践精神和动手能力，前者就需要靠平时上课的日积月累，后者在这门课程的后半部分小有实践。第一次的实践中，我们通过节点和网关的通信，实现了将节点测得的温度数据进行传输，在首次实践中，我们学习到了焊接的技术和了解节点和网关的通信原理，在焊接中更多的考验的是耐心和细心。第二次的实践中，我们需要在户外旅行、智慧农业等几个主题中进行选择，经过小组讨论，基于我们的认知，选择了智慧农业。头脑风暴、集思广益，结合实际应用，考虑到中国南方多种水稻，小组确定做一个检测水稻水位的预警系统。根据材料设计图纸，完成前期工作。我们先从包装做起，由于是水下工作，考虑防水性问题，我们需要做一个完全封闭的密闭盒子，采用激光切割裁出一个长宽高都约为8厘米的盒子，用双面胶粘起来即可。拿到老师下发的材料后，我们发现材料并不防水，无法在水下工作，面临这个难题，我们只得自行在网上购买防水材料的传感器，经过焊接组装初步得到了我们想要的产品，实现初步设计！接下来是调试阶段，将传感器插入水下，功能基本实现，但是会出现一些警报灯不灵的现象，通过更换led灯和重新焊接等方法调试，功能基本稳定。
从头脑风暴、视频剪辑到设计制作，离不开小组的密切合作，组长发挥统筹作用，结合每个组员的特长，合理分配任务，按时推进进度，保证最后顺利完成。完整的小组作业离不开密切的小组合作！
“纸上得来终觉浅，绝知此事要躬行。”在短暂的实践过程中，我们深深的感觉到自己所学知识的肤浅和在实际运用中的专业知识的匮乏，刚开始的一段时间里，感到无从下手，茫然不知所措。在学校总以为自己学的不错，一旦接触到实际，才发现自己知道的是多么少，这时才真正领悟到“学无止境”的含义!

## 设计需求：

元件名称 数量

控制主板PCB 1

探头板 1

XH2.54-2P直座 3

XH2.54-2P弯座 2

XH2.54-2P单头线 1

XH2.54-2P双头线 2

KF301-3P座 1

5V 继电器 1

8*8自锁开关 1

104瓷片电容 6

223独石电容 1

5MM LED 绿色 1

5MM LED 黄色 1

5MM LED 红色 2

1N4148二极管 5

14PIC座 1

LM324芯片 1

220欧电阻 1

1K电阻 2

2.2K电阻 3

4.7K电阻 1

10K电阻 2

47K电阻 9

100K电阻 2

1M电阻 2

25V100UF电解电容 1

25V10UF电容 1

8050三极管 2



