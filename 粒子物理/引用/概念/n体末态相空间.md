## 一、基本概念与定义

### 1. 相空间的物理意义

在粒子物理中，散射截面（或衰变宽度）的计算最终归结为：

$$d\sigma \propto |\mathcal{M}|^2 \times d\Phi_n$$

其中 $\mathcal{M}$ 是散射振幅（由费曼规则计算），$d\Phi_n$ 是**洛伦兹不变末态相空间**（Lorentz-Invariant Phase Space, LIPS）。

相空间的物理角色：
- 编码了**运动学允许的末态构型**的空间
- 反映了能量-动量守恒对末态的约束
- 决定了不同末态构型的**统计权重**

> 如果散射振幅 $\mathcal{M}$ 回答的是"这个过程发生的概率振幅有多大"，相空间 $d\Phi_n$ 回答的是"末态粒子可以去往哪些状态"。两者相乘并积分，才得到可观测的截面。

### 2. 洛伦兹不变相空间的定义

对于 $n$ 个末态粒子（质量 $m_i$，四动量 $p_i$），洛伦兹不变相空间定义为：

$$\boxed{d\Phi_n(P; p_1, p_2, \ldots, p_n) = \prod_{i=1}^{n}\frac{d^4p_i}{(2\pi)^4}\,(2\pi)\delta(p_i^2 - m_i^2)\,\theta(p_i^0)\;\cdot\;(2\pi)^4\delta^{(4)}\!\left(P - \sum_{i=1}^n p_i\right)}$$

其中：
- $P^\mu$：初态总四动量（$P^2 = s$，即质心系总能量的平方）
- $\delta(p_i^2 - m_i^2)\theta(p_i^0)$：将每个末态粒子约束在其**质壳**上（$p_i^2 = m_i^2$，$E_i > 0$）
- $\delta^{(4)}(P - \sum p_i)$：**四动量守恒**

### 3. 等价的三维形式

对每个 $d^4p_i$ 积分，利用 $\delta(p_i^2 - m_i^2)\theta(p_i^0)$ 消去 $p_i^0$：

$$\int\frac{d^4p_i}{(2\pi)^4}\,(2\pi)\delta(p_i^2 - m_i^2)\theta(p_i^0) = \int\frac{d^3p_i}{(2\pi)^3\,2E_i}$$

其中 $E_i = \sqrt{\mathbf{p}_i^2 + m_i^2}$。因此：

$$\boxed{d\Phi_n = (2\pi)^4\delta^{(4)}\!\left(P - \sum_{i=1}^n p_i\right)\prod_{i=1}^{n}\frac{d^3p_i}{(2\pi)^3\,2E_i}}$$

---

## 二、相空间的洛伦兹不变性

### 1. 证明概要

需要验证 $d\Phi_n$ 在 Lorentz 变换下不变。

**单粒子测度** $\dfrac{d^3p}{2E}$ 的不变性：

从[[质壳条件]] $p^2 = m^2$，$p^0 = E > 0$，可将 $d^4p$ 写为：

$$d^4p = dE\,d^3p = dE\,p^2\,dp\,d\Omega$$

利用 $\delta(p^2 - m^2) = \delta(E^2 - p^2 - m^2) = \dfrac{1}{2E}\delta(E - E_p)$，对 $E$ 积分：

$$\frac{d^3p}{2E} = \frac{p^2\,dp\,d\Omega}{2E}$$

在 Lorentz boost 下，$d^3p/E$ 是不变量（这可以从 $d^4p$ 和 $\delta(p^2-m^2)$ 的各自不变性直接看出）。

**四维 $\delta$ 函数**的不变性：

$\delta^{(4)}(P - \sum p_i)$ 中的四矢量 $P - \sum p_i$ 的模方是 Lorentz 标量，而 $\delta^{(4)}(k)$ 中 $d^4k$ 是不变测度，因此 $\delta^{(4)}(k)$ 本身是不变的。

因此 $d\Phi_n$ 整体是 **Lorentz 不变量**。

### 2. 维数分析

$d\Phi_n$ 的量纲：

$$[d\Phi_n] = \left[\frac{d^3p}{E}\right]^n \cdot [\delta^{(4)}(P)] = (\text{mass}^2)^n \cdot \text{mass}^{-4} = \text{mass}^{2n-4}$$

在自然单位制中：

$$[d\Phi_n] = M^{2n-4}$$

| $n$ | $[d\Phi_n]$ |
|-----|-------------|
| 2 | $M^0$（无量纲） |
| 3 | $M^2$ |
| 4 | $M^4$ |
| $n$ | $M^{2n-4}$ |

---

## 三、二体相空间（$n = 2$）

### 1. 一般公式

$$d\Phi_2 = (2\pi)^4\delta^{(4)}(P - p_1 - p_2)\frac{d^3p_1}{(2\pi)^3 2E_1}\frac{d^3p_2}{(2\pi)^3 2E_2}$$

### 2. 质心系计算

在质心系中 $P^\mu = (\sqrt{s}, \mathbf{0})$，利用 $\delta^{(3)}(\mathbf{p}_1 + \mathbf{p}_2)$ 消去 $\mathbf{p}_2 = -\mathbf{p}_1$：

$$\Phi_2 = \int\frac{d^3p_1}{(2\pi)^2\,4E_1 E_2}\,\delta(\sqrt{s} - E_1 - E_2)$$

记 $\mathbf{p}_1 = \mathbf{p}^*$（质心系动量），$|\mathbf{p}^*| = p^*$：

$$\Phi_2 = \int\frac{p^{*2}\,dp^*\,d\Omega}{(2\pi)^2\,4E_1 E_2}\,\delta(\sqrt{s} - E_1 - E_2)$$

对 $p^*$ 积分——需要计算 $\delta$ 函数的自变量对 $p^*$ 的导数：

$$\frac{d}{dp^*}(E_1 + E_2) = \frac{p^*}{E_1} + \frac{p^*}{E_2} = \frac{p^*(E_1 + E_2)}{E_1 E_2} = \frac{p^*\sqrt{s}}{E_1 E_2}$$

因此 $\delta(\sqrt{s} - E_1 - E_2) = \dfrac{E_1 E_2}{p^*\sqrt{s}}\,\delta(p^* - p^*_0)$，其中 $p^*_0$ 由 $\sqrt{s} = E_1 + E_2$ 确定。

积分后：

$$\boxed{\Phi_2 = \frac{p^*}{4\pi\sqrt{s}} \cdot 4\pi = \frac{p^*}{\sqrt{s}} \cdot \frac{1}{4\pi}\cdot(4\pi) = \frac{p^*}{4\pi\sqrt{s}}\cdot 4\pi}$$

更清楚地，分离角部分和径向部分：

$$d\Phi_2 = \frac{p^*}{4\pi\sqrt{s}}\;\frac{d\Omega}{4\pi}\cdot 4\pi = \frac{p^*\,d\Omega}{16\pi^2\sqrt{s}}\cdot 4\pi$$

规范地写：

$$\boxed{d\Phi_2 = \frac{|\mathbf{p}^*|}{16\pi^2\sqrt{s}}\,d\Omega}$$

对全立体角积分：

$$\boxed{\Phi_2 = \frac{|\mathbf{p}^*|}{4\pi\sqrt{s}} = \frac{|\mathbf{p}^*|}{8\pi E_{\text{cm}}}}$$

（两种写法差 $4\pi$ 因子，取决于是否将 $d\Omega$ 包含在微分相空间中。以下约定 $\Phi_n = \int d\Phi_n$ 为对所有角度积分后的总相空间体积。）

### 3. 质心系动量

$$|\mathbf{p}^*| = \frac{\lambda^{1/2}(s, m_1^2, m_2^2)}{2\sqrt{s}}$$

其中 **Källén 函数**：

$$\lambda(x,y,z) = x^2 + y^2 + z^2 - 2xy - 2xz - 2yz$$

等价形式：

$$|\mathbf{p}^*| = \frac{1}{2\sqrt{s}}\sqrt{[s-(m_1+m_2)^2][s-(m_1-m_2)^2]}$$

### 4. 特殊情况

**等质量粒子**（$m_1 = m_2 = m$）：

$$|\mathbf{p}^*| = \frac{1}{2}\sqrt{s - 4m^2}$$

$$\Phi_2 = \frac{\sqrt{1 - 4m^2/s}}{8\pi}$$

**无质量粒子**（$m_1 = m_2 = 0$）：

$$|\mathbf{p}^*| = \frac{\sqrt{s}}{2}, \qquad \Phi_2 = \frac{1}{8\pi}$$

**一个无质量、一个有质量**（$m_1 = 0$，$m_2 = m$）：

$$|\mathbf{p}^*| = \frac{s - m^2}{2\sqrt{s}}, \qquad \Phi_2 = \frac{s - m^2}{8\pi s}$$

---

## 四、三体相空间与 Dalitz 图（$n = 3$）

### 1. 三体相空间公式

$$d\Phi_3 = (2\pi)^4\delta^{(4)}(P - p_1 - p_2 - p_3)\prod_{i=1}^{3}\frac{d^3p_i}{(2\pi)^3 2E_i}$$

### 2. Lorentz 不变量的分解

三体相空间可以用两个独立的 Lorentz 不变量完全参数化。定义**不变质量平方**：

$$s_{ij} = (p_i + p_j)^2 = (P - p_k)^2 = m_i^2 + m_j^2 + 2p_i \cdot p_j \qquad (k \neq i, j)$$

三个不变量 $s_{12}$、$s_{23}$、$s_{13}$ 满足约束：

$$\boxed{s_{12} + s_{23} + s_{13} = s + m_1^2 + m_2^2 + m_3^2}$$

因此只有两个独立变量，通常取 $s_{12}$ 和 $s_{23}$。

### 3. Dalitz 图

三体相空间在 $(s_{12}, s_{23})$ 平面上的取值区域称为 **Dalitz 图**（Dalitz plot）。

**边界**：由运动学约束确定。在质心系中，对于给定的 $s_{12}$，粒子 3 的能量为：

$$E_3^* = \frac{s - s_{12} - m_3^2 + m_3^2}{2\sqrt{s}} = \frac{s - s_{12} + m_3^2}{2\sqrt{s}}$$

（更准确地，$E_3^* = \frac{s - s_{12} + m_3^2}{2\sqrt{s}}$。）

$E_3^*$ 必须满足 $E_3^* \geq m_3$（粒子 3 的能量不能小于其质量），这给出了 $s_{12}$ 的范围：

$$\boxed{(m_1 + m_2)^2 \leq s_{12} \leq (\sqrt{s} - m_3)^2}$$

类似地，$s_{23}$ 和 $s_{13}$ 也有相应的范围。

### 4. 三体相空间的微分形式

$$\boxed{d\Phi_3 = \frac{1}{128\pi^3\,s}\,ds_{12}\,ds_{23}}$$

（对所有角度积分后。）

**推导要点**：将三体问题分解为两步——先将粒子 1 和 2 组合为"虚粒子"（不变质量 $\sqrt{s_{12}}$），再将该虚粒子与粒子 3 视为二体衰变。利用：

$$d\Phi_3 = \frac{ds_{12}}{2\pi}\,d\Phi_2^{(12)}\,d\Phi_2^{(123)}$$

其中 $d\Phi_2^{(12)}$ 是粒子 1 和 2 在其质心系中的二体相空间，$d\Phi_2^{(123)}$ 是 $(12)$ 组合体与粒子 3 的二体相空间。

### 5. Dalitz 图的物理意义

如果散射振幅 $|\mathcal{M}|^2$ 在 Dalitz 图上是均匀的（常数），则末态粒子在 $(s_{12}, s_{23})$ 平面上均匀分布。但实际中：

- **共振态**：如果粒子 1 和 2 可以通过共振态（如 $\rho \to \pi\pi$）产生，则在 $s_{12} \approx m_\rho^2$ 处出现**增强带**（band）
- **角动量效应**：高自旋共振态在 Dalitz 图上产生特征性的干涉条纹
- **末态相互作用**：如 $K \to 3\pi$ 中的末态散射效应

```
s₂₃
 ↑
 │╲                    ╱
 │  ╲   允许区域      ╱
 │    ╲             ╱
 │      ╲         ╱
 │  ρ带→  ═══════    ←f₂带
 │          ╲     ╱
 │            ╲ ╱
 │             ╳  ←干涉区
 │           ╱  ╲
 │         ╱      ╲
 │       ╱          ╲
 └──────────────────────→ s₁₂
   (m₁+m₂)²    (√s - m₃)²
```

---

## 五、$n$ 体相空间的递推分解

### 1. 递推（级联）分解

$n$ 体相空间可以通过**逐级分解**为一系列二体相空间。这是计算高体相空间最强大的方法。

将 $n$ 个末态粒子分成两组：
- 组 A：粒子 $\{1, 2, \ldots, k\}$，总四动量 $q = p_1 + \cdots + p_k$
- 组 B：粒子 $\{k+1, \ldots, n\}$，总四动量 $P - q$

定义中间不变质量平方 $s_k = q^2$。

则：

$$\boxed{d\Phi_n(P; p_1, \ldots, p_n) = d\Phi_{n-k+1}(P; q, p_{k+1}, \ldots, p_n)\;\frac{ds_k}{2\pi}\;d\Phi_k(q; p_1, \ldots, p_k)}$$

其中 $s_k$ 的取值范围由所有粒子的质量决定。

### 2. 递推示例：四体相空间

$$d\Phi_4(P; p_1, p_2, p_3, p_4)$$

**第一步**：分成 $\{1,2\}$ 和 $\{3,4\}$：

$$d\Phi_4 = d\Phi_2(P; q_{12}, q_{34})\;\frac{ds_{12}}{2\pi}\;d\Phi_2(q_{12}; p_1, p_2)\;\frac{ds_{34}}{2\pi}\;d\Phi_2(q_{34}; p_3, p_4)$$

这将四体相空间分解为三个二体相空间的乘积。

**第二步**：每个二体相空间已经知道：

$$d\Phi_2(P'; p_a, p_b) = \frac{|\mathbf{p}_{ab}^*|}{16\pi^2\sqrt{s'}}\,d\Omega_{ab}$$

因此：

$$d\Phi_4 = \frac{ds_{12}}{2\pi}\frac{ds_{34}}{2\pi}\;\frac{|\mathbf{p}_{12}^*|\,d\Omega_{12}}{16\pi^2\sqrt{s}}\;\frac{|\mathbf{p}_1^*|\,d\Omega_1}{16\pi^2\sqrt{s_{12}}}\;\frac{|\mathbf{p}_3^*|\,d\Omega_3}{16\pi^2\sqrt{s_{34}}}$$

### 3. 一般递推公式

对于 $n$ 体相空间的总体积（对所有角度积分），递推给出：

$$\boxed{\Phi_n(s) = \frac{1}{2\pi}\int_{(m_1+m_2)^2}^{(\sqrt{s}-m_3-\cdots-m_n)^2} ds_{12}\;\Phi_2(s; s_{12}, m_3+\cdots)\;\Phi_k(s_{12}; m_1, m_2)\;\cdots}$$

每一步都涉及对中间不变质量的积分和低体相空间的递推调用。

---

## 六、$n$ 体相空间的封闭公式

### 1. 总相空间体积

对所有角度和不变质量积分后，$n$ 体相空间的总体积有以下封闭表达式：

$$\boxed{\Phi_n(s) = \frac{(2\pi)^{4-3n}}{2\Gamma(n-1)}\cdot\frac{(\pi/2)^{n-2}}{(n-2)!}\cdot\frac{[\lambda(s, m_1^2, (P-p_1)^2)]^{1/2}}{2\sqrt{s}}\;\cdots}$$

更实用的是以下等价形式。

### 2. 无质量末态的精确结果

当所有末态粒子无质量（$m_i = 0$）时：

$$\boxed{\Phi_n^{(0)}(s) = \frac{s^{n-2}}{(4\pi)^{2n-3}}\cdot\frac{(2\pi)^{2n-4}}{(n-1)!(n-2)!} = \frac{1}{8\pi}\cdot\frac{1}{(4\pi)^{n-2}}\cdot\frac{s^{n-2}}{(n-1)!(n-2)!}\cdot(2\pi)^{2n-4}}$$

更简洁地：

$$\Phi_n^{(0)}(s) = \frac{(2\pi)^{4-2n}}{2}\cdot\frac{s^{n-2}}{(n-1)!(n-2)!}\cdot\frac{\pi^{n-2}}{1}$$

实际使用时，以下公式更方便：

$$\boxed{\Phi_n^{(0)}(s) = \frac{1}{8\pi}\cdot\frac{(4\pi)^{n-2}}{(2n-3)!!}\cdot\frac{s^{n-2}}{(n-2)!\,(4\pi)^{2(n-2)}}}$$

对于具体数值，各 $n$ 的无质量相空间体积为：

| $n$ | $\Phi_n^{(0)}(s)$ |
|-----|-------------------|
| 2 | $\dfrac{1}{8\pi}$ |
| 3 | $\dfrac{1}{128\pi^3}\,s$ |
| 4 | $\dfrac{1}{2048\pi^5}\,s^2\cdot\dfrac{1}{3}$ |
| $n$ | $\propto s^{n-2}/(4\pi)^{2n-4}$ |

### 3. 有质量情况的一般表达式

对于有质量末态，不存在简洁的封闭公式，但有以下积分表示：

$$\Phi_n(s) = \frac{1}{2(2\pi)^{3n-4}}\int\prod_{i=1}^{n}\frac{d^3p_i}{2E_i}\;\delta^{(4)}\!\left(P - \sum p_i\right)$$

实际计算中，通常采用**递推分解 + 数值积分**或**蒙特卡洛方法**。

---

## 七、相空间的蒙特卡洛生成

### 1. 为什么需要蒙特卡洛？

在实际的粒子物理计算中：
- $n \geq 3$ 时相空间积分的维数很高（$3n - 4$ 维）
- 被积函数 $|\mathcal{M}|^2$ 通常具有尖锐的共振峰
- 解析积分通常不可能

因此需要**蒙特卡洛（MC）方法**来数值计算相空间积分。

### 2. RAMBO 算法

**RAMBO**（RAndom Momenta Beautifully Organized）是最经典的无质量相空间生成器：

**算法步骤**：

1. 生成 $n$ 个四矢量 $k_i^\mu$，每个分量独立地从高斯分布中采样
2. 计算总四动量 $K = \sum k_i$
3. 对每个 $k_i$ 施加 Lorentz boost，使其在 $K$ 的质心系中
4. 对每个 $k_i$ 施加标度变换，使其成为无质量的（$k_i^2 = 0$）
5. 最后施加一个 boost 将整个系统变换到总四动量 $P$ 的质心系

结果：$p_i^\mu$ 在 $n$ 体无质量相空间上**均匀分布**。

### 3. 有质量相空间的生成

对于有质量末态，常用**分层采样**（sequential sampling）：

**递推生成**：

1. 选择一种粒子分组方案（链式分解）：

$$1 + 2 + \cdots + n \to [(12)3]\cdots n$$

2. 依次采样中间不变质量 $s_{12}, s_{123}, \ldots$

3. 在每一步中，生成该级二体衰变的角度

4. 通过 Lorentz boost 将每级的子系统变换到总质心系

### 4. 带重要性采样的相空间生成

由于 $|\mathcal{M}|^2$ 通常在共振处有尖峰，需要**重要性采样**（importance sampling）：

- **[[Breit-Wigner 分布]]**采样中间共振质量：

$$\rho(s_{ij}) \propto \frac{1}{(s_{ij} - m_R^2)^2 + m_R^2\Gamma_R^2}$$

- **$1/t$ 传播子**在 $t$-channel 交换过程中，在小 $|t|$ 处有增强，需要在 $t$ 上非均匀采样

---

## 八、分波展开与相空间

### 1. 角动量分解

在质心系中，二体相空间的角分布可以按球谐函数展开：

$$\frac{d\Phi_2}{d\Omega} = \frac{p^*}{16\pi^2\sqrt{s}} = \text{常数} \quad (\text{各向同性})$$

但散射振幅 $\mathcal{M}$ 通常具有非平凡的角分布。将 $\mathcal{M}$ 按分波展开：

$$\mathcal{M}(\cos\theta) = \sum_{l=0}^{\infty}(2l+1)\,a_l\,P_l(\cos\theta)$$

截面：

$$\sigma \propto \int d\Phi_2\,|\mathcal{M}|^2 = \frac{p^*}{16\pi^2\sqrt{s}}\int d\Omega\,|\mathcal{M}|^2$$

利用球谐函数的正交性：

$$\int d\Omega\,|P_l(\cos\theta)|^2 = \frac{4\pi}{2l+1}$$

不同分波之间不干涉（对全角度积分后）：

$$\sigma \propto \frac{p^*}{4\pi\sqrt{s}}\sum_l (2l+1)|a_l|^2$$

---

## 九、相空间的阈行为

### 1. 二体阈

当 $\sqrt{s} \to m_1 + m_2$（阈值）时：

$$p^* \to 0, \qquad \Phi_2 \propto p^* \propto \sqrt{s - (m_1+m_2)^2}$$

即相空间在阈值处以 $\sqrt{s - s_{\text{thr}}}$ 的方式趋于零。这决定了截面在阈值附近的**开启行为**。

### 2. 一般 $n$ 体阈

在 $n$ 体阈值（$\sqrt{s} \to \sum m_i$）附近：

$$\Phi_n \propto (s - s_{\text{thr}})^{(3n-5)/2}$$

| $n$ | 阈行为 | 指数 |
|-----|--------|------|
| 2 | $\propto (s - s_{\text{thr}})^{1/2}$ | $(3\cdot2-5)/2 = 1/2$ |
| 3 | $\propto (s - s_{\text{thr}})^2$ | $(3\cdot3-5)/2 = 2$ |
| 4 | $\propto (s - s_{\text{thr}})^{7/2}$ | $(3\cdot4-5)/2 = 7/2$ |

> 末态粒子越多，相空间在阈值附近"开启"得越慢——因为更多的粒子需要分享有限的能量，每个粒子分到的动量更小，相空间更受压低。

---

## 十、相空间在截面和衰变率中的应用

### 1. 散射截面

$$\boxed{d\sigma = \frac{1}{2E_1 2E_2|\mathbf{v}_1 - \mathbf{v}_2|}\,|\mathcal{M}|^2\,d\Phi_n}$$

在质心系中，通量因子简化为：

$$\text{Flux} = 4E_1 E_2|\mathbf{v}_1 - \mathbf{v}_2| = 4p^*\sqrt{s}$$

因此：

$$d\sigma = \frac{|\mathcal{M}|^2}{4p^*\sqrt{s}}\,d\Phi_n$$

### 2. 衰变率

$$\boxed{d\Gamma = \frac{1}{2M}\,|\mathcal{M}|^2\,d\Phi_n}$$

其中 $M$ 是母粒子的质量（在母粒子的静止系中）。

总衰变率：

$$\Gamma = \frac{1}{2M}\int|\mathcal{M}|^2\,d\Phi_n$$

### 3. 部分宽度与分支比

如果粒子可以通过不同道衰变：

$$\Gamma_{\text{tot}} = \sum_f \Gamma_f, \qquad \text{Br}(f) = \frac{\Gamma_f}{\Gamma_{\text{tot}}}$$

---

## 十一、具体实例

### 例 1：$K^+ \to \mu^+\nu_\mu$（二体衰变）

$$\Gamma = \frac{|\mathcal{M}|^2}{16\pi M_K}\cdot\frac{p^*}{M_K} = \frac{|\mathcal{M}|^2\,p^*}{16\pi M_K^2}$$

其中 $p^* = \dfrac{M_K^2 - m_\mu^2}{2M_K}$。

### 例 2：$\pi^0 \to \gamma\gamma$（无质量二体衰变）

$$\Gamma = \frac{|\mathcal{M}|^2}{16\pi M_\pi} \cdot \frac{M_\pi/2}{M_\pi} = \frac{|\mathcal{M}|^2}{32\pi M_\pi}$$

### 例 3：$\mu^- \to e^-\bar{\nu}_e\nu_\mu$（三体衰变）

$$\Gamma = \frac{1}{2m_\mu}\int|\mathcal{M}|^2\,d\Phi_3$$

利用 $d\Phi_3 = \dfrac{ds_{12}\,ds_{23}}{128\pi^3 m_\mu^2}$（在 $\mu$ 静止系中），并假设 $m_e \approx 0$，$m_\nu = 0$：

$$s_{12} = (p_e + p_{\bar{\nu}_e})^2, \qquad s_{23} = (p_{\bar{\nu}_e} + p_{\nu_\mu})^2$$

运动学边界：

$$0 \leq s_{12} \leq m_\mu^2, \qquad 0 \leq s_{23} \leq m_\mu^2 - s_{12}$$

对 Fermi 理论振幅积分后得到标准结果：

$$\Gamma_\mu = \frac{G_F^2 m_\mu^5}{192\pi^3}$$

### 例 4：Dalitz 衰变 $\Delta^+ \to p\pi^0$

这是一个 $1 \to 2$ 衰变，只有一个末态不变量（$\sqrt{s_{p\pi}} = M_\Delta$ 在壳），因此相空间完全确定。

但如果 $\Delta$ 有宽度 $\Gamma_\Delta$，则需要对 [[Breit-Wigner 分布]]积分。

---

## 十二、相空间的高维结构

### 1. 独立变量的数目

$n$ 体末态的独立 Lorentz 不变量数目：

- $n$ 个四动量：$4n$ 个分量
- [[质壳条件]]：$n$ 个约束
- 四动量守恒：4 个约束
- 初态固定：$-2$（总四动量已知，但整体旋转给出 3 个约束中 2 个独立——实际上需减去整体旋转的自由度）

独立变量数 = $4n - n - 4 - (2n - 3 - (n-1)) = \cdots$

更系统地：

$$\boxed{N_{\text{indep}} = 3n - 4 - (2\text{ 个整体旋转自由度}) = 3n - 4 \quad \text{（对无极化观测）}}$$

实际上，完整的计数是：

- 末态 $n$ 个粒子的三维动量：$3n$ 个变量
- 四动量守恒（3 个空间分量）：$-3$
- 质壳条件（已在 $E_i = \sqrt{p_i^2 + m_i^2}$ 中使用）：已计入

所以独立变量 = $3n - 3$。再减去整体旋转的 3 个自由度（如果只关心 Lorentz 不变量）：

$$N_{\text{Lorentz inv}} = 3n - 4$$

（因为总能量 $\sqrt{s}$ 也是一个已知参数。）

| $n$ | $N_{\text{indep}}$ | 常用参数化                                                        |
| --- | ------------------ | ------------------------------------------------------------ |
| 2   | 2                  | $(\theta, \phi)$ 或 $d\Omega$                                 |
| 3   | 5                  | $(s_{12}, s_{23}, \theta, \phi, \chi)$ 或 Dalitz 图 + 3 角      |
| 4   | 8                  | $(s_{12}, s_{34}, s_{123}, t, \Omega_1, \Omega_2, \Omega_3)$ |
| $n$ | $3n-4$             | —                                                            |

### 2. 对称性约束

- **全同粒子**：如果末态中有 $k$ 个全同粒子，相空间需要除以 $k!$（或等价地，积分区域限制为有序的子区域）
- **玻色对称性**：$|\mathcal{M}|^2$ 在全同玻色子的交换下必须对称
- **费米统计**：$|\mathcal{M}|^2$ 在全同费米子的交换下必须反对称（在振幅层面）

---

## 十三、相空间积分的解析技巧

### 1. Passarino-Veltman 约化

当振幅中包含圈图修正时，相空间积分可能涉及张量结构。Passarino-Veltman 方法将张量积分约化为标量积分。

### 2. 洛伦兹不变量积分

在相空间积分中，经常遇到以下类型的积分：

$$I_{\mu\nu} = \int d\Phi_n\;p_\mu^{(a)}\,p_\nu^{(b)}$$

由 Lorentz 协变性，结果只能包含 $P_\mu$、$P_\nu$ 和 $\eta_{\mu\nu}$：

$$I_{\mu\nu} = A\,P_\mu P_\nu + B\,\eta_{\mu\nu}$$

系数 $A$、$B$ 可通过缩并确定。

### 3. 积分恒等式

以下恒等式在相空间积分中非常有用：

$$\int\frac{d^3p}{2E}\,f(p) = \int d^4p\;\delta(p^2 - m^2)\theta(p^0)\,f(p)$$

$$\int\frac{d^3p}{2E}\,(2\pi)^4\delta^{(4)}(P-p) = \frac{(2\pi)^4}{2E_P}\delta(s - M^2)\theta(P^0) \quad \text{（单粒子态）}$$

---

## 十四、总结

| 要点 | 内容 |
|------|------|
| **定义** | $d\Phi_n = (2\pi)^4\delta^{(4)}(P-\sum p_i)\prod_i \frac{d^3p_i}{(2\pi)^3 2E_i}$ |
| **洛伦兹不变性** | $d\Phi_n$ 是 Lorentz 标量 |
| **二体** | $d\Phi_2 = \frac{p^*}{16\pi^2\sqrt{s}}d\Omega$，无量纲 |
| **三体** | $d\Phi_3 = \frac{ds_{12}ds_{23}}{128\pi^3 s}$，Dalitz 图 |
| **递推分解** | $d\Phi_n = d\Phi_{n-k+1}\cdot\frac{ds_k}{2\pi}\cdot d\Phi_k$ |
| **无质量封闭公式** | $\Phi_n^{(0)} \propto s^{n-2}/(4\pi)^{2n-4}$ |
| **阈行为** | $\Phi_n \propto (s-s_{\text{thr}})^{(3n-5)/2}$ |
| **独立变量** | $3n - 4$ 个 Lorentz 不变量 |
| **截面** | $d\sigma = \frac{\|\mathcal{M}\|^2}{4p^*\sqrt{s}}d\Phi_n$ |
| **衰变率** | $d\Gamma = \frac{\|\mathcal{M}\|^2}{2M}d\Phi_n$ |
| **数值方法** | RAMBO、递推采样、重要性采样 |
