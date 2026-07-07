# A.2 PN结的物理特性

此部分着重讨论阶跃（突变式）PN结的基本物理模型（各种二级效应在正文中讨论）。其表示在厚度可以忽略不计的区域上p型半导体转变到了n型半导体。假定n型和p型区域之间的冶金结及边界是一个平面，所有载流子分布和电流在平行于边界面的截面上是均匀的，并且所有电流垂直于边界面。这种一维模型对于图中所示的代表性结构是合理的，并且对于大多数pn结是合理的。
（Figure A-2）

### **A.2.1 平衡态下的PN结**

当pn结处于均匀温度且没有外部干扰（如光或偏置电压）作用于它时，称为处于平衡状态。在平衡条件下，空穴电流和电子电流必须在半导体中的每一点都消失。当pn半导体接触时，其内部的电子发生扩散，电子从浓度较高的区域（n侧）扩散到浓度较低的区域（p侧）。每个这样的电子都会留下一个带净正电荷的施主原子，因为施主原子最初是中性的；这种电离的施主原子由图中的©符号表示。图中的圆圈表示束缚电荷（即不能移动的电荷）。类似地，空洞从p区域扩散到n区域。它们留下带有净负电荷的受主原子，因为受主原子最初是中性的；这种电离的受主原子由图中的©符号表示。（A-4B）

在pn半导体的交接处附近，由于携带不同的电荷，这些原子产生的电场具有抑制自由载流子扩散的方向。（A-3）换句话说，任何穿过结的电荷流动都是一个自我限制的过程，因为结上的电场是电荷传输的直接结果，它恰好增加到抵消空穴和电子扩散趋势所需的值。电场线从结n型一侧的施主离子延伸到p型一侧的受主离子。该电场的存在会在两种类型的半导体之间产生势垒，该势垒通常被称为接触电势或内置电势。

因此，扩散将在结点处建立一个违反中性条件的空间电荷区。空间电荷区通常被称为耗尽区，其中的空间电荷由掺杂离子组成。假设该耗尽区在结的两侧的深度为\\(+x_n, -x_p\\)，如图（A-4b）所示。

#### **A.2.1.a 内置电势**

这种平衡态下正负电荷处处相等，可得以下等式：

```katex
J_{p}=J_{p,drift}+J_{p,diff}=0 \tag{A-17a}
```
```katex
J_{n}=J_{n,drift}+J_{n,diff}=0 \tag{A-17b}
```
带入扩散和漂移公式可得：

```katex
q(p(x)\mu_nE(x)+D_n\frac{dn(x)}{dx})=0 \tag{A-18a}
```
```katex
q(p(x)\mu_pE(x)-D_p\frac{dp(x)}{dx})=0 \tag{A-18b}
```

解得电场公式为：

```katex
E=-\frac{D_n}{\mu_n}\frac{1}{n_n}\frac{dn_n}{dx}=-\frac{D_p}{\mu_p}\frac{1}{p_n}\frac{dp_n}{dx} \tag{A-19}
```

根据路径积分来内置电势：

```katex
\begin{equation}
\begin{split}
\phi_0 &= -\int_{-x_p}^{x_n}E(x)dx \\
&= -\frac{D_p}{\mu_p}\int_{-x_p}^{x_n}\frac{1}{p(x)}\frac{dp(x)}{dx}dx \\
&= \frac{D_p}{\mu_p}(\ln p(-x_p)-\ln p(x_n)) \\
&= \frac{D_n}{\mu_n}(\ln n(x_n)-\ln n(-x_p))
\end{split} \tag{A-20}
\end{equation}
```

假设中性区浓度均匀且分别为\\(n_{n0},n_{p0},p_{n0},p_{p0}，_{n0}/ _{p0}\\)指的是\\(n/p\\)型半导体区域结边界的浓度，则上述电势公式可化简为：

```katex
\phi_0 = \frac{D_p}{\mu_p}\ln\frac{p_{p0}}{p_{n0}}\approx\frac{kT}{T}\ln\frac{N_AN_D}{n_i^2} \tag{A-21}
```

其中\\(n_n0=N_A,p_p0=N_D,np=n_i^2\\)。这里也可以分别把\\(\phi_0\\)拆开看成\\(\phi_n+\phi_p\\)，见书中描述。

反过来，我们也可以用边界电势，写出耗尽区边缘的载流子浓度：

```katex
n_{p0}(-x_p)=n_{n0}(x_n)e^{-q\phi_0/kT} \tag{A-22a}
```
```katex
p_{n0}(x_n)=p_{p0}(-x_p)e^{-q\phi_0/kT} \tag{A-22b}
```


#### **A.2.1.a 耗尽区**

模型的推导简化高度依赖**耗尽近似**假设：半导体可以被分成不同的区域，在耗尽区（空间电荷区）内，自由载流子（电子和空穴）被完全耗尽，空间电荷仅由电离的杂质离子（施主和受主）提供；而其他区域则是中性的。

在掺杂完全电离\\(N_D^+\approx N_D,N_A^+\approx N_A\\)，以及自由载流子浓度远小于耗尽区中的净电离的掺杂浓度\\(p\ll N_A\\)假设下，泊松公式可做如下近似：

```katex
\frac{d^2\phi}{dx^2}=-\frac{\rho}{\varepsilon_s}=-\frac{q}{\varepsilon_s}(p-n+N_D^+-N_A^+)\approx-\frac{q}{\varepsilon_s}(N_D-N_A) \tag{A-23}
```

这个公式其实也是不可解的，即使我们做了那么多假设:( 因为掺杂浓度我们也没有确定。除了**a假设耗尽近似**以外，我们还需要假设其为**b假设阶跃结**，即掺杂浓度在\\(x=0\\)的时候从\\(N_A\\)阶跃至\\(N_D\\)，以及电荷扩散后，**c假设在耗尽区中移动多数载流子密度突然变得等于在耗尽区边缘的各个掺杂浓度**。因此，**d假设除了耗尽区外，所有地方的电荷密度都为零**。

好了我们终于可以来解泊松方程了hh，其实也很简单了，就是一个**分段常数的二阶微分方程**：


```katex
\begin{equation}
\begin{aligned}
\frac{d^2\phi}{dx^2}&=-\frac{dE(x)}{dx}=-\frac{qN_D}{\varepsilon_s}  \quad &&\text{for} \quad 0 \lt x \lt x_n\\
\frac{d^2\phi}{dx^2}&=-\frac{dE(x)}{dx}=\frac{qN_A}{\varepsilon_s}  \quad &&\text{for} \quad -x_p \lt x \lt 0 \\
\end{aligned} \tag{A-24}
\end{equation}
```

电场公式积分可得：

```katex
\begin{equation}
\begin{aligned}
E(x)&=-\frac{qN_D}{\varepsilon_s}(x_n-x)  \quad &&\text{for} \quad 0 \lt x \lt x_n \\
E(x)&=-\frac{qN_D}{\varepsilon_s}(x_p+x)  \quad &&\text{for} \quad -x_p \lt x \lt 0
\end{aligned} \tag{A-25}
\end{equation}
```
以上公式可以看出，结两边的耗尽区的宽度与掺杂浓度的大小成反比；掺杂浓度越高，耗尽区越窄。在结一侧的掺杂浓度远高于另一侧的高度不对称结中，耗尽区主要渗透到轻掺杂材料中，而重掺杂材料中的耗尽区的宽度往往可以忽略不计。电势公式继续通过电场积分可得：

```katex
\begin{equation}
\begin{aligned}
\phi(x)&=\phi_n-\frac{qN_D}{2\varepsilon_s}(x_n-x)^2  \quad &&\text{for} \quad 0 \lt x \lt x_n \\
\phi(x)&=\phi_p-\frac{qN_D}{2\varepsilon_s}(x_p+x)^2  \quad &&\text{for} \quad -x_p \lt x \lt 0
\end{aligned} \tag{A-26}
\end{equation}
```

耗尽区的宽度可通过内置电势以及掺杂浓度进行表示：

```katex
W=x_n+x_p=\sqrt{\frac{2\varepsilon_s}{q}\phi_0(\frac{1}{N_A}+\frac{1}{N_D})} \tag{A-27}
```

n和p型半导体内的耗尽区宽度与总宽度的关系：
```katex
x_p=W\frac{N_D}{N_A+N_D}
x_n=W\frac{N_A}{N_A+N_D} \tag{A-28}
```

当然还有其他方法来描述掺杂浓度分布，比如*线性分布*。其推导不在此进行讨论。电势、浓度分布等情况可见于（Figure A-5）

### **A.2.2 偏置情况下的非平衡态PN结**

除了平衡态下的假设，这里针对非平衡态做出以下额外假设：

1. 欧姆触点将p区和n区连接到外部电压源，以便在触点处降低可以忽略不计的电压。
2. 小电流流经中性区造成的电压降忽略不计。
3. 将n区接地，并将电压Vd施加到p区。

这些假设是为了能够保证额外施加的电压能够无损地施加到结的两端。那么偏置情况与平衡情况的唯一区别就是内置电势被替换为了带压降的结电势（就是把前面的\\(\phi_0\\)变为\\(\phi_0-V_D\\)）：
```katex
\phi_j=\phi_0-V_D
```

### **A.2.3 PN结内的电流**

#### **A.2.3.a 载流子连续性方程**
考虑（A-13）的电流密度公式：
```katex
J_{n}=q(n\mu_nE+D_n\frac{dn}{dx}) \tag{A-13b}
```
```katex
J_{p}=q(p\mu_pE-D_p\frac{dp}{dx}) \tag{A-13a}
```

在一维空间下，单位体积内载流子浓度随时间的变化率，等于该处**净流入的粒子流（即该处的电流密度导数除以电荷量）**与内部**产生/复合速率**之和：

```katex
\frac{\partial n}{\partial t}=\frac{1}{q}\frac{\partial J_n}{\partial x}+(G_n-R_n) \tag{A-29}
```

```katex
\frac{\partial p}{\partial t}=-\frac{1}{q}\frac{\partial J_p}{\partial x}+(G_p-R_p) \tag{A-29}
```

其中\\(Gn,Rn\\)和\\(Gp，Rp\\)分别表示电子和空穴在光、辐射或磁场等外部扰动作用下的产生和重组速率。将上述的电流密度公式带入上式中：

```katex
\frac{\partial n}{\partial t}=\frac{1}{q}\frac{\partial q(n\mu_nE+D_n\frac{dn}{dx})}{\partial x}+(G_n-R_n) \tag{A-30a}
```
```katex
\frac{\partial p}{\partial t}=-\frac{1}{q}\frac{\partial q(p\mu_pE-D_p\frac{dp}{dx})}{\partial x}+(G_p-R_p) \tag{A-30b}
```

展开即可得自由载流子的连续性方程，即一个考虑了影响半导体内载流子数量的各种机制的方程如下所示：

电子：
```katex
\frac{\partial n}{\partial t}=\mu_nn(x)\frac{\partial E(x)}{\partial x}+\mu_nE(x)\frac{\partial n(x)}{\partial x}+D_n\frac{\partial^2 n(x)}{\partial x^2}+(G_n-R_n) \tag{A-31a}
```

空穴：
```katex
\frac{\partial p}{\partial t}=-\mu_pp(x)\frac{\partial E(x)}{\partial x}-\mu_pE(x)\frac{\partial p(x)}{\partial x}+D_p\frac{\partial^2 p(x)}{\partial x^2}+(G_p-R_p) \tag{A-31b}
```
（A-31）假设迁移率p和扩散常数D不是x的函数。虽然这个假设在某些情况下不成立，但主要的物理效应包含在方程中且很少考虑更精确的公式。


#### **A.2.3.b 电流特性本质**

电气连接：n级接地p级接\\(V_D\\)。横截面面积为\\(A_J\\)且假设二极管内的载流子密度只受施加电压的影响。中性区的压降在电流较小的时候可以忽略。在这些假设下，结偏置电压为\\(\phi_J=\phi_0-V_D\\)。

如果\\(V_D\\)为正，即对于正向偏置，施加的电压降低了结处大多数载流子扩散的**势垒**。降低的势垒允许更多的载流子跨越耗尽区进入对方的中性区。在跨过耗尽区后，这些载流子成为少数载流子，在浓度梯度的驱动下，继续向中性区内部扩散的同时与从欧姆接触涌入的多数载流子迅速中和以保证电中性。

如果\\(V_D\\)为负，即反向偏置，则势垒增高，耗尽区中的少数载流子往往被耗尽，多数载流子浓度也同样降低。

上面这几点体现了少数载流子密度的重要性，可以收其决定了在pn结中流动的电流。多数载流子只是作为注入的少数载流子电流的供应者，或者作为中性区域的电荷中和者。**所以完全可以把多数载流子视为少数载流子所属的心甘情愿的“奴隶”**。所以我们的目标就是求得每个中性区域中少数载流子密度的连续性方程的解。

#### **A.2.3.b 边界上的少数载流子浓度**

给出以下假设：
1. 外加的偏压导致低水平注入
2. 外加的偏压足够小，使得跨越结区的多数载流子与少数载流子之间的精细平衡（**玻尔兹曼统计关系**）不会被明显破坏。

第一个假设意味着多数载流子几乎不变，所以中性区的电中性条件仍然成立，其内部电场可视为0（**泊松方程**），结果是保证可以忽略漂移电流的同时，边界的浓度可以被视为保持\\(N_A\\)。而第二个假设保证了**玻尔兹曼统计分布（A-22）**仍然成立，只是施加在结上的电压需要减去内置电势\\(\phi_0-V_D\\)。

在\\(V_D\\)电压足够小的前提下，这两个假设基本是成立的。不成立的情况请见（**Chap. 1)**。

因此，耗尽区边界的浓度（玻尔兹曼关系）为：
```katex
p_{n}(x_n)=p_{p}(-x_p)e^{-q(\phi_0-V_D)/kT} \tag{A-32a}
```
```katex
n_{p}(-x_p)=n_{n}(x_n)e^{-q(\phi_0-V_D)/kT} \tag{A-32b}
```

在低注入前提下，可以认为边界浓度与中性区平均浓度相同：\\(p_p(-x_p)\approx p_{p0}, n_n(x_n)\approx n_{n0}\\)

```katex
p_{n}(x_n)=p_{p0}(-x_p)e^{-q(\phi_0-V_D)/kT} \tag{A-33a}
```
```katex
n_{p}(-x_p)=n_{n0}(x_n)e^{-q(\phi_0-V_D)/kT} \tag{A-33b}
```

带入（A-22）公式：

```katex
p_{n}(x_n)=p_{p0}(x_n)e^{qV_D/kT} \tag{A-33a}
```
```katex
n_{p}(-x_p)=n_{p0}(-x_p)e^{-qV_D/kT} \tag{A-33b}
```

这个公式也被称为**结定律**，其将耗尽区边缘的少数载流子浓度的增加或减少与外加电压\\(V_D\\)的极性联系起来（Figure A-7）。如果我们用以下公式定义超额浓度:
```katex
p^\prime_{n}\equiv p_n-p_{n0} \tag{A-34a}
```
```katex
n^\prime_{p}\equiv n_p-n_{p0} \tag{A-34b}
```

则边界的超额少数载流子浓度公式如下：
```katex
p^\prime_{n}=p_{p0}(x_n)e^{qV_D/kT-1} \tag{A-33a}
```
```katex
n^\prime_{p}(-x_p)=n_{p0}(-x_p)e^{-qV_D/kT-1} \tag{A-33b}
```

**初见端倪**对不对，\\(I_S\\)的公式就要来了！


#### **A.2.3.d 长基区二极管**

现在我们可以开始考虑在中性区的连续性方程的解了。以p+n为例考虑注入n区的额外空穴，在n区的生成-复合过程中复合占主导地位。因此\\(R_p\\)可以由公式（A-16）来表示，并且假设\\(G_p\\)为0。连续性方程更新如下：
```katex
\frac{\partial p_n}{\partial t}=D_p\frac{\partial^2 p_n}{\partial x^2}-\frac{p_n-p_{n0}}{\tau_p} \tag{A-34}
```

其中下标n强调了空穴是在n区域中的。这里假设施主密度沿x恒定，且稳态的情况\\(\partial p/\partial t=0\\)，则上述方程可改写为关于公式中定义的超额密度\\(p^\prime_n\\)的全微分方程式：
```katex
D_p\frac{\partial^2 p^\prime_n}{\partial x^2}-\frac{p^\prime_n}{\tau_p} = 0 \tag{A-34}
```