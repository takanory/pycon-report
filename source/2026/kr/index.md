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
「**Make it hap.py**」というの言葉が今年のテーマのようです。

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
あとでも説明しますが、複数の建物を横移動したり、しかも斜面に複数の建物が建っているため、あるビルの9階から外に出ると普通に地上だったりして、建物の構造が複雑でしたが、そういうところも含めて大学っぽいなと感じました。

```{figure} images/university.jpg
:width: 600

Dongguk Universityの入り口
```

## Keynote: Deb Nicholson


最初のキーノートはDeb Nicholson氏によるものです。
Deb氏はPython Software Foundation（PSF：Pythonソフトウェア財団）[^psf]のExcective Directorであり、今回はPyCon Koreaのキーノートのためにアメリカから来ました。

[^psf]: Pythonの知的財産権と商標の管理や、PyPIの運営をする財団 <https://www.python.org/psf-landing/>

```{figure} images/deb.jpg
:width: 600

Deb Nicholson氏
```

なおトークには基本的に[Cockoo](https://www.cuckoo.so/ja)による翻訳が付いており、スライド横のQRコードを読み込むと選択した言語でトークの翻訳が見ることができて便利でした。
英語のキーノートは韓国語の他に日本語と中国語の翻訳が提供されていました。
以下の様に手元のスマートフォンで日本語で読めるのでありがたいです。

```{figure} images/translate.png
:width: 300

Cockooによる翻訳
```

まずはPSFそのものの紹介があり、PSFが存在することによってPythonは特定のベンダーに依存しない中立的な存在でいられるといことが語られていました。
他に、Pythonのパッケージリポジトリである[PyPI](https://pypi.org/)を運営していること、PyPIのトラフィックは2026年は**2 エクサバイト**になりそうということが語られました。
単位が大きすぎでどれくらいなのかちょっとピンと来ません。

Deb氏からPythonは「プログラミング言語のカピバラだ」という発言がありました（冒頭の写真）。
その意味するところは、カピバラはさまざまな動物と仲良く過ごすことができる、Pythonもさまざまなプログラミング言語と連携できるということだそうです。
PythonとC言語、Java、Go、JavaScript、Fortran、Haskellなど、他言語を連携するさまざまなツールが紹介されました。
また、システム同士をつなぐ役割もPythonが得意とするところです。

また、Deb氏が友人に助けを求めた話もありました。
PSFが米国政府の助成金を受けるために、どのような書類を用意するか、助成金の額をいくらにするかなどを、この助成金を受けている友人に相談したそうです。
その結果助成金の申請が無事にできたとのことで、同様にプログラミングの学習や困難なプロジェクトに対しても、1人で悩まずに友人に助けを求めましょうと語られていました。

最後に参加者にコミュニティもっと参加してほしい、とアクションプランがいくつか提案されました。

* Python使っている企業であれば[PSFのスポンサー](https://www.python.org/psf/sponsors/)となることを検討してほしい。韓国企業のPSFスポンサーもいる
* ローカルやグローバルのイベントに参加してほしい。ここでは[Python Asia Organization](https://pythonasia.org/)についても紹介していました
* [PSFのメンバーシップ](https://www.python.org/psf/membership/)への参加と、理事やパッケージングカウンシルへの投票の参加
* ミートアップなどで周囲へのアピールと共に学ぶこと

Pythonは（ヘビではなく）カピバラだ、という説明が個人的に面白かったです。
PSF、Python、コミュニティ、そして次のアクションへとつなぐキーノートでした。

## Python Asia Organizationブース、ランチ

日本からの参加者があまりいないため、筆者はPython Asia Organizationの理事である寺田さんからテーブルクロスを受け取って現地に持っていきました。
PyCon Koreaではコミュティブースが多数あり、その1つとしてPython Asia Organizationもブースを提供していました。

いつものように日本からお菓子を持っていて参加者に配りつつ、Python Asia Organizationのアピールをしました。

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

* スピーカー：Donghee Na

このセッションでは、Pythonのコアデベロッパーであり、2025、2026年のPython Steering Councilメンバー[^council]であるDonghee Na氏から、会社の中にPythonの言語サポートチームを構築した事例について紹介しました。

[^council]: [PEP 8107 – 2026 Term Steering Council election | peps.python.org](https://peps.python.org/pep-8107/)

```{figure} images/donghee.jpg
:width: 600

Donghee Na氏
```

会社の規模が大きくなる中で、バージョンの更新、セキュリティ対策、デバッグ、サプライチェーン攻撃への対応などの、システムを運用する上での課題が増えてきます。
これらを各チームが対応するのではなく、Python言語サポートチームを立ち上げ標準化を行い、運用コストを下げるという狙いとのことです。
他社事例としてGoogle、Microsoft、Meta、LinkedIn、LINEヤフーに言語サポートチームが存在することが述べられました。

Donghee氏が所属する[Karrot](https://www.karrotmarket.com/)では当初はボランティアベースで言語サポートチームの活動を開始しました。
トラブルシューティング、セキュリティ対応、ナレッジの共有、外部コミュニティ貢献などの活動を継続的に行い、その後会社として正式な部門となったそうです。
社内で毎月ミーティングを実施したり、技術に関するディスカッションを行ったりしているそうです。

社内でPython言語のサポートチームを立ち上げるという発想はなかったので、事例と共に紹介されており、ある程度の規模の企業には参考になるのではと思いました。

## Growth together with PyLadies Seoul

* スピーカー：Luna

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
:width: 600

韓国式焼き肉
```

焼酎のビール割り（調べてみると爆弾酒と呼ぶらしい）というものがあるらしく、ローカルのメンバーにおすすめされましたが、丁重にお断りしてビールと水を飲んでいました。

## Day 2 Opening

* Mir Jungさん

## Keynote: Cheuk

* Why Python Makes Us Hap.py
* Pythonが人生を変えてくれた
* イギリスで定職についていなかったときの話。
* ホームに帰らないといけないかもしれない
* Pythonのミートアップに行った。最初は無料のピザ目当てで
* 複数回参加する→顔を覚えられる→みんながしゃべっていることに注意を向ける
* 滞在するビザが取得できた

* なぜオーガナイザーになったか
* EuroPythonのオーガナイザーとなった。2018年が初めての参加でエジンバラ、5時間でいける
* たくさんの人がいるけど、みんな受け入れてくれた
* 受付でひもがからまっている、そのひもを直すことを申し出た
* 仕事をデータサイエンスからデベロッパーリレーションに変えた
* そのごEurioPythonSocietyに参加、PSFのboardとなる

* Pythonに出会う前は場所を探していた
* 私は場所を見つけた、それがPythonコミュニティ
* 明日から3つのことをやってほしい
  * スプリントでオープンソースに貢献する
  * 知らない人に声をかけてみよう。スピーカーに感謝を伝えたり
  * 自分の考えをきちんと伝える。SNSではなかう

## Keynote: Hugo

* Symbian
* 2005: Open source Boingboing
* 2008: Mobbler
* 2012: Python
* 2012: Pillow: find a bug -> fix a bug
* 2014: Pillow core team
* 2018: deprecation
* 2019: Breake

PIL_VERSIONとPILLOW_BERSIPONが存在。一度削除したが他が壊れた

* 2019: Pillow releses→リリースの自動化を進めた
* 2020: Drop Python 2.7
* PyPIで徐々に古いPollowのダウンロードが減っていった
* 2019: CPython
* 2022: CPython triager→mariattaから誘われた
* 2022: PEP editor
* 2022: Core sprint
* 2024: Core team
* 2023: core sprintでThomasからリリース手順を説明
* 2024: release manager
* 2025: Soverign Tech Fellowshjip

### Python release cycle

* pre-alpha, alpha, beta, release candidate
* 各Pythonは5年間サポート。2カ月ごとにバグ修正リリース
* Python 3.15のリリース候補がリリースされた
* Python 3.15の新機能の紹介

lazy import
frozendict: frozendictはdictのサブクラスではない
more color

* 3.16になるよ

https://hugovk.dev/

## PythonでDJワークフロー

* アニソンDJをしている
* ビートを合わせる
* キーが同じものを一緒にならす

https://github.com/hygn/Mixlyzer

## LT

TaiwanのWinnieさんの発表

## Closing

* PyCon Korea 2019のバッグが大量に余っており、みんなに配っていた。いままでどこに置いていたんだろう...
* スポンサーになにか渡すらしい?
* PyCon dance(Petr andreev)
* 438登録、383 attenndee
* 決算
* 7の海外スピーカー
* CoCの報告は1件
* 23人のorganizing member
* MVP: developers, designer, clown, Deep Dive, Session Manager
* 大学に感謝
