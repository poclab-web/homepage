---
title: "計算化学と機械学習の融合によるケトンの求核反応・還元反応の選択性の解析"
excerpt: "ケトン基の求核反応・還元反応を対象として、量子化学計算により得られた遷移状態構造およびその相互作用領域の特徴を抽出し、機械学習モデルと組み合わせることで選択性の予測を行っています。さらに、相互作用特徴と反応性との関連を定量的に解析し、反応選択性の要因の理解を深化させています。<br/>
src='../images/portfolio/QSSR_image.png' width='500' height='300'>
collection: portfolio
published: true
---

## プロジェクト概要
有機化学において、量子化学計算から得られる電子的情報や化学理論に基づく指標と、実験で得られる反応性との関連付けは極めて重要です。本研究では、この結び付けを強化するため、量子化学計算により得られた相互作用領域の特徴を有した電子情報を機械学習モデルに組み込み、化学反応選択性と相互作用領域との関連を定量的に解析しています。

## 研究の背景
有機合成化学において、反応選択性や反応性の制御は重要です。特に、ケトン基に対する求核反応や還元反応は反応性に富むアルコールを立体選択的に合成する方法として重要です。これまで、計算や実験、機械学習的なアプローチによってケトン基に対する反応選択性の説明や予測が試みられてきましたが、ケトン基や反応剤の構造は多様なため網羅的に選択性を説明することは困難でした。我々のグループでは、反応の本質を支配する立体電子状態の評価を軸に、計算化学とデータ駆動的なアプローチを融合し、反応選択性の網羅的な予測手法の確立や体系的な理解を目指しています。

## 研究テーマ
### 1. ケトンの求核反応の面選択性予測
#### 研究内容
- 分子の電子状態と反応選択性の間の関係を解明する新しい手法を開発
- 本手法を用いて 323 反応の選択性の定量的な予測に成功
- 天然物や医薬品分子の設計への応用が期待される
#### 🔬 **研究手法・アプローチ**
- 反応性と電子状態の関係(Salem-Klopman式)をもとに、立体電子状態を評価する手法を開発
- 理論的に記述が困難な要素には経験的なパラメータを導入し、データ駆動的に最適化
- これまで困難だった体系的な反応選択性の理解に成功!

### 2. ケトンの不斉還元反応の選択性解析
#### 研究内容
- ケトン基質の触媒による遷移状態構造を用いた相互作用解析機械学習モデルの開発
#### 🔬 **研究手法・アプローチ**
- 14種のケトン基質に対して、CBS還元反応の量子化学計算による遷移状態構造を導出
- それら14個の基質を得られたTS構造に基づいてクラスタリング、それ以外の90個の基質に対して仮想TS構造を導出
- 導出した遷移状態構造から分子間相互作用領域を導出し、機械学習モデルによって学習
- DFT計算（ωB97X-D/def2-TZVP）により基質と遷移状態を解析
- 反応部位での反応剤との立体・電子的相互作用をエネルギー分解して評価

![asymmetric reduction analysis abstruct]({{ site.baseurl }}/images/portfolio/shimono_abstruct.png)

### 3. 競争反応実験を用いた反応性の収集
#### 研究内容
- ケトンの還元選択性の予測
・競争反応を用いたケトンの還元選択性の定量実験法の開発
・機械学習を用いて2つのケトン基をもつジケトンの還元選択性(位置選択性＆面選択性)を予測
#### 🔬 **研究手法・アプローチ**
実験手法
- 同一系内で2種類の基質を反応させる競争反応を用いてケトンの還元反応の反応速度のデータ(約70基質)を取得

計算化学手法
1. 量子化学計算で構造最適化
　実験した基質の構造を最適化
2. 最適化された構造を解析
　電荷や振動情報、3次元的な電子状態などを算出

機械学習手法
1. 実験値と解析結果のデータセットを機械学習
　反応速度の予測モデルを作成
2. 還元選択性の予測
　作成したモデルを用いて還元選択性を予測

![competitive reaction abstruct]({{ site.baseurl }}/images/portfolio/competitive_reaction_abstruct.png)

### 🔍 **学術的・産業的意義**
反応の本質を支配している立体電子状態の評価を軸として、遷移状態解析とデータ駆動的なアプローチを融合することで様々な基質や反応剤に対する反応選択性の網羅的な理解が可能にしています。

## 関連論文
- Sakaguchi, Daimon, Kawasaki, Taisei, Itakura, Mayu, Tada, Chihiro, and Hiroaki Gotoh, "Competition Experiment-Based Kinetic Analysis of Ketone Reductions and Data-Driven Prediction of Regioselectivity" (2025) preparing.
- Sakaguchi, Daimon, Shimono, Masaki, and Hiroaki Gotoh, "Analysis of Asymmetric Reduction of Ketones Using Three-
Dimensional Electronic States" (2025) submitted.
- 坂口大門, 五東弘昭. "立体電子状態の定量評価による求核反応の面選択性の起源の解明." Journal of Computer Chemistry, Japan 24.1 (2025): A18-A24.
- Sakaguchi, Daimon, and Hiroaki Gotoh. "Using Three-Dimensional Information to Predict and Interpret the Facial Selectivities of Nucleophilic Additions to Cyclic Ketones." Journal of Chemical Information and Modeling 64.8 (2024): 3213-3221.
- Sakaguchi, Daimon, and Hiroaki Gotoh. "Quantification of steric hindrance by geometric calculation, prediction of the reductive selectivity of ketones, and clarification of reaction mechanism." (2022).
---
