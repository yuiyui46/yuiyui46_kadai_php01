①課題番号-プロダクト名
アンケートアプリ

②課題内容（どんな作品か）
政府系オープンデータを使った簡単データ分析サイトの登録画面

③DEMO
https//gs1.sakura.ne.jp/kadai_php01/resister.php
この先の自動遷移はなぜかしてくれません・・・

④作ったアプリケーション用のIDまたはPasswordがある場合
なし

⑤工夫した点・こだわった点
・resister：入力した初期情報をPHPMyAdminのusersDBへ格納
・login：login情報をPHPMyAdmin内のusersDBの情報と突合し、PHPMyAdminのuser_loginのDBへ格納

・select_data：userが突合・解析に使いたい自身のcsvデータをUploadしたら、PHPMyAdminのselect_dataのDB内に格納

・analyze_data：userが自身が登録したデータとe-Statで公表されているデータをAPI連携させ、自動解析(ここは指示出しと結果出力までは上手くできずAPI連携成功のみ確認)

⑥難しかった点・次回トライしたいこと(又は機能)
・登録画面から最後まで入力データを適切にDB格納をしながらの画面自動遷移（リダイレクト）
・XAMPPとMY SQLとPHPMyAdminがどうつながっているのかを理解するのにものすごく時間がかかった。その際に連動している他ファイル等等の書き替えも。
・ポートが競合しているエラーが何度かでて、その度にポート変えてやり直した
・API連携後のデータ活用（データ分析デザインやUI等はまだ全くできていないので慣れたらそこまでできるようになりたい）
・DBへのデータ格納の仕方も今回はお試しレベルなのできちんと何を何のために取得したいのか整理して設計したい

・さくらサーバーにデプロイするために、さくらサーバーのPHPMyAdminに新規登録し、XAMPPと一緒に使用していたPHPMyAdminのDBをすべてエクスポート→インポートした
・PHPのコードもサーバー名やデータベース名、パスワード等も書き換えた
・さくらサーバーでデプロイしようとすると画面が上手く開かないし遷移しない
　Httpsをhttpにするとresiter画面は開くが、情報入力後のlogin画面以降に自動遷移しない、login画面単独でhttpでURLを入れると出るが、、、

⑦質問・疑問・感想、シェアしたいこと等なんでも
質問：上記理由でものすごくはまり込んで終わらず、アップロードできる段階にもならずどうしてよいかわからなくなってしまいました。
　　　時間がないため、とりあえず（おかしいですが）アップロードします
   　 さくらサーバーへのデプロイとサーバーへ入れると様々なプログラムが機能していないところの原因を自分ではお手上げなので、どなたか教えて頂きたいです！
      こちらにはさくらサーバーへ入れる前の（サーバー名やデータベース名等書き換え前）ファイルを掲載します。
