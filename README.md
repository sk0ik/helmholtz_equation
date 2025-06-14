- [ヘルムホルツ方程式](#ヘルムホルツ方程式)
- [スカラー場](#スカラー場)
- [ベクトル場](#ベクトル場)

## ヘルムホルツ方程式

ファラデーの法則

$$
\nabla \times \boldsymbol {E} (\boldsymbol {r} , t) = -\frac{\partial \boldsymbol {B} (\boldsymbol {r} , t) } {\partial t}
$$

に対して両辺の回転を取ると

$$
\nabla \times (\nabla \times \boldsymbol {E} (\boldsymbol {r} , t) ) = - \mu_0 \nabla \times \frac{\partial \boldsymbol {H} (\boldsymbol {r} , t) }{\partial t}
$$

となります.ここでアンペールの法則

$$
\nabla \times \boldsymbol {H} (\boldsymbol {r} , t) = \epsilon_0 \frac{\partial \boldsymbol {E} (\boldsymbol {r} , t) }{\partial t}
$$

を代入すると

$$
\nabla \times (\nabla \times \boldsymbol {E} (\boldsymbol {r} , t) ) = - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} , t) }{\partial t^2}
$$

を得ます.ここで

$$
\nabla \times (\nabla \times \boldsymbol {E} (\boldsymbol {r} , t) ) = \nabla(\nabla \cdot \boldsymbol {E} (\boldsymbol {r} , t) ) - \nabla^2 \boldsymbol {E} (\boldsymbol {r} , t)
$$

より

$$
\nabla(\nabla \cdot \boldsymbol {E} (\boldsymbol {r} , t) ) - \nabla^2 \boldsymbol {E} (\boldsymbol {r} , t) = - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} , t) }{\partial t^2}
$$

を得ます.電荷がない場合は

$$
\nabla \cdot \boldsymbol {E} (\boldsymbol {r} , t) = 0
$$

より

$$
\begin{aligned}
-\nabla^2 \boldsymbol {E} (\boldsymbol {r} , t) &= -\epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} , t) }{\partial t^2} \\
\nabla^2 \boldsymbol {E} (\boldsymbol {r} , t) &= \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} , t) }{\partial t^2} 
\end{aligned}
$$

$$
\therefore \nabla^2 \boldsymbol{E} (\boldsymbol {r} , t) - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} , t)}{\partial t^2} = 0
$$

となります.ここで解の形を

$$
\boldsymbol {E} (\boldsymbol {r} , t) = \boldsymbol {E} (\boldsymbol {r}) f(t)
$$

と分離できると仮定します.これを代入すると

$$
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) f(t) - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} ) f(t)}{\partial t^2} = 0
$$

を得ます.ここでフーリエ変換

$$
F(\omega) = \frac{1}{\sqrt{2 \pi}}\int_{- \infty}^{\infty}f(t) e^{i \omega t}dt
$$

を考えると

$$
f(t) = \frac{1}{\sqrt{2 \pi}}\int_{- \infty}^{\infty}F(\omega) e^{-i \omega t}d \omega
$$

であるので代入すると

$$
\begin{aligned}
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) \frac{1}{\sqrt{2 \pi}}\int_{- \infty}^{\infty}F(\omega) e^{-i \omega t}d \omega - \epsilon_0 \mu_0 \frac{\partial^2 \boldsymbol {E} (\boldsymbol {r} )}{\partial t^2} \frac{1}{\sqrt{2 \pi}}\int_{- \infty}^{\infty}F(\omega) e^{-i \omega t}d \omega &= 0 \\
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) \frac{1}{\sqrt{2 \pi}}\int_{- \infty}^{\infty}F(\omega) e^{-i \omega t}d \omega + \frac{\epsilon_0 \mu_0 \omega ^2}{\sqrt{2 \pi}} \boldsymbol {E} (\boldsymbol {r} ) \int_{- \infty}^{\infty}F(\omega) e^{-i \omega t}d \omega &= 0 \\
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) + \epsilon_0 \mu_0 \omega ^2 \boldsymbol{E} (\boldsymbol {r} ) &= 0 \\
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) + \frac{\omega ^2}{c^2} \boldsymbol{E} (\boldsymbol {r} ) &= 0 \\
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) + \biggl (\frac{2 \pi f}{f \lambda} \biggr ) ^2 \boldsymbol{E} (\boldsymbol {r} ) &= 0 \\
\nabla^2 \boldsymbol{E} (\boldsymbol {r} ) + \biggl (\frac{2 \pi}{\lambda} \biggr ) ^2 \boldsymbol{E} (\boldsymbol {r} ) &= 0 \\
\therefore \nabla^2 \boldsymbol{E} (\boldsymbol {r} ) + k ^2 \boldsymbol{E} (\boldsymbol {r} ) &= 0
\end{aligned}
$$

を得ます.これはヘルムホルツ方程式と言うタイプの偏微分方程式です.

## スカラー場

もし電場がスカラー場(偏光分布が直線であるので厳密にはベクトル場であるが座標系を適当に選べば電場の大きさだけを考えればいい)であれば

$$
\boldsymbol{E}(\boldsymbol{r}) = u(x, y, z) e^{ikz} 
$$

のように書けます.これを先ほどのヘルムホルツ方程式に代入すると

$$
\begin{aligned}
\Bigl (\frac{\partial ^2}{\partial ^2 x} + \frac{\partial ^2}{\partial ^2 y} + \frac{\partial ^2}{\partial ^2 z} \Bigr ) \bigl (u(x, y, z) e^{ikz} \bigr ) + k^2 u(x, y, z) e^{ikz} &= 0 \\
\Bigl (\frac{\partial ^2 u}{\partial ^2 x} + \frac{\partial ^2 u}{\partial ^2 y} + \frac{\partial ^2 u}{\partial ^2 z} + 2ik \frac{\partial u}{\partial z} - k^2 u + k^2 u \Bigr ) e^{ikz} &= 0 \\
\frac{\partial ^2 u}{\partial ^2 x} + \frac{\partial ^2 u}{\partial ^2 y} + \frac{\partial ^2 u}{\partial ^2 z} + 2ik \frac{\partial u}{\partial z} &= 0
\end{aligned}
$$

を得ます.ここで近軸近似を考えると

$$
\frac{\partial ^2 u}{\partial ^2 x} + \frac{\partial ^2 u}{\partial ^2 y} + 2ik \frac{\partial u}{\partial z} = 0
$$

を得ます.

## ベクトル場

演算する関数がスカラー場の時、ラプラシアンを演算するということは

$$
\nabla ^2 f = \nabla \cdot (\nabla f)
$$

となり勾配をとった後に発散をとることに相当します.**(スカラーラプラス演算子)**

演算する関数がベクトル場の時,ラプラシアンを演算するということは

$$
\nabla ^2 \boldsymbol{f} = \nabla (\nabla \cdot \boldsymbol{f})
-\nabla \times (\nabla \times \boldsymbol{f})
$$

に相当します.**(ベクトルラプラス演算子)**

今は電荷が存在しないマクスウェル方程を考えているので右辺第1項はゼロになり

$$
\nabla \times \nabla \times \boldsymbol{E} -k^2 \boldsymbol{E} = 0
$$

となります.ここで解の形として

$$
\boldsymbol{E}(r, z) = U(r, z) e^{ikz} \boldsymbol{e}_\phi
$$

のように軸対称な解を考えます.
円筒座標系でのナブラは

$$
\nabla = \frac{\partial}{\partial r} \boldsymbol{e} _ r + \frac{1}{r} \frac{\partial}{\partial \phi} + \frac{\partial}{\partial z} \boldsymbol{e} _ z
$$

となりますが,今は $\phi$ が一定であるので

$$
\nabla = \frac{\partial}{\partial r} \boldsymbol{e}_r + \frac{\partial}{\partial z} \boldsymbol{e}_z
$$

となります.これを踏まえたうえで回転をとると

$$
\nabla \times \boldsymbol{E} = \Bigl (\frac{1}{r} \frac{\partial}{\partial \phi} E _ z - \frac{\partial}{\partial z} E_\phi \Bigr ) \boldsymbol{e} _ r + \Bigl (\frac{\partial}{\partial z} E_r - \frac{\partial}{\partial r} E _ z \Bigr ) \boldsymbol{e} _ \phi + \frac{1}{r} \Bigl (\frac{\partial}{\partial r} (r E_\phi) - \frac{\partial}{\partial \phi} E _ r \Bigr )\boldsymbol{e} _ z
$$

となりますが今は

$$
E _ r = E _ z = 0
$$

より

$$
\nabla \times \boldsymbol{E} = - \frac{\partial}{\partial z} E _ \phi \boldsymbol{e} _ r + \frac{1}{r} \frac{\partial}{\partial r} (r E_\phi) \boldsymbol{e} _ z
$$

$$
\begin{aligned}
\nabla \times (\nabla \times \boldsymbol{E})
&=
\frac{1}{r} \frac{\partial}{\partial \phi} \Bigl ( \frac{1}{r} \frac{\partial}{\partial r} (r E _ \phi) \Bigr ) \boldsymbol{e}_r - \Bigl ( \frac{\partial ^2}{\partial z ^2} E _ \phi + \frac{\partial}{\partial r} \Bigl ( \frac{1}{r} \frac{\partial}{\partial r} (r E _ \phi) \Bigr ) \Bigr ) \boldsymbol{e} _ \phi \newline
&=
-\Bigl ( \frac{\partial ^2}{\partial z ^2} E _ \phi + \frac{\partial}{\partial r} \Bigl ( \frac{1}{r} \frac{\partial}{\partial r} (r E _ \phi) \Bigr ) \Bigr ) \boldsymbol{e} _ \phi \newline
\end{aligned}
$$

※ $E _ \phi$ は $\phi$ を含まないので第1項はゼロ

いったん整理すると

$$
\begin{aligned}
\nabla \times \nabla \times \boldsymbol{E} -k^2 \boldsymbol{E} &= 0 \\
-\frac{\partial ^2}{\partial z ^2} E_\phi -\frac{\partial}{\partial r} \Bigl ( \frac{1}{r} \frac{\partial}{\partial r} (r E_\phi) \Bigr ) -k^2 E_\phi &= 0 \\
\end{aligned}
$$

となります.これを計算すれば

$$
\begin{aligned}
\Bigl ( -\frac{\partial ^2 U}{\partial z ^2} -2ik \frac{\partial U}{\partial z} +k^2 U +\frac{1}{r^2} U -\frac{1}{r} \frac{\partial U}{\partial r} -\frac{\partial ^2 U}{\partial r ^2} -k^2 U \Bigr ) e^{ikz} &= 0 \\
-\frac{\partial ^2 U}{\partial z ^2} -2ik \frac{\partial U}{\partial z} +\frac{1}{r^2} U -\frac{1}{r} \frac{\partial}{\partial r} \Bigl ( r \frac{\partial U}{\partial r} \Bigl ) &= 0 \\
\therefore \quad \frac{1}{r} \frac{\partial}{\partial r} \Bigl ( r \frac{\partial U}{\partial r} \Bigl ) -\frac{1}{r^2} U +2ik \frac{\partial U}{\partial z} +\frac{\partial ^2 U}{\partial z ^2} &= 0
\end{aligned}
$$

を得ます.例によって近軸近似をすると左辺第4項はゼロになるので

$$
\frac{1}{r} \frac{\partial}{\partial r} \Bigl ( r \frac{\partial U}{\partial r} \Bigl ) - \frac{1}{r^2} U + 2ik \frac{\partial U}{\partial z} = 0
$$

を得ます.
