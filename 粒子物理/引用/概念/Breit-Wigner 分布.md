## 一、物理起源

### 1.1 共振现象

在粒子物理实验中，当碰撞能量恰好"匹配"某个短寿命粒子的质量时，产生截面会出现一个显著的**峰**——这就是**共振**（resonance）。

> 想象推一个秋千。如果你推的频率恰好等于秋千的固有频率，振幅会急剧增大——这就是共振。类似地，当碰撞质心能量恰好等于某个不稳定粒子的质量时，产生概率急剧增大。

许多重要的粒子最初就是作为共振峰被发现的：

| 粒子 | 发现年份 | 共振过程 | 质量 | 宽度 |
|------|---------|---------|------|------|
| $\Delta(1232)$ | 1951 | $\pi N \to \pi N$ | $1232\;\text{MeV}$ | $117\;\text{MeV}$ |
| $\rho(770)$ | 1961 | $\pi\pi \to \pi\pi$ | $775\;\text{MeV}$ | $149\;\text{MeV}$ |
| $J/\psi$ | 1974 | $e^+e^- \to \text{hadrons}$ | $3097\;\text{MeV}$ | $0.093\;\text{MeV}$ |
| $Z^0$ | 1989 | $e^+e^- \to f\bar{f}$ | $91.2\;\text{GeV}$ | $2.50\;\text{GeV}$ |
| Higgs | 2012 | $gg \to H \to \gamma\gamma,ZZ$ | $125\;\text{GeV}$ | $4.1\;\text{MeV}$ |

### 1.2 核心问题

> **共振峰的线形（shape）由什么决定？**

答案就是 **Breit-Wigner 分布**。

---

## 二、从传播子推导

### 2.1 不稳定粒子的传播子

一个质量为 $M$、总衰变宽度为 $\Gamma$ 的不稳定粒子，其传播子在动量空间中具有如下形式：

$$\boxed{\widetilde{G}(s) = \frac{1}{s - M^2 + iM\Gamma}}$$

其中 $s = -p^\mu p_\mu$（采用度规 $(-,+,+,+)$）是 Mandelstam 变量。

### 2.2 传播子的模方

物理可观测量（截面）正比于振幅的模方，因此核心量是：

$$\boxed{|\widetilde{G}(s)|^2 = \frac{1}{(s - M^2)^2 + M^2\Gamma^2}}$$

这就是**Breit-Wigner 分布**。

### 2.3 推导的物理逻辑

为什么传播子具有这种形式？我们可以从多个角度理解：

**（1）从自能修正出发**

裸传播子经过量子修正后：

$$\widetilde{G}(s) = \frac{1}{s - M_0^2 - \Sigma(s)}$$

其中 $\Sigma(s)$ 是**自能函数**（self-energy）。在共振附近将 $\Sigma(s)$ 在 $s = M^2$ 处展开：

$$\Sigma(s) \approx \Sigma(M^2) + (s - M^2)\,\Sigma'(M^2) + \cdots$$

定义物理质量 $M^2 = M_0^2 + \mathrm{Re}\,\Sigma(M^2)$，并将虚部吸收进宽度：

$$\mathrm{Im}\,\Sigma(M^2) = M\Gamma$$

得到 Breit-Wigner 形式。

**（2）从阻尼谐振子类比**

经典力学中，一个阻尼谐振子的格林函数（频率域）：

$$G(\omega) = \frac{1}{\omega^2 - \omega_0^2 + i\gamma\omega}$$

在共振频率 $\omega_0$ 附近，分母中的虚部 $i\gamma\omega$ 给出有限的峰宽——与 Breit-Wigner 的结构完全类似。

**（3）从量子力学散射理论**

在分波展开中，$\ell$ 分波的散射振幅在共振附近具有形式：

$$f_\ell(s) \propto \frac{1}{E - E_R + i\Gamma/2}$$

这正是非相对论形式的 Breit-Wigner。

---

## 三、Breit-Wigner 的两种常见形式

### 3.1 相对论形式（$s$-channel）

$$\boxed{|\mathcal{A}(s)|^2 \propto \frac{1}{(s - M^2)^2 + M^2\Gamma^2}}$$

- 变量：$s$（不变质量的平方）
- 峰位：$s = M^2$
- 半高全宽（FWHM）：$\Delta s = 2M\Gamma$

### 3.2 非相对论形式（能量变量）

在 $s \approx M^2$ 附近，令 $s = (M + E)^2 \approx M^2 + 2ME$（$E \ll M$），代入：

$$|\mathcal{A}|^2 \propto \frac{1}{(2ME)^2 + M^2\Gamma^2} = \frac{1}{4M^2}\cdot\frac{1}{E^2 + (\Gamma/2)^2}$$

$$\boxed{|\mathcal{A}(E)|^2 \propto \frac{1}{E^2 + (\Gamma/2)^2}}$$

其中 $E = \sqrt{s} - M$ 是偏离共振峰的能量。

- 峰位：$E = 0$（即 $\sqrt{s} = M$）
- FWHM：$\Delta E = \Gamma$

> 这就是**洛伦兹线形**（Lorentzian line shape），在光学和原子物理中也广泛出现。

---

## 四、Breit-Wigner 的数学性质

### 4.1 归一化

对非相对论形式在全能量范围积分：

$$\int_{-\infty}^{+\infty}\frac{dE}{E^2 + (\Gamma/2)^2} = \frac{2\pi}{\Gamma}$$

因此归一化的 Breit-Wigner 分布为：

$$\boxed{f(E) = \frac{\Gamma/(2\pi)}{E^2 + (\Gamma/2)^2}}$$

这是一个**柯西分布**（Cauchy distribution）——概率论中著名的重尾分布。

### 4.2 峰值与半高

**峰值**（$E = 0$）：

$$f_{\max} = \frac{1}{(\Gamma/2)^2} \cdot \frac{\Gamma}{2\pi} = \frac{2}{\pi\Gamma}$$

**半高处**（$f = f_{\max}/2$）：

$$E_{1/2} = \pm\frac{\Gamma}{2}$$

因此**半高全宽**（FWHM）：

$$\boxed{\text{FWHM} = \Gamma}$$

### 4.3 累积分布

从 $-E_0$ 到 $+E_0$ 的积分概率：

$$P(|E| \leq E_0) = \frac{2}{\pi}\arctan\!\left(\frac{2E_0}{\Gamma}\right)$$

| 范围 | 积分概率 |
|------|---------|
| $\|E\| \leq \Gamma/2$（峰内） | $50\%$ |
| $\|E\| \leq \Gamma$ | $63.7\%$ |
| $\|E\| \leq 2\Gamma$ | $80.0\%$ |
| $\|E\| \leq 5\Gamma$ | $93.7\%$ |
| $\|E\| \leq 10\Gamma$ | $96.8\%$ |

> **注意**：Breit-Wigner 分布具有**重尾**——远离峰处的概率衰减为 $1/E^2$，比高斯分布的 $e^{-E^2}$ 慢得多。这意味着"翼部"的贡献不可忽略。

### 4.4 与高斯分布的对比

| 性质 | Breit-Wigner（柯西） | 高斯 |
|------|---------------------|------|
| 函数形式 | $\frac{1}{E^2 + (\Gamma/2)^2}$ | $e^{-E^2/(2\sigma^2)}$ |
| 峰值 | 有限 | 有限 |
| 翼部衰减 | $\sim 1/E^2$（慢） | $\sim e^{-E^2}$（快） |
| 均值 | 不存在（积分发散） | $\mu$ |
| 方差 | 不存在（积分发散） | $\sigma^2$ |
| 物理起源 | 量子力学（指数衰变） | 统计涨落（中心极限定理） |

> **物理理解**：高斯分布来自大量独立随机因素的叠加（中心极限定理）。Breit-Wigner 分布来自**量子力学中不稳定态的指数衰变**——它是能量-时间不确定性关系的直接数学体现。

---

## 五、从量子力学推导 Breit-Wigner

### 5.1 指数衰变的傅里叶变换

一个不稳定态 $|\psi\rangle$ 的时间演化：

$$|\psi(t)\rangle = e^{-i(E_0 - i\Gamma/2)t/\hbar}\,|\psi(0)\rangle$$

其模方：

$$|\psi(t)|^2 = e^{-\Gamma t/\hbar}$$

这正是指数衰变律，寿命 $\tau = \hbar/\Gamma$。

对时间演化函数做傅里叶变换，得到能量域的振幅：

$$\widetilde{\psi}(E) = \int_0^\infty e^{+iEt/\hbar}\,e^{-i(E_0 - i\Gamma/2)t/\hbar}\,dt = \frac{i\hbar}{E - E_0 + i\Gamma/2}$$

概率密度：

$$\boxed{|\widetilde{\psi}(E)|^2 = \frac{\hbar^2}{(E - E_0)^2 + \Gamma^2/4} \propto \frac{1}{(E - E_0)^2 + (\Gamma/2)^2}}$$

> **Breit-Wigner 分布就是指数衰变律的傅里叶变换**——这是它最深刻的物理根源。

### 5.2 能量-时间不确定性

$$\Delta E \cdot \Delta t \sim \hbar$$

- $\Delta t = \tau = \hbar/\Gamma$（粒子寿命）
- $\Delta E = \Gamma/2$（能量展宽的半宽）

因此：

$$\Gamma \cdot \tau = \hbar$$

> 粒子存在的时间越短（$\tau$ 小），它的能量（质量）就越不确定（$\Gamma$ 大）——Breit-Wigner 的宽度就是这种不确定性的量化。

---

## 六、散射截面中的 Breit-Wigner

### 6.1 共振散射截面

对于通过共振态 $R$ 进行的散射过程 $a + b \to R \to c + d$，截面具有 Breit-Wigner 形式：

$$\boxed{\sigma(s) = \frac{4\pi}{k^2}\,\frac{(2J_R + 1)}{(2s_a + 1)(2s_b + 1)}\,\frac{\Gamma_{\text{in}}\,\Gamma_{\text{out}}}{(s - M^2)^2 + M^2\Gamma_{\text{tot}}^2}}$$

其中：
- $J_R$：共振态自旋
- $s_a, s_b$：初态粒子自旋
- $\Gamma_{\text{in}}$：共振态衰变到初态道的**分宽度**（入射道）
- $\Gamma_{\text{out}}$：衰变到末态道的**分宽度**（出射道）
- $\Gamma_{\text{tot}} = \sum_i \Gamma_i$：**总宽度**
- $k$：质心系中动量

### 6.2 峰值截面

在 $s = M^2$ 处：

$$\sigma_{\max} = \frac{4\pi}{k_R^2}\,\frac{(2J_R + 1)}{(2s_a + 1)(2s_b + 1)}\,\frac{\Gamma_{\text{in}}\,\Gamma_{\text{out}}}{M^2\Gamma_{\text{tot}}^2}$$

当入射道和出射道相同时（弹性散射，$\Gamma_{\text{in}} = \Gamma_{\text{out}} = \Gamma_{\text{el}}$），且只有一条衰变道（$\Gamma_{\text{tot}} = \Gamma_{\text{el}}$）：

$$\sigma_{\max} = \frac{4\pi}{k_R^2}\,(2J_R + 1) \cdot \frac{1}{(2s_a + 1)(2s_b + 1)}$$

这就是著名的**幺正性极限**（unitarity limit）——截面不能超过这个值。

### 6.3 具体例子：$Z^0$ 玻色子共振

$e^+e^- \to f\bar{f}$ 过程在 $\sqrt{s} = M_Z$ 附近的截面：

$$\sigma_{e^+e^- \to f\bar{f}}(s) = \frac{12\pi}{M_Z^2}\,\frac{s\,\Gamma_e\,\Gamma_f}{(s - M_Z^2)^2 + M_Z^2\Gamma_Z^2}$$

在 $s = M_Z^2$ 处：

$$\sigma_{\max} = \frac{12\pi}{M_Z^2}\,\frac{\Gamma_e\,\Gamma_f}{\Gamma_Z^2}$$

$$= \frac{12\pi}{(91.2)^2}\,\frac{(0.084)(0.084)}{(2.495)^2} \approx 1.5 \times 10^{-3}\;\text{GeV}^{-2} \approx 58\;\text{nb}$$

> **实验验证**：LEP 对撞机在 $\sqrt{s} = 91.2\;\text{GeV}$ 附近扫描 $e^+e^-$ 湮灭截面，观测到完美的 Breit-Wigner 共振峰——这是标准模型最精确的检验之一。

---

## 七、能量依赖的宽度——推广的 Breit-Wigner

### 7.1 问题

标准 Breit-Wigner 假设 $\Gamma$ 是常数。但严格来说，宽度依赖于共振态的动量，因此依赖于 $s$。

### 7.2 动量依赖的分宽度

对于衰变 $R \to 1 + 2$，分宽度为：

$$\Gamma_{12}(s) = \frac{|\boldsymbol{p}^*(s)|}{8\pi s}\,|\mathcal{M}_{12}|^2$$

其中 $|\boldsymbol{p}^*(s)|$ 是末态粒子在母粒子静止系中的动量：

$$|\boldsymbol{p}^*(s)| = \frac{\lambda^{1/2}(s,\,m_1^2,\,m_2^2)}{2\sqrt{s}}$$

### 7.3 推广的 Breit-Wigner

$$\boxed{\sigma(s) \propto \frac{\Gamma_{\text{in}}(s)\,\Gamma_{\text{out}}(s)}{(s - M^2)^2 + M^2\,\Gamma_{\text{tot}}^2(s)}}$$

分母中的总宽度也依赖于 $s$：

$$\Gamma_{\text{tot}}(s) = \sum_i \Gamma_i(s)$$

### 7.4 具体形式：Blatt-Weisskopf 因子

对于角动量为 $\ell$ 的衰变道，还需引入**势垒穿透因子**（Blatt-Weisskopf barrier factor）$B_\ell(p)$：

$$\Gamma_\ell(s) = \Gamma_\ell(M^2)\,\frac{|\boldsymbol{p}^*(s)|}{|\boldsymbol{p}^*(M^2)|}\,\frac{M}{\sqrt{s}}\,|B_\ell(|\boldsymbol{p}^*|)|^2$$

$B_\ell$ 的具体形式：

| $\ell$ | $\|B_\ell(p)\|^2$ |
|--------|------------------|
| $0$ | $1$ |
| $1$ | $1 + (pR)^2$（$R \sim 1\;\text{fm}$） |
| $2$ | $9 + 3(pR)^2 + (pR)^4$ |

> **物理意义**：高角动量衰变需要克服**离心势垒**。在阈值附近（$|\boldsymbol{p}^*| \to 0$），势垒穿透概率趋于零，宽度被强烈压低——这使得某些高角动量共振态的寿命异常长。

---

## 八、相对论性 Breit-Wigner 的细节

### 8.1 不变量形式

完整的相对论性 Breit-Wigner 振幅：

$$\boxed{\mathcal{A}(s) = \frac{\sqrt{\Gamma_{\text{in}}(s)\,\Gamma_{\text{out}}(s)}\,M}{s - M^2 + iM\Gamma_{\text{tot}}(s)}}$$

满足**幺正性**条件：

$$\mathrm{Im}\,\frac{1}{\mathcal{A}} = -\frac{\Gamma_{\text{tot}}}{M\sqrt{\Gamma_{\text{in}}\Gamma_{\text{out}}}} \leq 0$$

### 8.2 $K$-矩阵参数化

为了保证幺正性在所有能量下成立（不仅在共振附近），可以使用**$K$-矩阵**方法：

$$\mathcal{A}(s) = K(s)\,[1 - i\rho(s)\,K(s)]^{-1}$$

其中 $\rho(s) = 2|\boldsymbol{p}^*|/\sqrt{s}$ 是相空间因子，$K(s)$ 是实函数。

> 多个共振态的贡献通过 $K$-矩阵自然地叠加，自动保持幺正性。

---

## 九、实验上的 Breit-Wigner 线形

### 9.1 窄共振 vs 宽共振

| 类型 | $\Gamma/M$ | 线形特征 | 例子 |
|------|-----------|---------|------|
| 极窄共振 | $\lesssim 10^{-3}$ | 近似 $\delta$ 函数，实验分辨率主导 | $J/\psi$, $\Upsilon$ |
| 窄共振 | $10^{-3} \sim 10^{-1}$ | 清晰的 Breit-Wigner 峰 | $Z^0$, Higgs |
| 宽共振 | $\gtrsim 0.1$ | 线形严重畸变，与相空间耦合 | $\rho$, $\Delta$ |

### 9.2 实验分辨率的卷积

实验测量的截面是理论 Breit-Wigner 与仪器分辨率函数 $R(\sqrt{s})$ 的**卷积**：

$$\sigma_{\text{meas}}(\sqrt{s}) = \int \sigma_{\text{BW}}(\sqrt{s'})\,R(\sqrt{s} - \sqrt{s'})\,d\sqrt{s'}$$

- 对于窄共振（$\Gamma \ll$ 分辨率）：测量到的宽度由分辨率主导，而非物理宽度
- 对于宽共振（$\Gamma \gg$ 分辨率）：分辨率的影响可忽略

> **实验技巧**：对于极窄的共振（如 $J/\psi$），需要高分辨率探测器或扫描测量来提取物理宽度。

### 9.3 干涉效应

当共振振幅与非共振（背景）振幅共存时，会发生**干涉**：

$$|\mathcal{A}_{\text{tot}}|^2 = |\mathcal{A}_{\text{BW}} + \mathcal{A}_{\text{bg}}|^2 = |\mathcal{A}_{\text{BW}}|^2 + 2\,\mathrm{Re}(\mathcal{A}_{\text{BW}}\mathcal{A}_{\text{bg}}^*) + |\mathcal{A}_{\text{bg}}|^2$$

干涉项可以导致线形的**不对称**——这在 $K$ 介子和 $D$ 介子的共振态中经常被观测到，称为 **Fano 线形**或 **Breit-Wigner-Fano 线形**。

---

## 十、Breit-Wigner 的量子场论基础

### 10.1 S 矩阵的解析结构

Breit-Wigner 分布的深层数学基础是 S 矩阵在**复 $s$ 平面**上的解析结构。

稳定粒子的传播子在实轴 $s = M^2$ 处有**极点**。

不稳定粒子的传播子极点移到复平面的**第二黎曼叶**（second Riemann sheet）：

$$s_{\text{pole}} = \left(M - \frac{i\Gamma}{2}\right)^2 = M^2 - iM\Gamma - \frac{\Gamma^2}{4}$$

对于窄共振（$\Gamma \ll M$）：

$$s_{\text{pole}} \approx M^2 - iM\Gamma$$

> **深刻理解**：Breit-Wigner 分布中的 $M^2 - iM\Gamma$ 不是人为引入的"虚部"——它是 S 矩阵在复能量平面上**极点位置**的自然体现。粒子的质量和宽度由**同一个复数极点**的实部和虚部决定。

### 10.2 极点与物理量

$$\boxed{
\begin{aligned}
&\text{极点位置：}\quad s_{\text{pole}} = M^2 - iM\Gamma \\[6pt]
&\text{实部} \to \text{质量}\;M \\[4pt]
&\text{虚部} \to \text{宽度}\;\Gamma\;\text{（寿命}\;\tau = \hbar/\Gamma\text{）}
\end{aligned}
}$$

| 情形 | 极点位置 | 物理含义 |
|------|---------|---------|
| 稳定粒子 | 实轴上 $s = M^2$ | 永不衰变 |
| 不稳定粒子 | 第二黎曼叶 $s = M^2 - iM\Gamma$ | 有限寿命 |
| 虚态（virtual state） | 负实轴 | 无物理质量的束缚态 |
| 离散的束缚态 | 正实轴以下（$s < 0$ 的适当位置） | 稳定束缚态 |

### 10.3 光学定理的体现

Breit-Wigner 分母中的虚部 $iM\Gamma$ 与光学定理直接相关：

$$\mathrm{Im}\,\mathcal{M}_{\text{forward}} = \sqrt{s}\,|\boldsymbol{p}|\,\sigma_{\text{tot}}$$

在共振处，向前散射振幅的虚部达到最大——这正是总截面最大的表现。

---

## 十一、Breit-Wigner 在不同领域的应用

### 11.1 粒子物理

| 应用 | 具体情况 |
|------|---------|
| 共振态搜索 | 在不变质量谱中寻找 Breit-Wigner 峰 |
| 质量和宽度测量 | 拟合峰形提取 $M$ 和 $\Gamma$ |
| 分支比测量 | 不同衰变道的分宽度比 |
| 新粒子搜索 | 在预期质量处寻找超出背景的共振结构 |

### 11.2 核物理

核反应中的共振（如 $s$-波中子俘获）：

$$\sigma_{\text{res}}(E) = \pi\lambdabar^2\,\frac{\Gamma_n\,\Gamma_\gamma}{(E - E_R)^2 + (\Gamma/2)^2}$$

其中 $\lambdabar$ 是约化德布罗意波长，$\Gamma_n$ 是中子道宽度，$\Gamma_\gamma$ 是辐射道宽度。

### 11.3 原子物理与光学

原子跃迁的**自然线形**：

$$I(\omega) \propto \frac{1}{(\omega - \omega_0)^2 + (\gamma/2)^2}$$

其中 $\gamma = 1/\tau$ 是自发辐射率，$\tau$ 是激发态寿命。

> 原子谱线的自然宽度就是 Breit-Wigner 宽度——由激发态的有限寿命决定。

### 11.4 电路与工程

RLC 电路的频率响应：

$$|Z(\omega)|^2 \propto \frac{1}{(\omega^2 - \omega_0^2)^2 + (\gamma\omega)^2}$$

品质因子 $Q = \omega_0/\gamma$ 类似于 $M/\Gamma$。

---

## 十二、总结

Breit-Wigner 分布的核心地位可以用以下关系链概括：

$$\boxed{
\begin{aligned}
&\text{不稳定态的指数衰变}\;e^{-\Gamma t/\hbar} \\[6pt]
&\qquad\xrightarrow{\text{傅里叶变换}} \\[6pt]
&\text{能量域的 Breit-Wigner 分布}\;\frac{1}{(E-E_0)^2+(\Gamma/2)^2} \\[6pt]
&\qquad\xrightarrow{\text{相对论推广}} \\[6pt]
&\text{传播子极点}\;\frac{1}{s - M^2 + iM\Gamma} \\[6pt]
&\qquad\xrightarrow{\text{S 矩阵解析性}} \\[6pt]
&\text{复 }s\text{ 平面上的极点}\;s_{\text{pole}} = M^2 - iM\Gamma
\end{aligned}
}$$

| 概念 | 表达式 | 物理含义 |
|------|--------|---------|
| 峰位 $M$ | 极点实部 | 粒子质量 |
| 宽度 $\Gamma$ | 极点虚部 | 衰变率，$\Gamma = \hbar/\tau$ |
| FWHM | $\Gamma$（能量变量） | 共振峰的宽度 |
| 归一化 | $\int f\,dE = 1$ | 概率守恒 |
| 幺正性 | $\sigma \leq \sigma_{\max}$ | 截面的理论上限 |

Breit-Wigner 分布是连接**微观量子力学**（指数衰变、传播子极点）与**宏观可观测量**（散射截面的共振峰形）的关键桥梁。