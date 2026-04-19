# Midtern-report-11424144

# 質量-彈簧-阻尼系統（Mass-Spring-Damper System）

## 問題描述
考慮系統受到正弦外力：
$
F(t) = F_0 \cos(\omega t)
$

其運動方程為：
$
m\ddot{x} + c\dot{x} + kx = F_0 \cos(\omega t)
$

---

## 解的結構
通解為：
$
x(t) = x_h(t) + x_p(t)
$

- $x_h(t)$：齊次解（Transient Response）
- $x_p(t)$：特解（Steady-State Response）

---

## A. 齊次解（Transient Response）

考慮齊次方程：
$
m\ddot{x} + c\dot{x} + kx = 0
$

特徵方程：
$
ms^2 + cs + k = 0
$

解得：
$
s = \frac{-c \pm \sqrt{c^2 - 4mk}}{2m}
$

### 欠阻尼情況（常見）：
$
x_h(t) = e^{-\frac{c}{2m}t}\left(C_1 \cos(\omega_d t) + C_2 \sin(\omega_d t)\right)
$

其中：
$
\omega_d = \sqrt{\frac{k}{m} - \left(\frac{c}{2m}\right)^2}
$

---

## B. 特解（Steady-State Response）

假設解為：
$
x_p(t) = X \cos(\omega t - \phi)
$

### 振幅：
$
X = \frac{F_0}{\sqrt{(k - m\omega^2)^2 + (c\omega)^2}}
$

### 相位角：
$
\phi = \tan^{-1}\left(\frac{c\omega}{k - m\omega^2}\right)
$

---

## 最終穩態解

當時間足夠長（忽略 transient）：
$
x(t) = \frac{F_0}{\sqrt{(k - m\omega^2)^2 + (c\omega)^2}}
\cos\left(\omega t - \tan^{-1}\left(\frac{c\omega}{k - m\omega^2}\right)\right)
$

---

## 物理意義

### 共振（Resonance）
當外力頻率接近自然頻率時：
$
\omega_n = \sqrt{\frac{k}{m}}
$

（實際有阻尼時）：
$
\omega_r = \sqrt{\frac{k}{m} - \frac{c^2}{2m^2}}
$

振幅會達到最大。

---

### 阻尼影響
- 阻尼 $c$ 增加 → 振幅降低
- 系統更穩定，但反應較慢
- 產生相位延遲 $\phi$

---

## 工程結論

- 系統最終會以外力頻率 $\omega$ 振動
- 阻尼控制振幅大小
- 避免共振是設計關鍵
