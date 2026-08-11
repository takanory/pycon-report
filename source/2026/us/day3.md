# カンファレンス3日目

カンファレンス最終日です。この日は筆者自身のライトニングトーク、PSFのセキュリティエンジニアや、Steering Councilからのトークなどがありました。

* タイムテーブル：<https://us.pycon.org/2026/schedule/talks/#May17>

## ライトニングトーク

PyCon USではカンファレンス中に4回（1日目夕、2日目朝、夕、3日目夕）ライトニングトークがあります。
2日目の朝は寺田さんがライトニングトークをしていました。
最後のライトニングトークに通ったので発表してきました。
タイトルは「Find Better 🐱 Cat Emojis with your text!」で、昨年のライトニングトーク[^2025-lt]の続きとなるトークです。

* スライド：[Find Better 🐱 Cat Emojis with your text!](https://slides.takanory.net/slides/20260517pyconus/#/)

今回も昨年同様、冒頭で「Do you like Cats?（ネコは好きですか？⁠）⁠」と問いかけて会場から「Yeeees!!」と答えてもらうところから本題をはじめました。
聴衆の中には「あれ、この流れ去年あったな？」と思ってくれた人もいたんじゃないかなと期待しています。

```{figure} images/takanory-lt.jpg
:width: 600

筆者のライトニングトークの様子
```

[^2025-lt]: [#03 Python Steering Councilの活動の今 ―PyCon USカンファレンス3日目/スプリントレポート | gihyo.jp](https://gihyo.jp/article/2025/06/pycon-us-2025-03)

## PSF - Update from our Security Engineers

* スピーカー：Seth Michael Larson、Mike Fiedler
* スライド：<https://speakerdeck.com/sethmlarson/psf-security-engineer-update-pycon-us-2026>

PSF（Pythonソフトウェア財団）のセキュリティエンジニアであるSeth氏とMike氏からの発表です。

```{figure} images/seth_and_mike.jpg
:width: 600

Seth氏（左）とMike氏
```

Pythonではパッケージのリポジトリとして[PyPI](https://pypi.org/)が存在します。
このリポジトリは日々攻撃にさらされており、セキュリティエンジニアのお二人はそれらの攻撃にも対処しています。
直近では特定のプロジェクトではなく、依存関係にあるプロジェクトを狙う手法があり、LightLLMなどのサプライチェーン攻撃などが発生しています。

* 参考：[AIゲートウェイがバックドアに：LiteLLMサプライチェーン侵害の内幕 | トレンドマイクロ (JP)](https://www.trendmicro.com/ja_jp/research/26/d/inside-litellm-supply-chain-compromise.html)

パッケージをアップロードするための認証情報を盗まれないための、**Trusted Publishers** プロトコルについても紹介されました。
このプロトコルを適用すると短い期間で期限が切れるトークンを使用するため、より安全にパッケージが公開できます。

* [GitHub Actionsでデジタル証明書付きPythonパッケージをリリースする方法 | gihyo.jp](https://gihyo.jp/article/2025/05/monthly-python-2505)

また、セキュリティ対策はAmazon、Google、Bloomberg、Alpha Omegaなどの企業の支援によって支えられています。

## ポスターセッション、ジョブフェア

* ポスター一覧：<https://us.pycon.org/2026/schedule/posters/list/>

Day 3は10時から13時までの3時間ポスターセッションとジョブフェアが行われておりトークはありません。
ポスターセッションはA0程度のサイズのポスターの前発表を行うスタイルです。
ジョブフェアは企業がブースを出して求職者と直接話ができる場です。

ポスターセッションにはPyCon Taiwanのメンバーでもあるpetertc氏がいました。
petertc氏はPyCon USに参加するのは初めてだそうです。
発表の内容はPythonからC言語のIOCTLとやりとりすることで、デバイスを直接制御するというものです。
実際に業務でも利用しているそうです。

```{figure} images/peter.jpg
:width: 600

petertc氏
```

他に朝のライトニングトークで紹介されていた、火星探査をするローバーの実物が展示されていました。
[JPL Open Source Rover](https://open-source-rover.readthedocs.io/en/latest/)というプロジェクトだそうです。
多くの来場者が興味深く見ていました。

```{figure} images/rover.jpg
:width: 400

ローバーの実物
```

ジョブフェアを眺めていると[Tower Research Capital](https://tower-research.com/)という会社のブースにたくさんの人がいます。
近づいてみると結構しっかりしたバックパックをグッズとして配布しています。
話を聞いて見ると特に登録とかしなくてもOKということで、お礼を言ってバックパックをもらいました。
周りにもこのバックパックを持っている人がたくさんいました。

```{figure} images/best-swag.jpg
:width: 600

ベストPyCon US 2026グッズ
```

````{admonition} コラム：肩の力を抜いて楽しむPyCon US
橘祐一郎（[@whitphx](https://github.com/whitphx/)）です。
PyCon US 2025に続き、今年も参加してきました。

今回の私は、発表者でもブース出展者でもなく、仕事として参加したわけでもありません。ただの一参加者としてロングビーチまで行きました。
単純に去年参加したPyCon USが楽しかったのと、それに加えて今年はロングビーチにも行ってみたかった程度の理由で、あまり気負わずに参加しました。

私は基本的に、海外のPyConにはトークが採択されたら行くようにしていました。飛行機代もホテル代も安くないので、せっかく行くならできれば発表して目立ちたいからです。
とはいえPyCon USは競争率が高く、「登壇できたら行く」と考えているといつまでも行く機会がないかと思い、去年から発表にこだわらず普通に参加者として行くことにしました。
去年はそれでも[Summitに出てみたり](https://gihyo.jp/article/2025/06/pycon-us-2025-01#ghbrRbSLSI)してそれなりに頑張っていましたが、今年は肩の力を抜いて特に気張るイベントを作らずに参加してみました。実際、それで十分楽しかったです。

想像通り、基本的にはセッションを聞いたり、キーノートやライトニングトークを眺めたり、ブースを回ったりして過ごしました。会場を歩いているだけでも知り合いに会いますし、ブースや飲み会で初対面の人と盛り上がることもあります。

```{figure} images/20260514_181108.jpg
:width: 600

個人的に知り合いの多いStreamlitブースを訪問
```

カンファレンス前日の夜には、会場近くのバーで日本から来ていた参加者たちと飲んでいたところ、PyCon USのバッジをつけた初対面の参加者と自然に同じテーブルを囲むことになりました。特に準備していなくても、同じイベントに来ている人同士で話が弾みます。
Python Asiaが音頭をとった飲み会に参加した時は、アジア各地から来た参加者が集まっていて、「また別の国のPyConで会いましょう」という話にもなりました。実際どこかのPyConに行くとよく会いますし、今回初めて知り合えた人もいて、輪が広がっている感じがします。

```{figure} images/20260513_213509.jpg
:width: 600

開幕前日の夜に行ったビアバー。フライト後すぐだったので軽く
```

```{figure} images/20260514_202048.jpg
:width: 600

知り合いメインの非公式ビール飲み会
```

```{figure} images/20260515_202758.jpg
:width: 600

スポンサー主催のパーティー
```

3日目は会場を抜け出して現地の友人と映画を観に行きました。ホテル代や参加費の元を取ろうと気負いすぎなくてもよいのだと思います。

スプリントでは、今年は特定のプロジェクトのテーブルには入らず、会場を仕事場のように使いながら自分のタスクを進めたり、近くに来た人と話したりしていました。
これも[去年](https://gihyo.jp/article/2025/06/pycon-us-2025-03#gh3794ZQjQ)とは大きな違いです。
スプリント2日目には、ランチに行くグループに混ぜてもらってタコスを食べた流れで、そのままロングビーチの観光地（クイーンメアリー号）を見に行き、夕方には海岸を散歩し、そのまま食事と飲みに行ってしまいました。

```{figure} images/20260519_151835.jpg
:width: 600

クイーンメアリー号
```

```{figure} images/20260519_193503.jpg
:width: 600

ロングビーチの砂浜
```

こんな感じで、意識の低い参加の仕方をしてみました。十分に楽しめましたし、それもアリではないかと思います、ということでこのコラムを締めたいと思います。
````

## Learning Computer Science with Python and Music(21) 

* トーク概要：<https://us.pycon.org/2026/schedule/presentation/127/>
* スピーカー：[Michael Scott Asato Cuthbert](https://us.pycon.org/2026/speaker/profile/137/)
* 録画：<https://www.youtube.com/watch?v=PhkGSj-KKD4>

このトークは、[music21](https://github.com/cuthbertLab/music21)というPython製の音楽分析ツールキットを使って、コンピュータサイエンス（CS）の基礎を学習する取り組みの紹介でした。

```{figure} images/michael.jpg
:width: 600

Michael氏
```

Michael氏は学生にCSを教えており、データベース設計やボット開発のようなアプリケーションは関心を引きにくい課題があるそうです。
そこで、CSの応用コースでmusic21と音楽理論を取り入れることによって、より学生の創造性を引き出し、CSへの理解度も高めることができているそうです。

```{figure} images/music21.jpg
:width: 600

music21のデモの様子
```

筆者は趣味の吹奏楽でトランペットを吹いており、音楽関係のライブラリとしてmusic21は興味深いものでした。
JupyterLab上でPythonのプログラムを書くと、その音やコードの楽譜が表示されたり、MIDIを再生できたりします。
確かに音楽は、同じようなパターンの反復や音程の移動を行うことがあるので、プログラミングの考え方と重なる部分があると思いました。
個人的にmusic21を自分の音楽活動で活かせないか、ちょっと調べてみようと思います。

## Keynote — Rachell Calhoun & Tim Schilling

PyCon US最後のキーノートは、[Djangonaut Space](https://djangonaut.space/)の共同設立者であるRachell Calhoun氏とTim Schilling氏によるものでした。
Djangonaut Spaceは、Python製のWebフレームワークであるDjangoのトレーニングプログラムを提供するコミュニティです。
自己学習プログラムと8週間のメンターシッププログラムを提供しており、Djangoへのコードの貢献を行い、将来のDjangoのコア開発者やメンテナーを育成することを目的としています。

```{figure} images/tim.jpg
:width: 600

Tim氏
```

参加者をサポートするために「ナビゲーター」と「キャプテン」という2つの役割があり、ナビゲーターはプロジェクトを推進するための技術的な支援、キャプテンは一人一人によりそった支援を行うそうです。
過去の参加者が成長して次のナビゲーターやキャプテンを務めるといった、コミュニティ内での良い循環もあるそうです。

コミュニティの取り組みとして興味深いなと感じました。
一方で、体制を維持して運営を継続するのはかなり大変なのではないかとも思いました。
Djangoへの貢献に興味のある方は、ぜひこの取り組みを参照してみてください。

## Python Steering Council

Pythonの言語仕様はPEP（Python Enhancement Proposal）というドキュメントで提案されますが、その採用、不採用を決めるのが5名のSteering Councilメンバーです。
Steering Councilメンバーは毎年CPythonのコア開発者の投票によって決まります。
2026年のメンバーについては以下のドキュメントを参照してください。

* [PEP 8107 – 2026 Term Steering Council election](https://peps.python.org/pep-8107/)

```{figure} images/council.jpg
:width: 600

5名のSteering Councilメンバー
```

最初にSteering Councilメンバーの紹介や開発体制について話がありました。
最近はコア開発者が一同に介して一週間程度の開発スプリントを行っています。
2026年はOpenAIがホストとなって開催されるそうです。

続いて、2026年10月にリリース予定のPython 3.15の新機能について紹介がありました。
Lazy imports（遅延インポート）、immutable（不変）な辞書、カラー表示の追加、新しいプロファイラー（Tachyon）などが紹介されました。

また、PEP 772[^pep772]によってPackaging CouncilというPythonのパッケージングに関する委員会を設立することが紹介されました。

[^pep772]: [PEP 772 – Packaging Council governance process](https://peps.python.org/pep-0772/)

他にはPythonの将来についての話がありました。
Free-threadingのデフォルト化は近い将来（3.16から3.20のどこか）で実現したいとのことです。
標準ライブラリにRustを導入することが検討されているとのことで、現在は検証を行っているところだそうです。

Rustの導入がどうなるかは注視していきたいと思います。

## Python Software Foundation Update

Closingの前にPSFのExective DirectorであるDeb Nicholson氏より、PSFの最新情報についての共有がありました。
PSFはPythonの権利を有しており、Python言語の普及、保護、発展を目指して活動している財団です。

```{figure} images/deb.jpg
:width: 600

Deb氏
```

PSFの大きなニュースとして、アメリカ府（国立科学財団：NSF）からの150万ドル（約2.2億円）の助成金を辞退したことが報告されました。
これは、助成金の契約の中に多様性、公平性、包含性（DEI）に関する活動を制限する内容が含まれていたためです。
そのためPSFは助成金を拒否したとのことです。
この件に関する詳細な情報は以下のブログを参照してください。

* [Python Software Foundation News: The PSF has withdrawn a $1.5 million proposal to US government grant program](https://pyfound.blogspot.com/2025/10/NSF-funding-statement.html)

## Closing

クロージングではイベントのChairであるElaine Wong氏が登壇し、関係者への感謝が述べられました。
イベントを表す数字としては参加者数が2003名、そのうち57.2%が初参加者とのことです。
また、151名のオンサイトのボランティア、148名の発表者、135のオープンスペースが開催されました。
PyCon USはやはり規模が大きいですね。

```{figure} images/closing1.jpg
:width: 600

参加者数などの情報
```

そしてPyCon US 2027のChairが発表されました。
2026ではCo-Chairを担当していたJon Banafato氏が、2027ではChairとなるそうです。

PyCon US 2027は2027年5月13日から18日に、2026と同じロングビーチで開催することが報告されました。

```{figure} images/closing2.jpg
:width: 600

PyCon US 2027もLong Beachで開催
```

## 各国PyConの宣伝

いつもはここでイベントが終わるんですが、今回はClosingのあとに各国PyConの宣伝タイムがありました（今までは朝のライトニングトークでした）。
1イベント1スライドを30秒程度で、各主催者が宣伝しました。
なにげに私はこのイベント宣伝をPyCon USでするのは初めてでした。
1日に2回メインステージに上がることができて、ラッキーです。

他にアジアからはPyCon Singapore、Indonesia、Korea、Taiwan、Hong Kongなどが宣伝をしていました。

```{figure} images/pyconjp-announce.jpg
:width: 600

PyCon JP 2026を宣伝しているところ（後ろに他イベントの主催者）
```

## 最後のパーティー

PyConのカンファレンスは終わりましたが、まだ終わりません！！
参加者が集まっているお店に行ってパーティーです。
このお店で飲んでいるときに、韓国から参加している初めての人とあいさつをすると「takanoryなの！？」と私のことを知っているようでした。
いったい、韓国でどういう噂をされているんだろう...

```{figure} images/party.jpg
:width: 600

パーティー
```

そのあとはローカルのクラフトビールが飲みたいので、アジアメンバー中心で[Beachwood Brewing: Downtown Blendery and Taproom](https://beachwoodbrewing.com/blendery.html#)に移動しました。
疲れている？のか、なぜかみんな床に座ってビールを飲んでいます（謎）。
こうしてPyCon USのカンファレンスは無事に終わりました。

```{figure} images/asian-style.jpg
:width: 600

なぜか床に座って飲む人々
```

## 終わりに

次の日（5月18日）はスプリントに参加し、夜にアナハイムに移動しました。
そして5月19日は2回目のカリフォルニアディズニーランドを訪問しました。
前回同様、ほぼスターウォーズエリアに1日中いるというスタイルです。

今年から出没するようになったハン・ソロがいたので「日本から来たんですよー」みたいに会話をして写真を撮ってもらいました。

```{figure} images/hansolo.jpg
:width: 600

ハン・ソロ（本物）と握手
```

その後は飛行機の都合でシアトル（初訪問）に移動し、ビール友達のShaneと毎日ビールを飲みまくり、大量のビールをおみやげにもらって無事帰国しました。
ビールが多すぎて、初めて関税を100円払いました。

```{figure} images/beer-and-dog.jpg
:width: 600

シアトルのビールの店はどこも犬同伴が可能、とてもいい所
```

さー、楽しかったし、来年もロングビーチ（とディズニーランド）に行くかー。

筆者と寺田さんがパーソナリティをしているPyCon JP TVでもPyCon USについて報告しています。
もしよかったらこちらも見てみてください。

<iframe width="560" height="315" src="https://www.youtube.com/embed/40mIepqo3k0?si=Iud1i-dLvggrJUFA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

