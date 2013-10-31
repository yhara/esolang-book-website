## 正誤表

本書の正誤表です。

もしも間違いを発見なさった場合には、お手数ですがTwitterの[@yhara](https://twitter.com/yhara)か、yutaka.hara.gmail.comまでお知らせください。

### 第二版

以下は第二版(と第一版)に当てはまる内容です。

* 2-2節
  * parse_multipleというメソッドを定義していますが、「掛け算」の英語は「multiplication」なので、parse_multiplicativeという名前の方が適切でした。

### 第一版

以下は第一版にのみ当てはまる内容です(第二版では修正されています)。

#### 重要な間違い

p.143, p.149 のfind_labelsメソッドにおいて、raiseの位置が間違っていて、ラベル命令が使えなくなっていました。申し訳ないです。

誤：

```
raise ProgramError, ...
if insn == :label
```

正：

```
if insn == :label    
　raise ProgramError, ...
```

#### その他の間違い

* 全般
  * `require "foo"`などのようにしてカレントディレクトリのファイル(この例では、foo.rb)を読み込んでいる箇所がありますが、Ruby 1.9.2以降では、`require "./foo"`のように明示的に`./`を付ける必要があるようになりました。

* 帯裏
  * 誤：False8
  * 正：False
  * 誤：Taxi4
  * 正：Taxi

* p.11 概要 
  * 誤：<code>$ aptitude install ...</code>
  * 正：<code>$ <strong>sudo</strong> aptitude install ...</code>
  * installには管理者権限が必要でした。

##### 1-1

* p.15 リスト2
  * 誤：<code>98..on the wall, <strong>99</strong> bottles...</code>
  * 正：<code>98..on the wall, <strong>98</strong> bottles...</code>

* p.25 上部
  * 誤：がが
  * 正：が

##### 1-2

* p.34 上部
  * 誤：ここでは **案2** を採用することにする
  * 正：ここでは **案1** を採用することにする

* p.34 上部
  * 誤：案1・2と **案3・4** は両立できるので
  * 正：案1・2と **案4** は両立できるので
  * 案3と案1・2は両立できませんでした。

##### 1-3

* p.45 リスト1
  * 誤：<code>>+.<strong>#</strong></code>
  * 正：<code>>+.</code>
  * 余計な「#」が付いていました。

* p.48 図の下
  * 誤：「 **+** 」命令も「 **-** 」命令も使っていないので..
  * 正：「 **>** 」命令も「 **<** 」命令も使っていないので..
  * +-命令ではポインタを移動できません。 

* p.50 (7)
  * 誤：次に実行される命令は「 **[** 」だが
  * 正：次に実行される命令は「 **]** 」だが
  * 誤：数値が0のとき、「 **[** 」命令は 
  * 正：数値が0のとき、「 **]** 」命令は 

* p.52 図1の上
  * 誤： **4つ** のトークンに分割する
  * 正： **6つ** のトークンに分割する

* p.59 リスト
  * 誤：<code>require 'normal-library</code>
  * 正：<code>require 'normal-library<strong>'</strong></code>

* p.60 1段落目
  * 誤：最終的に **NoMemoryErrorが発生する** が
  * 正：最終的に **メモリが足らなくなる** が
  * NoMemoryErrorが発生するかどうかは未確認でした。

* p.76 2段落目
  * このように **Braif*ck** の
  * このように **Brainf*ck** の

##### 1-4

* p.78 下部
  * 誤： **[Tab][Tab][Space]** なら足し算
  * 正： **[Tab][Space][Space][Space]** なら足し算

* p.91 表2
  * 誤：<code>[:<strong>mem</strong>_write] </code>
  * 正：<code>[:<strong>heap</strong>_write]</code>
  * 誤：<code>[:<strong>mem</strong>_read] </code>
  * 正：<code>[:<strong>heap</strong>_read]</code>

* p.93 箇条書き
  * 誤： **アンダースコア** で区切る。
  * 正： **アンダーバー** で区切る。
  * 表記ゆれ(ここだけアンダースコアになっていました。)

* p.110 リスト7
  * 誤：<code>[:label " ¥t¥t "],</code>
  * 正：<code>[:label<strong>,</strong> " ¥t¥t "],</code>

* p.114 下部
  * 誤：先に **ポップ** すればいい
  * 正：先に **プッシュ** すればいい

* p.119 1段落目
  * 誤： **initialize** で初期化した配列return_to
  * 正： **runメソッドの先頭** で初期化した配列return_to
  * ローカル変数でしたね。

* 1-4 全体
  * 「num_inは数値をスタックに積む」のような記述がありますが、ヒープに積むのでした。

##### 2-1

* p.136 2段落目
  * 誤：後に出てきたほう **で上書きされる**
  * 正：後に出てきたほう **は単に無視される**
  * 説明が逆でした。

* p.145,p.147 rotate命令
  * 誤：<code>z, y, x<strong>,</strong> = pop, pop, pop</code>
  * 正：<code>z, y, x = pop, pop, pop</code>
  * (動作は同じですが)余計なカンマがありました。

##### 2-2

* p.178 上部
  * 誤：<code><strong>3</strong>12</code>
  * 正：<code><strong>2</strong>12</code>
  * かけ算が間違っていました。(次のページも同様です)
