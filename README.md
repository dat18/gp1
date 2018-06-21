# ゲームプログラミング1年生
2018年度 デジタルアーツ東京 ゲームプログラミング１年生用リポジトリー

# 講義予定
- [シラバス](syllabus.md)

# 9回目(6/22)
## 宿題
- プレイヤー、アイテム、障害物、背景用のモデルをAsset Storeなどで探して、プロジェクトにインポートしておく
  - 採用したアセットのURL、あるいは、作者名＋アセット名をメモしておくこと(Googleドライブにドキュメントを作るなど)
  - MagicaVoxelで用意する場合は、モデルを作成して保存しておく
  
## 予定
- MagicaVoxelのモデルをBlenderでエクスポートした時に、テクスチャーを有効にする手順
  - ply形式は頂点カラーのみなので、マテリアルやテクスチャーが存在しない
  - 自分でテクスチャーをベイクして生成する必要がある
    - UV Mappingレイアウトに変更して、すべての面を選択
    - 3D ViewでEditモードにして、Mesh -> UV Unwrap -> Smart UV Projectを選択
    - Island Marginを0.06程度にしてOKでUV展開
    - UVエディターの下でNewをクリックして、テクスチャー名と、展開したマス目の数から適当なテクスチャーサイズを考えて(分割数x4程度)設定
    - 3D ViewをPropertiesに変更
    - 下から2番目ぐらいのBakeをクリックして開く
    - Bake ModeをVertex Colorsに変更して、Marginを4pxなどにしてBakeボタンをクリック
    - 以上でテクスチャーが生成されるので、UVエディターでイメージを保存
    - FileメニューからFBXなどでエクスポート
    - 以上で出力したFBXファイルとPNGファイルをUnityに読み込んで、マテリアルを展開後、テクスチャーをAlbedo欄にドラッグ＆ドロップ
- 前回、Visual Studioで作ったすべて取ったら止めるプログラムの実装例を紹介
- TextMesh Proを使って、タイトル画面を作る
- 各シーンのモックを作成
- 状態遷移を実装

## 田中の利用ツール
- MagicaVoxel https://ephtracy.github.io/
  - キャラクターのモデリングに作成
- Blender https://www.blender.org/
  - MagicaVoxelで作成したキャラクターのテクスチャーを作成
- PostProcessing Stack https://assetstore.unity.com/packages/essentials/post-processing-stack-83912
  - 画面を光らせる


# 8回目(6/15)
## 内容
- [前回までのメモ](https://github.com/dat18/csharp-manual)
- 以下の演習の確認
  - 50個ぐらいラベルを出して、それをすべて消す速さを競うゲームを作る
    - マウスと重なったラベルを画面から消す
    - 全てのラベルを消したらタイマーを止める
    - 新しい変数frameCountを定義して、1回タイマーを実行するたびに1増やす
    - ラベルを画面に配置して、frameCountを表示する
    - 以上を、13:30まで作業して、GitHubにリポジトリーを作成して、登録する
    - すでに完了している人は、ラベルの種類を増やして、触ったら即ゲームオーバーになる方法を検討しよう
- 状態遷移
  - https://docs.google.com/presentation/d/1yeiHMxu-t-3hemuMqLaaBPBKL5E1XPuMNxEfa8tyijU/edit?usp=sharing
  - よけとる2018の遷移図 https://www.lucidchart.com/invitations/accept/a6791c9a-9788-4e1a-93a4-b77c2ddba6c2
- Unityで実装

# 7回目(6/8)
## 内容
- [前回までのメモ](https://github.com/dat18/csharp-manual)
- 配列と繰り返し


# 6回目(6/1)
## 内容
- [前回までのメモ](https://github.com/dat18/csharp-manual)
- 前回の復習として、演習8-2以降をやる https://github.com/dat18/csharp-manual/blob/master/08.md#%E6%BC%94%E7%BF%928-1
- switch文の書き方(文法だけ確認)
- if文その2 複合演算子
  - 演習11
- 乱数
  - 演習12
- Unityでの跳ね返りの続き その2
  - https://docs.google.com/document/d/1oHhEYTuhYm_saZosKwEbLYlIvAKJt0N5yc0gsUcGbWo/edit?usp=sharing
- Unityでの乱数
  - https://docs.google.com/document/d/1bUtOQ6jVgO1ICYCmP2_Y5mCzlelq85slLIMeN5J9bvI/edit?usp=sharing


# 5回目(5/25)
## 課題の確認
- C#マニュアル 07.md の型違いの値を代入する方法を調べて、ドキュメントに記入する
- Unityで操作する

## 内容
- [前回までのメモ](https://github.com/dat18/csharp-manual)
- 前回の復習
  - 新しいプロジェクト fuku0525 を作成
  - ラベルを１つ置く
  - ボタンを5つ置いて、それぞれ、上、左、右、下、停止のように表示
  - タイマーを置く
  - ボタンを押すと、ラベルが、押したボタンの方向に移動を続ける(停止は停止)ようにせよ
- if文
  - 跳ね返りを作成
- マウス操作
  - ラベルをマウスで操作
- Unityでの跳ね返り
  - https://docs.google.com/document/d/1oHhEYTuhYm_saZosKwEbLYlIvAKJt0N5yc0gsUcGbWo/edit?usp=sharing

# 4回目(5/18)
## 復習用動画
- https://www.youtube.com/watch?v=qPHwOBHm4YI

## 内容
- [前回までのメモ](https://github.com/dat18/csharp-manual)
- 前回の復習
  - 前回、計算の章で飛ばした部分についてを埋める
  - 新しいプロジェクトを作成(プロジェクト名 fuku0518)
  - ラベルを配置
  - タイマーを配置
  - ラベルを自動的に**右上**に移動させる
- 書く教科書で学ぶC#
  - 変数


# 3回目(5/11)
## 復習用動画
- https://www.youtube.com/watch?v=cnxeKhGph8w

## 内容
- [前回までのメモ](https://github.com/dat18/csharp-manual)
- 前回の復習
  - 新しいプロジェクトを作成
  - ボタンを置く
  - ボタンをクリックしたら、ボタンの表示が変わって、ウィンドウの左端に移動させて、ボタンが押せないように無効にする
- 書く教科書で学ぶC#
  - 計算から

# 2回目(4/27)
## 話題
- [【お題にチャレンジ】あなたの欲しいアセットの50%分が手に入る！？アセットバウチャー総額 『$1,000（約10万円）＋α』山分けプレゼント](http://www.asset-sale.net/entry/ChallengeEvent180417)

## 復習用動画
- https://www.youtube.com/watch?v=-CkvvzFT5bE

## 内容
- 書く教科書で学ぶC#
  - プロパティの確認まで
- Paizaによる独習(C#)

# 1回目(4/20)
## 話題
- [【お題にチャレンジ】あなたの欲しいアセットの50%分が手に入る！？アセットバウチャー総額 『$1,000（約10万円）＋α』山分けプレゼント](http://www.asset-sale.net/entry/ChallengeEvent180417)

## 復習用動画
- https://www.youtube.com/watch?v=BmZN-ciT7sQ

## 内容
- ガイダンス-シラバスの確認、プログラミングの正体-
- Visual Studioを試す
- Unityを試す
- Paizaでの学び方
  - [Paizaラーニング C#](https://paiza.jp/works/cs/primer)
- ドットインストールでの学び方
  - [ドットインストール Unity(4.2)入門](http://dotinstall.com/lessons/basic_unity)
- [C# 書く教科書 はじめ方](cs-gettingstarted.md)

# 参考URL
- [Unity](http://japan.unity3d.com/)
- [Paizaラーニング](https://paiza.jp/works)
  - [Paizaラーニング C#](https://paiza.jp/works/cs/primer)
- [ドットインストール](http://dotinstall.com/)
  - [ドットインストール Unity(4.2)入門](http://dotinstall.com/lessons/basic_unity)
- [タイピング練習サービス e-typing](https://www.e-typing.ne.jp/)
- [C# 書く教科書](https://github.com/tanakaedu/csharp-man)
