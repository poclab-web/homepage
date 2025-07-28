---
title: "機械学習による抗酸化物質の予測と構造活性相関研究"
excerpt: "DPPH、ORAC等の抗酸化指標の予測と分子記述子を用いた構造活性相関の解明<br/><img src='/images/500x300.png'>"
collection: portfolio
---

## プロジェクト概要

活性酸素種（ROS）による酸化ストレスは、がん、心疾患、老化などの慢性疾患の原因となることが知られています。抗酸化物質は、これらのROSを除去することで生体を保護する重要な役割を果たします。本プロジェクトでは、機械学習と量子化学計算を組み合わせて、植物フェノール類の抗酸化活性を予測し、構造と活性の関係を定量的に解明することを目指しています。

## 研究内容

### 🎯 **主要な研究テーマ**

#### 1. **DPPH radical scavenging activity の構造活性相関**

- 178種類のフェノール類のDPPH抗酸化活性測定
- 分子記述子と量子化学計算による構造特性の解析
- イオン化ポテンシャル（IP）と抗酸化活性の相関解明
- 速度論的側面と熱力学的側面による抗酸化能の評価

#### 2. **多種抗酸化指標の包括的解析**

- ORAC（Oxygen Radical Absorbance Capacity）
- SOAC（Singlet Oxygen Absorption Capacity）
- ABTS（2,2'-azinobis(3-ethylbenzothiazoline-6-sulfonic acid)）
- MTT（3-(4,5-dimethylthiazole-2-yl)-2,5-diphenyltetrazolium bromide）
- DPPH（2,2-diphenyl-1-picrylhydrazyl）

#### 3. **機械学習による活性予測モデル**

- 18個の重要特徴量の選定
- XGBoostを用いた予測モデルの構築
- 次元削減技術（UMAP）による化学空間の可視化

### 🔬 **研究手法・アプローチ**

#### **実験的手法**

1. **DPPH抗酸化活性測定**: 統一された実験条件での大規模測定
2. **FTIR分光法**: 抗酸化反応の進行度評価
3. **UV-Vis分光法**: 反応速度論的解析

#### **計算化学手法**

1. **量子化学計算**: 半経験的分子軌道法や密度汎関数理論による分子最適化とエネルギー計算
2. **熱力学パラメータ算出**:
   - イオン化ポテンシャル（IP）
   - 結合解離エネルギー（BDE）
   - プロトン解離エンタルピー（PDE）
   - プロトン親和力（PA）
   - 電子移動エンタルピー（ETE）

#### **機械学習手法**

1. **特徴選択**: フィルター法による113個から18個への絞り込み
2. **回帰・分類**: XGBoost、線形回帰、ロジスティック回帰
3. **次元削減**: UMAP（Uniform Manifold Approximation and Projection）

## 研究成果

### 📊 **主要な発見**

#### **構造活性相関の解明**

- **イオン化ポテンシャル（IP）が最重要因子**: IP > 200 kcal/molで活性が大幅に低下
- **ヒドロキシ基数の影響**: 2個以上のヒドロキシ基で高い抗酸化活性
- **電子供与基の効果**: メトキシ基 > H > 電子求引性基の順で活性向上
- **後続反応の影響**: カテコール骨格やヒドロキノン骨格で後続反応による活性向上

#### **反応機構の分類**

- **SET-PT機構**: 単電子移動-プロトン移動（DPPH assayで主要）
- **HAT機構**: 水素原子移動（ORAC assayで主要）
- **SPLET機構**: 逐次プロトン脱離-電子移動

#### **機械学習モデルの性能**

- **18個の共通特徴量**で5つの異なる抗酸化指標を予測可能
- **化学空間の可視化**：フラボノイドを中心とした放射状分布
- **予測精度**: 各assayで良好な予測性能を達成

### 📄 **定量的成果**

- **178個のフェノール化合物**の包括的DPPH活性データベース構築
- **タンニン酸**で最高活性（15.4 TEmol/mol）
- **フェニル1,4-ジヒドロキシ-2-ナフトエート（DHNA-Ph）**が最適光増感剤

## 応用・展開

### 🚀 **実用化への展開**

#### **食品・医薬品分野**

1. **機能性食品開発**: 抗酸化活性の高い食品成分のスクリーニング
2. **医薬品探索**: 新規抗酸化剤の分子設計支援
3. **保存料開発**: 天然由来抗酸化保存料の最適化

#### **計算創薬への応用**

1. **バーチャルスクリーニング**: 大規模化合物ライブラリからの活性予測
2. **分子設計指針**: 構造活性相関に基づく新規化合物設計
3. **アッセイ選択**: 化合物特性に応じた最適なアッセイ法の推奨

### 🔍 **社会実装の可能性**

- **食品産業**: 酸化防止剤の効率的スクリーニング
- **化粧品業界**: 抗老化成分の開発指針
- **農業分野**: 植物の抗酸化能力評価システム

この研究により、従来の個別的な抗酸化研究から、包括的・予測的アプローチへの転換が可能となり、効率的な抗酸化物質の探索・設計が実現されます。

## 関連論文

- [Kinetic and thermodynamic evaluation of antioxidant reactions: factors influencing the radical scavenging properties of phenolic compounds in foods](https://scijournals.onlinelibrary.wiley.com/doi/10.1002/jsfa.70080)  
  *Journal of the Science of Food and Agriculture*, 2025

- [DPPH Measurements and Structure—Activity Relationship Studies on the Antioxidant Capacity of Phenols](https://www.mdpi.com/2076-3921/13/3/309)  
  *Antioxidants*, 2024, Vol. 13, No. 3, pp. 309

- [Feature Selection for the Interpretation of Antioxidant Mechanisms in Plant Phenolics](https://www.mdpi.com/1420-3049/28/3/1454)  
  *Molecules*, 2023, Vol. 28, No. 3, pp. 1454

- [Hydrophilic Oxygen Radical Absorbance Capacity Values of Low-Molecular-Weight Phenolic Compounds](https://link.springer.com/article/10.1007/s11224-022-01920-4)  
  *Structural Chemistry*, 2022

- [Prediction and Chemical Interpretation of Singlet-Oxygen-Scavenging Activity](https://pubs.rsc.org/en/content/articlehtml/2022/ra/d1ra08918h)  
  *RSC Advances*, 2022

- [Singlet-Oxygen-Scavenging Activity of Small Molecule Compounds by Using Machine Learning](https://www.mdpi.com/2076-3921/10/11/1751)  
  *Antioxidants*, 2021, Vol. 10, No. 11, pp. 1751
