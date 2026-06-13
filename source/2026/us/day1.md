# カンファレンス1日目

* タイムテーブル：<https://us.pycon.org/2026/schedule/talks/#May15>

## WelcomeとPSF Welcome

カンファレンスのオープニングはPyCon US 2026のChairであるElaine Wong氏によるWelcomeメッセージです。
最初に関係者、スポンサーなどへの感謝が述べられました。

```{figure} images/welcome.jpg
:width: 400

Elaine Wong氏によるWelcomeメッセージ
```

最初の方で「まわりの会ったことない人と会話してみましょう」というアイスブレイクがありました。
筆者は、前に座っていたMark Shannon氏とあいさつをしました。
Mark氏はPyCon JP 2022のキーノート[^marks-keynote]だった方で「私が日本から来たこと、日本でのキーノートをしたこと、日本にぜひ来てください」といった話をしました（2022のキーノートはリモート発表でした）。

[^marks-keynote]: [PyCon JP 2022: Day 1 OP & Keynote by Mark Shanonn - YouTube](https://www.youtube.com/watch?v=e_EbzeBf06g)

ボランティアの募集、会場の説明、PyLadiesの紹介、スプリントなどのイベントの説明がありました。
その中でPyCon US 2026での初めての取り組みとして以下が紹介されました。

* AIトラック（カンファレンス1日目）
* セキュリティトラック（カンファレンス2日目）
* Pablo氏によるスペイン語のキーノート（カンファレンス2日目の朝、同時通訳付き）

PyCon USで英語以外のキーノートを行うというのは、挑戦的だと思いました。
なお、Pablo氏は英語でも早口なので、母国語のスペイン語だとどんなスピードになってしまうんだろう。通訳は間に合うんだろうか？という感想を持ちました。

Welcomeの後はトップレベルのスポンサーによるショートトークがありました。
Nidia、Bloomberg、MetaがそれぞれCUDA、Memray、Pyrefly、Lazy imports、Free-threded Pythonなど、Pythonエコシステムへの貢献について紹介していました。

続いてDeb Nicholson氏によるPSF Welcomeです。Deb氏はPSFの[Executive Director](https://www.python.org/psf/records/staff/)です。
PSF(Python Software Foundation)はPythonの権利を管理する団体です。

```{figure} images/deb-opening.jpg
:width: 300

Deb Nicholson氏
```

Deb氏からは「魚を与えるだけでなく、釣り方を教えよ」ということわざを引用し、お互いに教えあうことがPythonコミュニティの強みである、と語られました。

## PEP 750 - T-strings: safer and smarter string processing

* トーク概要：<https://us.pycon.org/2026/schedule/presentation/70/>
* スピーカー：[Vinícius Gubiani Ferreira](https://us.pycon.org/2026/speaker/profile/73/)
* スライド：<https://github.com/vinigfer/pyconus_2026_slides/tree/main>

本トークではブラジルからやってきたVinícius氏から、Python 3.14で導入されたt-stringsについて紹介されました。
t-stringsについては以下の公式ドキュメントやgihyo.jpの記事を参照してください。

* [PEP 750: テンプレート文字列リテラル](https://docs.python.org/ja/3.14/whatsnew/3.14.html#whatsnew314-template-string-literals)
* [t-string：テンプレート文字列リテラルの紹介 | gihyo.jp](https://gihyo.jp/article/2025/11/monthly-python-2511)

t-stringsでは文字列ではなくTemplateオブジェクトが生成されること、`strings`と`interpolation`といった基本的な構造が説明されました。

トークの後半では具体的なユースケースとしてセキュリティ対策（XSSやSQLインジェクション等）、Jinjaなどの代わりとなるテンプレート、ログ出力処理についてあげられていました。
ログ出力については、1つのテンプレート文字列から人が読みやすいテキスト形式のログと、コンピューターが読みやすいJSON形式のログをそれぞれ出力するという例を、サンプルコードを交えて解説していました。

ログ出力の出し分けは、なかなか実用的だなと感じました。
今後どこかで使用するかもしれません。

## What's so hard about writing a type checker? A tour of ty

* トーク概要：<https://us.pycon.org/2026/schedule/presentation/143/>
* スピーカー：[Carl Meyer](https://us.pycon.org/2026/speaker/profile/151/)

本トークではAstral社のエンジニアであるCarl Meyer氏から、Pythonの静的型チェッカーtyの内部構造について解説がされました。
tyは高速な方チェッカーであり、高速に動作するためにアーキテクチャーやさまざまな工夫について語られました。

* ty公式ドキュメント：<https://docs.astral.sh/ty/>

```{figure} images/carl-meyer.jpg
:width: 400

Carl Meyer氏
```

tyの設計上の目標は高速に動作することであり、そのために**laziness（怠惰）**の原則に基づいて開発されています。
ここでいうlazinessは「不要なことはせずに、必要なときに行う（遅延処理する）」ということです。

tyではコードの依存関係グラフを持っています。
そしてtyの実行時に変更された箇所を検知し、その箇所に依存しているコードのみを型チェックの対象とします。

また内部ではRustの[Salsa](https://github.com/salsa-rs/salsa)を使用して自動的に情報のキャッシュが行われ、同じ入力を与えた場合にはSalssaは再計算を行わずにキャッシュから結果を返します。
また、依存グラフもSalsa内にあるため、必要な場合にはキャッシュを自動的に無効化します。

tyを高速に動作させるためにはただ単にrustを使っているというだけでなく、いろいろと内部のアーキテクチャでも工夫をしているということが感じられるトークでした。
Astral社のツールは[Ruff](https://docs.astral.sh/ruff/)、[uv](https://docs.astral.sh/uv/)も高速に動作しますが、それぞれにさまざまな工夫がされていると感じるトークでした。

## ランチ

ランチはビュッフェ形式です。
生野菜のサラダ、野菜のロースト、パスタ、チキン、デザートなどがメニューとして用意されています。
アメリカ滞在中はなかなか生野菜を食べる機会がないので、とてもありがたいです。

```{figure} images/lunch-day1.jpg
:width: 400

ランチはビュッフェスタイル
```

ランチのあとは企業ブースを回りました。
Metaのブースではコーヒーを提供していたので、その列に並びました。
列で待っている間にクイズに答えると、おまけでクッキーがもらえます。
クッキーには静的型チェッカー[Pyrefly](https://pyrefly.org/)ロゴが印刷されてました。

```{figure} images/meta-coffee.jpg
:width: 300

Metaブースのコーヒー
```

```{figure} images/pyrefly-cookie.jpg
:width: 300

Pyreflyクッキー
```

## The Bakery: How PEP810 sped up my bread operations business

* トーク概要：<https://us.pycon.org/2026/schedule/presentation/30/>
* スピーカー：[Jacob Coffee](https://us.pycon.org/2026/speaker/profile/31/)
* スライド：<https://fosdem.org/2026/events/attachments/HAAABD-python-pep810/slides/266934/talk_-_co_chhdrub.pdf>

Python 3.15で導入される`lazy import`を使用して、サンプルのCLIプログラムが速くなることを確認し、どのように`lazy import`を導入するとよいかという話がされました。
lazy importについては以下の公式ドキュメントを確認してください。

* [PEP 810: Explicit lazy imports](https://docs.python.org/ja/3.15/whatsnew/3.15.html#whatsnew315-lazy-imports)

```{figure} images/jacob.jpg
:width: 400

Jacob Coffee氏
```

サンプルプログラムの`breadctl`というCLIを使用してトークが進められます。
コードは以下のGitHubにあります。

* [JacobCoffee/breadctl: Bread Operations Inc.](https://github.com/JacobCoffee/breadctl)

まず問題点とPythonの起動が遅いということが述べられました。
`--help`オプションを指定してヘルプを表示するだけで234ミリ秒がかかっています。
これは起動時に全てのモジュールをimportしているために発生しています。

PEP 810で提案されたlazy importはPython 3.15から追加されます。
以下の様に書くとそのモジュールにアクセスしたときに、初めてimportsれます。

```{code-block} python
:caption: normal.py

# 起動時にすべてロードされる
from breadctl import bake
from breadctl import deliver
from breadctl import inventory

# それぞれ以下のモジュールが中でimportされている
# bake: collections、itertools
# deliver: httpx
# inventory: sqlite3
```

```{code-block} python
:caption: lazy.py

# アクセス時にロードされる
lazy import breadctl.bake as bake
lazy import breadctl.deliver as deliver
lazy import breadctl.inventory as inventory
```

`lazy import`はどのように動作しているのでしょうか。
まず解析フェーズではLazyModuleプロクシーを作成します。
この段階ではモジュールは読み込まれていません。

```{code-block} python
:caption: httpxをlazy importする

lazy import httpx
```

そして、実際にhttpxモジュールを使用するときに、はじめてモジュールが読み込まれます。

```{code-block} python
:caption: httpxが読み込まれる

response = httpx.get(url)  # httpxがここで読み込まれる
```

最初の`--help`オプションのlazy import版を実行すると、234ミリ秒から164ミリ秒と70%の起動時間になりました。

lazy importの活用する場所としてテスト実行の高速化、サーバーレスでの起動、CLIアプリケーションへの活用などがあげられました。

大量のテストコードがある場合には確かに有効そうです。
Python 3.15に移行したあとにlazy importを試してみたいと思いました。

## Free-threaded Python: past, present and future

* トーク概要：<https://us.pycon.org/2026/schedule/presentation/63/>
* スピーカー：[Thomas Wouters](https://us.pycon.org/2026/speaker/profile/67/)
* スライド：<https://fosdem.org/2026/events/attachments/HAAABD-python-pep810/slides/266934/talk_-_co_chhdrub.pdf>

本トークではPythonからGILを取り除くフリースレッドの状況について共有されました。
スピーカーのThomas Wouters氏は3.12と3.13のリリースマネージャーであり、Python Steering CouncilのメンバーでもあるというPython開発の中心人物の一人です。
Thomas氏はMetaに勤務しており、業務としてフリースレッドに取り組んでいるそうです。

```{figure} images/jacob.jpg
:width: 400

Thomas Wouters氏
```

Pythonで並行処理を行う方法としてマルチプロセス、サブインタープリター、asyncioなどがあるが、フリースレッドにもメリットがあるということが語られました。
マルチプロセスは各プロセスが独立して動きますが、プロセス起動のオーバーヘッドや、プロセス間でデータを受け渡すときにコストがかかります。
サブインタープリターでは独立したインタープリターが独立するためGILの制限を受けませんが、別のインタープリターのためデータの受け渡しコストがかかります。
asyncioはスレッドやプロセスを作成するオーバーヘッドがなく軽量ですが、シングルスレッドで動作しているため、CPU負荷が高い処理は同時に実行できません。

フリースレッドは複数のスレッドでPythonが同時に動作し、メモリも直接共有するためデータ受け渡しのコストは低いです。
ただし、フリースレッドに対応していないモジュールを使用すると使用できないという問題があります。が存在していることと、スレッド

また、Pythonがフリースレッドに対応するまでの長い道のりが紹介されました。
2013年のPyParallel、2015年のGilectomyを経て、Sam Gross氏が2021年にPython 3.9からGILを取り除いたPoC（概念実証）を作成しました。
この経験を元にPEP 703でCPythonでGILをオプションにする提案を行い、Python 3.13からフリースレッドが利用できるようになりました。

* [PyParallel](https://github.com/pyparallel/pyparallel)(2013)
* [Gilectomy](https://github.com/larryhastings/gilectomy)(2015) - Larry Hastings
* [NoGIL Python 3.9](https://github.com/colesbury/nogil)(2021) - Sam Gross
* [PEP 703 – Making the Global Interpreter Lock Optional in CPython](https://peps.python.org/pep-0703/)(2023) - Sam Gross
* フリースレッドが[Python 3.13で実験的機能](https://docs.python.org/ja/3.14/whatsnew/3.13.html#whatsnew313-free-threaded-cpython)、[Python 3.14で正式サポート](https://docs.python.org/ja/3.14/whatsnew/3.14.html#whatsnew314-free-threaded-cpython)

なお、Sam Gross氏がNoGILについて発表しているEuroPython 2022のキーノートを筆者が以前レポートしています。
4年前の発表から現在のPythonまで地続きになっていることが感じられます。

* [#02　Faster CPythonやGILの除去によるPythonの高速化 ―EuroPython Day 2、Day 3セッションレポート | gihyo.jp](https://gihyo.jp/article/2022/09/europython2022-02#ghsKDvixIi)

## ライトニングトーク

カンファレンス1日目の終わりはライトニングトークです。
以下の様なトークがありました。

* PyCon USに来ていろんな人とセルフィーを撮って友達を作るという話。https://ekohilas.github.io/linkedinsnap/ というWebアプリも紹介
* 求職活動でAIを使って嘘の情報を出す人が増えている話。PyCon USに参加しているときに写真などの証拠を残そう
* PyCon USで字幕を付けている人のトーク。[特殊なキーボード](https://ja.wikipedia.org/wiki/%E3%82%B9%E3%83%86%E3%83%8E%E3%82%BF%E3%82%A4%E3%83%97)を使用して高速に入力しているとのこと
* CUMBUCA DEV: ブラジルのマイノリティの開発コミュニティ。ポルトガル語のgithubの本を出したり。CUMBUCAはBOWLのこと
* たくさんのAIエージェントだと結局混乱するって話
* ハロウィンの動く装飾をRaspberry Pi ZeroとPythonで作成している話(参考：[Aspiring Roboticist's Profile | Hackaday.io](https://hackaday.io/ViennaMike))
* 韓国のSeongsoo Cho氏が、PyCon Koreaのスプリントの経験から自身がはじめた、オープンソースのメンターを育てる活動

```{figure} images/day1-lt1.jpg
:width: 400

特殊なキーボード（写真右の字幕は他の字幕スタッフが入力している）
```

```{figure} images/day1-lt2.jpg
:width: 400

Seongsoo Cho氏
```

## パーティーへ

カンファレンス終了後は企業主催のパーティーに参加しました。
カンファレンス中はいくつかのスポンサー企業が主催したパーティーが開かれています。
私は[Capital One](https://www.capitalone.com/)のパーティーに参加しました。
知らない人に声をかけられたと思ったら、アジアのどこかのPyConで一緒に飲んだことがある方でした（髪が短くなっていてわからなかった）。

```{figure} images/day1-party.jpg
:width: 400

パーティーの様子
```

1次会はあんまりいいビールがなかったので、アジアメンバーを中心に声をかけて[ISM Brewing](https://ism.beer/)に飲みに行きました。
日本、韓国、香港、アメリカと多国籍な感じで楽しくビールを飲みました（いつものこと）。

```{figure} images/day1-party2.jpg
:width: 400

パーティーの様子
```
