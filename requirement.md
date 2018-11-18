## 質問箱クローン 
オリジナル： https|//peing.net/  
リバース・エンジニアリング参考：https|//nabettu.hatenablog.com/entry/disassembly-peing

### 基本機能
- SNS上で自分の専用URLを公開し、アクセスしてきたユーザーは匿名で質問ができる。  
- 質問に対し回答すると、Twitterに回答が画像化された状態で投稿される。  
- 回答内容はマイページのフィード画面から一覧で見ることもできる。 
- 質問内容はストックしていき、回答者はその中から選んだものだけ回答することができる。
- twitterでアカウント作成し、ユーザープロフィールはTwitterの内容をそのまま登録する。登録後は任意で変更可能にする。

### 技術要件
- 言語:        Ruby v2.5.1
- FW:       Ruby on Rails v5.2.1
- 使用DB:      PostgreSQL
- 使用サーバー: heroku
- コントローラー：
 - question_controller... 質問者が操作する質問フォーム
    - new     :質問入力フォーム
    - create  :Questionインスタンス作成
    - destroy :投稿済みの質問を削除
 - user_controller... 回答者の登録、削除
- モデル：
 - Question
    - content:text
 - User
    - name:text
    - description:text
    - password
    - password_digest
    - image:text

