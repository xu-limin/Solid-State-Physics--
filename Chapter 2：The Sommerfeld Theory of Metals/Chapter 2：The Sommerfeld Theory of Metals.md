# Chapter 2：The Sommerfeld Theory of Metals

在德鲁德的时代，以及之后的许多年里，似乎有理由假设电子速度分布，就像密度为$n=N/V$的普通经典气体一样，在温度$T$下平衡状态时由麦克斯韦-玻尔兹曼分布给出。这给出了单位体积中速度在范围$d\mathbf{v}$内的电子数，约为$f_B(\mathbf{v})d\mathbf{v}$，其中
$$
f_{B}(\mathbf{v})=n\left(\frac{m}{2 \pi k_{B} T}\right)^{3 / 2} e^{-m v^{2} / 2 k_{B} T}
$$
我们在第一章中看到，结合Drude模型，这在数量级上符合Wiedemann-Franz定律，但也预测了没有观察到的每个金属对金属比热的$\frac32k_B$贡献。

这一悖论在德鲁德模型上投下了四分之一个世纪的阴影，直到量子理论的出现和人们认识到对于电子来说，泡利不相容原理要求用费米-狄拉克分布取代麦克斯韦-玻尔兹曼分布(1)，才消除了这一悖论：
$$
f(\mathbf{v})=\frac{(m / \hbar)^{3}}{4 \pi^{3}} \frac{1}{\exp \left[\left(\frac{1}{2} m v^{2}-k_{B} T_{0}\right) / k_{B} T\right]+1} .
$$
这里$\hbar$是普朗克常数除以$2\pi$,$T_0$是一个温度，其由归一化条件决定：
$$
n=\int d \mathbf{v} f(\mathbf{v})
$$
通常是几万度。在感兴趣的温度下(即小于$10^3\mathrm{K}$)，麦克斯韦-玻尔兹曼分布和费米-狄拉克分布在金属电子密度下有很大的不同(图1)。

<img src="https://github.com/Handsome-fat-boy/Solid-State-Physics--/raw/main/Chapter%202%EF%BC%9AThe%20Sommerfeld%20Theory%20of%20Metals/1.png" alt="avr" style="zoom:80%;" />

在这一章中，我们将描述费米-狄拉克分布(2)背后的理论，并概述金属电子气的费米-狄拉克统计的结果。

在发现需要泡利不相容原理来解释原子的束缚电子态后不久，Sommerfeld将同样的原理应用于金属的自由电子气，从而解决了早期Drude模型中最明显的热反常。在大多数应用中，Sommerfeld的模型只不过是Drude的经典电子气加上一个修正，即电子速度分布被认为是量子费米-狄拉克(Fermi-Dirac)分布而不是经典的麦克斯韦-玻尔兹曼分布。为了证明费米-狄拉克分布的使用及其大胆嫁接到其他经典理论上的合理性，我们必须研究电子气的量子理论。

为简单起见，在研究非零温度下的电子气之前，我们将先研究电子气的基态(即$T=0$)。事实证明，基态的性质本身就很有趣：我们会发现，**对于金属密度下的电子气来说，室温确实是一个非常低的温度，在许多情况下，它与T=0没有什么区别**。因此，即使在室温下，金属的许多(虽然不是全部)电子性质与$T = 0$时的值几乎没有差别。

## 电子气的基态性质

我们必须计算限制在体积$V$中的$N$个电子的基态性质。由于电子之间不相互作用(独立电子近似)，我们可以通过首先找到体积$V$中单个电子的能级，然后用与泡利不相容原理一致的方式填充这些能级，从而找到$N$个电子系统的基态。

单个电子可以用波函数$\psi(\mathbf{r})$和它的自旋来描述。如果电子没有相互作用，则与能级相关的单电子波函数满足与时间无关的薛定谔方程：
$$
-\frac{\hbar^{2}}{2 m}\left(\frac{\hat{c}^{2}}{\partial x^{2}}+\frac{\hat{\partial}^{2}}{\partial y^{2}}+\frac{\partial^{2}}{\partial z^{2}}\right) \psi(\mathbf{r})=-\frac{\hbar^{2}}{2 m} \nabla^{2} \psi(\mathbf{r})=\mathcal{E} \psi(\mathbf{r})
$$
我们将用方程(2.4)上的边界条件表示电子对体积V的限制(通过离子的吸引)。在处理与金属表面的影响没有明确关系的问题时，边界条件的选择在相当大程度上取决于数学上的方便性，因为如果金属足够大，我们应该期望它的整体性质不受其表面的详细配置的影响。本着这种精神，我们首先选择金属的形状，以适应我们分析的方便性。由来已久的选择是边长为$L=V^{1/3}$的立方体。

接下来，我们必须在薛定谔方程(4)上附加一个边界条件,反映了电子被限制在这个立方体中的事实。我们之所以做出这个选择，也是因为我们相信它不会影响计算的批量属性。**一种可能是要求波函数$\psi(\mathbf{r})$当$\mathbf{r}$位于立方体表面时为$0$。然而，这通常是不令人满意的，因为它导致(4)的驻波解，而电子导致的电荷和能量的传输从行波的角度来讨论要方便得多**。更令人满意的选择是通过完全处理表面来强调表面的不合理。我们可以通过想象立方体的每个面都连接到它对面的面来实现这一点，这样到达表面的电子不会反射回金属，而是离开金属，同时在相反表面的相应点重新进入。因此，如果我们的金属是一维的，我们就会简单地用一个圆周$L$来代替电子被限制到的从$0$到$L$的线。在三维空间中，边界条件的几何体现，即立方体上的三对相对的面被连接在一起，在三维空间中从拓扑上是不可能建立起来。然而，边界条件的解析形式很容易推广。在一维中，金属的圆形模型导致边界条件$\psi(x+L)=\psi(x)$，并且其推广到三维立方体是显而易见的:
$$
\begin{aligned}
\psi(x, y, z+L) &=\psi(x, y, z) \\
\psi(x, y+L, z) &=\psi(x, y, z) \\
\psi(x+L, y, z) &=\psi(x, y, z)
\end{aligned}\tag{5}
$$


方程(5)称为Born-von Karman(或周期)边界条件。我们会经常遇到它(有时是略微泛化的形式)。

我们现在解方程$(4)$，解为
$$
\psi_{\mathrm{k}}(\mathbf{r})=\frac{1}{\sqrt{V}} e^{i \mathbf{k} \cdot \mathrm{r}}\tag{6}
$$
带有能量
$$
\mathcal{E}(\mathbf{k})=\frac{\hbar^{2} k^{2}}{2 m}\tag{7}
$$
其中$\mathbf{k}$是任何与位置无关的向量。我们选取了(6)中的归一化常数，这样在整个体积中找到电子的概率为$1$：
$$
1=\int d \mathbf{r}|\psi(\mathbf{r})|^{2}\tag{8}
$$
为了看到矢量$\mathbf{k}$的重要性，请注意，能级$\psi_{\mathbf{k}}(\mathbf{r})$是动量算符的本征态，
$$
\mathbf{p}=\frac{\hbar}{i} \frac{\partial}{\hat{\mathrm{r}}}=\frac{\hbar}{i} \boldsymbol{\nabla}, \quad\left(\mathbf{p}_{x}=\frac{\hbar}{i} \frac{\partial}{\partial x}, \quad \text { etc. }\right)\tag{9}
$$
特征值为$\mathbf{p}=\hbar\mathbf{k}$.

由于处于算符本征态的粒子具有由本征值给出的相应可观测值的确定值，所以处于$\psi_{\mathbf{k}}(\mathbf{r})$能级的电子具有与$\mathbf{k}$成正比的确定动量：
$$
\mathbf{p}=\hbar\mathbf{k}\tag{11}
$$
和速度
$$
\mathbf{v}=\mathbf{p}/m=\frac{\hbar\mathbf{k}}{m}\tag{12}
$$
从这个角度来看，能量$(7)$可以被写成类似的经典形式：
$$
\varepsilon=\frac{p^{2}}{2 m}=\frac{1}{2} m v^{2}\tag{13}
$$
我们也可以把$\mathbf{k}$解释为波矢。平面波$e^{i\mathbf{k}\cdot\mathbf{r}}$在垂直于$\mathbf{k}$的任何平面上都是常数，它沿平行于$\mathbf{k}$的直线呈周期性，波长为
$$
\lambda=\frac{2\pi}{k}\tag{14}
$$
这是著名的德布罗意波长。

现在，我们使用边界条件$(5)$，这就导致了只有一些离散的$\mathbf{k}$值是允许的，因为
$$
e^{i k_{x} L}=e^{i k_{y} L}=e^{i k_{z} L}=1 .\tag{15}
$$
所以波矢$\mathbf{k}$的分类具有形式：
$$
k_{x}=\frac{2 \pi n_{x}}{L}, \quad \dot{k}_{y}=\frac{2 \pi n_{y}}{L}, \quad k_{z}=\frac{2 \pi n_{z}}{L}, \quad n_{x}, n_{y}, n_{z} \text { integers. }\tag{16}
$$
因此，在具有笛卡儿轴$k_x,k_y,k_z$的三维空间(称为$\mathbf{k}$**空间**)中，允许的波向量是其沿三个轴的坐标由$2n/L$的整数倍给出的那些，如图2.2(二维)所示。

<img src="https://github.com/Handsome-fat-boy/Solid-State-Physics--/raw/main/Chapter%202%EF%BC%9AThe%20Sommerfeld%20Theory%20of%20Metals/2.png" alt="avr" style="zoom:80%;" />

通常，量子化条件(16)的唯一实际用途是：人们通常需要知道在$2\pi/L$尺度上巨大的$\mathbf{k}$空间区域中包含多少$\mathbf{k}$的允许值，因此包含大量允许点。如果区域非常大，那么允许的点的数量近似为区域内包含的k空间的体积，除以网络中每个k空间点的体积。后者的体积(参见图2.2)仅为$(2\pi/L)^3$。因此我们得出结论，体积$\Omega$的$\mathbf{k}$空间的区域将包含
$$
\frac{\Omega}{(2 \pi / L)^{3}}=\frac{\Omega V}{8 \pi^{3}}\tag{17}
$$
个允许的$\mathbf{k}$点，或者等价地说，$\mathbf{k}$空间的单位体积允许的$\mathbf{k}$值的数量(也称为$\mathbf{k}$空间的**能级密度**)是
$$
\frac{V}{8\pi^3}\tag{18}
$$
在实践中，我们将处理非常大($~10^{22}$点)、非常规则(通常为球体)的$\mathbf{k}$空间区域，因此(17)和(18)都可以被认为是精确的。我们将很快开始应用这些重要的计数公式。

因为我们假设电子是不相互作用的，所以我们可以通过把电子放入我们刚刚发现的允许的单电子能级来建立$N$个电子的基态。泡利不相容原理在这一结构中起着至关重要的作用(就像它在建立许多电子原子态时一样)：我们在每个单电子能级上最多只能放置一个电子。单电子能级由波矢$\mathbf{k}$和电子自旋沿任意轴的投影指定，可以取两个值$\hbar/2$或$-\hbar/2$中的任何一个。因此，与每个允许的波矢$\mathbf{k}$相关的是两个电子能级，每个电子自旋方向一个。

因此，在建立$N$个电子的基态时，我们首先将两个电子放入单电子能级$\mathbf{k}=0$，这是单电子能量$\varepsilon=0$最低的能级。然后，我们继续添加电子，依次填充尚未占据的最低能量的单电子能级。由于单电子能级的能量与其波矢的平方成正比(见(7))，当$N$很大时，占据的区域将无法与球体区分开来(如果它不是球形的，它就不是基态，因为我们可以通过将离k=0最远的能级中的电子移动到离原点更近的空能级来构建一个较低能量的状态)。这个球体的半径称为$k_F$[$F$表示费米]，其体积$\Omega$为$4\pi k_F^3/3$。根据(17)，球体内$\mathbf{k}$的允许值的个数为
$$
\left(\frac{4 \pi k_{F}^{3}}{3}\right)\left(\frac{V}{8 \pi^{3}}\right)=\frac{k_{F}^{3}}{6 \pi^{2}} V\tag{19}
$$
因为每个允许的$\mathbf{k}$值导致两个单电子能级(每个自旋值一个)，为了容纳$N$个电子，我们必须有
$$
N=2 \cdot \frac{k_{F}^{3}}{6 \pi^{2}} V=\frac{k_{F}^{3}}{3 \pi^{2}} V\tag{20}
$$
因此，如果我们在体积$V$中有$N$个电子(即，电子密度$n=N/V$)，那么$N$个电子系统的基态是通过占据所有$\mathbf{k}$小于等于$k_F$的单粒子能级，并留下所有$\mathbf{k}$大于$k_F$的空能级未被占据，其中$k_F$由以下条件给出：
$$
n=\frac{k_{F}^{3}}{3 \pi^{2}}\tag{21}
$$
这种自由而独立的电子基态用一些相当没有想象力的术语来描述：

半径为$k_F$(费米波矢)的球体包含被占据的一个电子能级，称为**费米球**。

费米球的表面，将被占据的能级与未占据的能级分开，称为**费米面**。(从第八章开始，我们将看到**费米面是现代金属理论中的基本结构之一；通常它不是球形的**。)

占据的最高能级的单电子能级的动量$\hbar k_F=p_F$称为**费米动量**；它们的能量$\varepsilon_F=\hbar^2k_F^2/2m$是**费米能量**；它们的速度$v_F=p_F/m$是**费米速度**。**费米速度在金属理论中的作用相当于经典气体中的热速度**，$v=(3k_BT/m)^{1/2}$。

所有这些量都可以用传导电子密度，通过方程(21)来计算。为了从数值上估计它们，通常用无量纲参数$r_s/a_0$来表示它们更为方便，在金属元素中，$r_s/a_0$大约从$2$变化到$6$。我们有
$$
k_{F}=\frac{(9 \pi / 4)^{1 / 3}}{r_{s}}=\frac{1.92}{r_{s}}\tag{22}
$$
或者
$$
k_{F}=\frac{3.63}{r_{s} / a_{0}} \mathring{A}^{-1}\tag{23}
$$
由于费米波矢是逆埃量级的，所以最高能电子的德布罗意波长是埃量级的。

费米速度为
$$
v_{F}=\left(\frac{\hbar}{m}\right) k_{F}=\frac{4.20}{r_{s} / a_{0}} \times 10^{8} \mathrm{~cm} / \mathrm{sec}\tag{24}
$$
这是一个相当大的速度(大约是光速的1%)。从经典统计力学的观点来看，这是一个相当令人惊讶的结果，因为我们描述的是基态($T=0$)，而经典气体中的所有粒子在$T=0$时都是零速度。即使在室温下，具有电子质量的经典粒子的热(即平均)速度也只有$107cm/s$量级。

费米能可以方便地写成以下形式(因为$a_0=\frac{\hbar^2}{me^2}$):
$$
\varepsilon_{F}=\frac{\hbar^{2} k_{F}{ }^{2}}{2 m}=\left(\frac{e^{2}}{2 a_{0}}\right)\left(k_{F} a_{0}\right)^{2}\tag{25}
$$
这里的$e^2/2a_0$，称为里德堡(Ry)，是氢原子的基态结合能，13.6电子伏特。里德堡是一个方便的原子能量单位，就像玻尔半径是原子距离一样方便。由于$k_Fa_0$是单位$1$的数量级，所以式(25)证明了费米能具有典型原子结合能的量级。利用(23)和$a_0=0.529×10^{-8} \mathrm{cm}$，我们得到了显式的数值形式:
$$
\varepsilon_{F}=\frac{50.1 \mathrm{eV}}{\left(r_{s} / a_{0}\right)^{2}}\tag{26}
$$
表明金属元素密度的费米能量范围在$1.5$到$15$电子伏特之间。

表2.1列出了金属的费米能量、速度和波矢量,其传导电子密度在表1.1中给出了。

<img src="https://github.com/Handsome-fat-boy/Solid-State-Physics--/raw/main/Chapter%202%EF%BC%9AThe%20Sommerfeld%20Theory%20of%20Metals/3.png" alt="avr" style="zoom:80%;" />

为了计算体积$V$中$N$个电子的基态能量，我们必须把费米球内所有单电子能级的能量加起来：
$$
E=2 \sum_{k<k_{F}} \frac{\hbar^{2}}{2 m} k^{2}\tag{27}
$$
一般地，在所有允许的$\mathbf{k}$值上对任何光滑函数$F(\mathbf{k})$求和时，可以如下进行：

因为每个允许的$\mathbf{k}$值的$\mathbf{k}$空间的体积是$\Delta \mathbf{k}=\frac{8\pi^3}{V}$,它可以很方便地写成以下形式
$$
\sum_{\mathbf{k}} F(\mathbf{k})=\frac{V}{8 \pi^{3}} \sum_{\mathbf{k}} F(\mathbf{k}) \Delta \mathbf{k}\tag{28}
$$
在$\Delta\mathbf{k}\to 0$(即$V\to\infty$)的极限下，只要$F(\mathbf{k})$在$2\pi/L$数量级的$\mathbf{k}$空间距离上变化不是很大($F$不满足这一条件的最著名的例子是理想玻色气体的凝结。在金属的应用中，从来没有出现过这种问题），求和$\sum F(\mathbf{k})\Delta\mathbf{k}$可以用积分$\int d\mathbf{k} F(\mathbf{k})$近似。因为我们将(28)重写为
$$
\lim _{V \rightarrow \infty} \frac{1}{V} \sum_{\mathbf{k}} F(\mathbf{k})=\int \frac{d \mathbf{k}}{8 \pi^{3}} F(\mathbf{k})\tag{29}
$$
在将(29)应用于有限但宏观大的系统时，人们总是假设$(1/V)\sum F(\mathbf{k})$与其无限体积极限的差别可以忽略不计(例如，假设$1$立方厘米的铜中的单位体积的电子能量与$2$立方厘米中的单位体积的电子能量相同)。

使用$(29)$去计算$(27)$,我们发现电子气的能量密度为：
$$
\frac{E}{V}=\frac{1}{4 \pi^{3}} \int_{k<k_{F}} d \mathbf{k} \frac{h^{2} k^{2}}{2 m}=\frac{1}{\pi^{2}} \frac{\hbar^{2} k_{F}^{5}}{10 m}\tag{30}
$$
为了找到基态下每个电子的能量$E/N$,我们需要使用$N/V=k_F^3/3\pi^2$,这给出了
$$
\frac{E}{N}=\frac{3}{10} \frac{\hbar^{2} k_{F}^{2}}{m}=\frac{3}{5} \varepsilon_{F}\tag{31}
$$
我们也可以将这个结果写为
$$
\frac{E}{N}=\frac{3}{5} k_{B} T_{F}\tag{32}
$$
这里$T_F$,费米温度，是
$$
T_{F}=\frac{\varepsilon_{F}}{k_{B}}=\frac{58.2}{\left(r_{s} / a_{0}\right)^{2}} \times 10^{4} \mathrm{~K}\tag{33}
$$
注意，与此相反，经典理想气体中每个电子的能量$\frac32k_BT$在$T = 0$时为$0$，只有在$T=\frac25T_F\approx10^4K$时才能达到和(32)差不多大的值。

给定基态能量$E$，人们可以根据关系式$P=-(\partial E/\partial V)_N$来计算电子气施加的压力。由于$E=\frac35N\varepsilon_F$且$\varepsilon_F$与$k_F^2$成正比($k_F^2$通过因子$N^{2/3}=(N/V)^{2/3}$依赖于V)，因此得出如下结论：
$$
P=\frac23\frac{E}{V}\tag{34}
$$
我们也可以计算压缩系数$K$,或者体模量，$B=1/K$,定义为：
$$
B=\frac{1}{K}=-V \frac{\partial P}{\partial V}\tag{35}
$$
因为$E$正比于$V^{-2/3}$,方程$(34)$显示$P$是随着$V^{-5/3}$变化的，因此
$$
B=\frac{5}{3} P=\frac{10}{9} \frac{E}{V}=\frac{2}{3} n \mathcal{E}_{F}\tag{36}
$$
或者
$$
B=\left(\frac{6.13}{r_{s} / a_{0}}\right)^{5} \times 10^{10} \text { dynes } / \mathrm{cm}^{2}\tag{37}
$$
在表2.2中，我们比较了几种金属由$rs/a0$计算的自由电子体模量(37)与测量的体模量。较重的碱金属是相对比较一致的，但即使(37)像贵金属一样大幅下降，它仍然大约是正确的数量级(尽管通过表格，它从太大的三倍到太小的三倍不等)。指望自由电子气体压力本身就能完全决定金属的抗压强度是荒谬的，但表2.2表明，这种压力至少与任何其他影响一样重要。

<img src="https://github.com/Handsome-fat-boy/Solid-State-Physics--/raw/main/Chapter%202%EF%BC%9AThe%20Sommerfeld%20Theory%20of%20Metals/4.png" alt="avr" style="zoom:80%;" />



## 自由电子气体的热性质:费米-狄拉克分布

当温度不是零时，有必要考察$N$个电子系统的激发态及其基态，因为根据统计力学的基本原理，如果一个$N$粒子系统在温度$T$处于热平衡状态，那么它的性质应该通过对所有$N$粒子稳态取平均值，并赋予每个能量态一个与$e^{-E/k_BT}$成比例的权重$P_N(E)$来计算:
$$
P_{N}(E)=\frac{e^{-E / k_{B} T}}{\sum e^{-E_{\alpha}^{N} / k_{B} T}}\tag{38}
$$
(这里$E_{\alpha}^N$是$N$电子系统的第$\alpha$个稳态的能量，求和是对所有这样的态。)

(38)的分母是著名的配分函数，与Helmholtz自由能$F=U-TS$（这里$U$是内能，$S$是熵）有关：
$$
\Sigma e^{-E_{\alpha}^N{/ k_{B} T}}=e^{-F_{N} / k_{B} T}\tag{39}
$$
因此我们可以将$(38)$写成下列形式：
$$
P_{N}(E)=e^{-\left(E-F_{N}\right) / k_{B} T}\tag{40}
$$
由于不相容原理，要构造一个$N$电子态，必须填充$N$个不同的单电子能级。因此，每个$N$电子的稳态可以通过列出在该状态下哪个$N$单电子能级被填充来指定。需要知道的一个非常有用的量是$f_i^N$，它是当$N$电子系统处于热平衡状态时，在特定的单电子能级$i$中存在电子的概率。这个概率仅仅是在占据第$i$个能级的$N$个电子态中的任何一个中找到$N$个电子系统的独立概率的总和：
$$
f_{i}^{N}=\sum P_{N}\left(E_{\alpha}^{N}\right) \quad\tag{41}
$$
(summation over all $N$ -electron  states $\alpha$ in which there is an electron in the one-electron level $i$ ).

我们可以通过下面三个观察来计算$f_i^N$:

1. 由于电子在能级$i$中的概率正好是$1$减去在能级$i$中没有电子的概率(这是不相容原理所允许的仅有的两种可能性)，我们同样可以将(41)写为：
   $$
   f_{i}^{N}=1-\sum P_{N}\left(E_{\gamma}^{N}\right) \quad\tag{42}
   $$
   (summation over all $N$ -electron  states $\gamma$ in which there is no electron in the one-electron level $i$ ).

2. 通过取其中在单电子能级$i$中有一个电子的任何$N+1$个电子态，我们可以通过简单地去除第i能级中的电子，而保持所有其他能级的占据不变，来构造其中在第$i$能级中没有电子的$N$电子态。此外，任何在单电子能级$i$中没有电子的$N$电子态都可以由一个在$i$能级中有电子的$N+1$电子态构成。显然，任何$N$电子态和相应的$N+1$电子态的能量差为$\varepsilon_i$。因此，具有未占据能级$i$的所有$N$电子态的能量集合与具有占据能级$i$的所有$N+1$电子态的能量集合相同，只要后一集合中的每个能量减少$\varepsilon_i$。因此，我们可以用特殊的形式重写(42)
   $$
   f_{i}^{N}=1-\sum P_{N}\left(E_{\alpha}^{N+1}-\varepsilon_i\right) \quad\tag{43}
   $$
   (summation over all $N+1$ -electron  states $\alpha$ in which there is an electron in the one-electron level $i$ ).

   但是方程(40)可以允许我们将求和写为：
   $$
   P_{N}\left(E_{\alpha}^{N+1}-\varepsilon_{i}\right)=e^{\left(\varepsilon_{i}-\mu\right) / k_{B} T} P_{N+1}\left(E_{\alpha}^{N+1}\right)\tag{44}
   $$
   这里$\mu$是我们熟悉的**化学势**，在温度$T$时为：
   $$
   \mu=F_{N+1}-F_N\tag{45}
   $$
   代入$(43)$得到
   $$
   f_{i}^{N}=1- e^{\left(\varepsilon_{i}-\mu\right) / k_{B} T}\sum P_{N+1}\left(E_{\alpha}^{N+1}\right)\tag{46}
   $$
   (summation over all $N+1$ -electron  states $\alpha$ in which there is an electron in the one-electron level $i$ ).

   将(46)与$(41)$对比，得到：
   $$
   f_{i}^{N}=1-e^{\left(\varepsilon_{i}-\mu\right) / k_{B} T} f_{i}^{\mathrm{N}+1}\tag{47}
   $$

3. 方程(47)给出了$N$电子系统和$N+1$电子系统在温度$T$时单电子能级$i$被占据的概率之间的精确关系。当$N$非常大时(我们通常对$10^{22}$量级的$N$感兴趣)，想象通过增加一个额外的电子，我们可以显著地改变这一概率，而不是几个微不足道的单电子能级，这是荒谬的。因此，我们可以在$(47)$中用$f_i^{N+1}$来代替$f_i^N$，这使得我们可以解出$f_i^N$:
   $$
   f_{i}^{N}=\frac{1}{e^{\left(\varepsilon_{i}-\mu\right) / k_{B} T}+1}\tag{48}
   $$

在后面的公式中，我们将在记号上省去$N$，在任何情况下，$f_i$和$N$的依赖都是通过化学势$\mu$传递的(45)。在给定$f_i$的情况下，注意$f_i$是单能级$i$中的平均电子数,$N$的值总是可以计算的。由于电子总数$N$正好是每个能级中的平均数在所有能级上的总和，
$$
N=\sum_{i} f_{i}=\sum_{i} \frac{1}{e^{\left(\varepsilon_{i}-\mu\right) / k_{B} T}+1}\tag{49}
$$
它将$N$确定为温度$T$和化学势$\mu$的函数。然而，在许多应用中，给出的是温度和$N$(或者更确切地说，密度，$n=N/V$)。在这种情况下，使用(49)来确定作为$n$和$T$的函数的化学势$\mu$，从而允许从有利于温度和密度的后续公式中消除它。然而，化学势本身就具有相当大的热力学意义。附录B中总结了它的一些重要属性。

## 自由电子气体的热性质:费米-狄拉克分布的应用

在自由和独立电子的气体中，单电子能级由波矢$\mathbf{k}$和自旋量子数$s$指定，能量独立于$s$(在没有磁场的情况下)，并由方程(7)给出,也即：
$$
\varepsilon(\mathbf{k})=\frac{\hbar^{2} k^{2}}{2 m}\tag{50}
$$
我们首先验证分布函数(49)与上面导出的基态($T=0$)性质是一致的。在基态中，只有那些$\varepsilon(\mathbf{k})\le\varepsilon_F$的能级被占据，所以基态分布函数必须是：
$$
\begin{aligned}
f_{\mathrm{ks}} &=1, \quad \varepsilon(\mathbf{k})<\mathcal{E}_{F} \\
&=0, \quad \mathcal{E}(\mathbf{k})>\mathcal{E}_{F}
\end{aligned}\tag{51}
$$
另一方面，当$T\to 0$时，费米-狄拉克分布（48）变为：
$$
\begin{aligned}
\lim _{t \rightarrow 0} f_{\mathrm{ks}} &=1, \quad \varepsilon(\mathbf{k})<\mu \\
&=0, \quad \mathcal{E}(\mathbf{k})>\mu
\end{aligned}\tag{52}
$$
所以
$$
\lim _{T \rightarrow 0} \mu=\mathcal{E}_{F}\tag{53}
$$
我们很快就会看到，对于金属来说，化学势在很高的精度上仍然等于费米能量，一直到室温。因此，人们在处理金属时往往不会区分这两者。然而，这可能具有危险的误导性。在精确计算中，必须跟踪化学势$\mu$与其零温度值$\varepsilon_F$的不同程度。

费米-狄拉克统计最重要的单一应用是计算电子对金属定容比热的贡献，
$$
c_{v}=\frac{T}{V}\left(\frac{\partial S}{\partial T}\right)_{V}=\left(\frac{\partial u}{\partial T}\right), \quad u=\frac{U}{V}\tag{54}
$$
在独立电子近似下，内能$U$正好是一个电子能级$\varepsilon(\mathbf{k})$乘以该能级上平均电子数再求和：
$$
U=2 \sum_{\mathbf{k}} \mathcal{E}(\mathbf{k}) f(\mathcal{E}(\mathbf{k}))\tag{55}
$$
我们引入了**费米函数**$f(\varepsilon)$，以强调$f_{\mathbf{k}}$仅通过电子能量$\varepsilon(\mathbf{k})$依赖于$\mathbf{k}$:
$$
f(\varepsilon)=\frac{1}{e^{(\varepsilon-\mu) / k_{B} T}+1}\tag{56}
$$
将$(55)$除以体积$V$,由$(29)$得到能量密度$u=U/V$:
$$
u=\int \frac{d \mathbf{k}}{4 \pi^{3}} \mathcal{E}(\mathbf{k}) f(\varepsilon(\mathbf{k}))\tag{57}
$$
如果我们将$(49)$除以$V$,我们得到
$$
n=\int \frac{d \mathbf{k}}{4 \pi^{3}} f(\mathcal{E}(\mathbf{k}))\tag{58}
$$
在计算像$(57),(58)$这样的积分时
$$
\int \frac{d \mathbf{k}}{4 \pi^{3}} F(\varepsilon(\mathbf{k}))\tag{59}
$$
人们经常利用这样一个事实，即被积函数仅通过电子能量$\varepsilon=\hbar^2k^2/2m$依赖于$\mathbf{k}$，方法是在球坐标中计算积分，并将变量从$\mathbf{k}$改变为$\varepsilon$：
$$
\int \frac{d \mathbf{k}}{4 \pi^{3}} F(\varepsilon(\mathbf{k}))=\int_{0}^{\infty} \frac{k^{2} d k}{\pi^{2}} F(\mathcal{E}(\mathbf{k}))=\int_{-\infty}^{\infty} d \varepsilon g(\mathcal{E}) F(\mathcal{E})\tag{60}
$$
这里
$$
\begin{aligned}
g(\varepsilon) &=\frac{m}{\hbar^{2} \pi^{2}} \sqrt{\frac{2 m \mathcal{E}}{\hbar^{2}}}, & & \mathcal{E}>0 \\
&=0, & & \varepsilon<0
\end{aligned}\tag{61}
$$
因为积分$(59)$是对$(1/V)\sum_{\mathbf{k}s}F(\varepsilon(\mathbf{k}))$的一个估计，所以$(60)$中的形式显示了
$$
g(\mathcal{E})d\mathcal{E}=(1/V)\times[\text{the number of one-electron levels in the energy range from}\quad\mathcal{E}\quad to \quad\mathcal{E}+d\mathcal{E}  ]\tag{62}
$$
因此，$g(\mathcal{E})$称为单位体积的能级密度(或通常简称为能级密度)。一种在维度上更透明的书写$g$的方式是:
$$
\begin{aligned}
g(\mathcal{E}) &=\frac{3}{2} \frac{n}{\varepsilon_{F}}\left(\frac{\varepsilon}{\varepsilon_{F}}\right)^{1 / 2}, & & \varepsilon>0 \\
&=0, & & \varepsilon<0
\end{aligned}\tag{63}
$$
其中$\mathcal{E}_F$和$k_F$由零温公式(21)和(25)定义。一个特别重要的数值是费米能的能级密度，(61)和(63)以两种等价形式之一给出：
$$
g\left(\varepsilon_{F}\right)=\frac{m k_{F}}{\hbar^{2} \pi^{2}}\tag{64}
$$
或者
$$
g\left(\varepsilon_{F}\right)=\frac{3}{2} \frac{n}{\varepsilon_{F}}\tag{65}
$$
使用这个记号，我们将$(57),(58)$重写为
$$
u=\int_{-\infty}^{\infty} d \varepsilon g(\varepsilon) \varepsilon f(\varepsilon)\tag{66}
$$
和
$$
n=\int_{-\infty}^{\infty} d \varepsilon g(\varepsilon) f(\varepsilon)\tag{67}
$$
我们这样做既是为了符号简单，也是因为在这种形式下，**自由电子近似只通过能级密度$g$的特定估计(61)或(63)进入**。我们可以定义能级密度，通过(62)，根据这个密度，(66)和(67)对任何一组不相互作用(即，独立的)电子仍然有效。因此，我们稍后把从(66)和(67)推导出的结果应用于金属中更复杂的独立电子模型。

一般来说，积分(66)和(67)具有相当复杂的结构。然而，有一个简单的系统展开，它利用了这样一个事实，即在几乎所有金属感兴趣的温度下，$T$都远远小于费米温度(33)。在图2.3中，绘制了$T=0$和室温下典型金属密度($k_BT/\mu\approx0.01$)下的费米函数$f(\mathcal{E})$。显然，f与它的零温形式只在$\mu$附近宽度为几$k_BT$的一个很小的区域内不同。因此，形式$\int_{-\infty}^{+\infty}H(\mathcal{E})f(\mathcal{E})d\mathcal{E}$的积分与它们的零温度值$\int_{-\infty}^{E_F}H(\mathcal{E})d\mathcal{E}$的不同将完全由$\mathcal{E}=\mu$附近的$H(\mathcal{E})$形式决定。如果$H(\mathcal{E})$在$\mu$的约$k_BT$数量级的能量范围内变化不大，则积分的温度依赖关系应该相当准确地给出，方法是用其在$\mathcal{E}=\mu$处的泰勒展开式中的头几项代替$H(\mathcal{E})$：
$$
H(\varepsilon)=\left.\sum_{n=0}^{\infty} \frac{d^{n}}{d \varepsilon^{n}} H(\mathcal{E})\right|_{\varepsilon=\mu} \frac{(\varepsilon-\mu)^{n}}{n !}\tag{68}
$$
这个过程在附录C中给出，结果是以下的形式:
$$
\int_{-\infty}^{\infty} H(\varepsilon) f(\varepsilon) d \varepsilon=\int_{-\infty}^{\mu} H(\mathcal{E}) d \varepsilon+\left.\sum_{n=1}^{\infty}\left(k_{B} T\right)^{2 n} a_{n} \frac{d^{2 n-1}}{d \varepsilon^{2 n-1}} H(\mathcal{E})\right|_{\varepsilon=\mu}\tag{69}
$$
这就是众所周知的**索末菲展开**。$a_n$是单位数量级的无量纲常数。人们通常遇到的函数$H$在$\mu$量级的能量标度上具有主要变化，并且通常$\frac{d^n}{d \varepsilon^n} H(\mathcal{E})|_{\varepsilon=\mu}$是$\frac{H(\mu)}{\mu^n}$量级的。在这种情况下，索末菲展开式中的连续项减小了$O(k_BT/\mu)^2$，在室温下为$O(10^{-4})$。因此，在实际计算中，只有第一项和第二项(非常偶尔)保留在(69)的求和中。具体形式如下(附录C)：
$$
\begin{aligned}
&\int_{-\infty}^{\infty} H(\varepsilon) f(\varepsilon) d \varepsilon \\
&\quad=\int_{-\infty}^{\mu} H(\varepsilon) d \varepsilon+\frac{\pi^{2}}{6}\left(k_{B} T\right)^{2} H^{\prime}(\mu)+\frac{7 \pi^{4}}{360}\left(k_{B} T\right)^{4} H^{\prime \prime \prime}(\mu)+O\left(\frac{k_{B} T}{\mu}\right)^{6}
\end{aligned}\tag{70}
$$
为了计算金属在比$T_F$小的温度下的比热，我们对电子能量密度和数密度(方程(66)和(67))采用索末菲展开(70):
$$
\begin{aligned}
&u=\int_{0}^{\mu} \varepsilon g(\mathcal{E}) d \varepsilon+\frac{\pi^{2}}{6}\left(k_{B} T\right)^{2}\left[\mu g^{\prime}(\mu)+g(\mu)\right]+O\left(T^{4}\right)
\end{aligned}\tag{71}
$$

$$
\begin{aligned}
&n=\int_{0}^{\mu} g(\mathcal{E}) d \mathcal{E}+\frac{\pi^{2}}{6}\left(k_{B} T\right)^{2} g^{\prime}(\mu)+O\left(T^{4}\right)
\end{aligned}\tag{72}
$$

正如我们现在将详细看到的那样，等式(72)暗示$\mu$与它$T=0$时的值$\mathcal{E}_F$相差$T^2$的阶。因此，对于$T^2$的阶，我们可以写
$$
\int_{0}^{\mu} H(\mathcal{E}) d \varepsilon=\int_{0}^{\varepsilon_{F}} H(\mathcal{E}) d \varepsilon+\left(\mu-\mathcal{E}_{F}\right) H\left(\varepsilon_{F}\right)\tag{73}
$$
如果我们将这个展开式应用于(71)和(72)中的积分，并在这些方程中用已经是$T^2$级的项将$\mu$替换为$\mathcal{E}_F$，我们会发现
$$
\begin{aligned}
u=& \int_{0}^{\varepsilon_{F}} \varepsilon g(\varepsilon) d \varepsilon+\mathcal{E}_{F}\left\{\left(\mu-\varepsilon_{F}\right) g\left(\varepsilon_{F}\right)+\frac{\pi^{2}}{6}\left(k_{B} T\right)^{2} g^{\prime}\left(\varepsilon_{F}\right)\right\} \\
&+\frac{\pi^{2}}{6}\left(k_{B} T\right)^{2} g\left(\varepsilon_{F}\right)+O\left(T^{4}\right)
\end{aligned}\tag{74}
$$

$$
n=\int_{0}^{\varepsilon_{F}} g(\varepsilon) d \mathcal{E}+\left\{\left(\mu-\mathcal{E}_{F}\right) g\left(\varepsilon_{F}\right)+\frac{\pi^{2}}{6}\left(k_{B} T\right)^{2} g^{\prime}\left(\varepsilon_{F}\right)\right\} .\tag{75}
$$

(74)和(75)右侧与温度无关的第一项正好是基态的$u$和$n$的值。因为我们是在恒定密度下计算比热，所以$n$与温度无关，(75)化为
$$
0=\left(\mu-\varepsilon_{F}\right) g\left(\varepsilon_{F}\right)+\frac{\pi^{2}}{6}\left(k_{B} T\right)^{2} g^{\prime}\left(\varepsilon_{F}\right)\tag{76}
$$
它决定了化学势与$\mu-\mathcal{E}_F$的偏差:
$$
\mu=\varepsilon_{F}-\frac{\pi^{2}}{6}\left(k_{B} T\right)^{2} \frac{g^{\prime}\left(\mathcal{E}_{F}\right)}{g\left(\varepsilon_{F}\right)}\tag{77}
$$
因为对于自由电子，$g(\mathcal{E})$变化为$\mathcal{E}^{1/2}$(见公式(63))。这给出了
$$
\mu=\varepsilon_{F}\left[1-\frac{1}{3}\left(\frac{\pi k_{B} T}{2 \varepsilon_{F}}\right)^{2}\right]\tag{78}
$$
如上所述，这是$T^2$量级的偏移，通常仅约0.01%，即使在室温下也是如此。等式(76)将(74)中大括号中的项设置为零，从而简化了恒定电子密度下的热能密度的形式：
$$
u=u_{0}+\frac{\pi^{2}}{6}\left(k_{B} T\right)^{2} g\left(\varepsilon_{F}\right)\tag{79}
$$
这里$u_0$是基态能量密度。因此电子气的比热为
$$
c_{v}=\left(\frac{\partial u}{\partial T}\right)_{n}=\frac{\pi^{2}}{3} k_{B}^{2} T g\left(\varepsilon_{F}\right)\tag{80}
$$
或者，对于自由电子（见(65)）,
$$
c_{v}=\frac{\pi^{2}}{2}\left(\frac{k_{B} T}{\varepsilon_{F}}\right) n k_{B}\tag{81}
$$
与理想气体的经典结果$c_v=3nk_B/2$相比较，我们看到费米-狄拉克统计量的作用是使比热降低一个与温度成正比的因子$(\pi^2/3)(k_BT/\mathcal{E}_F)$，即使在室温下也只有$10^{-2}$个数量级。这解释了电子自由度对金属室温比热没有任何可观察到的贡献。

如果人们愿意省去精确的数值系数，人们可以非常简单地从费米函数本身的温度依赖性来理解比热的这种行为。
当温度从$T=0$升高时，电子能量的增加完全是因为一些能量在低于$\mathcal{E}_F$约$O(k_BT)$(图2.4的暗阴影区域)的电子被激发到高于$\mathcal{E}_F$ (图2.4的浅阴影区域)的$O(k_BT)$能量范围。被如此激发的单位体积的电子数是能量间隔的宽度$k_BT$乘以单位体积的能级密度$g(\mathcal{E}_F)$。此外，激发能是$k_BT$量级，因此总热能密度比基态能高出$g(\mathcal{E}_F)(k_BT)^2$量级。这与精确结果(79)相差了$\pi^2/6$倍，但它给出了一个简单的物理图像，对于粗略估计很有用。

<img src="https://github.com/Handsome-fat-boy/Solid-State-Physics--/raw/main/Chapter%202%EF%BC%9AThe%20Sommerfeld%20Theory%20of%20Metals/5.png" alt="avr" style="zoom:80%;" />

线性比热的预测是费米-狄拉克统计学最重要的结果之一，它为金属的电子气理论提供了进一步的简单检验，前提是人们可以确定，除了电子自由度之外，其他自由度的贡献不能与之相提并论，甚至更大。碰巧的是，离子自由度完全控制了高温下的比热。然而，在远低于室温的情况下，它们的贡献随着温度的立方而下降(第23章)，并且在非常低的温度下，它们的贡献下降到电子贡献以下，而电子贡献只随T线性地减小。为了将这两个贡献分开，绘制$c_v/T$与$T^2$的关系图已经成为一种惯例，即，因为如果电子和离子贡献一起导致低温形式,
$$
c_{v}=\gamma T+A T^{3}\tag{82}
$$
则
$$
\frac{c_{v}}{T}=\gamma+A T^{2}\tag{83}
$$
因此，可以通过线性向下推算$c_v/T$曲线到$T^2=0$，并注意它与$c_v/T$轴相交的位置来求出$\gamma$。测量的金属比热通常包含一个线性项，该项在开尔文几度时可与立方项相媲美。

比热数据通常以焦耳(或卡路里)/摩尔/开尔文表示。由于一摩尔自由电子金属含有$ZN_A$个传导电子(其中$Z$是价，$N_A$是阿伏伽德罗常数)，并且占据体积$ZN_A/n$，我们必须将单位体积的热容$c_v$乘以$ZN_A/n$，才能得到每摩尔的热容，$C$：
$$
C=\frac{\pi^{2}}{3} Z R \frac{k_{B} T g\left(\varepsilon_{F}\right)}{n}\tag{84}
$$
其中$R = k_BN_A = 8.314$焦耳/摩尔=$1.99$卡路里/摩尔$-K$。利用能级的自由电子密度(65)和$\mathcal{E}_F/k_B$的估计(33)，我们发现了自由电子对每摩尔热容的贡献为$C = \gamma T$，其中
$$
\gamma=\frac{1}{2} \pi^{2} R \frac{Z}{T_{F}}=0.169 Z\left(\frac{r_{s}}{a_{0}}\right)^{2} \times 10^{-4} \mathrm{cal}-\mathrm{mole}^{-1}-\mathrm{K}^{-2}\tag{85}
$$
表2.3中显示了一些粗略的$\gamma$测量值，表1.1中显示了(85)表示的自由电子值和$rs/a0$的值。请注意，碱金属和贵金属(铜、银、金)仍然可以用自由电子理论很好地描述。然而，还要注意的是，铁和锰($10$倍理论级的实验)以及Bi和Sb($0.1$倍理论级的实验)的差异是惊人的。这些大偏差现在已经在相当普遍的基础上得到定性的理解，我们将在第15章回到它们。

<img src="https://github.com/Handsome-fat-boy/Solid-State-Physics--/raw/main/Chapter%202%EF%BC%9AThe%20Sommerfeld%20Theory%20of%20Metals/6.png" alt="avr" style="zoom:80%;" />



## 金属中的索末菲导电理论

为了求出电子在金属中的速度分布，考虑$\mathbf{k}$点附近$\mathbf{k}$空间的体积为$d\mathbf{k}$的一个小体积元素(小到费米函数和其他物理函数在整个体积元中变化可以忽略不计，但又大到它包含非常多的单电子能级)。考虑到双重自旋简并，该体积元素中的单电子能级数为(见(18))
$$
\left(\frac{V}{4 \pi^{3}}\right) d \mathbf{k}\tag{86}
$$
每个能级被占据的概率正好是$f(\mathcal{E}(\mathbf{k}))$，因此$\mathbf{k}$ 空间体积元素中的电子总数为
$$
\frac{V}{4 \pi^{3}} f(\varepsilon(\mathbf{k})) d \mathbf{k}, \quad \mathcal{E}(\mathbf{k})=\frac{\hbar^{2} \mathbf{k}^{2}}{2 m}\tag{87}
$$
由于具有波矢$\mathbf{k}$ 的自由电子的速度为$\mathbf{v}=\hbar \mathbf{k}/m$(等式(12))，则体积$d\mathbf{v}$约为$\mathbf{v}$的元素中的电子数与体积$d\mathbf{k}=(m/\hbar)^3d\mathbf{v}$约$\mathbf{k}=m\mathbf{v}/\hbar$的体积元素中的电子数相同。因此，在速度$\mathbf{v}$附近一个体积为$d\mathbf{v}$的速度空间元中，实空间单位体积中电子的总数是
$$
f(\mathbf{v}) d \mathbf{v}\tag{88}
$$
这里
$$
f(\mathbf{v})=\frac{(m / \hbar)^{3}}{4 \pi^{3}} \frac{1}{\exp \left[\left(\frac{1}{2} m v^{2}-\mu\right) / k_{B} T\right]+1}\tag{89}
$$
索默菲尔德重新审视了德鲁德模型，用费米-狄拉克分布(89)取代了经典的麦克斯韦-玻尔兹曼速度分布(1)。在其他经典理论中使用由量子力学论断构造速度分布需要一些证明。如果一个人能够在不违反测不准原理的情况下，根据需要精确地指定电子的位置和动量，那么就可以用经典的方法描述电子的运动。

典型的金属中电子的动量是$\hbar k_F$量级的，所以要想得到一个好的经典描述，它的动量$\Delta p$的不确定性必须比$\hbar k_F$小。由于从(22),$k_F\sim 1/r_s$开始，位置的不确定性必须满足
$$
\Delta x \sim \frac{\hbar}{\Delta p} \gg \frac{1}{k_{F}} \sim r_{s}\tag{90}
$$
其中，从(1.2)开始，$r_s$是平均电子间距离的量级，即埃。因此，如果人们必须考虑电子局域到原子距离内(也是埃的量级)，经典的描述是不可能的。然而，金属中的传导电子并不与特定的离子结合，而是可以在金属的体积中自由游动。在宏观样品中，对于大多数目的，不需要将它们的位置指定到$10^{-8}$厘米的精度。德鲁德模型主要假设只在以下两种情况下知道电子的位置：

1. 当施加空间变化的电磁场或温度梯度时，必须能够在比场或温度梯度变化的距离$\lambda$更小的尺度上指定电子的位置。对于大多数应用来说，外加的磁场或温度梯度在埃的尺度上不会有明显的变化，电子位置定义的必要精度不一定会导致其动量的不可接受的大不确定性。例如，与可见光相关的电场只在$10^3\mathring{A}$量级的距离上有明显的变化。然而，如果波长比这个距离短得多(例如X射线)，人们就必须用量子力学来描述由电场引起的电子运动。
2. 在Drude模型中还有一个隐含的假设，即人们可以将一个电子局域到比平均自由程$l$小得多的范围内，因此当出现比几十埃短得多的平均自由程时，人们应该对经典论点持怀疑态度。幸运的是，正如我们将在下面看到的，金属中的平均自由程在室温下约为$100\mathring{A}$，并且随着温度的下降而变得更长。

因此，经典力学很好地描述了金属电子的行为，这是一种广泛的现象。然而，这并不能立即证明$N$个这样的电子的行为可以用经典力学来描述。既然泡利不相容原理如此深刻地影响着N个电子的统计，为什么它不应该对它们的动力学产生类似的剧烈影响呢？它不是从一个初等定理推导出来的，我们在没有证明的情况下陈述这个定理，因为证明虽然简单，但名义上是相当繁琐的：

考虑一个由$N$个电子组成的系统，它们之间的相互作用被忽略，并且暴露在任意的依赖于空间和时间的电磁场中。设时间$0$时的$N$电子态是通过占据$N$个单电子能级$\psi_1(0),\psi_2(0),\cdots,\psi_N(0)$而形成的。如果只有一个电子存在，它在零时处于$\psi_j(0)$能级，令$\psi_j(t)$是在电磁场的影响下能级$\psi_j(0)$随时间$t$演化到的能级。那么在时间$t$的正确的$N$电子态将是通过占据$N$个单电子能级$\psi_1(t),\cdots,\psi_N(t)$的集合而形成的状态。

因此，通过考虑$N$个独立的单电子问题，完全确定了$N$个非相互作用电子的动力学行为。特别地，如果经典近似对于这些单电子问题中的每一个都是有效的，那么它也将适用于整个$N$电子系统。

费米-狄拉克统计量的使用只影响德鲁德模型的那些预测，这些预测需要一些电子速度分布的知识才能进行估计。
如果电子经历碰撞的速率$1/\tau$不取决于它的能量，那么，只有我们对电子平均自由程的估计以及我们对热导率和热功率的计算，才会受到平衡分布函数变化的影响。

* **平均自由程**：使用$v_F$(方程(24))作为经典电子速度的衡量，我们可以从方程(1.8)计算平均自由程$l=v_F\tau$:
  $$
  \ell=\frac{\left(r_{s} / a_{0}\right)^{2}}{\rho_{\mu}} \times 92 \AA\tag{91}
  $$
  由于电阻率以微欧厘米$\rho_{\mu}$为单位，在室温下通常为$1$到$100$，由于$r_s/a_0$通常为$2$到$6$，即使在室温下也可能有$100$埃的平均自由程长。

* **热导率**：我们使用(51)来估计热导率：
  $$
  \kappa=\frac{1}{3} v^{2} \tau c_{v}\tag{92}
  $$
  修正的比热(81)比经典的Drude猜想小一个数量级$k_BT/\mathcal{E}_F$因子；$v^2$的正确估计不是经典的$k_BT/m$量级的热均方速度，而是$v_F^2=2\mathcal{E}_F/m$，比经典值大$\mathcal{E}_F/k_BT$数量级的因子。在(92)中插入这些值，并消除弛豫时间，以有利于(1.6)的电导率，我们发现
  $$
  \frac{\kappa}{\sigma T}=\frac{\pi^{2}}{3}\left(\frac{k_{B}}{e}\right)^{2}=2.44 \times 10^{-8} \text { watt-ohm } / \mathrm{K}^{2}\tag{93}
  $$
  由于对$k_BT/\mathcal{E}_F$的阶进行了两次补偿性修正，这与Drude偶然获得的良好值非常接近，并且与表1.6中的数据非常吻合。我们将看到(第13章)洛伦兹数的这个值比(93)式的非常粗略的推导结果要好得多。

* **热功**：德鲁德对热功的过高估计也可以用费米-狄拉克统计来解决。将(81)式中的比热代入(1.59)式中，我们发现：
  $$
  Q=-\frac{\pi^{2}}{6} \frac{k_{B}}{e}\left(\frac{k_{B} T}{\varepsilon_{F}}\right)=-1.42\left(\frac{k_{B} T}{\varepsilon_{F}}\right) \times 10^{-4} \operatorname{volt} / \mathrm{K}\tag{94}
  $$
  在室温下这比Drude的估计(60)小了大约$O(k_BT/\mathcal{E}_F)\sim0.01$。

* **其他性质**：由于电子速度分布的形式在计算直流或交流电导率、霍尔系数或磁电阻时不起作用，因此无论使用Maxwell-Boltzmann统计还是Fermi-Dirac统计，第一章中给出的估计都是相同的。

  然而，如果一个人使用能量依赖的松弛时间，情况就不是这样了。例如，如果人们认为电子与固定的散射中心相撞，那么自然会采取与能量无关的平均自由程，因此弛豫时间$\tau=l/v \sim l/\mathcal{E}^{1/2}$。在德鲁德提出金属的电子气模型后不久，H.A.洛伦兹利用经典的麦克斯韦-玻尔兹曼速度分布证明，与能量有关的弛豫时间将导致直流和交流电导率的温度依赖性，以及不消失的磁电阻和温度。正如人们现在可能从经典速度分布的不妥当中预料到的那样，这些修正都不能以任何方式使德鲁德模型的差异与金属的观测事实更好地吻合。此外，我们将看到(第13章)，当使用正确的费米-狄拉克速度分布时，增加弛豫时间的能量依赖性对金属中的大多数感兴趣的量几乎没有显著影响。如果假设$\tau(\mathcal{E})$与能量相关,去计算直流或交流电导率、磁电阻或霍尔系数，结果与假设$\tau(\mathcal{E})$与能量无关的结果相同。在金属中，这些数量几乎完全取决于费米能级附近电子的散射方式。这是泡利不相容原理的另一个非常重要的结果，其证明将在第13章给出。

