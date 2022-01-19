[TOC]

参考サイト
変更してみる

http://physics.thick.jp/Plasma_Physics/Plasma_Physics_top.html



1. Introduction

   1.1. Definition of a Plasma

   1.2. Geophysical Plasmas

   1.3. Magnetospheric Currents

   1.4. Theoretical Approaches

2. Single Particle Motion

   2.1. Field Equations

   2.2. Gyration

   2.3. Electric Drifts

   2.4. Magnetic Drifts

   2.5. Adiabatic Invariants 

3. Trapped Particles

   3.1. Dipole Field

   3.2. Bounce Motion

   3.3. Drift Motion

   3.4. Sources and Sinks

   3.5. Ring Current

4. Collisions and Conductivity

   4.1. Collisions

   4.2. Plasma Conductivity

   4.3. Ionosphere Formation

   4.4. Ionospheric Conductivity

   4.5. Ionospheric Currents

   4.6. Auroral Emissions

5. Convection and Substorms

   5.1. Diffusion and Frozen Flux

   5.2. Convection Electric Field

   5.3. Corotation and Plasmasphere

   5.4. High-Latitude Electrodynamis

   5.5. Auroral Electrojets

   5.6. Megnetospheric Substorms

   5.7. Substorm Currents

   









# 1. Introduction

- 地球物理の対象の変遷
- 地球の外では、電離した状態の物質が存在 ->  プラズマ
- プラズマは電場と磁場の影響を受けやすく、予想外の振る舞いをする
  - space plasma physicsは地球物理学の一分野となった
- 地球のコアや、周囲を取り巻く磁場の理解に使われれる

## 1.1. Definition of a Plasma

- プラズマの定義

  - gas of charged particles 

  - 正電荷と負電荷が同数

  - 定常状態で準中性の振る舞い **準中性とは？**

    - >On average a plasma looks electrically neutral to the outside, since the
      >randomly distributed particle electric charge fields mutually cancel.

- 自由粒子の一般論

  - 以下の条件のもとで、粒子は自由粒子とみなせる
    - (potential energy) << (thermal energy)
    - 衝突なし

- プラズマ粒子の場合

  - 周囲の粒子(異なる電荷の粒子)とくっつかないために数eVの熱エネルギーを持つはず **eVとは？**
    - http://physics.thick.jp/Plasma_Physics/Section1/1-3.html
  - 典型的なプラズマはhotで電離している

- 存在の知られている物質の99%以上がプラズマ状態

### Debye Shielding

- 温度や密度の変化が急峻な場所ではそれだけ小さいスケールの単位体積を考える必要がある？
- 密度や温度の変化のスケールよりも大きな単位体積を考えていたら？

>For the plasma to behave quasineutral in the stationary state, it is necessary to have about
>
>equal numbers of positive and negative charges per volume element. 
>
>定常状態で準中性的に振舞うためには、単位体積あたりに同量の正電荷と負電荷が必要
>
>
>
>Such a volume element must be large enough to contain a sufficient number of particles, yet small enough
>
>compared with the characteristic lengths for variations of macroscopic parameters such
>as density and temperature. 
>
>そのような単位体積は、十分な粒子を含める程度には大きい必要があるが、特徴的な長さよりは小さい必要がある。(特徴的な = マクロ量が変化する長さ）
>
>
>
>In each volume element the microscopic space charge fields of the individual charge carriers must cancel each other to provide macroscopic charge neutrality.
>
>それぞれの単位体積において、個々の電荷は互いにキャンセルしあっているはず。

クーロン力

$$
\phi_c = \frac{q}{4\pi\epsilon_0r}
$$

デバイ遮蔽
$$
\phi_D = \frac{q}{4\pi\epsilon_0r}\exp(-\frac{r}{\lambda_D})
$$

> 考え方
>
> 1. まずイオンと電子が互いに運動しているプラズマを考える。準中性状態
> 2. 電場がかかる(どこかに大きな電荷が発生すると)
> 3. 電子の方が軽いので、中性にする方向に移動しやすい
> 4. しかし完全には打ち消し合わない(熱運動もあるため)





デバイ長：熱エネルギーと静電エネルギーのバランスで決まる

熱エネルギー：電気的中性状態を乱す

静電エネルギー：電気的中性状態に戻そうとする
$$
\lambda_D = \left(\cfrac{\epsilon_0k_BT_e}{n_ee^2}\right)^{1/2}
$$

- 電子温度とイオン温度を等しいと仮定
- 温度と平均エネルギーを同じ意味として扱う

>**First plasma criterion**
>$$
>\lambda_D << L
>$$

- デバイ長以下の系だと、中性がやぶれている



###  Plasma Parameter

debye sphere : 半径がデバイ長の球

- 内部には十分な粒子が必要(**なぜ**？)

>**Second plasma criterion**
>$$
>\Lambda = n_e\lambda_D^3 >> 1
>$$



この式の意味は：(熱エネルギー) >>  (ポテンシャルエネルギー)



ここまでのまとめ

- プラズマは準中性状態 - > デバイ長以上のスケールで考える(1st criterion)
- 十分な粒子が含まれている ⇔ (周囲の粒子からのポテンシャルエネルギー) << (熱エネルギー) (2nd criterion)



### Plasma Frequency

完全電離したプラズマ周波数

- 準中性状態のプラズマに外力が加わると、動きやすい電子は電気的中性に戻す方向に振動

  

>**Plasma frequency**
>$$
>\omega_{pe} =\left( \frac{n_ee^2}{m_e\epsilon_{0}}\right)^{1/2}
>$$



- 電離圏プラズマは完全には電離しておらず、中性粒子とプラズマが多く衝突する場合、中性粒子と電子が平衡状態(熱的？)になり、中性ガスとして振る舞う

- 電子が中性粒子との衝突の影響を受けないためには、平均の衝突するまでの時間とプラズマ周波数の積が1以上

>**Third plasma criterion**
>$$
>\omega_{pe}\tau_n >> 1
>$$



# 1.2. Geophysical Plasmas

- 電離圏以上の領域ではプラズマ物理の手法が適用できる

### Solar Wind

- 500km/s
- electrons, protons, and 5% Helium ions
- ne ~ 5 /cc, Te ~ 10^5 K (near the Earth)
- (1eV = 11,600 K)
- 5 nT

地球の地場に衝突すると減速し、周辺に反射

運動エネルギーが熱エネルギーに変換

### Magnetosphere

- 惑星間磁場が領域に入り込めず、プラズマも磁力線に凍結していて離れられないため
- magnetopause(磁気圏界面)
- 後方へは月の軌道くらいまでtailがのびている
- 太陽風と電離圏起源のプラズマがmain
- He+, O+：電離圏起源、He++：太陽風起源

[fig. 1.4]magnetosphere内での分類

radiation belt：高エネルギー粒子が行ったり来たり

- ne ~ 1 /cc , Te ~ 5x10^7 K
- 100 ~ 1000 nT

tailのプラズマの大部分はプラズマシート内に分布

- ne ~ 0.5 /cc, Te ~ 5 x 10^6 K , B ~ 10 nT

magnetotail lobe : magnetotailの外側

- 希薄なプラズマ
- ne ~ 10^02 /cc, Te ~ 5 x 10^5 K, B ~ 30 nT

## Ionosphere

太陽紫外線が中性大気を一部電離させる

- 80kmより上では、衝突が高頻度で発生し、急速な組み換えと永続的な電離が起こる
- ne ~ 10^5 /cc, Te ~ 10^3 K, B ~ 10^4 nT
- plasmasphereと徐々に結合していく。
  - coolだが密度の濃いプラズマが存在、自転と一緒に回転
- プラズマシートの電子が磁場に沿って電離圏に侵入し、中性大気を電離させ、オーロラを引き起こす



# 1.3 Magnetospheric Currents

- 電子とイオンが別々に運動し、電流が末世する

  - 電荷、質量、運動量、エネルギーを運ぶ、磁場を形成

- 昼側の地磁気はmagnetopause currentに沿って圧縮

- 夜側はtail current flowingとneutral sheet currentに沿って広がる

  - Θ-like：上記２つの電流が成している

- ring current

  - 西向き
  - radiation belt粒子が発生させている
  - プロトンは西向きに、電子は東向きに動くことで、実質的な電荷の移動がおこっている

- 電離圏の電流システム

  - auroral electrojets
  - Sq currents
  - equatorial electrojet

- Field-aligned currents

  - 磁気圏電流と接続し、磁気圏から電離圏の極域の範囲で存在している
  - 電子から構成されており、これらの領域の間でエネルギーや運動量の交換をになっている

  

  # 1.4 Theoretical Approaches

  プラズマの運動は電場と磁場の間での電荷の移動の相互作用に支配される

  - 電場、磁場が外から与えられるならシンプルなのだが、粒子のうんどうによって
    - 局所的な電荷の偏り
    - 運動による電流とそれにより発生する磁場
  - によって複雑になっている

- 完全に解くことよりも、マクロな量を求めることに関心がある

- sngle particle motion：集団的な運動は解けないが、密度の低いリングカレントなどでのプラズマの研究に用いられる

- MHD：単一の導電性の流体とする。局所的な平衡状態を仮定

- multi-fluid ：粒子種によって異なる運動を溶ける

  - 分極電場、高周波の波動を見れる

- 運動論的な取り扱い：統計的手法。位相空間における分布関数を見る



# 2.3. Elctric Drifts

外部電場による、gyro運動のドリフトの効果

主に

- 静電場
- 時間に依存する電場
- 空間に非一様な電場

## E x B Drift

地球物理学では、多くの並行な電場は電子によって打ち消し合い、維持できない。
$$
m \frac{d\bold{v}}{dt} = q(\bold{E}+\bold{v}\times{\bold{B}})　(2.7)
$$

$$
v'_y = v_y + E_x/B
$$

が大事

E = Ex,  B = Bz

なら、E x B = - Ex x Bz  で、y成分に-EBが入る。



Fig.2.3. 

ジャイロ半径が上むきに 運動するときは大きくなり、下向きに移動する時は小さくなると、結果的に右に進んでしまう様子



# Polarization Drift 分極ドリフト

ベクトル三重積
$$
\bold{a} \times (\bold{b} \times \bold{c}) = (\bold{a} \cdot \bold{c})\bold{b}-(\bold{a}\cdot \bold{b})\bold{c} \\
(\bold{a} \times \bold{b}) \times \bold{c} = (\bold{a} \cdot \bold{c})\bold{b}-(\bold{b}\cdot \bold{c})\bold{a}
$$
式(2.7)
$$
\frac{m}{q} \frac{d\bold{v}}{dt} = \bold{E}+(\bold{v}\times{\bold{B}}) \\

\frac{m}{q} \frac{d\bold{v}}{dt} \times \frac{\bold{B}}{B^2} = \frac{\bold{E}\times{\bold{B}}}{B^2} + (\bold{v}\times\bold{B})\times\frac{\bold{B}}{B^2}
\\
$$


ここで三重積より
$$
(\bold{v}\times\bold{B})\times\frac{\bold{B}}{B^2} = (\bold{v}\cdot\frac{\bold{B}}{B^2})\bold{B}-(\bold{B}\cdot\frac{\bold{B}}{B^2})\bold{v}
\\
= \frac{\bold{B}(\bold{v}\cdot\bold{B})}{B^2} - \bold{v}
$$
よって(11)を整理すると
$$
\bold{v} -\frac{\bold{B}(\bold{v}\cdot\bold{B})}{B^2} = \frac{\bold{E}\times{\bold{B}}}{B^2} -\frac{q}{m} \frac{d\bold{v}}{dt}\times\frac{\bold{B}}{B^2}
\\
$$


ジャイロ周期で平均化すると、垂直方向の運動をドリフト運動とみなせる

磁場が時間に依存しないとすると、 微分のなかに入れてしまい、
$$
\bold{v_d} = \bold{v_E}-\frac{m}{qB^2}\frac{d}{dt}(\bold{v}\times\bold{B})
$$
(2.21)の電場を使う
$$
\bold{v_d}=\bold{v_E}+\frac{1}{\omega_gB}\frac{d\bold{E_{\perp}}}{dt}
$$
ここで
$$
\omega_g = \frac{qB}{m}
$$
分極ドリフト
$$
\bold{v_p} = \frac{1}{\omega_gB}\frac{d\bold{E_{\perp}}}{dt}
$$
E x Bドリフト：電荷にも、質量にもよらない。どんなプラズマもB とEに垂直な同じ方向に運動する

分極ドリフト：質量に比例する。電場に沿った向きに運動。電子とイオンで反対むき



したがって、分極ドリフトは
$$
\bold{j}_p = n_ee(\bold{v}_pi-\bold{v}_pe)=\frac{n_e(m_i+m_e)}{B^2}\frac{dE_{\perp}}{dt}
$$
のような電流を発生させる

mi >> me　なので、分極電流は主にイオンを運ぶ



## Electric Drift Corrections

(2.24) は以下のような補正によって非一様な電場におけるドリフトも表せる。

微分の項を時間微分と対流微分の和とする。
$$
d/dt = \partial / \partial t + \bold{v}\cdot\nabla
$$
ここで、v = E x Bと近似すると対流微分の項はE^2 に比例するが、このような非線形の寄与は大抵の場合時間変化に比べて小さいため無視できる。



ジャイロ運動一周期の中で電場が大きく変動するような場合に、ドリフト運動に補正がかかる

有限ラーモア半径効果

非一様な電場の下でのドリフト速度は以下のようになる
$$
\bold{v}_E = (1 + \frac{1}{4}r_g^2\nabla^2)\frac{\bold{E}\times\bold{B}}{B^2}
$$
マクロな視点では無視されるが、境界における状態や、プラズマ遷移、微小スケールの現象などでは重要になってくる。



http://physics.thick.jp/Plasma_Physics/Section2/2-9.html

#### 

# 2.4. Magnetic Drifts

大抵の磁場は強度に勾配があり、向きも曲がっている

磁場の時間変化それ自体は、ローレンツ力が粒子の運動方向に常に垂直なので、加減速に寄与しないが、ファラデーの電磁誘導の法則
$$
\frac{\partial \bold{B}}{\partial t} = -\nabla \times \bold{E}
$$


から、電場が粒子にエネルギーを与えてドリフトを起こす



## General Force Drift

(2.1)のクーロン力の式
$$
\bold{F}_c = q \bold{E}
$$
(2.19)のE x B driftの式
$$
\bold{v}_E = \frac{\bold{E}\times \bold{B}}{B^2}
$$
より一般的な外力によるドリフトの表式が得られる。
$$
\bold{v}_F = \frac{1}{\omega_g}(\frac{\bold{F}}{m}\times \frac{\bold{B}}{B})
$$
ここで
$$
\omega_g = \frac{qB}{m}
$$
すべての粒子のドリフトは、その速さがジャイロ運動の速度よりも十分小さい限り、適切な外力の項を導入することでいつでも表現することができる

例

grad B ドリフト
$$
\bold{F}_{\nabla} = - \mu \nabla\bold{B}
$$
分極ドリフト
$$
\bold{F}_P = -m \frac{d\bold{E}}{dt}
$$
重力ドリフト
$$
\bold{F}_G = -mg
$$
重力は普通他の外力よりも非常に小さく、太陽の表面以外では大抵の場合無視される。

(24)の表式から、クーロン力以外の外力によって生じるドリフトはすべて$\omega_g$に起因する電荷に依存するため、電子とイオンでドリフトの方向が真逆である。したがって、それらのドリフトによって、外力を横切るような電流が発生する。

さらに、これらのドリフトは電荷の質量にも依存するのでドリフト速度はイオンと電子で大きく異なる。



## 

# Adiabatic Invariants　断熱不変量

磁気モーメント
$$
\mu = W_{\perp}/B
$$
断熱不変量の一種

粒子運動の周期の典型的なタイムスケールと比べて、断熱不変量の変化がゆっくりな場合を考える



３種類の断熱不変量

- 磁気モーメント
- longitudinalinvariant
- Drift Invariant



一般的に
$$
J_{i} = \oint p_i d_i
$$
が断熱不変量となる

$p_i$はハミルトン力学系における一般化座標と一般化運動量



## Magnetic Moment

