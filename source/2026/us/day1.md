# カンファレンス1日目

* 5月15日
* https://us.pycon.org/2026/schedule/talks/#May15

## Welcome

PyCon US 2026のChairであるElaineさんからのあいさつがありました。
最初に関係者、スポンサーなどへの感謝が述べられました。

最初の方で「まわりの会ったことない人と会話してみましょう」というアイスブレイクがありました。
筆者は、たまたま前に座っていたMark Shannonさんとあいさつをしました。
Mark ShannonさんはPyCon JP 2022のキーノート[^marks-keynote]だった方で、私が日本から来たこと、日本でのキーノートをしたこと、日本にぜひ来てくださいという話をしました（2022のキーノートはリモート発表でした）。

[^marks-keynote]: [PyCon JP 2022: Day 1 OP & Keynote by Mark Shanonn - YouTube](https://www.youtube.com/watch?v=e_EbzeBf06g)

ボランティアの募集、会場の説明、PyLadiesの紹介、スプリントなどのイベントの説明がありました。
その中でPyCon US 2026での初めての取り組みとして以下が紹介されました。

* AIトラック（カンファレンス1日目）
* セキュリティトラック（カンファレンス2日目）
* Pablo氏によるスペイン語のキーノート（カンファレンス2日目の朝、同時通訳付き）

Pablo氏は英語でも早口なので、母国語のスペイン語だとどんなスピードになっていしまうんだろう。通訳は間に合うんだろうか？という感想を持ちました。
とはいえ、PyCon USで英語以外のキーノートを行うというのは、挑戦的だと思いました。

## PSF Welcome

## Keynote — Lin Qiao

* Fireworks AIのCEO、Co-Founder
* MetaでPyTorch開発やっていた
* 2026はyear of agents
* cursor, Uber, Shopifyを例にあげる

## Mind the Gap

* Mind the gap! Why static typing requires more than just adding annotations - PyCon US 2026
* https://us.pycon.org/2026/schedule/presentation/15/
* コード例を示して型ヒントでどういうことがあるか説明
* 型ヒントを入れたときのメリットなどを説明

## PEP 750 - T-strings: safer and smarter string processing - PyCon US 2026

* https://us.pycon.org/2026/schedule/presentation/70/
* ブラジルの人
* Python公式ドキュメントの翻訳やっている
* ログを人用とマシン用に出し分ける例

## What's so hard about writing a type checker? A tour of ty - PyCon US 2026

* https://us.pycon.org/2026/schedule/presentation/143/
* tyのlaziness
  * 依存関係グラフを持っている
  * その中でも必要なところしかチェックしない
  * query-based architecture
  * RustのSalsaを使って依存関係を管理
  * Salsaで必要なときにキャッシュを使わなくなる

## The Bakery: How PEP810 sped up my bread operations business - PyCon US 2026

* https://us.pycon.org/2026/schedule/presentation/30/
* Python起動時に重たいよね
* PEP 810でlazy import。3.15から追加
* 1. Parse Pahse
* 2. proxyが作られる
* 3. 実際にアクセスするときに実際にimportしてproxyを透過する
* 移行
  * python -X importtime -c "import mymodule" で計測

## How to port a Python kernel to Pyodide for a blazingly fast in-browser coding experience - PyCon US 2026

* https://us.pycon.org/2026/schedule/presentation/78/
* marimoのノートブックがブラウザ上で動くっぽい
* marimoがでた→WASMで動くようにした?
* httpが違う。patchをあてる
* パフォーマンスをあげるために: Custom Pyodide build、Custom lockfile、Reveal editor before kernel-ready

## Free-threaded Python: past, present and future - PyCon US 2026

* https://us.pycon.org/2026/schedule/presentation/63/
* Thomas Wouters
* マルチプロセス、サブインタープリター、asyncioがあるけど、フリースレッドのメリットもある
* PyParallel(2013)
* Larry Hastings' GILEctomu(2015)
* Samm Gross's NoGIL Python 3.9(2021)
* Sam's NoGIL, PEP 703
* 3.13でexperimental、3.14でサポート

## Lock-Free Multi-Core Performance with Behavior-Oriented Concurrency - PyCon US 2026

* https://us.pycon.org/2026/schedule/presentation/54/
* bocpy: BOC in Python
* https://github.com/microsoft/bocpy
* Cownクラス
* @whenデコレーター
* [食事する哲学者の問題 - Wikipedia](https://ja.wikipedia.org/wiki/%E9%A3%9F%E4%BA%8B%E3%81%99%E3%82%8B%E5%93%B2%E5%AD%A6%E8%80%85%E3%81%AE%E5%95%8F%E9%A1%8C)
* 3.12からフルのパフォーマンスは出る
* $ pip install bocpy[boids]
* bocpy-boids
* 8コアまではパフォーマンス出るけど14コアではあまり速くならない

## LT

* いろんな人とセルフィーを撮る
* hiringでAIとかを使う、ハックされたLinkedInとか→PyCon USに参加しているときに証拠を残そう
* 字幕の人のLT
* CUMBUCA DEV: ブラジルのマイノリティの開発コミュニティ。ポルトガル語のgithubの本を出したり。CUMBUCAはBOWLのこと
* たくさんのAIエージェントだと結局混乱するって話
* ハロウィンのかざりのためのPythonアプリいろいろ
* 赤ちゃんが生まれる数を予測。季節を考慮した予測をするっぽい
* re.subを書きやすくするデコレーター
* PyCon Korea: スプリントの経験からはじまた

