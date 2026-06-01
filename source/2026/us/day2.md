# Day 2

````{admonition} コラム：(terapyon LTコラム)
このコラムはPython Asia Organizationの寺田（@terapyon）がお届けします。

私はPyCon USに参加すると、コミュニティーブースの運営や各国のコミュニティーメンバーとの交流を中心に活動しています。そのため、発表する側よりも聞く側になることが多いのですが、今年はLightning Talk（LT）で登壇する機会を得ました。

PyCon USでは会期中に複数回のLTセッションが開催されます。発表時間は5分間です。短い時間ではありますが、毎年多くの応募があり、人気の企画となっています。

当初はDay 1の夕方に行われるLT枠に応募したいと考えていました。夕方のLTは参加者も多く、会場の盛り上がりも大きいからです。しかし、ブース対応などをしているうちに締切時間を過ぎてしまい、その日の応募はできませんでした。

そこで翌朝の募集に応募し、Day 2の朝のLTセッションで2番手として登壇することになりました。なんと朝8:05からのLT登壇でした。

私は海外カンファレンスでLTをした経験はありますが、PyCon USでのLTは今回で2回目です。また、これまでのLTはコミュニティー活動やイベント運営に関する話題が多く、技術的な内容を中心に発表する機会はそれほど多くありませんでした。

今回紹介したのは、最近取り組んでいる画像検索の仕組みです。

「[Searching 23,000 Photos with Modern VLMs: From Text to Image](https://speakerdeck.com/terapyon/searching-23000-photos-with-modern-vlms-from-text-to-image)」と題し、PyCon JPの過去の写真をセマンティック検索する仕組みを紹介しました。

5分間という制約もあるため、アルゴリズムの詳細や評価結果については触れず、「どのようなことができるのか」を中心に紹介しました。特に、実際に動作するデモを見せることを重視して準備を進めました。

発表当日は朝のセッションということもあり、十分に見直す時間を確保できませんでした。また、自分でも少し頭が回っていなかったように思います。自己紹介に想定以上の時間を使ってしまい、最後に話そうと思っていた内容まで到達できませんでした。

![寺田がLTで発表している様子](./images/PyConUS2026-teradaLT.jpg)

LTはたった5分ですが、限られた時間の中で何を伝えるかを整理することの難しさを改めて感じました。
一方で、デモは問題なく動作しました。会場からも反応があり、想定していたポイントで笑いや驚きの声が上がったのは嬉しかったです。

発表後には何人かの参加者から反響を聞けました。

「同じようなものを作ってみたい」
「どうやって実装しているのか興味がある」

自分が取り組んでいる内容に興味を持ってもらえたことは素直に嬉しかったです。

PyCon USには世界中から参加者が集まります。英語で発表することには毎回緊張しますが、自分が作ったものを直接紹介し、その場で反応を得られることは貴重な経験です。

今回は時間配分に課題が残りましたが、コミュニティー活動だけでなく技術的な取り組みについても発信できた良い機会になりました。
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

````{admonition} コラム：(koxudaxiコラムタイトル)
ここにコラムを書いてね
````

## mypyc?

## PyLadis Auction


