---
title: "機械学習や量子化学計算を用いた機能性材料の探索"
excerpt: "計算化学と機械学習を融合した手法により、新規機能性材料の設計・予測・最適化を目指す<br/>
<img src='../images/portfolio/MQM-information.png' width='500' height='300'>"
collection: portfolio
published: true
---

## プロジェクト概要

現代の材料科学において、従来の試行錯誤的な研究手法から脱却し、理論計算と機械学習を組み合わせた予測的アプローチが注目されています。本プロジェクトでは、量子化学計算によって得られる分子の電子構造情報・吸光特性と機械学習アルゴリズムを融合し、機能性物質の効率的な探索と設計を行っています。

## 研究内容

### 🎯 **主要な研究テーマ**

#### 1. **光重合開始剤の最適化研究**
- ナフトエ酸誘導体を用いた光増感剤の開発
- LED光源（405nm）に対応した新規光重合システムの構築
- 分子設計による光吸収特性の制御

#### 2. **量子化学計算による物性予測**
- DFT計算を用いた分子の電子状態解析
- 励起状態計算による光学特性の予測
- 反応経路計算による機構解明

#### 3. **機械学習を活用した材料探索**
- 分子記述子と物性値の相関解析
- 深層学習による構造-活性相関の予測
- ベイズ最適化による効率的な分子設計

#### 4. **機械学習・MD計算を活用した新規高分子材料の探索**
- モノマー情報とポリマー物性の相関解析
- 機械学習とMD計算のハイブリッド化で予測の高速化
- MD計算が現実的でない物性の予測

### 🔬 **実験・計算アプローチ**

#### **理論計算手法**
1. **分子動力学計算**: MD計算による分子物性の予測
2. **半経験手法** : xTBを用いた一点計算、構造最適化、振動計算、CRESTを用いた配座探索・交差点の探索
3. **量子化学計算**: Gaussian, pyscf等を用いたDFT計算
4. **励起状態計算**: TD-DFT法による光学特性の予測

#### **機械学習手法**
1. **特徴量エンジニアリング**: 分子記述子の最適化
2. **回帰・分類モデル**: Random Forest, XGBoost, Generative Pre-trained Transformer, Gaussian Process Regression, Neural Network
3. **能動学習**: コストを考慮した自己改善型スクリーニング戦略

#### **実験検証**
1. **FTIR分光法**: 重合反応の進行度評価
2. **UV-Vis分光法**: 光吸収特性の測定
3. **蛍光消光実験**: 分子間相互作用の解析
4. **photo-DSC** : 重合開始性能評価

## 研究成果

### 📊 **達成された成果**

#### **光重合開始剤の研究**
- フェニル1,4-ジヒドロキシ-2-ナフトエート（DHNA-Ph）が最適な光増感剤であることを発見
- LED光源（405nm）使用時の重合促進効果を確認
- 電子移動メカニズムによる光増感機構を解明
- 従来材料比で高性能な材料設計(未発表)

#### **計算化学の成果**
- 励起状態間の電子移動過程を理論的に解明
- 分子構造と光学特性の相関関係を定量化
- 新規分子の物性予測精度を大幅に向上

#### **機械学習の成果**
- 言語モデルによる分子生成
- GNNモデルによる分子物性値予測モデルの構築
- 高コストなDFT計算を最適化するスクリーニングモデルの構築

## 🚀今後の展開

### **研究の発展方向**
1. **AI駆動型材料設計**: オートエンコーダ等を用いた新規分子構造の提案
2. **高スループット計算**: 大規模並列計算による物性データベース構築
3. **実験との融合**: 合成品の実験値を測定、生成モデルにフィードバックし、生成精度向上を目指す
4. **高分子物性予測モデルの開発**: モノマー情報のみでポリマーの各種物性の予測を目指す

### **応用展開**
1. **3Dプリンティング材料**: 高精度造形用光硬化樹脂の開発
2. **環境調和型材料**: バイオベース光重合開始剤の設計
3. **エネルギー材料**: 太陽電池・LED用有機材料の最適化

この研究により、従来の経験に依存した材料開発から、理論と機械学習に基づく予測的材料設計への転換を目指しています。

## 学会発表
- 渡辺 裕也、宇都口 真彦、関澤 拓也、檜森 俊一、山田 暁彦、五東 弘昭, 量子化学計算及び機械学習を用いた新規光重合開始剤であるオキシムエステルの設計及び開発,第14回CSJ化学フェスタ(P9-015)

- 渡邉翔琉、髙畑風花、長野遥、檜森俊一、山田暁彦、五東弘昭, 量子化学計算及び機械学習を用いた新規光重合開始剤の探索,第15回CSJ化学フェスタ(P3-005)


## 関連論文

- [Naphthoic Acid Derivatives as Photosensitizers for Short-wavelength α-Hydroxyacetophenone Photoinitiators](https://www.jstage.jst.go.jp/article/photopolymer/37/1/37_135/_article/-char/ja/)  
  *Journal of Photopolymer Science and Technology*, 2024, Vol. 37, No. 1, pp. 135-140

- [Mechanism for the photodegradation of 9,10-dibutoxyanthracene in the presence of air](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0263526)
  *PLoS ONE*, 2022, 17(3): e0263526
  
- [Polymerization inhibition mechanism of 1, 4-naphthoquinone by experimentation and DFT calculations](https://www.nature.com/articles/s41428-019-0206-3)
  *Polymer Journal*, 2020, 52, 499–507

- [関連研究論文 (Nature Polymer Journal)](https://www.nature.com/articles/s41428-019-0206-3)  
  *Polymer Journal*, Nature Publishing Group

## 関連特許

- US12065521B2[Compound having polycyclic aromatic skeleton, and endoperoxide compound of same](https://patents.google.com/patent/US12065521B2/en)
