## 一、基本形式

### 1.1 标准 Breit-Wigner 公式

能量 $E$ 处的散射截面或反应截面：

$$\boxed{\sigma(E) = \frac{\pi}{k^2} \cdot \frac{(2J+1)}{(2s_1+1)(2s_2+1)} \cdot \frac{\Gamma^2}{(E - E_R)^2 + \dfrac{\Gamma^2}{4}}}$$

| 符号 | 含义 |
|:---:|:---|
| $E$ | 入射粒子质心系总能量 |
| $E_R$ | 共振能量（截面峰值位置） |
| $\Gamma$ | 共振总宽度（半高全宽） |
| $J$ | 共振态总角动量 |
| $s_1, s_2$ | 入射粒子自旋 |
| $k$ | 质心系波矢大小 |
| $\Gamma_i$ | 第 $i$ 个衰变道的分宽度 |

### 1.2 归一化的线形函数

定义归一化的 Breit-Wigner 线形：

$$\boxed{BW(E) = \frac{1}{2\pi} \cdot \frac{\Gamma}{(E - E_R)^2 + \dfrac{\Gamma^2}{4}}}$$

满足归一化：

$$\int_{-\infty}^{+\infty} BW(E)\, dE = 1$$

> **这就是粒子质量分布 $\rho(M)$ 的来源**——将能量 $E$ 替换为质量 $M$、共振能量 $E_R$ 替换为粒子质量 $m$，即得：

$$\rho(M) = \frac{1}{2\pi} \cdot \frac{\Gamma}{(M - m)^2 + \dfrac{\Gamma^2}{4}}$$

---

## 二、从 S 矩阵到 Breit-Wigner

### 2.1 S 矩阵的极点结构

在量子力学的散射理论中，S 矩阵在复能量平面上的**极点**对应共振态。

对一个共振态，S 矩阵元在极点附近的行为为：

$$S(E) \sim 1 - \frac{i\Gamma}{E - E_R + i\Gamma/2}$$

在共振能量 $E_R$ 处，$|S|$ 偏离单位圆（弹性散射不守恒），表明发生了**非弹性过程**（粒子被吸收后衰变）。

### 2.2 传播子的推导

考虑一个寿命有限的不稳定粒子，其传播子不再是自由传播子的形式，而是包含**自能修正** $\Sigma(E)$：

$$G(E) = \frac{1}{E - m_0 - \Sigma(E)}$$

在共振附近，将自能展开：

$$\Sigma(E_R) = \text{Re}\,\Sigma(E_R) + i\,\text{Im}\,\Sigma(E_R)$$

定义：
- **物理质量**：$m = m_0 + \text{Re}\,\Sigma(E_R)$
- **宽度**：$\Gamma = -2\,\text{Im}\,\Sigma(E_R)$

则传播子在共振附近变为：

$$\boxed{G(E) \approx \frac{1}{E - m + i\Gamma/2}}$$

传播子的模方给出质量的概率密度：

$$|G(E)|^2 = \frac{1}{(E - m)^2 + \Gamma^2/4}$$

归一化后即得 Breit-Wigner 分布。

### 2.3 与光学定理的联系

**光学定理**将总截面与前向散射振幅联系起来：

$$\sigma_{\text{tot}} = \frac{4\pi}{k}\,\text{Im}\,f(0)$$

在共振附近，散射振幅的分波展开中，共振分波的振幅为：

$$f_l(E) = \frac{\Gamma/2}{E_R - E - i\Gamma/2} \cdot e^{2i\delta_l^{\text{bg}}}$$

取模方后得到 Lorentz 型的截面——这就是 Breit-Wigner 公式。

---

## 三、分宽度与分支比

### 3.1 总宽度 = 分宽度之和

共振态可以通过多个衰变道衰变，每个道有对应的**分宽度** $\Gamma_i$：

$$\boxed{\Gamma = \sum_i \Gamma_i}$$

### 3.2 分支比

第 $i$ 个衰变道的**分支比**（branching ratio）：

$$\boxed{BR_i = \frac{\Gamma_i}{\Gamma} = \frac{\Gamma_i}{\sum_j \Gamma_j}}$$

$$\sum_i BR_i = 1 \quad \checkmark$$

### 3.3 实例：$Z^0$ 玻色子

| 衰变道 | 分宽度 $\Gamma_i$ | 分支比 $BR_i$ |
|:---:|:---:|:---:|
| $Z^0 \to e^+e^-$ | $83.9\ \text{MeV}$ | $3.36\%$ |
| $Z^0 \to \mu^+\mu^-$ | $83.8\ \text{MeV}$ | $3.36\%$ |
| $Z^0 \to \tau^+\tau^-$ | $83.8\ \text{MeV}$ | $3.37\%$ |
| $Z^0 \to$ hadrons | $1744\ \text{MeV}$ | $69.9\%$ |
| $Z^0 \to \nu\bar\nu$（每种） | $166\ \text{MeV}$ | $6.67\%$ |
| **总计** | $\Gamma = 2495\ \text{MeV}$ | $100\%$ |

### 3.4 含分宽度的完整 Breit-Wigner

如果只观测特定衰变道 $i \to f$，截面中的宽度需要替换为对应的分宽度：

$$\sigma_{i \to f}(E) \propto \frac{\Gamma_i \Gamma_f}{(E - E_R)^2 + \Gamma^2/4}$$

> **峰值截面** $\propto \Gamma_i \Gamma_f / \Gamma^2 = BR_i \cdot BR_f$。

---

## 四、能量依赖的宽度

### 4.1 阈值效应

当衰变产物的质量不可忽略时，宽度 $\Gamma$ 不再是常数，而是依赖于能量：

$$\Gamma(E) = \Gamma_R \cdot \left(\frac{p}{p_R}\right)^{2l+1} \cdot \frac{m_R}{E}$$

其中：
- $p = \sqrt{(E^2 - (m_1+m_2)^2)(E^2 - (m_1-m_2)^2)}\,/\,2E$ 是衰变产物的质心动量
- $l$ 是衰变的轨道角动量
- $p_R = p(E_R)$ 是共振处的动量

> 当 $E < m_1 + m_2$（低于阈值）时，$p \to 0$，$\Gamma \to 0$——粒子不能衰变到该道。

### 4.2 修正后的 Breit-Wigner

$$\boxed{\sigma(E) \propto \frac{\Gamma_i(E)\, \Gamma_f(E)}{(E - E_R)^2 + \Gamma(E)^2/4}}$$

> 这种形式称为**能量依赖宽度的 Breit-Wigner 公式**，在处理近阈共振时尤为重要。

---

## 五、Breit-Wigner 分布的性质

### 5.1 基本性质

| 性质 | 表达式 |
|:---|:---:|
| 峰值位置 | $E = E_R$ |
| 峰值高度 | $\propto 4/\Gamma^2$ |
| 半高全宽（FWHM） | $\Gamma$ |
| 归一化 | $\int_{-\infty}^{+\infty} BW(E)\, dE = 1$ |
| 期望值 | $\langle E \rangle = E_R$ |
| 方差 | $\langle (\Delta E)^2 \rangle$ 发散（重尾分布） |

### 5.2 与 Gauss 分布的对比

```
概率
  │
  │   ╭──╮        Breit-Wigner（Lorentz型）
  │  ╱    ╲       有长尾，方差发散
  │ ╱  ╭─╮ ╲
  │╱  ╱   ╲  ╲
  │  ╱     ╲  ╲───
  │ ╱       ╲─────
  │╱Gauss     ────────
  ┼────────────────────→ E
       E_R
```

| 性质 | Breit-Wigner（Lorentz） | Gauss |
|:---:|:---:|:---:|
| 函数形式 | $\propto [(E-E_R)^2 + \Gamma^2/4]^{-1}$ | $\propto e^{-(E-E_R)^2/2\sigma^2}$ |
| 尾部衰减 | $\sim 1/E^2$（慢） | $\sim e^{-E^2}$（快） |
| 方差 | **发散** | $\sigma^2$（有限） |
| 物理来源 | 量子共振（有限寿命） | 经典涨落（中心极限定理） |
| Fourier 变换 | 指数衰减 $e^{-\Gamma t/2}$ | Gauss 波包 |

> **Breit-Wigner 的 Fourier 变换是指数衰减**——这正是不稳定粒子的概率随时间的衰减规律 $P(t) = e^{-\Gamma t}$。

---

## 六、从量子力学推导

### 6.1 含时方法

不稳定粒子的衰变由含时 Schrödinger 方程描述。设共振态 $|R\rangle$ 与连续谱 $|E\rangle$ 耦合：

$$i\frac{d}{dt}|R\rangle = E_R|R\rangle + \int V_E |E\rangle\, dE$$

在 Born 近似下（Fermi 黄金规则）：

$$\Gamma = 2\pi \sum_f |\langle f|V|R\rangle|^2 \rho(E_f)$$

对 $|R\rangle$ 做 Laplace 变换，得到传播子：

$$G(s) = \frac{1}{s - E_R + i\Gamma/2}$$

Fourier 变换回能量空间：

$$G(E) = \frac{1}{E - E_R + i\Gamma/2}$$

$$|G(E)|^2 = \frac{1}{(E - E_R)^2 + \Gamma^2/4}$$

### 6.2 含时衰减

共振态的存活概率：

$$P(t) = |G(t)|^2 = e^{-\Gamma t}$$

平均寿命：

$$\tau = \int_0^\infty t\, \Gamma\, e^{-\Gamma t}\, dt = \frac{1}{\Gamma}$$

---

## 七、实验中的应用

### 7.1 共振的识别

在实验数据中，Breit-Wigner 共振表现为：

1. **截面在特定能量处出现峰值**
2. **峰值附近截面的线形符合 Lorentz 型**
3. **相移在共振处快速通过 $\pi/2$**

### 7.2 经典实例

| 共振态 | 共振能量 $E_R$ | 宽度 $\Gamma$ | 衰变道 | 发现方式 |
|:---:|:---:|:---:|:---:|:---|
| $\Delta(1232)$ | $1232\ \text{MeV}$ | $\sim 120\ \text{MeV}$ | $N\pi$ | $\pi N$ 散射截面峰值 |
| $\rho(770)$ | $770\ \text{MeV}$ | $\sim 150\ \text{MeV}$ | $\pi\pi$ | $\pi\pi$ 不变质量谱 |
| $Z^0$ | $91.2\ \text{GeV}$ | $2.5\ \text{GeV}$ | $l^+l^-, q\bar q, \nu\bar\nu$ | $e^+e^-$ 质心能量扫描 |
| Higgs | $125\ \text{GeV}$ | $\sim 4\ \text{MeV}$ | $ZZ^*, WW^*, \gamma\gamma, \ldots$ | 不变质量谱重建 |

### 7.3 数据拟合

实验上测量截面 $\sigma_i$ 后，用 Breit-Wigner 公式拟合：

$$\sigma_{\text{fit}}(E) = \frac{A\, \Gamma^2}{(E - E_R)^2 + \Gamma^2/4} + \text{背景项}$$

拟合参数：$E_R$（共振位置）、$\Gamma$（宽度）、$A$（归一化系数）。

---

## 八、与粒子质量分布的联系

回到粒子质量的讨论，Breit-Wigner 公式给出了**不稳定粒子质量的测量值分布**：

$$\rho(M) = \frac{\Gamma}{2\pi\left[(M-m)^2 + \dfrac{\Gamma^2}{4}\right]}$$

| Breit-Wigner 参数 | 粒子物理对应 |
|:---:|:---:|
| $E_R$ | 粒子质量 $m$ |
| $\Gamma$ | 粒子宽度 $\Gamma$ |
| $1/\Gamma$ | 粒子寿命 $\tau$ |
| $BW(E_R) \propto 1/\Gamma^2$ | 共振峰值高度 |
| $\Gamma_i / \Gamma$ | 分支比 $BR_i$ |

> **核心联系**：不稳定粒子的质量不是确定值，而是由 Breit-Wigner 分布描述的几率分布。宽度 $\Gamma$ 越大，质量的不确定度越大，粒子寿命越短。这就是量子力学中**能量-时间不确定关系** $\Delta E \cdot \Delta t \sim \hbar$ 的直接体现。

---

## 九、总结

$$\boxed{\rho(E) = \frac{1}{2\pi}\frac{\Gamma}{(E - E_R)^2 + \Gamma^2/4}, \qquad \tau = \frac{1}{\Gamma}, \qquad BR_i = \frac{\Gamma_i}{\Gamma}}$$

| 层面 | Breit-Wigner 公式的含义 |
|:---|:---|
| **数学** | 复平面上单极点的模方 |
| **量子力学** | 有限寿命态的能量分布 |
| **散射理论** | 共振分波的截面线形 |
| **粒子物理** | 不稳定粒子的质量分布 |
| **实验** | 截面峰值的拟合函数 |