---
title: "ケトン反応選択性の解析と予測"
description: "実験・計算化学・機械学習を組み合わせ、ケトン反応の選択性予測と決定要因の解析を進めています。"
excerpt: "実験・計算化学・機械学習を組み合わせ、ケトン反応の選択性予測と決定要因の解析を進めています。<br/>
<img src='../images/portfolio/QSSR_image.png' width='500' height='300'>"
collection: portfolio
published: true
---

## プロジェクト概要
有機化学における反応選択性の理解には、反応の山場である遷移状態（TS構造<a href="#ts-structure"><sup>1</sup></a>）や、その周辺で働く三次元的な電子状態を捉えることが重要です。本研究では、ケトンの求核反応や、不斉還元反応・競争反応などの実験と、計算化学、さらに機械学習を組み合わせることで、反応選択性を予測すると同時に、その決定要因を定量的に解析しています。

<div style="padding: 0.9rem 1rem; margin: 1rem 0 1.3rem; background: #f7fafc; border-left: 4px solid #2b8a3e; color: #494e52;">
<strong>キーワード</strong>: DFT計算 / 電子状態 / 遷移状態解析 / 反応選択性 / 求核反応 / 不斉還元 / 位置選択性 / 機械学習
</div>

## メンバー
- [坂口 大門]({{ site.baseurl }}/members/sakaguchi-daimon/)
- 一澤 要守
- 板倉 茉由
- 尾石 智紀

## 研究の流れ

実験・DFT計算・遷移状態解析で反応データを集め、三次元電子状態や相互作用特徴を抽出し、機械学習で選択性を予測・解釈します。

<div style="text-align:center; margin: 1rem 0 1.6rem;">
  <img src="../../images/portfolio/QSSR_image.png" width="100%" alt="実験と計算を組み合わせたケトン反応選択性研究の概要">
</div>

<div style="display:flex; flex-wrap:wrap; gap:12px; margin: 0 0 1.4rem;">
  <div style="flex:1; min-width:220px; padding:12px 14px; background:#f8fbf8; border:1px solid #d9ece2; border-radius:8px; color:#494e52;">
    <strong>1. データ取得</strong><br/>
    競争反応実験、量子化学計算、遷移状態解析から反応性データを収集
  </div>
  <div style="flex:1; min-width:220px; padding:12px 14px; background:#fffaf3; border:1px solid #f0e0bc; border-radius:8px; color:#494e52;">
    <strong>2. 特徴量設計</strong><br/>
    電子密度、静電ポテンシャル、相互作用領域、三次元電子状態を定量化
  </div>
  <div style="flex:1; min-width:220px; padding:12px 14px; background:#f8f6ff; border:1px solid #ddd7ff; border-radius:8px; color:#494e52;">
    <strong>3. 予測と解釈</strong><br/>
    面選択性・不斉選択性・位置選択性を予測し、決定要因を解明
  </div>
</div>

## 研究の背景
有機合成化学において、反応選択性や反応性の制御は重要です。特に、ケトン基 (C=O) に対する求核反応や還元反応は、反応性に富むアルコールを立体選択的に合成する方法として広く利用されています。これまでにも計算や実験、機械学習によるアプローチが試みられてきましたが、基質や反応剤の構造は多様であり、網羅的に選択性を説明することは容易ではありません。我々のグループでは、反応の本質を支配する立体電子状態の評価を軸に、計算化学とデータ駆動的アプローチを融合し、反応選択性の予測と体系的理解を目指しています。

## 研究テーマ
### 1. ケトンの求核反応の面選択性予測
---

本研究では、<span style="font-weight:700; color:#0b7285;">分子の電子状態と面選択性<a href="#facial-selectivity"><sup>2</sup></a>の相関</span>を定量的に記述する新しい手法を開発し、323 件の反応に対して <span style="font-weight:700; color:#0b7285;">面選択性を高精度に予測</span> することに成功しました。提案手法は、天然物合成や医薬品化学における立体選択的変換の設計指針としても応用可能であり、実用的な反応設計ツールとしての拡張性を持っています。

### 🔬 **研究手法・アプローチ**

研究手法は、Salem-Klopman 式<a href="#salem-klopman"><sup>3</sup></a> に基づく反応性理論を出発点として、求核攻撃点における立体電子的要因を定量化することで特徴づけられます。理論的扱いが難しい寄与については経験的パラメータを導入し、それらをデータ駆動的に最適化することで、従来は困難だった複雑な選択性要因を体系的に理解する枠組みを構築しています。この結果、電子状態に根ざした反応選択性の予測精度が向上し、幅広い反応系に適用できる方法論として確立されています。

![nucleophilic addition abstract](../../images/portfolio/nucleophilic_addition_abstruct.png)

### 2. ケトンの不斉還元反応の選択性解析
---

この研究では、3 種類の触媒を対象にケトンの不斉還元反応を幅広く収集し、それぞれの反応で R 体と S 体のどちらが優先的に生成するかという選択性を整理しました。

### 🔬 **研究手法・アプローチ**

反応前のケトン分子 300 種類について電子密度<a href="#electron-density"><sup>4</sup></a>や静電ポテンシャル<a href="#esp"><sup>5</sup></a>を計算し、分子の電子的性質を詳細に把握しました。これらの電子構造情報を基盤に、<span style="font-weight:700; color:#0b7285;">三次元電子状態</span>をそのまま扱える CoMFA<a href="#comfa"><sup>6</sup></a> を用い、構造と選択性の関係を学習させました。このプロセスによって構築したモデルは、300 件のケトン反応について生成物の向き (R 体 / S 体) の違いを高い精度で予測できるようになりました。さらに、反応途中の構造である遷移状態を DFT<a href="#dft"><sup>7</sup></a> 計算により求め、その中で働く弱い相互作用を NCI plot<a href="#nci"><sup>8</sup></a> や SAPT<a href="#sapt"><sup>9</sup></a> 法で解析しました。これにより、<span style="font-weight:700; color:#0b7285;">不斉選択性の起源</span>を分子レベルで理解する基盤が得られました。

<div style="text-align:center; margin: 1rem 0 1.2rem;">
  <img src="../../images/portfolio/cbs_acetophenone.gif" width="58%" alt="不斉還元反応における遷移状態構造の例">
</div>

![asymmetric reduction analysis abstract](../../images/portfolio/shimono_abstruct.png)

### 3. 競争反応実験を用いた反応性の収集
---

この研究では、競争反応を利用してケトン還元反応の選択性を定量的に評価する実験手法を開発し、そのデータをもとに機械学習を用いてジケトン分子の位置選択性<a href="#regioselectivity"><sup>10</sup></a>と面選択性の両方を予測することを目指しています。複数の反応経路が同一条件下で競合する状況を観測することで、個々の基質の反応性を直接的かつ体系的に取得できる点が特徴です。

### 🔬 **研究手法・アプローチ**

実験面では、同一の反応条件下で二種類の基質を同時に反応させる競争反応法を用いて、ケトンの還元反応における相対的な反応速度の情報を取得しています。この手法は、絶対反応速度を測定するよりも簡便で再現性が高く、複数の基質の反応性を体系的に比較できる利点があります。

計算化学の側面では、まず実験で用いた基質の構造を量子化学計算によって最安定構造へ最適化し、その構造を基盤として分子特性を抽出しています。これには電荷分布、振動特性、三次元的な電子状態などが含まれ、これらは反応性を理解する上で重要な情報として扱われています。

機械学習のプロセスでは、実験から得られた反応速度と計算化学によって得られた分子記述子を組み合わせたデータセットを用いて予測モデルを構築しています。このモデルによって反応速度を予測し、その結果をもとにジケトンにおける還元の位置選択性と面選択性を予測するという体系的なアプローチを実現しています。

![competitive reaction abstract](../../images/portfolio/competitive_reaction_abstruct.png)

---

### 🔍 **学術的・産業的意義**
反応の本質を支配する立体電子状態の評価を軸として、遷移状態解析とデータ駆動的アプローチを融合することで、さまざまな基質や反応剤に対する反応選択性の網羅的理解が可能になります。これは、新規反応条件の設計、触媒開発、合成経路の効率化に資する基盤技術です。

## 学会発表・受賞

### 2025年度
- 2025年12月: D. Sakaguchi, M. Shimono, H. Gotoh. Fusion of transition state analysis and data-driven approach for stereoselectivity prediction in asymmetric ketone reduction. Pacifichem, Hawaii.
- 2025年10月: 板倉 茉由さんが [第15回CSJ化学フェスタ2025で「優秀ポスター発表賞」を受賞](https://www.ynu.ac.jp/hus/engk2/34505/detail.html). 受賞発表タイトル: 「競争反応の実験データを活用したケトンの還元選択性の予測」.

### 2024年度
- 2024年12月: 坂口 大門さんが [第47回ケモインフォマティクス討論会で優秀講演賞を受賞](https://www.ynu.ac.jp/hus/engk2/32847/detail.html).
- 2024.12.17-18: 坂口 大門, 下野 真輝, 五東 弘昭. ケトンの不斉還元反応に関する関連研究を [第47回ケモインフォマティクス討論会](https://sites.google.com/view/chemoinfo2024/%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%A0?authuser=0) で発表. 金沢.
- 2024.10.20: 坂口 大門, 五東 弘昭. 立体電子状態を評価する機械学習モデルによるケトンの求核反応の面選択性の予測と解釈. [日本コンピュータ化学会2024年秋季年会](https://touche-np.org/sccj), 室蘭, 1O07.

## 関連リンク
- [横浜国立大学プレスリリース: 分子の電子状態の解析による化学反応選択性の予測モデルの開発](https://www.ynu.ac.jp/hus/koho/31704/detail.html)
- [ケムステ: 機械学習と計算化学を融合したデータ駆動的な反応選択性の解明](https://www.chem-station.com/blog/2024/04/nack.html)

## 関連論文
- Sakaguchi, D.; Kawasaki, T.; Itakura, M.; Tada, C.; Gotoh, H. "Competition Experiment-Based Kinetic Analysis of Ketone Reductions and Data-Driven Prediction of Regioselectivity." (2025) preparing.
- Sakaguchi, D.; Shimono, M.; Gotoh, H. "[Analysis of Asymmetric Reduction of Ketones Using Three-Dimensional Electronic States.](https://doi.org/10.1021/acs.jpca.5c03510)" The Journal of Physical Chemistry A 129.39 (2025): 8945-8958.
- 坂口 大門, 五東 弘昭. "[立体電子状態の定量評価による求核反応の面選択性の起源の解明.](https://doi.org/10.2477/jccj.2024-0043)" Journal of Computer Chemistry, Japan 24.1 (2025): A18-A24.
- Sakaguchi, D.; Gotoh, H. "[Using Three-Dimensional Information to Predict and Interpret the Facial Selectivities of Nucleophilic Additions to Cyclic Ketones.](https://doi.org/10.1021/acs.jcim.4c00101)" Journal of Chemical Information and Modeling 64.8 (2024): 3213-3221.
- Sakaguchi, D.; Gotoh, H. "[Quantification of Steric Hindrance by Geometric Calculation, Prediction of the Reductive Selectivity of Ketones, and Clarification of Reaction Mechanism.](https://doi.org/10.21203/rs.3.rs-1715167/v1)" (2022).

---
## 用語集
**<span id="ts-structure">1. TS構造</span>**：
分子は反応するとき、結合の長さや結合角を変化させながら反応します。その過程では分子のエネルギーが一度上昇し、生成物へ向かう途中で極大値をとります。このエネルギー極大点に対応する瞬間の構造を TS 構造といいます。

**<span id="facial-selectivity">2. 面選択性</span>**：
炭素などが環状につながり、その環にケトン基が結合している分子を還元した場合、ヒドロキシ基が環に対して上側に結合する場合と下側に結合する場合の 2 パターンが生じます。このようにアルコールの立体がさまざまな要因から決定される現象を面選択性といいます。

**<span id="salem-klopman">3. Salem-Klopman 式</span>**：
求核剤と基質の相互作用を、軌道相互作用や静電相互作用などの観点から整理して反応性を議論するための考え方です。どの部位が反応しやすいか、どの方向から反応が進みやすいかを理解する際の基礎になります。

**<span id="electron-density">4. 電子密度</span>**：
分子内の各位置にどれだけ電子が存在しやすいかを表す量です。反応しやすい部位や相互作用の起こりやすさを議論する際の基礎になります。

**<span id="esp">5. 静電ポテンシャル</span>**：
分子のまわりの電荷分布に由来するポテンシャルで、分子がほかの分子とどのような静電的相互作用を示すかを可視化・定量化するのに用いられます。

**<span id="comfa">6. CoMFA</span>**：
Comparative Molecular Field Analysis の略称です。分子の周囲に広がる立体場や静電場を三次元グリッド上で表現し、構造と活性・選択性の関係を解析する手法です。

**<span id="dft">7. DFT</span>**：
Density Functional Theory（密度汎関数理論）の略称です。電子密度を基本量として分子の電子状態を求める量子化学計算手法で、反応経路や遷移状態の解析によく用いられます。

**<span id="nci">8. NCI plot</span>**：
Non-Covalent Interaction plot の略称です。電子密度とその勾配を用いて、分子内外で働く弱い相互作用を可視化する手法です。

**<span id="sapt">9. SAPT</span>**：
Symmetry-Adapted Perturbation Theory の略称です。分子間相互作用エネルギーを静電相互作用、分散力、交換反発などの成分に分けて解析する理論です。

**<span id="regioselectivity">10. 位置選択性</span>**：
ケトン基が複数ある分子では、それぞれのケトン基の周辺環境によって還元されやすさが異なります。このようにどのケトン基が還元されるかが決まる現象を位置選択性といいます。

**11. 量子化学計算**：
原子や分子の電子状態をシュレーディンガー方程式をもとに数値的に求める方法です。原子は原子核と電子から構成され、その特性は主に電子の状態によって決まります。電子は非常に小さいため、運動方程式 mα = F のような古典力学では運動を記述できませんが、量子力学の基本方程式であるシュレーディンガー方程式を近似することで数値的な表現が可能になります。([参考リンク](https://www.jstage.jst.go.jp/article/oubutsu/86/8/86_720/_pdf/-char/en))

**12. 構造最適化**：
分子の最も安定な、すなわち最も存在確率の高い立体構造を求めることです。

**13. 機械学習**：
入力したデータのパターンや規則性をコンピュータが学習することです。定期テスト対策のために過去問を解き、テストの傾向をつかもうとすることに近いイメージです。

**14. モデル**：
正しい予測結果を得るために、データをどのように判断するかを仕組み化したものです。学習した結果をもとに作成されます。過去問を解いたあと、教科書のどのあたりを重点的に勉強すれば点数が取れそうか、逆にどこには勉強時間を割くべきでないか、といった指針を立てるイメージです。
