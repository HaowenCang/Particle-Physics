## 一、为什么需要 Foldy-Wouthuysen 变换？

### 1. 狄拉克方程的"困境"

狄拉克方程在描述自旋 $\frac{1}{2}$ 粒子方面取得了巨大成功，但它有一个概念上的不便：

$$H_{\text{Dirac}} = \boldsymbol{\alpha}\cdot\mathbf{p} + \beta m + q\phi$$

其中 $\boldsymbol{\alpha}$ 和 $\beta$ 是 $4\times4$ 的狄拉克矩阵，波函数 $\psi$ 是**四分量旋量**——包含粒子态（正能态）和反粒子态（负能态）的混合。

**问题**：哈密顿量中的 $\boldsymbol{\alpha}\cdot\mathbf{p}$ 项**耦合了正能态和负能态**，使得非相对论物理解释变得困难。我们无法直接从中读出"粒子"的薛定谔型方程。

### 2. 核心思想

Foldy-Wouthuysen 变换的目标是找到一个**幺正变换** $U$，使得变换后的哈密顿量：

$$H_{\text{FW}} = U H_{\text{Dirac}} U^{-1}$$

成为**块对角**形式——正能态与负能态完全解耦。这样，上两分量（粒子）和下两分量（反粒子）各自满足独立的方程，非相对论极限变得完全透明。

> **通俗理解**：想象狄拉克方程描述了一个"纠缠"在一起的粒子-反粒子系统。FW 变换就像一把精确的手术刀，将这两个自由度干净地分离——分离之后，粒子的非相对论物理自然显现。

---

## 二、数学准备：奇偶算符的分类

### 1. 定义

在狄拉克表象中，$\beta = \gamma^0 = \begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix}$ 具有天然的块对角结构。利用 $\beta$，将所有算符分为两类：

$$\text{偶算符（even）：}\quad \beta\mathcal{E}\beta = \mathcal{E} \quad \Leftrightarrow \quad [\beta, \mathcal{E}] = 0$$

$$\text{奇算符（odd）：}\quad \beta\mathcal{O}\beta = -\mathcal{O} \quad \Leftrightarrow \quad \{\beta, \mathcal{O}\} = 0$$

**偶算符**是块对角的（不耦合正负能态），**奇算符**是块反对角的（耦合正负能态）。

### 2. 基本算符的分类

| 算符 | 类型 | 矩阵结构 |
|------|------|---------|
| $\beta$ | 偶 | $\begin{pmatrix} I & 0 \\ 0 & -I \end{pmatrix}$ |
| $I$ | 偶 | $\begin{pmatrix} I & 0 \\ 0 & I \end{pmatrix}$ |
| $\boldsymbol{\Sigma} = \begin{pmatrix}\boldsymbol{\sigma} & 0 \\ 0 & \boldsymbol{\sigma}\end{pmatrix}$ | 偶 | 块对角 |
| $\boldsymbol{\alpha} = \begin{pmatrix}0 & \boldsymbol{\sigma} \\ \boldsymbol{\sigma} & 0\end{pmatrix}$ | **奇** | 块反对角 |
| $\gamma^5 = \begin{pmatrix}0 & I \\ I & 0\end{pmatrix}$ | **奇** | 块反对角 |

### 3. 乘积规则

$$\text{偶} \times \text{偶} = \text{偶}, \qquad \text{奇} \times \text{奇} = \text{偶}$$
$$\text{偶} \times \text{奇} = \text{奇}, \qquad \text{奇} \times \text{偶} = \text{奇}$$

### 4. 分解狄拉克哈密顿量

将狄拉克哈密顿量分解为偶部和奇部：

$$H = \beta m + \mathcal{E} + \mathcal{O}$$

对于电磁场中的带电粒子（电荷 $q$）：

$$\mathcal{E} = q\phi \quad (\text{偶：静电势})$$
$$\mathcal{O} = \boldsymbol{\alpha}\cdot\boldsymbol{\pi} \quad (\text{奇：动量耦合项})$$

其中 $\boldsymbol{\pi} = \mathbf{p} - q\mathbf{A}$ 是正则动量。

**目标**：通过幺正变换逐阶消除奇算符 $\mathcal{O}$。

---

## 三、自由粒子的精确 FW 变换

### 1. 自由狄拉克哈密顿量

$$H_0 = \boldsymbol{\alpha}\cdot\mathbf{p} + \beta m$$

对于自由粒子，$\mathcal{O} = \boldsymbol{\alpha}\cdot\mathbf{p}$，$\mathcal{E} = 0$。

### 2. 精确变换

定义幺正变换：

$$\boxed{U_{\mathbf{p}} = \frac{E_p + \beta(\boldsymbol{\alpha}\cdot\mathbf{p} + m)}{\sqrt{2E_p(E_p + m)}}}$$

其中 $E_p = \sqrt{\mathbf{p}^2 + m^2}$。

可以验证 $U_\mathbf{p} U_\mathbf{p}^\dagger = I$。

### 3. 变换结果

$$\boxed{H_{\text{FW}}^{(0)} = \beta\,E_p = \beta\sqrt{\mathbf{p}^2 + m^2}}$$

这是一个**完全块对角**的哈密顿量：
- 上两分量（粒子）：$H_{\text{FW}} = +\sqrt{\mathbf{p}^2 + m^2}$
- 下两分量（反粒子）：$H_{\text{FW}} = -\sqrt{\mathbf{p}^2 + m^2}$

正负能态**完全解耦**！

### 4. 幂级数展开

将 $E_p$ 展开为 $|\mathbf{p}|/m$ 的幂级数：

$$\beta\sqrt{\mathbf{p}^2 + m^2} = \beta\left(m + \frac{\mathbf{p}^2}{2m} - \frac{\mathbf{p}^4}{8m^3} + \frac{\mathbf{p}^6}{16m^5} - \cdots\right)$$

各项的物理意义：

| 项 | 表达式 | 物理意义 |
|---|---|---|
| 零阶 | $\beta m$ | 静止质量能 |
| 一阶 | $\beta\dfrac{\mathbf{p}^2}{2m}$ | 非相对论动能 |
| 二阶 | $-\beta\dfrac{\mathbf{p}^4}{8m^3}$ | 动能的相对论修正 |
| $n$ 阶 | $\sim \mathbf{p}^{2n}/m^{2n-1}$ | 更高阶相对论修正 |

> 自由粒子的 FW 变换精确地将狄拉克哈密顿量"旋转"到了粒子-反粒子分离的表象中。在这个新表象里，正能态粒子的哈密顿量就是 $\sqrt{\mathbf{p}^2+m^2}$——这正是我们对相对论性粒子的预期能量-动量关系。

---

## 四、相互作用情形的微扰 FW 变换

当存在电磁相互作用时，一般不存在封闭形式的精确变换，需要**逐阶微扰展开**。

### 1. 策略

将哈密顿量按"奇性"和 $1/m$ 的幂次组织：

$$H = \beta m + \mathcal{E} + \mathcal{O}$$

其中 $\mathcal{O}$ 被视为"小量"（因为最终要消除它），$\beta m$ 是大项。

通过一系列幺正变换 $U_n = e^{iS_n}$，逐阶消除奇算符：

$$H \xrightarrow{U_1} H_1 \xrightarrow{U_2} H_2 \xrightarrow{U_3} \cdots \to H_{\text{FW}}$$

### 2. 第一步：消除 $\mathcal{O}$ 的领头阶

选择变换生成元：

$$S_1 = -\frac{i}{2m}\beta\mathcal{O}$$

利用 Baker-Campbell-Hausdorff 展开：

$$H_1 = H + i[S_1, H] + \frac{i^2}{2!}[S_1,[S_1, H]] + \cdots$$

逐项计算（利用 $\beta\mathcal{O}\beta = -\mathcal{O}$ 等关系）：

$$i[S_1, H] = -\mathcal{O} + \frac{\beta\mathcal{O}^2}{m} + \frac{\beta}{2m}[\mathcal{O}, \mathcal{E}]$$

其中：
- $-\mathcal{O}$：恰好**消除**了原始的奇算符
- $\frac{\beta\mathcal{O}^2}{m}$：新的偶算符（$\mathcal{O}^2$ 是奇×奇=偶）
- $\frac{\beta}{2m}[\mathcal{O}, \mathcal{E}]$：新的**残余奇算符**（奇×偶-偶×奇=奇），为 $\mathcal{O}(1/m)$ 量级

### 3. 后续步骤

用 $S_2$ 消除残余的 $\mathcal{O}(1/m)$ 奇算符，$S_3$ 消除 $\mathcal{O}(1/m^2)$，依此类推。

### 4. 一般公式

经过完整的逐阶消除后，FW 哈密顿量的一般形式为：

$$\boxed{H_{\text{FW}} = \beta\left(m + \frac{\mathcal{O}^2}{2m} - \frac{\mathcal{O}^4}{8m^3}\right) + \mathcal{E} - \frac{1}{8m^2}[\mathcal{O},[\mathcal{O},\mathcal{E}]] + \mathcal{O}\!\left(\frac{1}{m^3}\right)}$$

**所有项都是偶算符**——正负能态完全解耦。

---

## 五、应用于电磁场中的狄拉克粒子

### 1. 核心计算：$\mathcal{O}^2$

对于 $\mathcal{O} = \boldsymbol{\alpha}\cdot\boldsymbol{\pi}$，需要计算：

$$\mathcal{O}^2 = (\boldsymbol{\alpha}\cdot\boldsymbol{\pi})^2 = \alpha^i\alpha^j\pi^i\pi^j$$

利用狄拉克矩阵的代数关系：

$$\alpha^i\alpha^j = \delta^{ij} + i\epsilon^{ijk}\Sigma^k$$

其中 $\Sigma^k = \begin{pmatrix}\sigma^k & 0 \\ 0 & \sigma^k\end{pmatrix}$ 是自旋矩阵。

因此：

$$\mathcal{O}^2 = \delta^{ij}\pi^i\pi^j + i\epsilon^{ijk}\Sigma^k\pi^i\pi^j = \boldsymbol{\pi}^2 + \frac{i}{2}\epsilon^{ijk}\Sigma^k[\pi^i, \pi^j]$$

**关键对易关系**：$[\pi^i, \pi^j] = iqF^{ij}$（$F^{ij}$ 是电磁场张量的空间分量）

利用 $\frac{1}{2}\epsilon^{ijk}F_{ij} = B^k$（磁场），得到：

$$\boxed{\mathcal{O}^2 = \boldsymbol{\pi}^2 - q\boldsymbol{\Sigma}\cdot\mathbf{B}}$$

> $(\boldsymbol{\alpha}\cdot\boldsymbol{\pi})^2$ 并不简单地等于 $\boldsymbol{\pi}^2$——狄拉克矩阵的非对易性产生了一个额外项 $-q\boldsymbol{\Sigma}\cdot\mathbf{B}$，这正是自旋与磁场的耦合。这个项在 FW 变换中自然涌现，**不需要任何额外假设**。

### 2. 完整的 FW 哈密顿量（到 $\mathcal{O}(1/m^2)$）

$$\boxed{H_{\text{FW}} = \beta\!\left(m + \frac{\boldsymbol{\pi}^2}{2m} - \frac{\boldsymbol{\pi}^4}{8m^3}\right) + q\phi - \frac{q}{2m}\beta\boldsymbol{\Sigma}\cdot\mathbf{B} - \frac{q}{8m^2}\nabla\cdot\mathbf{E} - \frac{q}{4m^2}\boldsymbol{\Sigma}\cdot(\mathbf{E}\times\boldsymbol{\pi})}$$

各项逐一解读：

---

#### (a) 静止质量

$$\beta m$$

在正能态取 $+m$，负能态取 $-m$。这是粒子物理学中最基本的关系 $E = mc^2$。

#### (b) 非相对论动能

$$\beta\frac{\boldsymbol{\pi}^2}{2m} = \beta\frac{(\mathbf{p}-q\mathbf{A})^2}{2m}$$

标准的带电粒子在磁场中的动能项，对应薛定谔方程中的 $\frac{(\mathbf{p}-q\mathbf{A})^2}{2m}$。

#### (c) 动能的相对论修正

$$-\beta\frac{\boldsymbol{\pi}^4}{8m^3}$$

来自 $\sqrt{\mathbf{p}^2+m^2}$ 展开的第二项。对氢原子能级给出**精细结构修正**。

#### (d) 静电势能

$$q\phi$$

标准的库仑势能。

#### (e) **磁偶极相互作用**——$g = 2$ 的来源

$$\boxed{-\frac{q}{2m}\beta\boldsymbol{\Sigma}\cdot\mathbf{B}}$$

对正能态（$\beta \to 1$，$\boldsymbol{\Sigma} \to \boldsymbol{\sigma}$），这给出：

$$-\frac{q}{2m}\boldsymbol{\sigma}\cdot\mathbf{B} = -\frac{q}{m}\mathbf{S}\cdot\mathbf{B} = -\boldsymbol{\mu}\cdot\mathbf{B}$$

其中磁矩 $\boldsymbol{\mu} = \dfrac{q}{m}\mathbf{S} = 2\cdot\dfrac{q}{2m}\mathbf{S}$，因此：

$$\boxed{g_{\text{Dirac}} = 2}$$

**FW 变换自动从狄拉克方程的结构中"涌现"出 $g=2$——不需要任何额外输入。** 这是 FW 变换最深刻的结果之一。

#### (f) Darwin 项

$$-\frac{q}{8m^2}\nabla\cdot\mathbf{E}$$

这是一个**纯量子力学效应**，没有经典对应。对于氢原子（$\nabla\cdot\mathbf{E} = Ze\delta^3(\mathbf{r})/\epsilon_0$），它给出 $s$ 轨道的能量位移。

> Darwin 项来源于电子在康普顿波长 $\lambda_C = 1/m$ 范围内的"颤动"（Zitterbewegung）感受到的电势平均效应。它只影响 $l=0$ 的态（因为只有 $s$ 轨道的波函数在原点不为零）。

#### (g) 自旋-轨道耦合

$$-\frac{q}{4m^2}\boldsymbol{\Sigma}\cdot(\mathbf{E}\times\boldsymbol{\pi})$$

对于氢原子（$\mathbf{E} = \dfrac{Ze}{4\pi r^2}\hat{\mathbf{r}}$，$\boldsymbol{\pi} \approx \mathbf{p}$）：

$$\mathbf{E}\times\mathbf{p} = \frac{Ze}{4\pi r^3}\mathbf{r}\times\mathbf{p} = \frac{Ze}{4\pi r^3}\mathbf{L}$$

因此：

$$H_{SO} = \frac{Ze^2}{4\pi \cdot 4m^2 r^3}\boldsymbol{\Sigma}\cdot\mathbf{L} = \frac{1}{2m^2r^3}\frac{Ze^2}{4\pi}\,\mathbf{S}\cdot\mathbf{L}$$

> **关键优点**：FW 变换**自动包含 Thomas 进动修正**。如果用半经典方法推导自旋-轨道耦合，需要额外引入 Thomas 因子 $1/2$。FW 变换从第一性原理给出了正确的系数，无需任何额外修正。

---

## 六、物理图景的总结

### 1. FW 表象中的"位置算符"

在原始狄拉克表象中，位置算符 $\mathbf{x}$ 不是粒子"真实"位置的良好描述——它受到 **Zitterbewegung**（相对论性颤动）的影响，即粒子位置以光速在康普顿波长 $\lambda_C \sim 1/m$ 尺度上快速振荡。

FW 变换定义了**平均位置算符**（也称 Newton-Wigner 位置）：

$$\mathbf{X}_{\text{FW}} = U_{\text{FW}}\,\mathbf{x}\,U_{\text{FW}}^{-1}$$

这个算符描述的是"抹平"了 Zitterbewegung 之后的粒子位置，具有正确的非相对论性质（各分量对易：$[X_i, X_j] = 0$）。

### 2. FW 变换的物理意义总览

| 原始狄拉克表象 | FW 表象 |
|---|---|
| 粒子-反粒子混合 | 粒子-反粒子分离 |
| $\mathbf{x}$ 含 Zitterbewegung | $\mathbf{X}_{\text{FW}}$ 是平滑位置 |
| 自旋-轨道耦合需 Thomas 修正 | 自动包含正确的 Thomas 因子 |
| $g=2$ 不直接可见 | $g=2$ 从 $-\frac{q}{2m}\beta\boldsymbol{\Sigma}\cdot\mathbf{B}$ 直接读出 |
| 四分量旋量方程 | 约化为二分量 Pauli 方程（到 $\mathcal{O}(1/m)$） |

### 3. FW 变换后正能态的有效哈密顿量

投影到正能态（$\beta \to +1$），到 $\mathcal{O}(1/m^2)$：

$$H_{\text{eff}} = m + \frac{(\mathbf{p}-q\mathbf{A})^2}{2m} + q\phi - \frac{q}{2m}\boldsymbol{\sigma}\cdot\mathbf{B} - \frac{q}{8m^2}\nabla\cdot\mathbf{E} - \frac{q}{4m^2}\boldsymbol{\sigma}\cdot(\mathbf{E}\times\mathbf{p})$$

这正是**泡利方程**加上相对论修正项。FW 变换严格证明了：狄拉克方程在非相对论极限下自动约化为泡利方程，且所有系数都是确定的。

---

## 七、与氢原子能级的联系

FW 哈密顿量的各项修正对氢原子能级的贡献：

### 1. 非相对论项（$H_0$）

$$E_n^{(0)} = -\frac{m(Z\alpha)^2}{2n^2}$$

### 2. 相对论动能修正

$$\Delta E_{\text{rel}} = -\frac{m(Z\alpha)^4}{2n^3}\left(\frac{1}{j+\frac{1}{2}} - \frac{3}{4n}\right)$$

### 3. 自旋-轨道耦合

$$\Delta E_{SO} = \frac{m(Z\alpha)^4}{4n^3}\cdot\frac{j(j+1)-l(l+1)-\frac{3}{4}}{l(l+\frac{1}{2})(l+1)}$$

### 4. Darwin 项（仅影响 $l=0$）

$$\Delta E_{\text{Darwin}} = \frac{m(Z\alpha)^4}{8n^3}\delta_{l0}$$

### 5. 合并：精细结构

这三项之和给出著名的**狄拉克精细结构公式**：

$$\boxed{E_{nj} = m\left[1 + \left(\frac{Z\alpha}{n - (j+\frac{1}{2}) + \sqrt{(j+\frac{1}{2})^2 - (Z\alpha)^2}}\right)^2\right]^{-1/2}}$$

展开到 $\mathcal{O}(\alpha^4)$：

$$E_{nj} \approx -\frac{m(Z\alpha)^2}{2n^2} - \frac{m(Z\alpha)^4}{2n^3}\left(\frac{1}{j+\frac{1}{2}} - \frac{3}{4n}\right) + \cdots$$

> FW 变换的价值在于：精细结构的每一项都有明确的物理来源（动能修正、自旋-轨道耦合、Darwin 项），使得物理图像完全透明。

---

## 八、局限性与推广

### 1. FW 变换的局限

| 局限 | 说明 |
|------|------|
| 仅适用于单粒子理论 | 多粒子问题需要量子场论的二次量子化 |
| 非相对论展开 | 本质上是 $|\mathbf{p}|/m$ 的幂级数，高能时发散 |
| 不能处理粒子产生/湮灭 | FW 表象中粒子数守恒，无法描述正负电子对产生等过程 |
| 与规范场的耦合 | 对非阿贝尔规范场（如 QCD），FW 变换变得非常复杂 |

### 2. 推广

- **Feshbach-Villars 表象**：Klein-Gordon 方程的类似分解
- **Lévy-Leblond 方程**：自旋 $\frac{1}{2}$ 粒子的非相对论极限的几何化表述
- **FW 变换在凝聚态物理中的应用**：石墨烯、拓扑绝缘体中有效哈密顿量的推导（将狄拉克型色散关系投影到低能子空间）
- **色散关系方法**：在量子场论中，FW 变换的思想推广为各种有效场论的匹配条件

---

## 九、总结

| 要点 | 内容 |
|------|---|
| **核心目标** | 幺正变换消除狄拉克哈密顿量中的奇算符，分离正负能态 |
| **自由粒子** | 精确变换 $U_\mathbf{p}$，$H_{\text{FW}} = \beta\sqrt{\mathbf{p}^2+m^2}$ |
| **相互作用** | 微扰逐阶消除，到 $1/m^2$ 给出完整结果 |
| **$g=2$ 的起源** | 来自 $\mathcal{O}^2 = \boldsymbol{\pi}^2 - q\boldsymbol{\Sigma}\cdot\mathbf{B}$ 中的 $-q\boldsymbol{\Sigma}\cdot\mathbf{B}$ 项 |
| **自旋-轨道耦合** | 自动包含 Thomas 进动修正 |
| **Darwin 项** | 纯量子效应，来自 Zitterbewegung 的平均 |
| **物理意义** | 定义了无 Zitterbewegung 的"真实"位置（Newton-Wigner 位置） |
| **局限** | 单粒子理论框架，非相对论展开，不能处理粒子产生 |
