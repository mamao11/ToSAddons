# ToSAddons
Tree of saviorはワールド統合され、チャットには英語や韓国語（ハングル）が流れるようになったりました。  
チャットに読めない文字が流れてくるとなんかモヤモヤする……。  
ToSに備わっている翻訳機能はいちいち選択して翻訳操作しなくちゃいけないし、パーティリンクとか含んでると翻訳もできない。  
超不便……というわけで作ってみました。  
<br>
### これは何？
これはTree of savior用アドオンです。  
  
ToS翻訳アプリと連動して韓国語を日本語訳して表示する機能を持っています。  
ただしアドオン単体では機能しません。  
別リポジトリに上げているToS翻訳アプリを起動しておくことでアドオンと連携し、翻訳APIの翻訳結果をToS上で表現します。  
<br>
### ざっと機能一覧
* 翻訳するのは韓国語のみ。英語はがんばって読んでください
* 翻訳に利用できるAPIは２種類
  * みんなの自動翻訳
  * DeepL
* 翻訳後チャットへの反映方法は以下２種類のうちどちらかを選択
  * 原文に追記
  * 原文を置き換え
* メッセージの書き換えはローカル表示のみでサーバのメッセージは書き換えない。というかできない<br>（だからMAP移動などすると元の韓国語に戻る）
* パーティ名は翻訳するとたぶん機能しなくなるので翻訳せずハングルのまま表示
<br>

## 導入手順
#### ［ToS翻訳ツールの導入と設定］
　**（※環境によっては.NET Framework 4.7.2ラインタイムのインストールが必要かも。別途インストールしてください）**  
1. みんなの自動翻訳、DeepL翻訳ツールにアカウント登録（どちらか片方でも良い）  
2. TosTranslateリポジトリからToS翻訳アプリをダウンロード  
3. 解凍したらToSTranslator.exeを起動  
4. 注意事項をしっかり読む（※しっかり読んでね！）  
5. 翻訳キー等を設定（※各翻訳サービスで登録した後に貰える情報を入れる）  
![image](https://github.com/mamao11/ToSAddons/assets/36460192/c2588780-c5e9-4ae3-8cf7-c60a7ad1cd09)  
上記はみんなの自動翻訳の例

7. 翻訳APIをプルダウンから指定  
8. ステータスボックスが青色（翻訳は緑色）になったらToS翻訳ツールの準備OK  
![image](https://github.com/mamao11/ToSAddons/assets/36460192/02fc7a59-5f65-408c-bb73-b90ce7f5a7c7)
  
#### ［ToSアドオンの導入］

1. 当リポジトリから（chatkonyaku-📖-v0.0.1.ipf）をダウンロード
2. 「インストール先\Tree of Savior (Japanese Ver.)\data」フォルダへコピー  
  （※アドオンマネージャに登録してないので手でコピーしてね）  
  
以上で導入完了。  
<br>
## 起動してみる
ToSを起動。MAPにログインしてみる  
**※起動順はToS翻訳アプリ→ToSの順です。逆にすると翻訳できません。**  

システムメッセージでこんな感じのメッセージが出る。  
  
![image](https://github.com/mamao11/ToSAddons/assets/36460192/5af43927-27e5-4321-8f72-a81fdde8642b)  
大事なのは送信-OK、受信-OKの文字  
<br>
そしてToS翻訳アプリのステータスボックスが青から緑に変われば接続OK  
  
![image](https://github.com/mamao11/ToSAddons/assets/36460192/97b1e362-d763-46cb-8ffe-bbbf4c2b5c33)

あとは韓国語で発言されれば自動的に翻訳され、数秒後にチャットに反映される。  
  
![image](https://github.com/mamao11/ToSAddons/assets/36460192/c791f97a-24d6-494d-9104-0f57e0c7b1a8)  
上の例は**原文を置き換え**の例。赤い菱形は翻訳された文章を示すマーク。  
<br>
#### ［翻訳エラー？］
各サービスにおいて翻訳回数等の制限がある。  
みんなの自動翻訳は日単位。DeepLは月単位の制限のもよう。  
<br>
制限にひっかかるとToSチャット欄は「翻訳失敗」と表示され、ToS翻訳アプリにERROR表示が出る。  
<br>
![image](https://github.com/mamao11/ToSAddons/assets/36460192/3ef36763-48c4-412b-bb11-257f5942915c)
<br>
制限にひっかかったら諦めて翻訳APIを切り替えてください。  
