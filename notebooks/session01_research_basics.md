# 第1回：研究とは何か・論文の構造(IMRAD)・統計/機械学習の必要性

### DSゼミナール3（2026年度）
熊本大学 データサイエンス学科


---



# お手伝いいただける実験技術職員様

所属：研究開発戦略本部 技術部門
居室：総合研究棟　207

小嶌 一生
kojima@cs.kumamoto-u.ac.jp

青木 敏裕
aoki@cs.kumamoto-u.ac.jp


---


# 自己紹介

![](images/2025-10-31-19-03-13.png)




1972年生まれ 54歳
放射線診断学専門医

医師生活29年のうち
- 12年を一般病院
- 4年を大学院 (医学研究科)
- 13年を大学病院勤務

統計・機械学習・プログラミングは独学

<div class="bottom1">
<div class="bottom2">
2010年ころ 天草地域医療センター勤務時
</div>
</div>


---


# 研究実績 (2025年末)






- 英語査読付き論文: 357編
	1st.または2nd., 責任著者: 146編
- 国内招待講演 57回
- 海外招待講演 14回
- 特許 3件
- 科学研究費補助金 13件, 代表3件
- 委員など
	JJR, Associate Editor (人工知能)
	日本医学放射線学会　代議員
	電子情報・人工知能委員会 委員
  日本X線CT医学会 理事


![](images/h-index_2025.png)


---

# 過去5年論文引用数






<div align="center">

![](images/Cites_2020-2024.png)

</div>

<div class="bottom1">
<div class="bottom2">
https://incites.clarivate.com/#/analysis/0/person
</div>
</div>


---

# 医学研究・応用分野から見たデータサイエンス入門

- 私は医学部在籍時は技術に詳しい医師の育成に携わっていました。

- 今度はデータサイエンスを学ぶ学生の皆さんを対象に、応用分野の一部である医学研究の立場からデータサイエンスをどのように活用しているかを紹介します。



---



## 📋 本日の目標

1. 研究プロセスの全体像を理解する
2. 科学論文の基本構造（IMRAD）を学ぶ
3. データサイエンス研究における統計学・機械学習の役割を理解する
4. ZoteroとPandocの使い方を学ぶ



---



## 0. なぜ論文（客観的証拠）が必要なのか？






- 私たちが新しい発見をしたり、自分の意見を他人に伝えようとするとき、単に「私はこう思う」と言うだけでは、相手を納得させることは困難です。
- 客観的な証拠（エビデンス）がない主張は、第三者からは**単なる個人の思い込み** や **偶然の出来事**と見なされてしまう可能性があります。

![](images/why_paper_needed.png)


---


## 証拠（論文）の役割




1. **客観性の確保**: 誰が見ても納得できるデータや分析結果を示すことで、独りよがりな解釈を防みます。
2. **再現性の保証**: どのような手順でその結果を得たかを公開することで、他人が同じ方法で確認できるようにします。
3. **知識の共有と蓄積**: 正確と検証された知識を論文として残すことで、人類全体の知的な財産として積み上がっていきます。

特に医学やデータサイエンスの分野では、**人の命に関わる意思決定**を扱うため、厳密に検証された「証拠」に基づく判断（EBM: Evidence-Based Medicine）が不可欠です。


---


## 生成AI時代における論文・研究の意義 - 何が変わったか？

ChatGPT・Gemini・Claude などの**生成AIの登場**により、プログラミングを取り巻く環境は大きく変化しました。

- コードを1行ずつ手書きしなくても、AIに「やりたいこと」を伝えるだけでコードが生成される時代
- 統計処理・グラフ描画・機械学習モデルの構築まで、AIがドラフトを作れる




では、「統計学・機械学習・プログラミングを学ぶ意味はなくなったのか？」


---


## 何が重要になったか？




**答えはNO。むしろ「考える力」の重要性が高まっています。**

<div align="center">

| 以前                               | 生成AI時代                                 |
| :--------------------------------- | :----------------------------------------- |
| コードを正確に書く技術             | ✅ 引き続き有用だが必須ではなくなりつつある |
| **何を分析するか目標を設定する力** | ⭐ さらに重要                               |
| **結果が正しいか評価する力**       | ⭐ さらに重要                               |
| **モデルの限界を理解する力**       | ⭐ さらに重要                               |

</div>



AIは「指示された通りにコードを書く」ことはできますが、**「何を目的とするか」「結果が正しいか」「研究として意味があるか」を判断することはできません。**


---


### 本ゼミで重視すること


#### 1. 内容の理解（Why）
- 統計的検定や機械学習モデルが**何をしているか**を理解する
- AIが生成したコードの意味を読み解ける

#### 2. 目標設定（What）
- 研究課題に対して**どの手法が適切か**を選択できる
- 「とりあえずAIに聞く」ではなく、**問いを正確に立てる**


#### 3. 評価項目の設定（How good）
- 分析結果が**科学的に妥当か**を判断できる
- 精度・AUC・p値などの指標の**意味と限界**を理解する
- AIの出力を鵜呑みにせず、**批判的に検証**する


---


> **まとめ**: 生成AI時代に求められるのは「コードを書く人」ではなく、  
> **「何を分析するか設計し、結果を正しく評価できる研究者」** です。  
> 本ゼミはその力を育てることを目標とします。


---


### 1. 研究とは何か？

### 1.1-2 研究の定義とプロセス
研究(Research)とは：
- 新しい知識を発見すること
- 既存の知識を検証・拡張すること
- 問題を解決するための体系的な調査


![](images/research_process.png)




---


### 1.3 良い研究の条件

- **新規性（Novelty）**: 新しい発見や視点がある
- **妥当性（Validity）**: 方法論が適切で、結果が信頼できる
- **再現性（Reproducibility）**: 他の研究者が同じ結果を得られる
- **意義（Significance）**: 学術的・社会的に価値がある


---



### 2.1 IMRADとは？
科学論文の標準的な構成：
- **I**ntroduction（序論）
- **M**ethods（方法）
- **R**esults（結果）
- **A**nd
- **D**iscussion（考察）


---


### 2.2 各セクションの役割
#### Introduction（序論）
**目的**: 研究の背景と目的を説明
が含まれる内容：
- 研究分野の背景
- 先行研究のレビュー
- 研究の必要性（ギャップ）
- 研究の目的・仮説

**読者への問い**: 「なぜこの研究が必要なのか？」


---


#### Methods（方法）
**目的**: 研究の手法を詳細に記述
が含まれる内容：
- 研究デザイン
- データ収集方法
- サンプルサイズ、対象者
- 分析手法（統計手法、機械学習モデル）
- 使用したソフトウェア・ツール

**読者への問い**: 「どうやって研究したのか？」


---


#### Results（結果）
**目的**: 分析結果を客観的に報告
が含まれる内容：
- 記述統計（平均、標準偏差など）
- 統計的検定の結果（p値、信頼区間）
- 図表（グラフ、表）
- 機械学習モデルの性能（精度、AUCなど）

**読者への問い**: 「何がわかったのか？」


---


#### Discussion（考察）
**目的**: 結果の意味を解釈し、研究の意義を論じる
が含まれる内容：
- 結果の解釈
- 先行研究との比較
- 研究の限界（Limitations）
- 今後の研究方向
- 結論（Conclusion）

**読者への問い**: 「結果は何を意味するのか？」


---


## 🗂️ 3. Zotero — 文献管理ツール

### Zoteroとは？

- **無料**のオープンソース文献管理ソフト
- 論文のPDFとメタデータ（著者・タイトル・DOI）を自動取得
- Word / Google Docs と連携して**引用を自動挿入**
- BibTeX形式でエクスポート → Pandocで活用




🔗 https://www.zotero.org/download/


---


### Zoteroのインストール

1. https://www.zotero.org/download/ にアクセス
2. **Zotero** をダウンロード・インストール
3. ブラウザ拡張 **Zotero Connector** をインストール  
   （Chrome / Firefox / Safari 対応）


---


### 論文をZoteroに登録してみよう

**DLR論文を実際にZoteroに追加する**




**方法① Chrome拡張から追加（推奨）**
> https://link.springer.com/article/10.1007/s00330-024-11212-6 をブラウザで開く  
> → Zotero Connectorアイコンをクリック  
> → 自動でメタデータ＋PDFを取得




**方法② DOIから追加**
> Zotero画面の「+」→「Add Item by Identifier」  
> → `10.1007/s00330-024-11212-6` を入力


---


### プラグインのインストール：Zotero PDF Translate

**英語論文をZotero内で日本語翻訳できるプラグイン**




1. https://github.com/windingwind/zotero-pdf-translate にアクセス
2. 最新の `.xpi` ファイルをダウンロード
3. Zotero → **Tools** → **Add-ons** を開く
4. `.xpi` ファイルをドラッグ＆ドロップ  
   または「Install Add-on From File」で選択
5. Zoteroを再起動


---


### 自分のライブラリに論文を追加してみよう

**先生の論文をZoteroに登録してみる**




1. **PubMed**（https://pubmed.ncbi.nlm.nih.gov/）で `Nakaura T` を検索
2. 興味のある論文ページで Zotero Connector をクリック
3. PDF付きで自動登録される




> 💡 Google Scholar / 出版社ページでも同様に登録できます


---


### 英語論文を日本語で読んでみよう

**Zotero PDF Translate の使い方**




1. Zoteroでライブラリの論文をダブルクリック（PDFビューアが開く）
2. 翻訳したいテキストを**マウスでドラッグ選択**
3. 右クリック → **Translate** で翻訳結果が表示




> ⚙️ **Settings → Translate Engine** でDeepL / Google翻訳などを選択可能


---


### 2.3 【実論文】この論文でIMRADを理解しよう




**Deep learning再構成がCT検査の放射線量とがんリスクに与える影響**

> Kobayashi N, **Nakaura T**, et al.  
> *European Radiology* (2025) 35:3499–3507

https://link.springer.com/article/10.1007/s00330-024-11212-6




この論文のアブストラクトを使って、**IMRADの各セクションを実際に識別**してみましょう。


---


### 📖 アブストラクトを読んでみよう ①

**[Purpose]**

> The purpose of this study is to estimate the extent to which the implementation of **deep learning reconstruction (DLR)** may reduce the risk of radiation-induced cancer from CT examinations, utilizing **real-world clinical data**.




**Q: これはIMRADのどのセクションに対応しますか？**

→ **Introduction**（研究の目的）


---


### 📖 アブストラクトを読んでみよう ②

**[Methods]**

> We retrospectively analyzed scan data of adult patients who underwent body CT during two periods: a **12-month pre-DLR phase** (n = 5553) using hybrid iterative reconstruction and a **12-month post-DLR phase** (n = 5494).  
> **Propensity score matching** 1:1 was employed based on age, sex, and BMI.  
> **Organ-specific equivalent doses**, total effective doses, and **Lifetime Attributable Risk (LAR)** for cancer were estimated.


---


### 📖 アブストラクトを読んでみよう ③

**[Results]**

> After propensity score matching, **5247 cases** from each group were included.  
> Post-DLR, the total effective dose significantly decreased to **15.5 ± 10.3 mSv** from **28.1 ± 14.0 mSv** (p < 0.001), a **45%** reduction.  
> The estimated annual cancer incidence decreased from **0.247%** pre-DLR to **0.130%** post-DLR.


---


### 📖 アブストラクトを読んでみよう ④

**[Conclusion]**

> The implementation of DLR has the possibility to **reduce radiation dose by 45%** and the risk of radiation-induced cancer from **0.247 to 0.130%** as compared with the iterative reconstruction.




💡 **ポイント**: アブストラクト自体がIMRAD構造の縮小版になっている！




---




## 📌 第1コマのまとめ

| テーマ   | 学んだこと                  |
| :------- | :-------------------------- |
| 研究とは | 客観的証拠（論文）の重要性  |
| IMRAD    | 科学論文の標準構造          |
| Zotero   | 文献管理・PDF翻訳・日本語化 |
| DLR論文  | 실際の論文でIMRADを体験     |




**次回（第2コマ）**: Pandoc + Markdownで論文を書いてみよう


---





# 第2コマ：論文の書き方とデータサイエンス

### DSゼミナール3（2026年度）
熊本大学 データサイエンス学科


---



## 📋 第2コマの目標

1. 論文を書く順番はIMRADと違うことを理解する
2. Results（結果）を書くために統計・機械学習が必要な理由を知る
3. 先生の論文の結果（図・表）を読んで理解する
4. PandocでMarkdown → Wordに変換する


---


## 5. 論文を書く順番はIMRADとは違う

### 「読む順番」と「書く順番」

論文は **IMRAD の順番で書かれている** ものですが、  
実際に書くときの順番は**異なります**。

<div align="center">

| 掲載順番（IMRAD） | 書く順番（実際）           |
| :---------------- | :------------------------- |
| Introduction      | **① Results（結果）**      |
| Methods           | **② Methods（方法）**      |
| Results           | **③ Introduction（序論）** |
| Discussion        | **④ Discussion（考察）**   |
| —                 | **⑤ Abstract（最後！）**   |

</div>


---


### なぜ Results から書くのか？




> **論文の核心は「データで何を示したか（Results）」**




- **Results が決まって初めて**、それを検証した Methods に説得力が生まれる
- **Results を踏まえて初めて**、なぜこの研究が必要かの Introduction が書ける
- Abstract は全セクションの要約なので、**最後に書く**




→ まずデータを分析・可視化して、**Results（結果）を固めることが論文執筆の第一歩**


---


### Results を書くために何が必要か？




データから「何がわかったか」を示すには：

- **記述統計**：平均・分散・分布でデータの特徴を把握
- **仮説検定**：「差がある」「関連がある」を統計的に確認
- **機械学習**：大量データからパターンを自動抽出
- **可視化**：表・グラフ・図で「見える化」




→ これが **データサイエンスが論文に必要な理由**


---


### 3. なぜ統計学・機械学習が必要か？

### 3.1 データサイエンス研究の特徴

現代の研究では、大量のデータを扱うことが一般的：
- 医学：電子カルテ、医学画像、ゲノムデータ
- 社会科学：アンケート、SNSデータ
- 工学：センサーデータ、シミュレーション結果
→ **統計学・機械学習が不可欠**


---


### 3.2 統計学の役割
#### 記述統計
- データの特徴を要約（平均、分散、分布）
- 可視化（ヒストグラム、散布図）

#### 推論統計
- サンプルから母集団の性質を推定
- 仮説検定（差があるか？関連があるか？）
- 信頼区間の計算


---


**母集団と標本**:  
研究の対象となるグループ全体を **母集団(Population)** と呼びますが、現実的にその全員を調査することは不可能です。そのため、一部のデータ（**標本：Sample**）を抽出し、そこから全体の特徴を推測します。

![](images/sampling_inference.png)


---


**推論の流れ**:
1. **サンプリング**: 母集団から一部のデータを集める
2. **統計的推論**: 集めたデータの結果に基づき、母集団全体でも同じことが言えるかを確率的に判断する


---


**例**: 新薬の効果を検証
- 仮説：「新薬は既存薬より効果がある」
- 方法：臨床試験でデータ収集
- 分析：t検定でp値を計算
- 結論：p < 0.05なら「統計的に有意な差がある」


---


### 3.3 機械学習の役割
#### 予測モデルの構築
- 過去のデータから未来を予測
- 例：患者の予後予測、疾患の診断
#### パターンの発見
- データから隠れたパターンを抽出
- 例：遺伝子発現データのクラスタリング
#### 自動化
- 人間が行っていた作業を自動化


---


### 3.4 統計学 vs 機械学習




<div align="center">

| 項目     | 統計学                   | 機械学習                 |
| :------- | :----------------------- | :----------------------- |
| 目的     | 仮説検定、因果推論       | 予測、パターン認識       |
| 解釈性   | 高い（係数の意味が明確） | 低い（ブラックボックス） |
| データ量 | 少量でもOK               | 大量のデータが必要       |
| 例       | t検定、回帰分析          | ニューラルネットワーク等 |

どちらか一方ではなく、**両方を使い分ける**ことが重要

</div>


---


### 📊 論文の図を読んでみよう ① 総放射線量の変化

![](images/DLR_RadiationDose/Total_Dose.png)

- **a, b**: DLR導入前（IR法）の男女別分布
- **c, d**: DLR導入後（DLR法）の男女別分布
- 縦軸：実効線量 [mSv] 横軸：年齢
- 点群が大幅に**下方移動** → 線量が全体的に減少


---


### 📊 論文の図を読んでみよう ② 臓器別がんリスク（LAR）

![](images/DLR_RadiationDose/Organ_Dose.png)

- 各臓器の **LAR**（生涯がん発症リスク / 100,000人）を比較
- 薄色：IR法　濃色：DLR法
- 肺・大腸でリスク低下が顕著
- **女性の方がリスクが高い傾向**


---


### 📊 論文の図を読んでみよう ③ 年齢別LARの変化量

<div align="center">

![height:400](images/DLR_RadiationDose/LAR_DLR.png)
</div>

- **a（青）**: 男性　**b（赤）**: 女性
- 縦軸：DLR導入によるLAR変化量 （マイナス = リスク減少）
- **若年者, 女性ほど効果が大きい**



---


## 4. 医学データサイエンス研究の例

「新型コロナウイルスの空気伝播に対するマスクの防御効果」  
(Effectiveness of Face Masks in Preventing Airborne Transmission of SARS-CoV-2)  
-> マスクは感染予防効果に重要




新型コロナウイルス感染対策による聴き取り阻害を定量化する試み  
-> 遮蔽板とマスクを併用した場合は聞き取り阻害の原因になりうる


---


それぞれの論文は**矛盾している**わけではありません。それぞれの論文が**「誰を対象に」「何を目的として」「どのような条件で」**研究を行ったかが異なるからです。




<div align="center">


|          | 論文① (感染リスク) | 論文② (聴き取り環境) |
| :------- | :----------------- | :------------------- |
| **対象** | 一般集団           | 聴力疎通環境         |
| **目的** | 感染拡大防止       | 聴き取りへの影響     |
| **結論** | 感染予防に有効     | 併用は阻害しうる     |

</div>


---


論文を読み際には、以下の点を必ず確認しましょう：

1. **対象（Population）**: どんな集団・環境を研究しているか？
2. **目的（Objective/Intervention）**: 何を調べているか？
3. **結論（Conclusion）**: その条件のもとで何が言えるか？（限界は？）


---




## 📄 6. Pandoc — MarkdownをWordに変換

### Pandocとは？

- **Markdown** → Word (.docx) / PDF / HTML などへ変換
- 文献引用（BibTeX）も自動処理
- コマンドライン1行で変換完了
- 無料・オープンソース


---


### Pandocのインストール

**Mac:**
```bash
brew install pandoc
# または https://pandoc.org/installing.html から .pkg をダウンロード
```

**Windows:**
> https://pandoc.org/installing.html → `.msi` インストーラーをダウンロード


---


### プラグインの追加：Better BibTeX for Zotero

**Pandocでの引用を簡単・確実にする必須プラグイン**




1. https://retorque.re/zotero-better-bibtex/installation/ にアクセス
2. 最新の `.xpi` ファイルをダウンロード
3. Zotero → **Tools** → **Add-ons** → ⚙️ → **Install Add-on From File...** で選択
4. Zoteroを再起動

**設定のポイント：**
- **Citation Key**: `[auth][year]` などの形式で固定のキーを自動生成
- **Keep updated**: 論文を追加すると `references.bib` を自動更新


---


### Pandocの動作確認

```bash
pandoc --version
```

**基本変換コマンド：**

```bash
# markdown → Word
pandoc input.md -o output.docx

# 引用文献付き
pandoc input.md \
  --bibliography references.bib \
  --citeproc \
  -o output.docx
```


---


### Markdownの基本記法

```markdown
# 見出し1　## 見出し2

**太字** と *イタリック*

- 箇条書き1

| 列A | 列B |
| --- | --- |
| 値1 | 値2 |

引用は [@kobayashi2025] のように書きます。
```


---


## 📝 7. ハンズオン：論文の元データを書く

### 課題の概要

以下のテンプレートを使って、自分でIMRAD構造のMarkdownファイルを作成し、  
Pandocで `.docx` に変換してください。




**使うもの**
- テキストエディタ（VS Code 推奨）
- Pandoc（インストール済み）
- Zotero + BibTeX（`references.bib`）


---


### テンプレート（`my_paper.md`）

```markdown

---

title: "論文タイトル"
author: "氏名"
date: "2026年"
bibliography: references.bib

---


# Introduction

先行研究として [@kobayashi2025] が報告した...

# Methods

本研究では...

# Results

結果として...

# Discussion

考察...

# References
```


---


### 変換コマンド

```bash
pandoc my_paper.md \
  --bibliography references.bib \
  --citeproc \
  -o my_paper.docx
```




✅ `my_paper.docx` が生成されれば完了！


---


### ✏️ 課題内容

今日学んだDLR論文 (Kobayashi et al., 2025) のアブストラクトをもとに、  
**自分の言葉でIMRAD構造のMarkdown**を書いてみましょう。




1. **Results**: 何がわかったか（数値を含めて）← 最初に書く
2. **Methods**: どのように調査したか（2〜3文）
3. **Introduction**: なぜこの研究が必要だったか（1〜2文）
4. **Discussion**: この結果の意義と限界（1〜2文）




📌 引用は `[@kobayashi2025]` のように入れてください。


---




## 📌 第2コマのまとめ

| テーマ         | 学んだこと                                    |
| :------------- | :-------------------------------------------- |
| 論文執筆の順番 | Results → Methods → Introduction → Discussion |
| 統計・MLの役割 | Resultsを書くために必要                       |
| DLR論文の結果  | 図・表で読むResultsの実践                     |
| Pandoc         | Markdown → Word 変換                          |
| ハンズオン     | 自分でIMRAD構造の文書を作成                   |




**次回**: データの記述統計と可視化