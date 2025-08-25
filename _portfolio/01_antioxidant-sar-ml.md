---
title: "抗酸化物質の構造活性相関研究"
excerpt: "ポリフェノールのチカラをデータで見える化-AIと計算化学で食品の抗酸化能を未来予測！-<br/>
<img src='../images/portfolio/food_informatics_flowchart.png' width='500' height='300'>"
collection: portfolio
published: true
---

## プロジェクト概要

近年、野菜・果物・茶葉などに豊富に含まれるポリフェノール類は、体内で発生する活性酸素（ROS）を抑制し、老化や生活習慣病のリスク低減に寄与すると考えられています。しかし、試験管内で測定される抗酸化能の値をどう解釈し、食品の機能性につなげるのかは、食品科学分野で30年来の課題でした。

さらに近年、**フェロトーシス（鉄依存性細胞死）**という新たな細胞死のメカニズムが注目されており、がん・神経変性疾患・炎症性疾患などとの関連が示唆されています。ポリフェノールの一部には、フェロトーシスを制御する可能性があることも報告されており、抗酸化能とフェロトーシス制御の関係性を探ることは、食品の新たな機能性評価につながると期待されています。

本研究では、**食品情報学（Food Informatics）**という新しい学術分野を切り開き、以下を目指します：

- 食品成分（特にポリフェノール）の構造情報を解析し、試験法ごとにばらつく抗酸化能データを統一的に解釈
- 計算化学と機械学習を組み合わせた予測モデルで、抗酸化能およびフェロトーシス制御能を事前に予測できる仕組みを構築
- 抗酸化活性とフェロトーシス制御を基盤とした食品の新しい価値評価基盤を提案
- これにより、試行錯誤に依存してきた評価から、データ駆動型で理解・予測できる食品科学へ転換し、食品開発・健康科学・栄養設計への応用を目指します。

## 研究の全体像

私たちは、食品に含まれる数千種規模のフェノール類化合物を対象に、以下の統合ワークフローを進めています：

**領域探索 → 測定 → 計算 → 予測 → 活性比較**

### 1. 抗酸化能データの整理と統合

- ORAC法、DPPH法など主要な抗酸化試験で得られたデータを体系化
- 文献やデータベース（FoodDBなど）から化合物情報を抽出
- 測定条件の違いによるばらつきの整理

### 2. 構造情報の数値化（Food Informatics）

- 化学構造を記述子に変換（分子記述子、量子化学パラメータ）
- BDE、HOMO、イオン化ポテンシャルなどを計算
- 構造‐活性の関係を可視化（クラスタリング、化学空間マップ）

### 3. 機械学習による抗酸化能予測モデル

- 小規模データでも機能するアルゴリズム（XGBoost, 転移学習など）
- 特徴量選択とSHAP解析による説明可能な予測モデルの構築
- WEBアプリとして公開を目指しています（例：[DPPH予測アプリ](https://dpph-prediction.streamlit.app/)）

### 4. 新規食品成分・高機能化合物の提案

- 食品由来フェノール類の化合物空間を俯瞰
- 予測モデルを活用した有望成分の探索
- 健康機能性食品や医薬品リード化合物の開発支援

## 研究の特徴

### 食品情報学（Food Informatics）の先駆け

食品成分をデータ科学で解析し、予測可能な科学へ

### 分野横断的アプローチ

化学・栄養・情報科学を融合

### 社会実装志向

健康寿命の延伸、食品機能性の科学的裏付け、産業連携

## 将来展望

- 抗酸化能だけでなく、香り・味・代謝活性など多様な機能性予測へ拡張
- データベースと機械学習を組み合わせた食品成分の総合的な設計支援プラットフォームを構築
- 食品産業・創薬・栄養学・化粧品分野への応用展開

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
