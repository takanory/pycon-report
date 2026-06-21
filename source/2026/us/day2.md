# Day 2

````{admonition} コラム：(terapyon LTコラム)
このコラムはPython Asia Organizationの寺田（[@terapyon](https://x.com/terapyon)）がお届けします。

私はPyCon USに参加すると、コミュニティーブースの運営や各国のコミュニティーメンバーとの交流を中心に活動しています。そのため、発表する側よりも聞く側になることが多いのですが、今年はLightning Talk（LT）で登壇する機会を得ました。

PyCon USでは会期中にLTが複数回あり、1枠5分ながら毎年人気です。
当初は参加者の多いDay 1夕方のLT枠を狙っていましたが、ブース対応中に締切を過ぎて応募できませんでした。
そこで翌朝の募集に応募し、Day 2朝のLTで2番手として登壇しました。私のLTの開始は朝8:05でした。

私は海外カンファレンスでLTをした経験はありますが、PyCon USでのLTは今回で2回目です。また、これまでのLTはコミュニティー活動やイベント運営に関する話題が多く、技術的な内容を中心に発表する機会はそれほど多くありませんでした。

今回紹介したのは、最近取り組んでいる画像検索の仕組みです。

「[Searching 23,000 Photos with Modern VLMs: From Text to Image](https://speakerdeck.com/terapyon/searching-23000-photos-with-modern-vlms-from-text-to-image)」と題し、PyCon JPの過去の写真をセマンティック検索する仕組みを紹介しました。

5分間という制約もあるため、アルゴリズムの詳細や評価結果については触れず、「どのようなことができるのか」を中心に紹介しました。特に、実際に動作するデモを見せることを重視して準備を進めました。

ただ、発表では時間配分をミスして、最後まで話すことができませんでした。

```{figure} images/PyConUS2026-teradaLT.jpg
:width: 600

寺田がLTで発表している様子
```

LTはたった5分ですが、限られた時間の中で何を伝えるかを整理することの難しさを改めて感じました。
一方で、デモは問題なく動作しました。会場からも反応があり、想定していたポイントで笑いや驚きの声が上がったのは嬉しかったです。

発表後には何人かの参加者から反響を聞けました。
「同じようなものを作ってみたい」
「どうやって実装しているのか興味がある」
自分が取り組んでいる内容に興味を持ってもらえたことは素直に嬉しかったです。

PyCon USには世界中から参加者が集まります。英語で発表することには毎回緊張しますが、自分が作ったものを直接紹介し、その場で反応を得られることは貴重な経験です。

今後もコミュニティー活動だけでなく技術的な取り組みについても発信していきたいと思います。
````


## Member Lunch

* Grantの期間はみじかくなった
* 金額はAfricaが多いなぁ
* 質疑応答
* 寺田さんと吉田さんの質問

````{admonition} コラム：PSF Member Lunchについて
一般社団法人PyCon JP Association理事の吉田([@koedoyoshida](https://twitter.com/koedoyoshida/))です。PyCon US のメンバーランチに参加してきました。

```{figure} images/member-lunch-desc.jpg
:height: 400

Deb Nicholson氏の説明の様子
```


```{figure} images/member-lunch-food.jpg
:height: 400

食事の様子
```

PSFメンバーランチはランチを取りながら、PSF（Python Software Foundation）のメンバーが一堂に会し、財団の現状やこれからについて語り合う、毎年恒例の場です。

今年もPSFのExecutive DirectorであるDeb Nicholson氏から説明がありました。

例年であればこのランチで PSF の昨年の財務報告のサマリとなる資料が共有されるのですが、今年は財務資料の配布については見送りとなりました。

そこで私は「今年は財務資料の配布がないようですが、昨年の財務状況はどうだったのでしょうか。資料はWebで公開されるのでしょうか？」と直接質問してみました。すると運営側から率直な回答が返ってきました。

回答内容は「会計担当の体制が変わった影響で、今回はまとまった数字をお見せできる状態に間に合わせられなかった。ただ財務の透明性は大切にしているので、体制が整い次第あらためて資料を公表する予定です」といったものです。
数字の詳細こそその場では出ませんでしたが、財務状況をめぐる考え方や今後の方針について、こちらの疑問にきちんと答えてくれました。

PSFメンバーランチは、PSFメンバーが事前登録のうえ参加できる貴重なイベントで、その場で質問も可能です。たとえば、月に5時間程度、PythonやPyConに継続的に関わっているなどの条件を認められれば、PSFメンバーのうちContributing Memberとして登録が可能で、理事選挙の投票権なども得られます。該当する方や興味のある方は、ぜひ以下のページで詳細をご確認ください。

[Become a Member of the PSF](https://www.python.org/psf/membership/)


````

## Tachyon: Python 3.15's sampling profiler is faster than your code - PyCon US 2026

* https://us.pycon.org/2026/schedule/presentation/31/
* python -m profile.sampling
* capture mode

```
python -m profile.sampling run main.py
python -m profile.sampling attach <pid>
```

reporters

* visualizeされる
* 最初に見るのは --pstats

what;s happening now?

* フレームグラフがカラーで見れる

* --heatmap
* --diff-framegraph →パフォーマンスが上昇したか見れる
* --gecko: Firefoxのprofilerを使える
* あとでanalyzeする: --binary

````{admonition} コラム：三年連続のPyCon US登壇で考えた、プロポーザルを書くということ

このコラムは青野 高大（[@koxudaxi](https://github.com/koxudaxi)）がお届けします。

今年は [Beyond Optional in Real-World Projects: Missing, None, and Unset](https://us.pycon.org/2026/schedule/presentation/28/) というタイトルで登壇しました。ありがたいことに、PyCon USでは2024年から三年連続で登壇する機会をいただきました。

```{figure} images/koxudaxi-talk.jpg
:width: 600

PyCon US 2026で登壇する筆者
```

登壇を重ねるなかで感じるのは、話すテーマは、普段の開発と切り離された特別な話ではない、ということです。これまでのトークも、仕事やOSS活動の中で何度も見かけてきた問題がもとになっています。プロポーザルを書くたびに、その問題を自分用のメモのままにせず、聞いた人が「自分のプロジェクトでも使えそうだ」と思える形に整えられないかと考えてきました。

今年扱ったのは、「値がないように見えるものにも、実はいくつか違う意味がある」という話です。Pythonでは `None` を使う場面がとても多いのですが、Web APIや設定ファイルのように外部からデータを受け取る場面では、値が指定されていないことと、明示的に `null` が送られてきたことは、必ずしも同じではありません。

たとえば、PATCHメソッドでユーザー情報を一部だけ書き換える場面を考えてみます。`{"nickname": null}` が送られてきたら、ニックネームを消したいという意味かもしれません。一方で `nickname` というフィールド自体が送られていなければ、今の値を変えない、という意味になります。Python側で `payload.get("nickname")` のように書くと、どちらも `None` になり、リクエストの意図が失われます。

こうした問題は、私がメンテナンスしている[datamodel-code-generator](https://github.com/koxudaxi/datamodel-code-generator)でも何度も議論になってきました。これは、OpenAPIやJSON Schemaなどのスキーマから、PydanticモデルやdataclassesなどのPythonコードを生成するOSSです。スキーマでは、必須かどうか、`null` を許すか、省略されたときの扱いが、それぞれ別の意味を持ちます。これをPythonの型やデフォルト値にどう落とすかは、見た目以上に難しい問題です。

今回のトークでは、payloadの形は `TypedDict` で表し、送られない可能性のあるフィールドは `NotRequired` で表しました。また、関数呼び出しで値が指定されていないことは `UNSET` のようなsentinelで表し、最後に `dataclasses` のモデルへ変換する流れを紹介しました。外から来たデータの意味を失わないために、どこで何を区別するかという話です。

一つひとつのissueだけを見ると、細かい仕様の話に見えることがあります。しかし、似た話題が何度も出てくるということは、多くの人が同じところで迷っている、ということでもあります。その迷いを、特定のライブラリの中だけの話にせず、Pythonを書く人が持ち帰れる形にどう切り出すか。プロポーザルを書くときは、毎回そこを考えています。

三年続けてプロポーザルを書いてみて、話すテーマは、やはり普段の開発の中にあるのだと感じています。日々の仕事やOSS活動で何度も見かける小さな違和感を、丁寧に整理して言葉にすること。それもまた、Pythonコミュニティに知見を共有する一つの形なのだと思います。
````

## mypyc?

## PyLadis Auction
