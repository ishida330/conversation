---

copyright:
  years: 2015, 2018
lastupdated: "2018-02-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# サポートされる言語
{{site.data.keyword.conversationshort}} サービスでサポートされる言語をリストします。 サービスの各機能は、どの言語についても多かれ少なかれサポートされます。
{: shortdesc}

以下の表では、言語と機能のサポートのレベルを次のコードで示しています。

- **GA** - この機能はこの言語で一般提供されていて、サポートされています。 一般提供された後も、機能の更新は継続される可能性があることに注意してください。
- **ベータ** - この機能はベータ版でのみサポートされています。この言語での一般提供に向けてまだテスト中です。
- **空白** - コードがない場合は、この言語では機能を利用できないことを意味しています。

|                  | **[インテント](intents.html)**、 **[エンティティー](entities.html)**、**[ダイアログ](dialog-build.html)の定義** | **[絶対スコアリングと「不適当としてマークを付ける (Mark as irrelevant)」](intents.html#mark-irrelevant)** | **システム・エンティティー([数](system-entities.html#sys-number)、 [通貨](system-entities.html#sys-currency)、 [パーセンテージ](system-entities.html#sys-percentage)、 [日付、時刻](system-entities.html#sys-datetime))** | **[エンティティーのファジー・マッチング](entities.html#fuzzy-matching)** |
|:---|:---:|:---:|:---:|:---:|
| **英語 (en)**                   | GA | GA | GA </br> ベータ ([場所](system-entities.html#sys-location)、 [人](system-entities.html#sys-person)) | ベータ (ステミング、つづりの誤り、部分一致) |
| **アラビア語 (ar)**                    | GA | ベータ | ベータ | ベータ (つづりの誤りのみ) |
| **中国語 (簡体字) (zh-cn)**   | ベータ | ベータ | ベータ |  |
| **中国語 (繁体字) (zh-tw)**  | ベータ | ベータ |  |  |
| **チェコ語 (cs)**                     | ベータ | ベータ | ベータ | ベータ (つづりの誤りのみ) |
| **オランダ語 (nl)**                     | ベータ | ベータ | ベータ |  |
| **フランス語 (fr)**                    | GA | GA | GA | ベータ (つづりの誤りのみ) |
| **ドイツ語 (de)**                    | GA | GA | GA | ベータ (つづりの誤りのみ) |
| **イタリア語 (it)**                   | GA | GA | GA | ベータ (つづりの誤りのみ) |
| **日本語 (ja)**                  | GA | GA | GA | ベータ (つづりの誤りのみ) |
| **韓国語 (ko)**                    | GA | GA | GA | ベータ (つづりの誤りのみ) |
| **ポルトガル語 (ブラジル) (pt-br)** | GA | GA | GA | ベータ (つづりの誤りのみ) |
| **スペイン語 (es)**                   | GA | GA | GA | ベータ (つづりの誤りのみ) ||

**注意:** {{site.data.keyword.conversationshort}} サービスは上記のように複数の言語をサポートしますが、ツールのインターフェース自体 (説明、ラベルなど) は英語です。 サポートされるすべての言語は、英語のインターフェースを通じて入力してトレーニングできます。

**GB18030 準拠**: GB18030 は、中国語市場で使用される拡張コード・ページを指定した中国語規格です。中華人民共和国国家情報技術標準化技術委員会 (China National Information Technology Standardization Technical Committee) により、2001 年 9 月 1 日以降に中国語市場にリリースされるソフトウェア・アプリケーションは GB18030 対応であることが義務付けられていることから、このコード・ページ規格はソフトウェア業界にとって重要です。
{{site.data.keyword.conversationshort}} サービスはこのエンコードをサポートしており、GB18030 に準拠していることが認定されています。

## ワークスペースの言語の変更

ワークスペースを作成した後にその言語を変更することはできません。 ワークスペースのサポート言語を変更する必要がある場合は、ユーザーがワークスペースをダウンロードする必要があります。 次に、生成された JSON ファイルをテキスト・エディターで編集して、`language` という JSON プロパティーを検索します。

`language` プロパティーは、ワークスペースの元の言語に設定する必要があります。例えば、英語は `en` にする必要があります。 このプロパティーの値を必要な言語に変更します (フランス語は `fr`、ドイツ語は`de` など)。 JSON ファイルに変更を保存し、変更したファイルを {{site.data.keyword.conversationshort}} サービス・インスタンスにインポートします。

## 双方向言語の構成
{: #configuring-bi-directional}

アラビア語などの双方向言語の場合は、それに合わせてワークスペースの設定を変更することができます。 ワークスペースのタブから*「アクション」*ドロップダウン・メニューを選択して、**「双方向の設定 (Bidi preferences)」**を選択します (このオプションは、双方向言語が設定されたワークスペースでのみ利用できます)。

![双方向の設定 (Bidi preferences)](images/bidi_prefs.png)

ワークスペースについて以下のオプションから選択します。

- **GUI の方向 (GUI Direction)**: グラフィカル・ユーザー・インターフェースのボタンやメニューなどの要素のレイアウトの方向を指定します。 `「LTR」` (左から右) または `RTL` (右から左) を選択します。 指定しない場合、ツールは Web ブラウザーの GUI の方向の設定に従います。
- **テキストの方向 (Text Direction)**: 入力されたテキストの方向を指定します。 `「LTR」` (左から右) または `「RTL」` (右から左) を選択するか、システムの設定に基づいてテキストの方向を自動的に選択する`「自動 (Auto)」`を選択します。 `「なし (None)」`オプションは、左から右にテキストを表示します。
- **数値のシェーピング (Numeric Shaping)**: 通常の数字を表示する場合に使用する数値形式を指定します。 `「公称 (Nominal)」`、`「アラビア - インド (Arabic-Indic)」`、または`「アラビア - ヨーロッパ (Arabic-European)」`から選択します。 `「なし (None)」`オプションは、西洋式の数字を表示します。
- **カレンダーのタイプ (Calendar Type)**: ワークスペース UI で日付のフィルタリングを選択する方法を指定します。 `「イスラム暦 (一般) (Islamic-Civil)」`、`「イスラム暦 (表計算) (Islamic-Tabular)」`、`「イスラム暦 (ウンム・アルクラー) (Islamic-Umm al-Qura)」`、または `「グレゴリオ (Gregorian)」`を選択します。 **注意**: この設定は、「Try it out」パネルには適用されません。

![双方向オプション](images/bidi_opts.png)

選択を完了したら、**「更新」**をクリックして保存し、ワークスペースのタブに戻ります。

## アクセント付き文字の処理
{: #working-with-accents}

会話の設定では、ユーザーは {{site.data.keyword.conversationshort}} サービスとの対話でアクセントを使用したり使用しなかったりします。 このため、インテント検出とエンティティー認識で、アクセントありとアクセントなしの両方のバージョンの単語が同じものとして処理されることがあります。

ただし、スペイン語などの一部の言語では、アクセントによってエンティティーの意味が変わることがあります。 このため、エンティティーの検出では、元のエンティティーに暗黙的にアクセントがある場合でも、サービスは同じエンティティーのアクセントなしのバージョンに一致させることができます。ただし、信頼度スコアは少し低くなります。

例えば、アクセントありの「barrió」という単語は動詞「barrer」(拭く) の過去形に相当しますが、サービスは「barrio」(近所) という単語にも一致させることができます。ただし、信頼度は少し低くなります。

システムは、完全一致のエンティティーでは、最も高い信頼度スコアを与えます。 例えば、`barrió` がトレーニング・セットに含まれていれば `barrio` は検出されません。また、`barrio` がトレーニング・セットに含まれていれば `barrió` は検出されません。

システムのトレーニングには、正しい文字とアクセントを使用する必要があります。 例えば、`barrió` を応答として想定している場合は、`barrió` をトレーニング・セットに入力してください。

アクセント・マーク以外にも、スペイン語の文字 `ñ` と文字 `n` による「uña」と「una」のような単語の使い方にも、同じことが当てはまります。 この場合、文字 `ñ` は単にアクセントが付いた `n` ではなく、スペイン語特有の別の文字です。

お客様が適切なアクセントを使用しなかったり、単語のつづりを誤ったりする (`ñ` の代わりに `n` を使用するなど) と考えられる場合は、ファジー・マッチングを有効にしたり、トレーニングのサンプルに明示的に含めたりすることができます。
