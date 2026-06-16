# 背景
植物の葉は、受ける光の波長帯によって、異なる分光特性を示す。特に、400–700 nmの光合成有効放射であるPAR（Photosynthetically Active Radiation：光合成有効放射）は、クロロフィルなどの光合成色素によってよく吸収されます。一方で、700–1000 nmの近赤外域であるNIR（Near-Infrared Radiation：近赤外放射）は、光合成にはほとんど利用されず、葉内細胞において主に反射または透過されます。そのため、生の葉はPARを吸収し、NIRは通す光学的なフィルターとしても捉えられます。

このような葉レベルの分光特性は、個葉が集まった葉群を透過する光環境を考える上でも重要です。林冠内の葉群量が大きくなるほど、林冠を通過するPARは葉によって強く減衰します。一方で、NIRは反射や透過を繰り返しながら林冠内を拡散します。その結果、林冠下に到達する透過光では、PARに対するNIRの割合が相対的に高くなります。すなわち、林冠下のNIR/PAR比は、葉群量の増減を反映する指標として利用できるというわけです。

Kume et al. （2011）（DOI 10.1007/s10265-010-0346-1）はこの葉の分光特性に着目し、林冠下で測定される透過NIRと透過PARの比から、林冠によるPAR吸収割合および単一表面あたりの片側葉面積であるLAI（Leaf Area Index）を推定できることを示しました。Kume et al.（2011）は、携帯型の分光式葉面積指数計測計（MIJ-LAI, 日本環境計測, 日本）を用いて、冷温帯落葉広葉樹林において林冠上および林冠下のPAR・NIRを連続観測し、実測されたLAIとの対応関係を解析しました。その結果、林冠下まで透過するNIR/PAR比とLAIの間には強い対数関係が認められ、LAI = 2.80 ln(NIRt/PARt) + 0.69 という経験式が提示されました。

私も、Kume et al.（2011）によって提案されたPAR/NIR比に基づくLAI推定式を用いて、長野県のカヤの平成熟林（ブナが優占）や長野県のおたの申す平成熟林（コメツガなどが優占）における葉群分布を階層別に定量化しました。具体的には、環境省モニタリングサイト1000に登録されている1haの固定調査区を10m格子点上に区切ったの121地点において、地上0 m、2.5 m、5 mの3高度でLAIを推定し、それぞれの差分から樹冠層、中低木層、ササ層の葉群量を推定しました。この研究内容の一部は奥山学会誌にて報告しています（植田時, 廣田充. 樹冠ギャップが成熟林の葉群分布と炭素固定量に与える影響, 日本奥山学会誌, 第12巻, 第1号, 54-67, 2025.）。

しかし、その報告の中でも指摘している通り、私の方法には問題があります。それは、Kume et al.（2011）によって提案されたLAIの推定式を、優占樹種の異なる森林、ひいてはササのLAIの推定にまで当てはめてしまっている点です。

葉のPARおよびNIRに対する反射率・透過率は、樹種、葉厚、クロロフィル量（もっと言えば垂直な葉が多いのか水平な葉が多いのかを示す葉角分布も）などによって異なることが多くの先行研究で示されています（e.g. Hovi et al. 2017）。そのため、Kume式の係数をそのまま適用した場合、樹冠層、中低木層、ササ層それぞれのLAIが過大または過小に推定される可能性があります。したがって、PAR/NIR比を用いたLAI推定の精度を高めるためには、サイトごと、さらには主要な構成種や階層ごとに、葉の分光特性を考慮して推定式の係数を補正する必要があると考えました。



## 生の葉を用いた補正
まず初めに、生の葉っぱを用いた補正方法を考案した。方法は以下の通りです。

---
1.	ある個体を対象に、成熟した葉から直径4cmの円形葉切片を切り抜く（図1）。
<img width="314" height="340" alt="image" src="https://github.com/user-attachments/assets/3e6d51f6-cd2a-47f3-8941-dcb3afce03d5" />

図1. 切り出した円形葉切片

2.	計測は開けた明るい場所で実施する。
3.	円形葉切片をPAR光センサーの上に乗せ、PARの光エネルギー量 (μmol s^−1m^−2)を計測する（図2）。この時同時に、円形葉切片を上に乗せないコントロールのPARも計測する（LAI計2台を同時並行で継続ログする）。

<img width="338" height="342" alt="image" src="https://github.com/user-attachments/assets/3a03cba0-4c87-4db3-8e92-4d43f41fe9cc" />

図2. 円形葉切片を光センサーに乗せた様子


5.	PARセンサー上の円形葉切片の数を、1枚ずつ増やしていく。

6.	3.と4.の行程をNIRセンサーでも同様に行う。
---

円形葉切片は、光センサーを全て覆っているため、円形葉切片の枚数はそのままLAIとして換算できます。また、円形葉切片を乗せていないコントロールの値から、光センサーに当たるPARとNIRの光エネルギー、および円形葉切片を透過したPARとNIRの光エネルギーの値を得ることができます。
実際にXXを対象として実施してみると、以下のような結果が得られました。

XXX

また、1種だけでなく、2種あるいは3種の葉を対象にして計測を行ってみました。ここで、葉の上下方向の順番も、PAR/NIR吸光割合になんらかの影響を与えているかもしれないと考え、並べ方を全通り試しました。すると、以下のような結果が得られました。

XXX

これらの結果から、種ごとあるいは種の組み合わせごとの係数が得らます。

しかし、こういったLAI推定式の補正方法は果たして妥当なのでしょうか。実際の森林を想定すると、問題が色々とありそうです。以下にその可能性を挙げてみます。

①　実際の森林が持つ複雑さとの乖離
例えば、数種ごとに単純化して補正した推定式の係数を実際の計測に際してどのように用いるべきでしょうか。MIJ-LAIは180度の視野角を持っています。先行研究によって、LAIの推定値の空間的自己相関が、18.25mでほぼ無視できることが示されています（Tanioka et al. 2022）。このことから、MIJ-LAIはおよそ半径10mの範囲の光を拾ってきているのだと推測できます。実際の森林における半径10mの範囲内に存在する葉群を想像すると、その葉群を構成する種は極めて複雑であると思われます。その複雑性をこのような補正方法でカバーできるとは思えません。

加えて、例えば林床で計測したPAR/NIRからLAIを推定する場合を考えます。ここで、MIJ-LAI上にある葉群は、単純化すると「林冠木」と「ササ」の２種類です。おそらく、林冠木の葉群量は地点ごとに異なると思われます。林冠木が存在する場合と存在しない場合とで、係数を分けるか。林冠木の葉群量によって、林床で計測した場合の係数を柔軟に（地点ごとに）調整するか。悩ましい点です。

②葉角を考慮していない
かの有名なMonsi & Saeki（1953）やSaeki（1960）が指摘したように、群落を通る光の透過しやすさの指標である透過係数Kは、葉の角度によって決定されます。水平な葉が多いほど、林床に届く光量子の数が少なくなりやすいという理論です。XXXXX。

そこで、PC上で仮想の葉群モデルを作成し、FLiES（Forest Light Environmental Simulator）と呼ばれる3次元放射伝達シミュレーションモデルを用いて、PAR/NIRの吸光割合を計算することで、Kume式LAI推定（Kume et al. 2011）において提示されている汎用式の係数を補正することができないかと考えました（アドバイスをくださった東大の仮屋園さんありがとうございます！）。



## 仮想葉群モデルを用いた補正

### FLiESとは
森林内で光がどのように入射・散乱・吸収・透過するかを計算するための3次元放射伝達シミュレーションモデルです。このモデルでは、太陽から入射した放射が、葉、枝・幹などの木部構造、地表面との相互作用を経た結果、吸収・散乱・反射・透過される過程を計算します。森林内の光環境は、林冠構造、葉面積密度（Leaf Area Density; LAD）、葉角分布、葉が持つPARおよびNIRの反射率・透過率、地表面反射率、太陽高度などによって大きく変化します。そのためFLiESでは、これらの条件を入力値として与え、森林内外における放射の分布を数値的に推定します。

・FLiES 公式HP：https://flies.sakura.ne.jp/WP/JA/radiative-transfer-code/

・FLiES 原著論文 (Kobayashi & Iwabuchi, 2008): https://doi.org/10.1016/j.rse.2007.04.010

・LiDAR データを用いた放射伝達計算 (Béland & Kobayashi, 2024): https://doi.org/10.1016/j.rse.2023.113951


### 仮想の葉群について
FLiESの光シミュレーションでは本来、LiDARから得られるボクセルごとのLAD（Leaf Area Density）データなどからleafvoxのボクセルデータの値を計算します。
ですがここでは、枝などの木部構造のない、仮想の葉群として設定します（とりあえず）。

設定としては以下の5通りです。
1. 林冠木のみ（1種）
2. 林冠木のみ（2種）
3. ササのみ
4. 林冠木（1種）とササ
5. 林冠木（2種）とササ

FLiESのディレクトリ構成やコンパイルなどは仮屋園さんが以下のレポジトリでわかりやすくまとめてくださっているのでここでは省略します。



### 1. 実行の流れ

```bash
1. 仮想葉群の構造を決める
   ↓
2. leafvox.txt を作成する
   ↓
3. PAR 用の設定ファイルを作成する
   ↓
4. NIR 用の設定ファイルを作成する
   ↓
5. FLiESvox を実行する
   ↓
6. 出力から PAR/NIR の透過割合を取り出す
   ↓
7. LAI と ln(NIR/PAR) の関係を解析する
```

FLiESvox では、葉群の3次元構造を leafvox.txt に入力します。
leafvox.txt には、各ボクセルの位置、葉面積密度、葉の光学特性などを記述します。

このシミュレーションで見たいのは、3のln(NIR/PAR)とLAIの関係です。FLiESでは、LAIを設定することができないため、このシミュレーションでは、葉群の厚さを2.5mに統一し、LAI=LAD÷2mという式でLAIを算出することにします。葉群の厚さを2.5mに設定したのは、私が行っている上述のLAIの階層分けが、2.5mごとに分けられていることに由来します。これは、林冠木の樹冠長（樹冠のtopからbottomの高さ）としても大きなズレはないと考えています（針葉樹だともっと長いかも）。



### 2. leafvox.txtの意味

leafvox.txt は、スペース区切りのテキストファイルです。
ヘッダー行は付けず、以下の順番で値を入力します。

```bash
xmin ymin zmin xmax ymax zmax LAD iANG WAD leaf.refl leaf.trans woody.refl CI
```
| 列名           | 意味                 | 説明                           |
| ------------ | ------------------ | ---------------------------- |
| `xmin`       | x方向の最小座標           | ボクセルの左端の位置                   |
| `ymin`       | y方向の最小座標           | ボクセルの手前側の位置                  |
| `zmin`       | z方向の最小座標           | ボクセルの下端の高さ                   |
| `xmax`       | x方向の最大座標           | ボクセルの右端の位置                   |
| `ymax`       | y方向の最大座標           | ボクセルの奥側の位置                   |
| `zmax`       | z方向の最大座標           | ボクセルの上端の高さ                   |
| `LAD`        | Leaf Area Density  | 葉面積密度。1 m³ あたりの葉面積。単位は m²/m³ |
| `iANG`       | 葉角度分布タイプ           | 葉の傾き方を指定する番号                 |
| `WAD`        | Woody Area Density | 枝・幹など木部の面積密度                 |
| `leaf.refl`  | 葉の反射率              | 葉に当たった光のうち、反射される割合           |
| `leaf.trans` | 葉の透過率              | 葉に当たった光のうち、葉を透過する割合          |
| `woody.refl` | 木部の反射率             | 枝・幹などに当たった光の反射率              |
| `CI`         | Clumping Index     | 葉の集中度を表す係数                   |

例えば、

```bash
0 0 27.5 1 1 30.0
```

という座標情報は、x = 0–1 m、y = 0–1 m、z = 27.5–30.0 m の範囲にあるボクセルを意味します。

iANGは、葉の角度分布を指定するための番号です。
最初の単純な仮想葉群モデルでは、iANG = 1 で固定して計算を始めてみることにします。

WADは枝や幹などの木部の面積密度を表します。
本研究で最初に作成する仮想葉群では、枝や幹を含まない「葉だけ」のモデルを作るため、WAD = 0.0 とします。

leaf.reflは葉の反射率を表します。
これは、葉に当たった光のうち、葉で反射される割合です。

leaf.transは葉の透過率を表します。
これは、葉に当たった光のうち、葉を通り抜ける割合です。

leaf.reflとleaf.transは、PARとNIRで異なる値を設定する必要があります。
そのため、同じ葉群構造であっても、PARを計算する場合とNIRを計算する場合では、leafvox.txt内の光学特性を変える必要があります。

つまり、想定する種ごとに、PARとNIRの反射率および透過率のデータが必ず必要というわけです。ですが、葉の分光特性のデータを得るのは簡単ではありません。そこで本シミュレーションでは、データベース（EcoSIS; https://ecosis.org）および先行研究で報告されているデータを利用することとしました。


woody.reflは、枝や幹などの木部の反射率を表します。
ただし、葉だけの仮想葉群モデルでは木部を入れないため、WADと同様woody.refl = 0.0 とします。

CIは葉の集中度を表す係数です。
葉がランダムに分布している場合は、基本的に CI = 1.0 とします。
CI < 1.0 にすると、葉が空間的にまとまって分布している状態を表すことができます。また、葉が集中して分布している場合、同じ LAI であっても光が抜けやすくなる可能性があるのでこの値もLAIの推定には大事ですが、とりあえず1としておきます（あとで感度分析的にLAIとの関係性を見てみます）。



### 3. まずは葉のみのモデルを作ってみる
最初は、枝や幹を含まない「葉だけ」のモデルを作ってみます。
そのため、以下のように設定します。

```bash
WAD = 0.0
woody.refl = 0.0
CI = 1.0
iANG = 1
```

それぞれの意味は以下の通りです。
| 項目           |   値 | 意味              |
| ------------ | --: | --------------- |
| `WAD`        | 0.0 | 木部を入れない         |
| `woody.refl` | 0.0 | 木部がないので反射率も0にする |
| `CI`         | 1.0 | 葉の集中・クランピング補正なし |
| `iANG`       |   1 | 最初は固定して計算する     |



### 4. 林冠木のみ（1種）でモデルを作る


4.1. モデル設定
ここでは、以下のような単純なモデルを作ってみます。

```bash
種：ブナ（長野県カヤの平における林冠優占種）
水平サイズ：20 m × 20 m
高さ方向：35 m
ボクセルサイズ：1m × 1m × 2.5 m
ブナ葉層：z = 27.5–30.0 m
葉群の厚さ：2.5 m
木部：なし
```

つまり、高さ 27.5–30 m の位置に、厚さ 2.5 m のブナ葉層を作ります。
1m × 1m × 2.5 mのボクセルが、20 m × 20 m = 400個分並んでいます。


4.2. leafvox.txt の例

例えば、ブナ葉層の LAI を 1.0 にしたい場合、葉群の厚さは 2.5 m なので、

```bash
LAD = 1.0 / 2.5
LAD = 0.4
```

として設定します。

1つのボクセルは次のように書きます。

```bash
0 0 27.5 1 1 30.0 0.4 1 0.0 0.08 0.05 0.0 1.0
```

ただし、これは x = 0–1、y = 0–1 の1つのボクセルだけです。
実際には、20 m × 20 m の領域全体に葉を置きたいので、x と y のすべてのボクセルについて同じような行を作成します。


4.3. ブナ葉のみの leafvox.txt を自動生成する

手作業で 20 × 20 = 400 行を書くのは大変なので、Python で leafvox.txt を作成します。
以下のコードを make_leafvox_beech_only.py として保存します。

```bash
# ブナ葉のみの仮想葉群を作成するスクリプト

# 1. 基本設定
# 水平方向のボクセル数
nx = 20
ny = 20

# ブナ葉層を置く高さ
# ここでは z = 27.5–30.0 m に 2.5 m 厚の葉群を置く
zmin = 27.5
zmax = 30.0

# 目標 LAI
target_lai = 1.0

# 葉群の厚さ
layer_thickness = zmax - zmin

# LAD を計算
# LAI = LAD × 葉群の厚さ なので、
# LAD = LAI / 葉群の厚さ
LAD = target_lai / layer_thickness

# 2. 光学特性の設定
# ここでは例として PAR 用の値を入れています。
# NIR を計算する場合は、leaf_refl と leaf_trans を NIR 用の値に変更する。

leaf_refl = 0.08
leaf_trans = 0.05

# 木部は入れない
WAD = 0.0
woody_refl = 0.0

# 葉角度分布
iANG = 1

# クランピング補正なし
CI = 1.0

# 出力ファイル名
output_file = "leafvox_beech_LAI1_PAR.txt"



# 3. leafvox.txt を作成

with open(output_file, "w") as f:
    for x in range(nx):
        for y in range(ny):
            line = (
                f"{x} {y} {zmin} "
                f"{x+1} {y+1} {zmax} "
                f"{LAD} {iANG} {WAD} "
                f"{leaf_refl} {leaf_trans} {woody_refl} {CI}\n"
            )
            f.write(line)

print(f"Created: {output_file}")
print(f"Target LAI = {target_lai}")
print(f"Layer thickness = {layer_thickness} m")
print(f"LAD = {LAD}")
```

```bash
python make_leafvox_beech_only.py
```

実行すると、以下のファイルが作成されます。

```bash
leafvox_beech_LAI1_PAR.txt
```

このファイルが、ブナ葉のみ・LAI = 1.0かつPAR用の leafvox.txt です。


4.3. PAR用とNIR用で分ける

同じ葉群構造でも、PARとNIRでは葉の反射率・透過率が異なります。
そのため、PAR用とNIR用で別々の leafvox.txt を作ります。

PAR用では、PAR帯の葉の反射率と透過率を入力します。

```bash
leaf_refl = 0.08
leaf_trans = 0.05
output_file = "leafvox_beech_LAI1_PAR.txt"
```

NIR 用では、NIR 帯の葉の反射率と透過率を入力します。

```bash
leaf_refl = 0.45
leaf_trans = 0.40
output_file = "leafvox_beech_LAI2_NIR.txt"
```

重要なのは、葉群構造は同じで、光学特性だけを PAR用・NIR用に変えることです。


4.4. config.yml を作成する

次に、FLiESvoxを実行するための設定ファイルを作ります。
ここでは、PAR 用の設定ファイルを config_beech_LAI1_PAR.yml とします。

```bash
path:
  version: "Version_1.5.5_flux"
  leafvox: "experiment/lai_test/input/leafvox_beech_LAI2_PAR.txt"
  output_dir: "experiment/lai_test/output/beech_LAI2_PAR"

landscape:
  size: 20
  sizeh: 35
  xmax: 20

vegetation:
  shoot: 1.0

optics:
  soil_ref: 0.05

solar:
  sza: 0
  saa: 0
  dif: 0.0

view:
  vza: 0
  raa: 0

simulation:
  np_photons: 100000
  cmode: 3
  amode: 2
  stype: 2
  elev: 0.0
  nts: 1
```
各項目の意味は以下の通りです。

| 項目           | 意味                     |
| ------------ | ---------------------- |
| `version`    | 使用する FLiESvox のバージョン   |
| `leafvox`    | 入力する `leafvox.txt` のパス |
| `output_dir` | 計算結果の出力先               |
| `size`       | 水平方向のボクセル数             |
| `sizeh`      | 高さ方向のボクセル数             |
| `xmax`       | x方向の実空間サイズ             |
| `shoot`      | シュートクランピング係数           |
| `soil_ref`   | 地表面・リターの反射率            |
| `sza`        | 太陽天頂角                  |
| `saa`        | 太陽方位角                  |
| `dif`        | 散乱光割合                  |
| `vza`        | 観測天頂角                  |
| `raa`        | 観測方位角                  |
| `np_photons` | 計算に使うフォトン数             |
| `cmode`      | 計算モード。3 は 3D 解析        |
| `amode`      | 大気モード                  |
| `stype`      | 地表タイプ                  |
| `elev`       | 地表標高                   |
| `nts`        | 樹種数                    |


テスト計算では np_photons = 100000 程度で良いと思います。
（本計算では、計算を安定させるために10000000程度まで増やす？）

NIR 用の計算では、leafvoxとoutput_dirをNIR用に変更する必要があります。
（soil_refも NIR帯に対応した値に変更する？）




#### 4.5. FLiESvox を実行する

以下を実行します。

```bash
python py-flies/pipeline/FLiESvox_Run_APAR.py experiment/lai_test/config/config_beech_LAI2_PAR.yml
```

計算が成功すると、output_dir に指定した場所に結果が出力されます。

例：
```bash
experiment/lai_test/output/beech_LAI2_PAR/
```

同様に、NIR 用の設定ファイルを作成し、実行します。

```bash
python py-flies/pipeline/FLiESvox_Run_APAR.py experiment/lai_test/config/config_beech_LAI2_NIR.yml
```


4.6. LAIを変えて実行する

```bash
LAI = 0.5, 1.0, 2.0, 3.0, 4.0, 5.0
```

本解析では葉群の厚さを 2.5 mに固定するため、各LAIに対応するLADは以下のように計算できます。

| LAI | LAD |
| --: | --: |
| 0.5 | 0.2 |
| 1.0 | 0.4 |
| 2.0 | 0.8 |
| 3.0 | 1.2 |
| 4.0 | 1.6 |
| 5.0 | 2.0 |

それぞれの LAI について、

```bash
PAR 用 leafvox.txt
NIR 用 leafvox.txt
PAR 用 config.yml
NIR 用 config.yml
```

を作成し、FLiESvox を実行します。
が、
LAI ごとに手作業でleafvox.txtを作成するのは大変なので、Pythonで一括生成します。

以下のコードでは、LAI = 0.5 から 5.0 までの PAR 用 leafvox.txt をまとめて作成します。


```bash
# ブナ葉のみの leafvox.txt を LAI ごとに一括作成するスクリプト
# PAR 用

# 水平方向のボクセル数
nx = 20
ny = 20

# ブナ葉層を置く高さ
zmin = 27.5
zmax = 30.0

# 葉群の厚さ
layer_thickness = zmax - zmin

# 計算する LAI のリスト
lai_values = [0.5, 1.0, 1.5, 2.0, 2.5, 3.0, 3.5, 4.0, 4.5, 5.0]

# PAR 用の葉の光学特性
leaf_refl = 0.08
leaf_trans = 0.05

# 木部なし
WAD = 0.0
woody_refl = 0.0

# 葉角度分布
iANG = 1

# クランピング補正なし
CI = 1.0

for target_lai in lai_values:

    # LAI から LAD を計算
    LAD = target_lai / layer_thickness

    # ファイル名に LAI の値を入れる
    output_file = f"leafvox_beech_LAI{target_lai}_PAR.txt"

    with open(output_file, "w") as f:
        for x in range(nx):
            for y in range(ny):
                line = (
                    f"{x} {y} {zmin} "
                    f"{x+1} {y+1} {zmax} "
                    f"{LAD} {iANG} {WAD} "
                    f"{leaf_refl} {leaf_trans} {woody_refl} {CI}\n"
                )
                f.write(line)

    print(f"Created: {output_file}")
    print(f"  Target LAI = {target_lai}")
    print(f"  LAD = {LAD}")
```

このコードを例えば以下の名前で保存します。

```bash
make_leafvox_beech_only_PAR_allLAI.py
```

実行します。

```bash
python make_leafvox_beech_only_PAR_allLAI.py
```

実行すると、以下のように LAI ごとの PAR 用 leafvox.txt が作成されます。

```bash
leafvox_beech_LAI0.5_PAR.txt
leafvox_beech_LAI1.0_PAR.txt
leafvox_beech_LAI1.5_PAR.txt
leafvox_beech_LAI2.0_PAR.txt
...
leafvox_beech_LAI5.0_PAR.txt
```


4.8. NIR 用の leafvox.txt も作成する

NIR 用も基本的な構造は PAR 用と同じです。
変更するのは、葉の反射率と透過率です。

PAR 用では、

```bash
leaf_refl = 0.08
leaf_trans = 0.05
```

としていましたが、NIR 用では、例えば以下のように設定します。

leaf_refl = 0.45
leaf_trans = 0.40

NIR 用の一括作成コードは以下のようになります。

```bash
# ブナ葉のみの leafvox.txt を LAI ごとに一括作成するスクリプト
# NIR 用

nx = 20
ny = 20

zmin = 27.5
zmax = 30.0
layer_thickness = zmax - zmin

lai_values = [0.5, 1.0, 1.5, 2.0, 2.5, 3.0, 3.5, 4.0, 4.5, 5.0]

# NIR 用の葉の光学特性
leaf_refl = 0.45
leaf_trans = 0.40

WAD = 0.0
woody_refl = 0.0

iANG = 1
CI = 1.0

for target_lai in lai_values:

    LAD = target_lai / layer_thickness

    output_file = f"leafvox_beech_LAI{target_lai}_NIR.txt"

    with open(output_file, "w") as f:
        for x in range(nx):
            for y in range(ny):
                line = (
                    f"{x} {y} {zmin} "
                    f"{x+1} {y+1} {zmax} "
                    f"{LAD} {iANG} {WAD} "
                    f"{leaf_refl} {leaf_trans} {woody_refl} {CI}\n"
                )
                f.write(line)

    print(f"Created: {output_file}")
    print(f"  Target LAI = {target_lai}")
    print(f"  LAD = {LAD}")
```

このコードを例えば以下の名前で保存します。

```bash
make_leafvox_beech_only_NIR_allLAI.py
```

実行します。

```bash
python make_leafvox_beech_only_NIR_allLAI.py
```

これにより、NIR 用の leafvox.txt も LAI ごとに作成されます。

```bash
leafvox_beech_LAI0.5_NIR.txt
leafvox_beech_LAI1.0_NIR.txt
leafvox_beech_LAI1.5_NIR.txt
leafvox_beech_LAI2.0_NIR.txt
...
leafvox_beech_LAI5.0_NIR.txt
```

4.9. config.yml も LAI ごとに作成する

FLiESvox を実行するには、各 leafvox.txt に対応する config.yml が必要です。
そのため、PAR 用と NIR 用について、LAI ごとの設定ファイルを作成します。

手作業で作ることもできますが、LAI が10段階あり、PAR と NIR の2種類があるため、合計20個の config.yml が必要になります。
そこで、これも Python で一括作成します。

以下のコードでは、PAR 用と NIR 用の config.yml をまとめて作成します。


```bash
# ブナ葉のみの config.yml を LAI ごとに一括作成するスクリプト

lai_values = [0.5, 1.0, 1.5, 2.0, 2.5, 3.0, 3.5, 4.0, 4.5, 5.0]

bands = ["PAR", "NIR"]

for band in bands:
    for target_lai in lai_values:

        leafvox_path = f"experiment/lai_test/input/leafvox_beech_LAI{target_lai}_{band}.txt"
        output_dir = f"experiment/lai_test/output/beech_LAI{target_lai}_{band}"

        # soil_ref は波長帯によって変更する
        if band == "PAR":
            soil_ref = 0.05
        else:
            soil_ref = 0.30

        config_text = f"""path:
  version: "Version_1.5.5_flux"
  leafvox: "{leafvox_path}"
  output_dir: "{output_dir}"

landscape:
  size: 20
  sizeh: 35
  xmax: 20

vegetation:
  shoot: 1.0

optics:
  soil_ref: {soil_ref}

solar:
  sza: 0
  saa: 0
  dif: 0.0

view:
  vza: 0
  raa: 0

simulation:
  np_photons: 100000
  cmode: 3
  amode: 2
  stype: 2
  elev: 0.0
  nts: 1
"""

        output_file = f"config_beech_LAI{target_lai}_{band}.yml"

        with open(output_file, "w") as f:
            f.write(config_text)

        print(f"Created: {output_file}")
```

このコードを例えば以下の名前で保存します。

```bash
make_config_beech_only_allLAI.py
```

実行します。

```bash
python make_config_beech_only_allLAI.py
```

実行すると、以下のように LAI ごとの設定ファイルが作成されます。

```bash
config_beech_LAI0.5_PAR.yml
config_beech_LAI0.5_NIR.yml
config_beech_LAI1.0_PAR.yml
config_beech_LAI1.0_NIR.yml
...
config_beech_LAI5.0_PAR.yml
config_beech_LAI5.0_NIR.yml
```

4.10. LAI ごとに FLiESvox を実行する

作成した config.yml を使って、LAI ごとに FLiESvox を実行します。

1つずつ実行する場合は、以下のようにします。

```bash
python py-flies/pipeline/FLiESvox_Run_APAR.py experiment/lai_test/config/config_beech_LAI0.5_PAR.yml
```
```bash
python py-flies/pipeline/FLiESvox_Run_APAR.py experiment/lai_test/config/config_beech_LAI0.5_NIR.yml
```

```bash
python py-flies/pipeline/FLiESvox_Run_APAR.py experiment/lai_test/config/config_beech_LAI1.0_PAR.yml
```

```bash
python py-flies/pipeline/FLiESvox_Run_APAR.py experiment/lai_test/config/config_beech_LAI1.0_NIR.yml
```

これを LAI = 0.5 から 5.0 まで繰り返します。

ただし、設定ファイルが多い場合は、batch_exe.py を使って一括実行する方が便利です。
batch_exe.py は指定したディレクトリ内の config.yml をまとめて実行するためのスクリプトです。

例えば、すべての設定ファイルを以下のディレクトリに入れておきます。

```bash
experiment/lai_test/config/beech_only/
```

そのうえで、batch_exe.py の中の設定ファイルディレクトリを以下のように変更します。

```bash
config_dir = "experiment/lai_test/config/beech_only"
```

その後、以下を実行します。

```bash
python py-flies/pipeline/batch_exe.py
```

これにより、ブナ葉のみの PAR/NIR 計算を LAI ごとにまとめて実行できます。


4.11. 出力結果を整理する

計算が成功すると、各条件の結果は output_dir に指定したフォルダに出力されます。

例えば、以下のようなフォルダが作成されます。

```bash
experiment/lai_test/output/beech_LAI0.5_PAR/
experiment/lai_test/output/beech_LAI0.5_NIR/
experiment/lai_test/output/beech_LAI1.0_PAR/
experiment/lai_test/output/beech_LAI1.0_NIR/
...
experiment/lai_test/output/beech_LAI5.0_PAR/
experiment/lai_test/output/beech_LAI5.0_NIR/
```

各出力フォルダには、FLiESvox の計算結果ファイルが保存されます。
この中から、PAR と NIR の透過割合を取り出します。

ここでは、PAR の透過割合を T_PAR、NIR の透過割合を T_NIR とします。

```bash
T_PAR = PAR の透過割合
T_NIR = NIR の透過割合
```

PAR と NIR の透過割合が得られたら、以下を計算します。

```bash
NIR_PAR_ratio = T_NIR / T_PAR
ln_NIR_PAR = ln(T_NIR / T_PAR)
```

例えば、ある LAI 条件で以下の値が得られたとします。

```bash
T_PAR = 0.25
T_NIR = 0.55
```

この場合、

```bash
NIR_PAR_ratio = 0.55 / 0.25 = 2.20
ln_NIR_PAR = ln(2.20) = 0.79
```

となります。

4.12. 最終的に作成するデータ表

最終的には、各 LAI 条件について、入力した LAI、LAD、PAR 透過割合、NIR 透過割合、ln(NIR/PAR) をまとめた表を作成します。

表の形式は以下のようにします。

| scenario           | species       | LAI | LAD | T_PAR | T_NIR | NIR_PAR_ratio | ln_NIR_PAR |
| ------------------ | ------------- | --: | --: | ----: | ----: | ------------: | ---------: |
| canopy_one_species | Fagus crenata | 0.5 | 0.2 |       |       |               |            |
| canopy_one_species | Fagus crenata | 1.0 | 0.4 |       |       |               |            |
| canopy_one_species | Fagus crenata | 1.5 | 0.6 |       |       |               |            |
| canopy_one_species | Fagus crenata | 2.0 | 0.8 |       |       |               |            |
| canopy_one_species | Fagus crenata | 2.5 | 1.0 |       |       |               |            |
| canopy_one_species | Fagus crenata | 3.0 | 1.2 |       |       |               |            |
| canopy_one_species | Fagus crenata | 3.5 | 1.4 |       |       |               |            |
| canopy_one_species | Fagus crenata | 4.0 | 1.6 |       |       |               |            |
| canopy_one_species | Fagus crenata | 4.5 | 1.8 |       |       |               |            |
| canopy_one_species | Fagus crenata | 5.0 | 2.0 |       |       |               |            |


各列の意味は以下の通りです。

| 列名              | 意味                         |
| --------------- | -------------------------- |
| `scenario`      | シミュレーション条件                 |
| `species`       | 使用した葉の種類                   |
| `LAI`           | 入力した葉群の LAI                |
| `LAD`           | LAI を 2.5 m 厚の葉群に変換した葉面積密度 |
| `T_PAR`         | PAR の透過割合                  |
| `T_NIR`         | NIR の透過割合                  |
| `NIR_PAR_ratio` | `T_NIR / T_PAR`            |
| `ln_NIR_PAR`    | `ln(T_NIR / T_PAR)`        |


この表を CSV ファイルとして保存します。

```bash
summary_canopy_one_species.csv
```

この CSV を使って、LAI と ln(NIR/PAR) の関係を解析します。


4.13. LAI と ln(NIR/PAR) の関係を解析する

作成した表を用いて、入力した LAI と ln(NIR/PAR) の関係を確認します。

久米式 LAI 推定式では、LAI は以下のように表されます。

```bash
LAI = a × ln(NIR/PAR) + b
```

本解析では、FLiESvox によって得られた T_PAR と T_NIR から、

```bash
ln_NIR_PAR = ln(T_NIR / T_PAR)
```

を計算し、それを説明変数として LAI との関係を調べます。

ブナ葉のみの仮想葉群で得られた関係は、林冠木1種のみの場合における LAI 推定式の基礎となります。
この結果を、後で作成する「林冠木2種」「ササのみ」「林冠木 + ササ」のモデルと比較することで、葉の種類や下層植生の有無が LAI 推定に与える影響を検討します。

