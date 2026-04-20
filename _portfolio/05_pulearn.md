---
title: "有機合成における新規データ駆動的アプローチの探索"
excerpt: "有機合成実験を効率化する、新たなデータ駆動的アプローチを開発しています。<br/>
<img src='../images/portfolio/pulearn_image.png' width='500' height='300'>"
collection: portfolio
published: true
---


<style>
b {
  color: #03af7a;
}

.marquee {
  overflow: hidden;
}   

.marquee-text {
  display: inline-block;
  padding-left: 100%;
  white-space: nowrap;
  animation: marquee 30s linear infinite;
}

@keyframes marquee {
  0% { transform: translate(0); }
  100% { transform: translate(-100%); }
}
</style>


<div class="marquee">
  <p class="marquee-text">
    <span style="color: #005aff">
      有機合成における新規データ駆動的アプローチの探索
      <span style="color: #4dc4ff">Exploring New Data-Driven Approaches in Organic Synthesis</span>
      Exploration de nouvelles approches fondées sur les données dans la synthèse organique
      <span style="color: #4dc4ff">Exploración de nuevos enfoques basados en datos en la síntesis orgánica</span>
      Erforschung neuer datengestützter Ansätze in der organischen Synthese
      <span style="color: #4dc4ff">Исследование новых подходов к органическому синтезу на основе данных</span>
      有机合成中新型数据驱动方法的探索
      <span style="color: #4dc4ff">有機合成中新型數據驅動方法的探索</span>
      유기 합성에서의 새로운 데이터 기반 접근법 탐구
    </span>
  </p>
</div>


## プロジェクト概要

<center><font size="6">
  <span style="font-weight: bold; color: #ffffff; text-shadow: 0px 0px 10px rgb(0, 90, 255);">
    <p>
      機械学習で
      <span style="color: #ffff80">反応する分子</span>
      を予測する
    </p>
  </span>
</font></center>

有機合成化学では、目的の化合物をつくるために多くの反応条件を試す必要があります。  
しかし、実験には時間もコストもかかるため、 <b>どの分子が反応しやすいのか</b> を事前に予測できれば研究は大きく前に進みます。  
私たちは、実験結果だけに頼らず、データと機械学習を使って有機反応を効率化する新しいアプローチを探っています。

<div style="text-align:center">
  <img src="{{ site.baseurl }}/images/portfolio/pulearn_GA.png">
</div>


## 研究内容

### 🎯 **主要な研究テーマ**

#### 1. **PU learningを用いた反応予測**
機械学習により有機反応の結果を予測することは、目的物が十分に得られない実験の抑制に繋がり、資源の節約に有用である。その際、予測モデルに学習させる反応データ源として、科学文献や特許が考えられる。しかし、これらのデータ源は低収率反応 (負例) が報告されにくいという「報告バイアス」によって、その有用性が制限されている。負例が不足したデータで学習されたモデルは反応性を過大評価する傾向に陥りやすく、資源節約に重要な「負例の特定」という点において性能が不十分になりやすい。
そこで、本研究は正例と未ラベルのサンプルから二値分類を行う<b>positive and unlabeled learning (PU learning)</b> という機械学習手法を有機反応予測に適用させ、負例が不足した状況においても有意な反応予測ができることを実証した。PU learningは無機材料探索の合成可能性や固体-固体相転移の発現の予測に用いられた先行例があったが、有機反応予測に用いられた例は存在しなかった。

#### 2. **基質適用範囲の定量的評価**
近年の有機合成化学の反応開発において、論文で反応例として報告される基質の数は増加しています。この傾向は、反応の有用性を示すために、基質の数が指標として用いられている現状を示しています。  
しかし、基質の数が多くても類似した基質ばかりでは、反応の有用性を示すことはできません。有用性を示すために必要なのは数ではなく多様性ですが、基質の多様性を定量化する方法は確立されていません。  
私たちは、 <b>基質の多様性</b> を <b>定量化</b> し、基質の数に代わる新たな反応条件の <b>評価指標</b> の確立を目指しています。


### 🔬 **実験・計算アプローチ**

#### :abacus: **理論計算手法**
- **Gaussian 16**: 量子化学計算
- [**RDKit**](https://www.rdkit.org): 化合物データの処理, 特徴量算出
- **ECFP**: 構造的類似性尺度
- [**Python**](https://www.python.org): データ処理, 機械学習, 計算自動化


#### :brain: **機械学習手法**
- **効率的なデータ収集**: :globe_with_meridians: [PubChem](https://pubchem.ncbi.nlm.nih.gov), [ChEMBL](https://www.ebi.ac.uk/chembl/), [ChEBI](https://www.ebi.ac.uk/chebi/), [CAS SciFinder](https://scifinder-n.cas.org/) with [Python](https://www.python.org), [pandas](https://pandas.pydata.org), [RDKit](https://www.rdkit.org)
- **特徴量エンジニアリング**: 分子記述子の選択・最適化
- **分類**: Random Forest, Decision Tree, SVM etc.
- **次元削減**: 解釈性の向上・データ分布の可視化 (PCA, t-SNE, UMAP)


#### :alembic: **実験検証**
- **有機合成**: 実験によるデータ収集
- **qNMR**: 目的物の収量測定
- **予測基質の反応性検証**: 機械学習によって得られた結果を実験で検証


## 研究成果

### :bar_chart: **達成された成果**

#### 1. **PU learning を用いた反応予測**
- PU learningを用いることで、負例が不足した状況においても有意な反応予測ができることを実証

#### 2. **基質適用範囲の定量的評価**
- 基質適用範囲を基質の多様性の観点から定量化 :eyes:
- 反応条件の特徴を捉える評価指標を新たに定義 :magic_wand:
- 評価指標を計算する[Webアプリ](https://substrate-scope-metrics.streamlit.app)を公開 :iphone:


### 🔊 **学会発表**
1. 一澤 要守, 西井 崇文, 長野 遥, 坂口 大門, 五東 弘昭. フェノール類の酸化的カップリングにおける反応条件の基質適用範囲の評価と予測. [日本コンピュータ化学会2024年秋季年会](https://touche-np.org/sccj), 2024.10.20, 室蘭, P108.

2. 西井 崇文, 一澤 要守, 長野 遥, 坂口 大門, 五東 弘昭. PUラーニングを用いたフェノールの酸化的ホモカップリングにおける反応条件の基質適用範囲の予測と解釈. [第14回CSJ化学フェスタ2024](https://festa.csj.jp/2024/), 2024.10.23, 東京, P4-040.

3. 西井 崇文, 一澤 要守, 長野 遥, 坂口 大門, 五東 弘昭. PUラーニングを用いたフェノールの酸化的ホモカップリングにおける反応条件の基質適用範囲の予測と解釈. [第47回ケモインフォマティクス討論会](https://sites.google.com/view/chemoinfo2024/ホーム), 2024.12.17, 金沢, P03.

4. 西井 崇文, 一澤 要守, 長野 遥, 向井 裕哉, 坂口 大門, 五東 弘昭. PU Learningを用いたフェノールの酸化的ホモカップリングにおける反応性予測. [第19回日本ケミカルバイオロジー学会](https://jscb.jp/annual-meeting/outline/), 2025.6.5-6, 京都, P-049.

5. 一澤 要守, 西井 崇文, 五東 弘昭. フェノール類の酸化的カップリングにおける基質適用範囲の評価. [日本コンピュータ化学会2025年春季年会](https://www.sccj.net/events/nenkai/2025sp/program.html), 2025.6.6, 東京, 2P17.

6. 一澤 要守, 西井 崇文, 五東 弘昭. フェノール類の酸化的カップリングにおける基質適用範囲の評価. [第15回CSJ化学フェスタ2025](https://festa.csj.jp/2025/), 2025.10.24, 東京, P8-019.


### :page_facing_up: **論文**
1. Nishii, T.; Ichizawa, K.; Nagano, H.; Mukai, H.; Sakaguchi, D.; Gotoh, H. Predicting Substrate Reactivity in Oxidative Homocoupling of Phenols using Positive and Unlabeled Machine Learning. *ACS Omega* **2025**, *10* (42), 49805–49815.  
DOI: [10.1021/acsomega.5c05523](https://doi.org/10.1021/acsomega.5c05523)

2. Ichizawa, K.; Nishii, T.; Gotoh, H. Substrate Scope in Organic Reactions: Comparison of Fingerprint-Based and Reactivity-Based Similarity Metrics. *Journal of Chemical Information and Modeling* **2026**, *66* (7), 3878–3891.  
DOI: [10.1021/acs.jcim.5c03167](https://doi.org/10.1021/acs.jcim.5c03167)


### :computer: **ソフトウェア**
1. Substrate Scope Metrics  
[![](https://img.shields.io/badge/Streamlit-Substrate_Scope_Metrics-red?logo=streamlit)](https://substrate-scope-metrics.streamlit.app/)
[![](https://img.shields.io/badge/GitHub-streamlit--substrate--scope--metrics-green?logo=github)](https://github.com/poclab-web/streamlit-substrate-scope-metrics)
[![](https://img.shields.io/badge/Zenodo-10.5281/zenodo.19564343-blue?logo=zenodo)](https://doi.org/10.5281/zenodo.19564343)


### :newspaper: **紹介記事**
1. [【プレスリリース】有機反応の「適用範囲」を定量評価する新手法を開発](https://www.ynu.ac.jp/hus/koho/34873/detail.html)

2. [有機反応の適用範囲を“見える化”した研究](https://zenn.dev/poclab_techblog/articles/e122ee49f88a70)


## 今後の展開

### :rocket: **次のステップ**

- **様々な反応系への応用**: 教科書に載っている人名反応をはじめとする、様々な反応へ応用していく。
- **分子特性予測と反応性予測の融合**: 有用な特性を持つ分子の予測とそれらの合成可能性の予測を組み合わせ、さらに効率的な実験が可能になる。
- **PNU learning を用いた機械学習モデルの構築**: 負例(Negative)データも活用した反応予測法の開発、より明確な基質適用範囲の予測が期待される。
