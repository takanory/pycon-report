# PyCon Korea 2026

鈴木たかのり（[@takanory](https://x.com/takanory)）です。
2026年8月に韓国のソウルで開催された、プログラミング言語Pythonのカンファレンス「PyCon Korea 2026」に参加してきたので、その様子をレポートします。

## PyCon Korea 2026とは

PyCon Korea 2026のイベント概要は以下の通りです。

|項目|内容|
|--|--|
|URL|<https://2026.pycon.kr/>|
|日程| カンファレンス: 2026年8月15日（土）、16日（日）|
| | チュートリアル、スプリント: 2026年8月17日（月）|
|場所| ソウル市 |
|会場| Dongguk University |
|参加費|個人：60,000 KRW（約7,000円）、Tシャツ 15,000 KRW |
|主催| Python Korea |

公式サイトは以下の様なデザインで、ドット絵で描かれた遊園地でレトロ感があります。
「**Make it hap.py**」という言葉が今年のテーマのようです。

```{figure} images/pyconkorea2026.png
:width: 600

PyCon Korea 2026公式サイト
```

筆者が前回PyCon Koreaに参加したのは2023年でした。2023年の様子は以下のレポートを参照してください。

* [PyCon Korea 2023 カンファレンスレポート | gihyo.jp](https://gihyo.jp/article/2023/08/pycon-korea-2023)

## 韓国への道のり

カンファレンス前日に韓国入りしました。初めて金浦空港を利用しましたが、到着のみなのであまり記憶には残っていません。
[e-Arrival Card](https://www.e-arrivalcard.go.kr/)でWebで事前に申告を済ませておくと、入国審査もスムーズでした。

```{figure} images/welcome-seoul.jpg
:width: 600

Welcome Seoulのサイン
```

## カンファレンス会場へ

カンファレンス会場からそれほど遠くないところにホテルをとったので歩いて会場に向かいました。
Dongguk Universityという大学がカンファレンス会場です。
大学は斜面に沿って複数の校舎が建っているため、構造が複雑でした。そのため、複数の建物を横移動したり、あるビルの9階から外に出ると普通に地上だったりして、そういうところも含めて大学っぽいなと感じました。

```{figure} images/university.jpg
:width: 600

Dongguk Universityの入り口
```

## Keynote: Deb Nicholson

* トーク概要：[Let's Build the Future of Python Together!](https://2026.pycon.kr/presentations/4406c268-1f99-49d5-a932-eeb2637342fb#Lets-Build-the-Future-of-Python-Together)
* 動画：<https://www.youtube.com/watch?v=zyDGfvFic78>

最初のキーノートはDeb Nicholson氏によるものです。
Deb氏はPython Software Foundation（PSF：Pythonソフトウェア財団）[^psf]のExecutive Directorであり、今回はPyCon Koreaのキーノートのためにアメリカから来ました。

[^psf]: Pythonの知的財産権と商標の管理や、PyPIの運営をする財団 <https://www.python.org/psf-landing/>

```{figure} images/deb.jpg
:width: 600

Deb Nicholson氏
```

なおトークには基本的に[Cuckoo](https://www.cuckoo.so/ja)による翻訳が付いており、スライド横のQRコードを読み込むと選択した言語でトークの翻訳を見ることができて便利でした。
英語のキーノートは韓国語の他に日本語と中国語の翻訳が提供されていました。
以下の様に手元のスマートフォンで日本語で読めるのでありがたいです。

```{figure} images/translate.png
:width: 300

Cuckooによる翻訳
```

まずはPSFそのものの紹介があり、PSFが存在することによってPythonは特定のベンダーに依存しない、中立的な存在でいられることが語られていました。
他に、Pythonのパッケージリポジトリである[PyPI](https://pypi.org/)を運営していること、PyPIのトラフィックは2026年は**2エクサバイト**になりそうということが語られました。
単位が大きすぎてどれくらいなのかちょっとピンと来ません。

Deb氏からPythonは「プログラミング言語のカピバラだ」という発言がありました（冒頭の写真）。
その意味するところは、カピバラはさまざまな動物と仲良く過ごすことができる、Pythonもさまざまなプログラミング言語と連携できるということだそうです。
PythonとC言語、Java、Go、JavaScript、Fortran、Haskellなど、他言語と連携するためのさまざまなツールが紹介されました。
また、システム同士をつなぐ役割もPythonが得意とするところです。

また、Deb氏が友人に助けを求めた話もありました。
PSFが米国政府の助成金を受けるために、どのような書類を用意するか、助成金の額をいくらにするかなどを、この助成金を受けている友人に相談したそうです。
その結果助成金の申請が無事にできたとのことで、同様にプログラミングの学習や困難なプロジェクトに対しても、1人で悩まずに友人に助けを求めましょうと語られていました。

最後に参加者に「コミュニティにもっと参加してほしい」とアクションプランがいくつか提案されました。

* Pythonを使っている企業であれば[PSFのスポンサー](https://www.python.org/psf/sponsors/)となることを検討してほしい。韓国企業のPSFスポンサーもいる
* ローカルやグローバルのイベントに参加してほしい。ここでは[Python Asia Organization](https://pythonasia.org/)についても紹介がありました
* [PSFのメンバーシップ](https://www.python.org/psf/membership/)への参加と、理事やパッケージングカウンシルへの投票の参加
* ミートアップなどで周囲へのアピールと共に学ぶこと

Pythonは（ヘビではなく）カピバラだ、という説明が個人的に面白かったです。
PSF、Python、コミュニティ、そして次のアクションへとつなぐキーノートでした。

## Python Asia Organizationブース、ランチ

日本からの参加者があまりいないため、筆者はPython Asia Organizationの理事である寺田さんからテーブルクロスを受け取って現地に持っていきました。
PyCon Koreaではコミュニティブースが多数あり、その1つとしてPython Asia Organizationもブースを提供していました。

いつものように日本から持っていったお菓子を参加者に配りつつ、Python Asia Organizationのアピールをしました。

```{figure} images/pythonasia.jpg
:width: 600

ブースの様子
```

その後ランチは大学の食堂です。全員同じメニューが提供されていました。
キムチが付いてくるのが韓国の学食だなーという感じです。

```{figure} images/lunch.jpg
:width: 600

ランチ
```

## Let's Build a Python Language Support Team

* トーク概要：[Let’s Build a Python Language Support Team](https://2026.pycon.kr/presentations/cbe161d5-d8ea-4bc0-80b8-aadd75c7c971#Lets-Build-a-Python-Language-Support-Team)
* スピーカー：Donghee Na
* 動画：<https://www.youtube.com/watch?v=5cZkGfiNZwk>

このセッションでは、Pythonのコアデベロッパーであり、2025、2026年のPython Steering Councilメンバー[^council]であるDonghee Na氏から、会社の中にPythonの言語サポートチームを構築した事例について紹介がありました。

[^council]: [PEP 8107 – 2026 Term Steering Council election | peps.python.org](https://peps.python.org/pep-8107/)

```{figure} images/donghee.jpg
:width: 600

Donghee Na氏
```

会社の規模が大きくなる中で、バージョンの更新、セキュリティ対策、デバッグ、サプライチェーン攻撃への対応など、システムを運用する上での課題が増えてきます。
これらを各チームが対応するのではなく、Python言語サポートチームを立ち上げ標準化を行い、運用コストを下げるという狙いとのことです。
他社事例としてGoogle、Microsoft、Meta、LinkedIn、LINEヤフーに言語サポートチームが存在することが述べられました。

Donghee氏が所属する[Karrot](https://www.karrotmarket.com/)では当初はボランティアベースで言語サポートチームの活動を開始しました。
トラブルシューティング、セキュリティ対応、ナレッジの共有、外部コミュニティ貢献などの活動を継続的に行い、その後会社として正式な部門となったそうです。
社内で毎月ミーティングを実施したり、技術に関するディスカッションを行ったりしているそうです。

社内でPython言語のサポートチームを立ち上げるという発想はなかったので、事例と共に紹介されており、ある程度の規模の企業には参考になるのではと思いました。

## Growth together with PyLadies Seoul

* トーク概要：[Growth together with PyLadies Seoul](https://2026.pycon.kr/presentations/077c5c22-fc2d-482f-8855-ff5cc0b74957#Growth-together-with-PyLadies-Seoul)
* スピーカー：Luna
* 動画：<https://www.youtube.com/watch?v=4A8QtEaV5do>

このセッションでは[PyLadies Seoul](https://pyladies.kr/en/)の立ち上げメンバーであるLuna氏から、PyLadies Seoulを再始動させて成長してきたプロセス、コミュニティ運営から得られた学びが語られました。

```{figure} images/luna.jpg
:width: 600

Luna氏
```

技術分野で女性の参加者が少ない、ロールモデルが見つけにくい、[PyCon Korea 2023](https://2023.pycon.kr/)で女性スピーカーだと女性スピーカーが3名だったといったことに危機感を感じたそうです。
2023年末から再始動に向けて準備を進めていたそうです。
その中で、東京で開催された[PyCon APAC 2023](https://2023-apac.pycon.jp/)に参加し、そのイベントで[PyLadies Tokyo](https://tokyo.pyladies.com/)のメンバーと出会い、「毎月開催する」という指針を得たそうです。
そうして2024年3月から再始動し、毎月開始し、ここまで42回のイベントを開催しているそうです（すごい）。

Luna氏は国内の活動だけでなく、PyCon USへの参加、海外のPyLadiesチャプター（Tokyo、Taiwanなど）との交流も積極的に行っています。
筆者もPyCon USでLuna氏とも会っており、精力的に活動しているなと感じています。

最後のメッセージとして「完全に準備が整うタイミングは永久に来ない」と延べ、完璧を待たずに今できる小さな一歩（ライトニングトーク、勉強会への参加、運営の手伝いなど）からコミュニティに関わり、助け合うことの大切さを呼びかけていました。

仲間と共にコミュニティを再始動させ、運営させている本人からの経験に基づくトークでした。
PyLadies Seoulが今後も継続的に発展するとよいなと思います。

## Lightning Talks

* 動画：<https://www.youtube.com/watch?v=2zNPbMJLyTM>

ライトニングトークからは3本紹介します。
Kir氏はPyCon Taiwanの運営メンバーをやっており、プロポーザルのレビューをAIと人間で行い、その結果によって採択を行ったという内容です。
AIのみでもなく人間のみでもなく、その双方が「よい」と判断したプロポーザルを採択するというのは、なかなか面白いアプローチだと思いました。

```{figure} images/lt-kir.jpg
:width: 600

Kir氏
```

Makino氏は[PyCon JP 2026](https://2026.pycon.jp/ja)の主催メンバーでもあり、来週に迫ったイベントの紹介を[Pyxel](https://github.com/kitao/pyxel)製のゲームで行うというものでした。
PyCon KoreaのWebサイトと似たイメージの遊園地をステージにしたゲームをプレイしながらイベントを紹介する、というなかなか斬新なデモでした。
Makinoさんは初めての海外PyCon参加でライトニングトークも発表して、すごいなと思いました。

```{figure} images/lt-makino.jpg
:width: 600

Makino氏
```

筆者もライトニングトークで発表を行いました。
タイトルは「Find Better 🐱 Cat Emojis with your text!」で、LLMを使って入力されたテキストに対して適切なネコチャン絵文字を選択するというものです。
デモが途中うまくいかず、発表時間がタイムアップしてしまいました……

```{figure} images/lt-takanory.jpg
:width: 600

筆者のライトニングトーク
```

## 韓国式焼き肉へ

この日は友人でPython Asia Organization理事のKwonHan氏が韓国式焼き肉を予約するということでそこに参加しました。
どういう風に焼き肉をすればいいのか全然わからなくて途方に暮れていると（私のテーブルにはアメリカ、ヨーロッパメンバーがいた）、私たちのテーブルに韓国ローカルの人が来てくれて色々やってくれて助かりました。

```{figure} images/bbq.jpg
:width: 6002

韓国式焼き肉
```

焼酎のビール割り（調べてみると爆弾酒と呼ぶらしい）というものがあるらしく、ローカルのメンバーにおすすめされましたが、丁重にお断りしてビールと水を飲んでいました。

## Keynote: Cheuk Ting Ho

* トーク概要：[Python makes us hap.py](https://2026.pycon.kr/presentations/26a6f8c6-f896-46fa-9e98-fad5305b30e0#Python-makes-us-happy--the-joy-of-finding-a-community-where-you-belong)
* 動画：<https://www.youtube.com/watch?v=Q4S-jEFw76g>

Day 2最初のキーノートはPSFの理事であるCheuk Ting Ho氏から「Python Makes Us Hap.py」と題して、Cheuk氏のバックグラウンドストーリーが語られました。


```{figure} images/cheuk.jpg
:width: 6002

Cheuk Ting Ho氏
```

Cheuk氏とは以前から友人ですが、彼女のPythonコミュニティ以前の話は初めて聞いたもので、とても衝撃的でした。
Pythonコミュニティが文字通り彼女の人生を変えてくれたというものです。
香港からイギリスに移住したが定職が見つけられず、チラシ配りのアルバイトをして家賃が払えなくてホームレスになるかも知れないという状況だったそうです。
そして、無料のピザを目当てに女性、マイノリティ向けのミートアップに参加し、そこでPythonと仲間に出会いました。
複数回参加する中で参加者に顔を覚えてもらい、みんなが話していることに注意を向け、徐々にPythonの知識を得ました。
その後Couseraで学習を終了し英国企業にデータサイエンティストとして就職でき、生活基盤を安定させられたそうです。

なぜコミュニティの主催者となっていたかについては、2018年に初めてEuroPythonに参加し、そこで受付に行くと名札のヒモが絡まっていて、スムーズに受付が進んでいませんでした。
そこで「このヒモをほどいて事前に参加者に渡せば受付がスムーズになる」と考えて提案し、その場で手伝いをしたことからEuroPythonの運営チームに誘われたそうです。
その後EuroPythonの理事、2024年にはPSFの理事となりました。
また仕事もデータサイエンティストから現在はデベロッパーリレーション（DevRel）に変わったとのことです。

Pythonに出会う前は自分の居場所を探しており、そしてCheuk氏はPythonコミュニティを見つけた。

最後に参加者に以下の3つのことを実施してほしいと告げてトークは終わりました。

* スプリントなどに参加してオープンソースに貢献する
* 参加者やスピーカー、スタッフに声を書けたり感謝を伝える
* SNSで不満を投稿するのではなく、自分の考えを直接伝えて建設的な関係を伝える

Cheuk氏がどん底からPythonコミュニティに出会って今の活躍があるということにとてもびっくりしました。
当然本人の努力も相当だと思いますが、コミュニティと出会うことでHap.pyな状態になって、本当によかったなと思います。

## Keynote: Hugo van Kemenade

* トーク概要：[How to become a Python release manager](https://2026.pycon.kr/presentations/50fe8d0c-6c1a-4a11-866d-f10a5141791e#How-to-become-a-Python-release-manager)
* 動画：<https://www.youtube.com/watch?v=lqqrTy9sIjo>

最後のキーノートはHugo van Kemenade氏です。
Hugo氏はCPythonのコア開発者であり、Python 3.14と3.15のリリースマネージャーを務めています。
自身のオープンソース活動やリリースマネージャーに選ばれるまで、PythonのリリースプロセスとPython 3.15の新機能について語られました。

```{figure} images/hugo.jpg
:width: 600

Hugo van Kemenade氏
```

大学卒業後、仕事ではSymbian OS向けのアプリ開発を行い、オープンソース活動はモバイル上のアプリ開発をはじめたとのことです。
2012年頃からPythonに関連を初め、2012年頃からPillowのバグの修正を行っていたところ、2014年にPillowのコアチームに入ることになったそうです。
2018年から2019年にかけて、PIL_VERSIONとPILLOW_VERSIONという2つの定数が存在するため、古い`PIL_VERSION`の削除を行いました。その際にtorchvisonなど大規模プロジェクトに影響が出たそうです。
そのときの経験から「誰もドキュメントを読まないので、実行時にDeprecationWarningを出すことが重要である」と認識したそうです。

CPythonへの関わりは2019年からで、簡単なドキュメントのtypoにの修正から貢献を開始し、2022年にMariatta氏に誘われてトリアージチームに参加、2022年にはPEPの作者にもなり、コアチームに参加するようになったそうです。
2023年に参加したコア開発者のスプリントでThomas Wouters氏（Python 3.12、3.13のリリースマネージャー）からリリース手順の説明を受けたそうです。
その後、Python 3.14と3.15のリリースマネージャーに選出されました。

また、2025年にはドイツ政府の資金提供を受けた「Soverign Tech Fellowship」に参加し、現在はフルタイムでCPythonの開発者として活動しているそうです。

Pythonのリリースは17カ月でpre-alpha、alpha、beta、release candidateという段階を得てリリースされます。
リリース後は5年間サポートされ、2カ月ごとにバグ修正リリースされます。

```{figure} images/release-cycle.jpg
:width: 600

Pythonのリリースサイクル
```

現在はPython 3.15のrelease candidate（リリース候補）がリリースされたところです。
主な新機能としてはlazy import（遅延インポート）、frozendict（イミュータブルな辞書）、REPLや各種標準ライブラリで出力のカラー化が行われていることが紹介されました。

地道なオープンソース活動から、CPythonへ徐々に取り組み、現在はリリースマネージャーという重要な役割を担うようになったHugo氏の歴史をたどるキーノートでした。

## Building a DJ Workflow with Python

* トーク概要：[Building a DJ Workflow with Python](https://2026.pycon.kr/presentations/29e2ba75-3cfd-4e6d-bb46-0955c48027b7#Building-a-DJ-Workflow-with-Python)
* スピーカー：SiYeong Jang
* 動画：<https://www.youtube.com/watch?v=keBdXG-d7rI>

このトークではアニソン/サブカルチャーDJをしているSiYeong氏が、DJを行うために作成した音楽分析、可視化、自動化ツール**Mixlyzer**についてデモを交えて紹介しました。

* <https://github.com/hygn/Mixlyzer>

```{figure} images/siyeong.jpg
:width: 600

SiYeong Jang氏
```

アニソンでは曲中でBPM（テンポ）が大きく変わる曲、転調する曲が多く存在しています。
そういった曲をDJでつなげるためには、楽曲の手動でタイミングを調整する必要があり、作業が大変だそうです。
そこで、Pythonによって音楽解析を行いBPMを推定し、2つの曲を同期させてスムーズに繋げられるようにしたそうです。
他にも、曲のコードを判定し、同じコード同士を重ねたりとかも簡単になったそうです。

私も趣味で音楽（吹奏楽）で演奏活動をしており、曲のコード判定には興味がわきました。
自分がDJを行うためにツールを作り込むのは、すごいなと思いました。

## クロージング

* 動画：<https://www.youtube.com/watch?v=5Zg1W0W74ZY>

クロージングの前半ではスポンサーやコミュニティのみなさんに感謝状のようなものが贈られていました。
そしてクロージングが始まるかと思ったら前の方になにやら人が集まりはじめました。

今回の参加者でもある[Petr Andreev氏](https://www.linkedin.com/in/petrpy/)（中央の緑のポロシャツの男性）が考案した（らしい）、**PyCon Dance**をみんなで踊っていました。
今後はPyCon Koreaの定番になるんでしょうか。

<blockquote class="twitter-tweet" data-media-max-width="560"><p lang="ko" dir="ltr">와... 개발자들 다 내향적인 줄 알았는데 공개적으로 춤추러 나오는 사람이 이렇게나 많다니 막 신기하고 놀랍고 대단하고 다들 내향적인 척만 했던 건가 싶고 ㅋㅋ<a href="https://x.com/hashtag/pyconkr?src=hash&amp;ref_src=twsrc%5Etfw">#pyconkr</a><a href="https://x.com/hashtag/%EC%84%B8%EA%B3%84%EC%B5%9C%EC%B4%88%ED%8C%8C%EC%9D%B4%EC%8D%AC%EC%B6%A4?src=hash&amp;ref_src=twsrc%5Etfw">#세계최초파이썬춤</a> <a href="https://t.co/5ObnTE5PuL">pic.twitter.com/5ObnTE5PuL</a></p>&mdash; seungho kim (@raccoonyy) <a href="https://x.com/raccoonyy/status/2089162080352088067?ref_src=twsrc%5Etfw">August 17, 2026</a></blockquote> <script async src="https://platform.x.com/widgets.js" charset="utf-8"></script> 

クロージングでは参加者が登録ベースで438名、来場者数は383名、決算や、7名の海外スピーカーがいたことなどが報告されました。
[主催メンバー](https://2026.pycon.kr/about/organizer)は23名とのことです。
みなさんお疲れさまでした！！


```{figure} images/closing.jpg
:width: 600

クロージング
```

## スプリント

3日目（8月17日）は開発スプリントです。この日は韓国は祝日だそうで、そのためPyCon Koreaは例年この時期に開催されています。

会場に行ってスタッフに話を聞くと、スプリントは基本的に以下のページにある「CPython」などのテーマに参加する想定のようです。
「特にテーマに参加しないで自分の作業をしたいんだけど」と伝えると、教室の後ろの方に席を作ってくれました。罰ゲームのような席で自分の作業をしていました。

* スプリントのページ：<https://2026.pycon.kr/program/sprint>

```{figure} images/sprint.jpg
:width: 600

罰ゲームのような席
```

その後、筆者は友人にあいさつをして夕方頃に会場を離れ、釜山へと向かいました。
こうして久しぶりのPyCon Koreaは終了しました。

## 終わりに

海外から招待した3名のキーノートスピーカー、海外、国内の英語で発表するスピーカー、翻訳アプリでのサポートなど、以前参加した2023年に比べると国際化が進んだPyCon Koreaでした。

その後、釜山に向かう特急（KTX）が祝日のため全然取れなかったり、釜山では無料のWorkation Centerで快適に仕事をしたり、下関へ向かうフェリーで寝れなかったりしながら、無事（？）広島に到着しました。
そして8月20日（木）からPyCon JP 2026の運営、参加を行いやっと東京の自宅に帰り着きました（疲れた）。
そのときの様子を以下のスライドにまとめて社内発表しました。

* [PyCon Korea珍道中](https://slides.takanory.net/slides/20260903bpstyle/#/)

```{figure} images/kanmon.jpg
:width: 300

下関港のスタンプは「KANMON」
```
