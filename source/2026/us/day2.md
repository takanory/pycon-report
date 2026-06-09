# Day 2

````{admonition} コラム：(terapyon LTコラム)
ここにコラムを書いてね
````


## Member Lunch

* Grantの期間はみじかくなった
* 金額はAfricaが多いなぁ
* 質疑応答
* 寺田さんと吉田さんの質問

````{admonition} コラム：(yoshida MemberLunchについて書かない?)
ここにコラムを書いてね
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

登壇を重ねるなかで感じるのは、話すテーマは、普段の開発と切り離された特別な話ではない、ということです。これまでのトークも、仕事やOSS活動の中で何度も見かけてきた問題がもとになっています。プロポーザルを書くたびに、その問題を自分用のメモのままにせず、聞いた人が「自分のプロジェクトでも使えそうだ」と思える形に整えられないかと考えてきました。

今年扱ったのは、「値がないように見えるものにも、実はいくつか違う意味がある」という話です。Pythonでは `None` を使う場面がとても多いのですが、Web APIや設定ファイルのように外部からデータを受け取る場面では、値が指定されていないことと、明示的に `null` が送られてきたことは、必ずしも同じではありません。

たとえば、PATCHメソッドでユーザー情報を一部だけ書き換える場面を考えてみます。`{"nickname": null}` が送られてきたら、ニックネームを消したいという意味かもしれません。一方で `nickname` というフィールド自体が送られていなければ、今の値を変えない、という意味になります。Python側で `payload.get("nickname")` のように書くと、どちらも `None` になり、リクエストの意図が失われます。

こうした問題は、私がメンテナンスしているdatamodel-code-generatorでも何度も議論になってきました。これは、OpenAPIやJSON Schemaなどのスキーマから、PydanticモデルやdataclassesなどのPythonコードを生成するOSSです。スキーマでは、必須かどうか、`null` を許すか、省略されたときの扱いが、それぞれ別の意味を持ちます。これをPythonの型やデフォルト値にどう落とすかは、見た目以上に難しい問題です。

今回のトークでは、payloadの形は `TypedDict` で表し、送られない可能性のあるフィールドは `NotRequired` で表しました。また、関数呼び出しで値が指定されていないことは `UNSET` のようなsentinelで表し、最後に `dataclasses` のモデルへ変換する流れを紹介しました。外から来たデータの意味を失わないために、どこで何を区別するかという話です。

一つひとつのissueだけを見ると、細かい仕様の話に見えることがあります。しかし、似た話題が何度も出てくるということは、多くの人が同じところで迷っている、ということでもあります。その迷いを、特定のライブラリの中だけの話にせず、Pythonを書く人が持ち帰れる形にどう切り出すか。プロポーザルを書くときは、毎回そこを考えています。

三年続けてプロポーザルを書いてみて、話すテーマは、やはり普段の開発の中にあるのだと感じています。日々の仕事やOSS活動で何度も見かける小さな違和感を、丁寧に整理して言葉にすること。それもまた、Pythonコミュニティに知見を共有する一つの形なのだと思います。
````

## mypyc?

## PyLadis Auction

