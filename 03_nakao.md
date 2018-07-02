[[AJACS23]]

&size(25){''Galaxy でできるゲノムスケール共同研究''};

担当：中尾光輝（ライフサイエンス統合データベースセンター）

~目次
#contents


#  今日のゴール [#ba46e36f]
ゲノムスケールデータの共同研究を進めるための Webベースのゲノム情報解析ツール Galaxy の使い方を学ぶ。

#  ゲノムデータの解析 [#o006e1a6]
##  超大量 [#y7d3ab1a]
- 1000人ゲノム
    - 70TB
- 一回の実験
    - 数テラバイトのデータ
    - 数ギガバイトのFASTQファイル
##  データのファイル形式が多種 [#e859890e]
- データ変換が大変
##  ツールが多様 [#r3c73790]
- インストールが大変
- 使い方を覚えるのが大変

##  定型処理と個別処理 [#k5b11f25]
- データセットに依存してくりかえし
- 試行錯誤して解析を深める部分
- 論文作成時はくりかえしデータセットから統計値をとりだす

#  ゲノムスケール共同研究に必要なこと [#jb829182]
メールに添付して解析データを共同研究者と共有するのがほぼ不可能になってきている。
しっかりとしたセキュリティ管理のあるFTPサイトやウェブサイトを構築するのも簡単なことではない。

##  データセットの共有 [#jfefaacd]
- 大量データの共有
##  解析手順の共有 [#i66d9183]
##  解析の再現性 [#x4f1b10e]
##  アクセス権のコントロール [#hfb36036]


#  Galaxy とは [#j9f6a6e8]
##  大量、多様、多種のうち、多様と多種を解決できるいま静かなブームになりつつあるツール。 [#p89075a2]
##  ツールのダウンロードやインストールの手間無しに、どこからでも、解析できるウェブアプリ [#y08c98c3]
- インストール不要
- クラウド型サービス

##  マルチプルアラインメント、ゲノムアノテーション比較、メタゲノムサンプルプロファイル解析などなど可能 [#da02a3cb]

##  データヒストリ機能 [#l92aef57]
- データのアップロード
    - ローカルファイル
    - URL （例：http://genome.kazusa.or.jp/cyanobase/Synechocystis/genes.txt）
- データ取得
    - [[UCSC Table Browser>http://genome.ucsc.edu/cgi-bin/hgTables?command=start]]
    - [[BioMart>http://www.biomart.org/biomart/martview]]
- データ公開
- データフォーマットの変換

##  データ解析ツール [#af952213]
- データ可視化
- 簡単な統計計算
- プログラムの実行
- EMBOSS ツールの実行

##  ゲノム解析向け機能 [#x63261ff]
- ゲノム座標計算（座標の重なりなど）
- ゲノムとデータの関連付け（ビルド番号指定）
    - hg18 などのビルドを指定すると、自動的にゲノムブラウザへのリンクをつける。
- シンテニーアライメントの取得
- シンプルな[[ゲノムブラウザを内蔵>http://bitbucket.org/galaxy/galaxy-central/wiki/Visualization]]
- メタゲノム解析

##  ワークフロー機能 [#ib6e6ef1]
- 複数の解析ツールの連鎖

##  共有機能 [#z8cf66cc]
- データセット
- ワークフロー
- 解析結果（サプリメントデータ）
- こまかいアクセス権の制御が可能
- データライブラリ
- ページ

##  http://usegalaxy.org にて公開サービス [#m2603883]
- ペンシルバニア州立大学で主に開発されている。

##  オープンソースソフトウェア [#t33391a6]
- ダウンロードして、簡単にイントラネットに設置できる。
    - 10分くらいでセットアップが終わります。
- ツールを作って、追加できる。
    - シェルスクリプトにできるものはすべてツールに組み込めます。

##  豊富なドキュメントとスクリーンキャスト [#m5d1d984]
- ウィキ http://bitbucket.org/galaxy/galaxy-central/wiki/Home
- スクリーンキャスト http://galaxycast.org/


#  Galaxy 活用事例紹介 [#r1adea01]
##  Windshield splatter analysis with the Galaxy metagenomic pipeline, Genome Research [#g906b294]
- http://genome.cshlp.org/content/19/11/2144.full
- 身近にいる生物の多様性をメタゲノム解析
    - サンプルは、高速道路を走行する[[自動車のフロントバンパー>http://www.google.co.jp/images?hl=ja&safe=off&client=safari&rls=en&q=2006+Dodge+Caravan&um=1&ie=UTF-8&source=univ&ei=9GvSTLOjEcWycLvDvbgM&sa=X&oi=image_result_group&ct=title&resnum=2&ved=0CDMQsAQwAQ&biw=1030&bih=932]]に付着する生き物（昆虫、花粉等）
    - [[北米で500km ほど走行（二カ所）>http://maps.google.co.jp/maps?f=q&source=s_q&hl=ja&geocode=&q=NY&ie=UTF8&hq=&hnear=%E3%83%8B%E3%83%A5%E3%83%BC%E3%83%A8%E3%83%BC%E3%82%AF,+%E3%82%A2%E3%83%A1%E3%83%AA%E3%82%AB%E5%90%88%E8%A1%86%E5%9B%BD&ll=43.084937,-70.576172&spn=13.041254,26.960449&z=6&brcurrent=3,0x0:0x0,0]] http://genome.cshlp.org/content/19/11/2144/F1.expansion.html
- メタゲノム解析では、ツールや計算機パワーへの要求が依然として厳しい
-  それを、いまの最善の知識で取り組んでみた。（Galaxyで）
- さらに、[[ライブサプリメントマテリアル>http://usegalaxy.org/u/aun1/p/windshield-splatter]]を公開、世界初。（Galaxyで）
- 解析フロー
    - 1. リードのクオリティを評価し、高品質セグメントを選択
        - phred スコア
    - 2. 既存のデータベースの高スコアのヒットを検索
        - MegaBLASTをNCBI WGSとNTに対して実行
    - 3. データベースのマッチから配列リードに系統的ラベルを付与
    - 4. メタゲノムサンプルの系統的比較を可視化
    - 5. 二つのサンプルの系統的構成を比較する
- 結果
    - すべてのステップをGalaxyの中で完結できた。
        - ワークフロー：http://genome.cshlp.org/content/19/11/2144/F3.expansion.html
    - 「ライブ」サプリメントデータを提供。解析フローをすぐに再現可能。
        - 通常のサプリメントデータは、PDFやExcel、PowerPoint書類の表や図。
    - それらから解析の再現や検証をするには、手間がかかっていた。
        - http://usegalaxy.org/u/aun1/p/windshield-splatter
    - 二つのメタゲノムのサンプルの違い
        - [[網（Class）>http://en.wikipedia.org/wiki/Class_(biology)]]レベルの差：http://genome.cshlp.org/content/19/11/2144/F2.expansion.html
        - まとめの表：http://genome.cshlp.org/content/19/11/2144/T2.expansion.html
        - [[アブラムシ>http://ja.wikipedia.org/wiki/アブラムシ]]の[[共生菌ブフネラ>http://en.wikipedia.org/wiki/Buchnera_aphidicola]]（Gamma Proteobacteria）の存在感
        - [[轢死動物>http://en.wikipedia.org/wiki/Roadkill]]

#  実習：Galaxy 入門 [#ncbbcc78]
##  準備 [#i983b2ed]
+ Galaxy をウェブブラウザで開く：http://galaxy.dbcls.jp もしくは http://usegalaxy.org

##  簡単なデータ操作 [#v9e93706]
###  1. データのアップロード [#w783132c]
+ 1. 「ツール」→「Get Data」→「Upload File」ツールを選択
+ 2. 「URL/Text:」に下記のデータをコピー＆ペースト
 chr22 1000 5000 cloneA 960 + 1000 5000 0 2 567,488, 0,3512
 chr22 2000 6000 cloneB 900 - 2000 6000 0 2 433,399, 0,3601
+ 3. スペースをタブに変換
++ 1.「ツール」→「Text Manipulation」→「Convert」ツールを選択

###  2. 行の取り出し [#j14d41d5]
行の選択：cloneA を含む行を選択
+ 1. 「ツール」→「Filter and Sort」→「Filter」ツールを選択
+ 2. 「With following condition:」の値を c4=='cloneA' に書き換えて実行
+ 3. あたらしくできたヒストリーを確認する。

###  3. 列の取り出し [#j14d41d5]
列の選択：カラム（１、４）を抜き出す
+  1. 「ツール」→「Text Manipulation」→「Cut」ツールを選択
+  2. 「Cut columns:」の値を c1, c4 に変更して実行
+ 3. あたらしくできたヒストリーを確認する。

###  4. メタデータの編集 [#g00bba82]
+ 1. ヒストリパネルの「1: Pasted Entry」鉛筆アイコン（Edit attributes）をクリック
+ 2. メタデータを確認する
++ Name：表示される名前
++ Info：ヒストリの「情報」に表示される内容
++ Database/Build：帰属するゲノムのビルドなど
+ 3.Name を「My Data」に変更する。
+ 4. Save して確認する


##  Galaxy 101: The first thing you should try [#ic9ff331]
- http://main.g2.bx.psu.edu/galaxy101 を見ながらすすめてみましょう。
- スクリーンキャスト http://screencast.g2.bx.psu.edu/galaxy101/
###  1. UCSC からデータを取得する [#x7a9cf64]
###  2. かんたんなデータ操作をおこなう [#m49f74ea]
###  3. Galaxy のヒストリーシステムを理解する [#fc00b808]
###  4. ワークフローを作成し編集してみる [#q3e594c3]
###  5. ワークフローに自分のデータを適用してみる [#x09e1f25]


#  まとめ [#e15de9f6]
+ Galaxy の紹介をし、簡単な使い方の紹介をしました。
+ アカウント作成すると、共有機能（送る側）も利用できます。

#  参照 [#r0711829]
- 紹介した論文
    - [[Windshield splatter analysis with the Galaxy metagenomic pipeline ― Genome Research>http://genome.cshlp.org/content/19/11/2144.full]]
    - ライブサプリメント http://usegalaxy.org/u/aun1/p/windshield-splatter
- Galaxy ウェブサイト
    - http://usegalaxy.org
    - エクササイズ　http://usegalaxy.org/learn
    - ダウンロードとインストール　http://getgalaxy.org
    - スクリーンキャスト http://galaxycast.org
    - ウィキhttp://bitbucket.org/galaxy/galaxy-central/wiki/Home
- DBCLS Galaxy （DBCLSの追加ツールあります）
    - http://galaxy.dbcls.jp
    - [[インストール方法>http://galaxy.g.hatena.ne.jp/morita_hideyuki/archive]]
- 統合TVでも紹介しています
    - [[統合TV (togotv) - Galaxyを使い倒す-特定の転写因子予測結合領域と遺伝子上流領域の「交差点」をリストアップする>http://togotv.dbcls.jp/20090310.html#p01]]
    - [[統合TV (togotv) - DBCLS Galaxyの利用法>http://togotv.dbcls.jp/20100809.html#p01]]
- [[ DBCLS Galaxyではじめるゲノムスケールデータの共同研究. 山口 敦子. 中尾 光輝>http://www.pdbj.org/workshop/201008/Yamaguchi_Nakao.pdf]]
- [[Galaxy ツールを作る>http://wiki.lifesciencedb.jp/mw/index.php/Galaxy_%E3%83%84%E3%83%BC%E3%83%AB%E3%82%92%E4%BD%9C%E3%82%8B]]
