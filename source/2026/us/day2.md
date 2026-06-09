# Day 2

````{admonition} コラム：(terapyon LTコラム)
ここにコラムを書いてね
````


## Member Lunch

* Grantの期間はみじかくなった
* 金額はAfricaが多いなぁ
* 質疑応答
* 寺田さんと吉田さんの質問

````{admonition} コラム：PSFメンバーランチについて
一般社団法人PyCon JP Association理事の吉田([@koedoyoshida](https://twitter.com/koedoyoshida/))です。開催されたメンバーランチに私も参加してきました。

例年PSFメンバーランチではランチを取りながら、PSFのスタッフとボードメンバーから昨年の活動や会計に関する報告がされ、他のPSFメンバーとディスカッションができます。

今年もPSFのExecutive DirectorであるDeb Nicholson氏から説明がありました。

例年であればこのランチでPSFの昨年の財務報告のサマリとなる資料が共有されるのですが、今年は会計部門の人員交代が重なり、財務資料の配布については見送りとなりました。
このことについて直接質問してみると、運営側から率直な回答が返ってきました。数字の詳細こそ出なかったものの、財務状況をめぐる考え方や今後の方針について、こちらの疑問にきちんと回答いただけました。財務資料は体制が整い次第あらためて公表する予定とのことでした。

このようにPSFメンバーランチは、PSFメンバーが事前登録のうえ参加できる貴重なイベントで、その場で質問も可能です。たとえば、月に5時間程度、PythonやPyConに継続的に関わっているなどの条件を認められれば、PSFメンバーのうちContributing Memberとして登録が可能で、理事選挙の投票権なども得られます。該当する方や興味のある方は、ぜひ以下のページで詳細をご確認ください。

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

````{admonition} コラム：(koxudaxiコラムタイトル)
ここにコラムを書いてね
````

## mypyc?

## PyLadis Auction


