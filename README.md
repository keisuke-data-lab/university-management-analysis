# 日本の大学経営における構造的課題の定量分析
## Quantitative Analysis of Structural Issues in University Management

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Analysis](https://img.shields.io/badge/Analysis-University%20IR-green.svg)
![Status](https://img.shields.io/badge/Status-Active-success.svg)

### 📌 プロジェクトの目的 (Purpose)
本プロジェクトは、大学経営における「定員割れリスク」および「ガバナンス不全」が財務に与える影響を、**IR担当者および経営層が即時評価できる形でモデル化・定量化すること**を目的としています。

#### 📄 レポートの概要（3行まとめ）
* **課題定義:** 少子化環境下における大学の**定員管理・ガバナンス不全が生む財務リスク**を定量化
* **分析手法:** 学部ごとの**ブランド毀損率（η）**
が財務に与える影響をシミュレーション
* **成果:** IR担当者が即時に試算できる**簡易モデル（Python）**を構築

### 📂 成果物 (Outputs)
本分析の詳細は、以下のレポートおよびノートブックにまとめています。

* **📄 [詳細分析レポート (PDF)](docs/university_management_report.pdf)**
    * ガバナンス構造と財務リスクの相関を、PESTEL/7Sフレームワークを用いて論じた包括的レポートです（A4 4ページ）。
* **🐍 [財務損失シミュレーション (Python Notebook)](./university_financial_loss_simulation.ipynb)**
    * *※現在実装中 (Day 3公開予定)*
    * ブランド毀損率に基づく損失額を計算するコードと可視化グラフを格納しています。

---

### 🔍 分析のアプローチ (Methodology)

#### 1. ガバナンス視点での課題抽出
大学経営において、数値（財務）の悪化は「結果」に過ぎず、真の原因は「組織構造（ガバナンス）」にあります。本分析では以下の視点で課題を定義しました。
* **意思決定の遅延:** 理事会・評議員会の権限不均衡によるリスク
* **専門職の不在:** データに基づく経営判断（IR）を行う専門人材の不足

#### 2. 定量評価モデル (Financial Loss Model)
「ブランド力の低下」という定性的なリスクを、具体的な「損失金額」に変換するために、以下の簡易モデルを構築しました。
このモデルは、数学的な専門知識がないステークホルダー（事務職員・教員）でも理解できるよう、変数を最小限に絞っています。

$$L = N \times T \times \eta$$

この数式は、Python Notebook 内の関数 `loss_simulation()` として実装されています。

| 変数 | 定義 | 意味 (IR的視点) |
| :--- | :--- | :--- |
| **$L$** | **Loss (損失額)** | 経営への直接的な財務インパクト |
| **$N$** | **Number (学生数)** | 定員規模（学部の規模感） |
| **$T$** | **Tuition (授業料)** | 学費単価（収益構造のベース） |
| **$\eta$** | **Eta (減少率)** | ブランド毀損による入学者減少率（感度分析対象） |

---

### ▶ 使い方 (How to Use)
本リポジトリに含まれる Python Notebook は、以下の手順で即座にシミュレーションを実行できます。

1. `university_financial_loss_simulation.ipynb` を開く。
2. セルを上から順に実行するだけで、損失額の試算結果が算出されます。
3. 変数 $N$（定員）・$T$（授業料）・$\eta$（ブランド毀損率）の数値を変更することで、**貴学の状況に合わせた感度分析**が可能です。

### 🔮 今後の拡張計画 (Roadmap)
本プロジェクトは継続的な改善を予定しています。大学IRの実務において、より精緻な意思決定支援を行うためのロードマップです。

* [ ] 学部別の実データ（募集人数・充足率）を用いた検証
* [ ] 年度推移を可視化するダッシュボード（Power BI / Tableau）版の作成
* [ ] 在籍率・就職率データと連動した統合モデルへの拡張

---

### 🛠 使用技術・ツール (Tech Stack)
大学IRの実務において、再現性と透明性を担保するために以下の技術を選定しました。

* **Analysis & Logic:**
    * PESTEL Framework (Macro Environment)
    * McKinsey 7S Framework (Internal Environment)
* **Simulation & Visualization:**
    * **Python:** データ加工およびシミュレーション計算
    * **Pandas:** データの構造化処理
    * **Matplotlib:** 感度分析結果の可視化
* **Documentation:**
    * **GitHub:** 分析プロセスのバージョン管理と公開
    * **VS Code:** コーディングおよびドキュメント作成

---

### 👤 Author
**Keisuke Nakamura (keisuke-data-lab)**
* Data Analyst / University IR Specialist
* 現場データの収集・統合から、経営層への戦略提言までを一貫して担当。
* "Data-Driven Decision Making for Higher Education"

---
© 2025 Keisuke Nakamura | [GitHub Profile](https://github.com/keisuke-data-lab)