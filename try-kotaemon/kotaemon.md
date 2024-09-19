# kotaemon を使ってみる

## End User向けドキュメント

URL: https://cinnamon.github.io/kotaemon/

### ollamaとのチャット

1. zipファイルをダウンロード
2. 展開
3. 実行された
4. ollamaを使うように設定する
   1. Resource → LLMs のViewタブでollama行を選択して、Set defaultにチェックをつける
   2. Specificationを設定する
      - api_keyは変更不要
      - base_urlもおそらく変更不要
      - modelは使いたいモデルを記入
   3. Test connectionの▼をクリックし、testボタンを表示して、testボタンをクリックする
      - 成功したらLLMにollamaを使えている
   4. Resource → Embeddings のViewタブでollama行を選択して、Set defaultにチェックをつける
   5. Specificationを設定する
      - api_keyは変更不要
      - base_urlもおそらく変更不要
      - modelは使いたいモデルを記入
   6. Test connectionの▼をクリックし、testボタンを表示して、testボタンをクリックする
      - 成功したらEmbeddingsにollamaを使えている

### チャットを試す

1. Chatを開く
2. Chat inputにメッセージを書き込む
   - しばらくthinkingと表示されてから応答が返ってくる

### RAGを試す

1. Filesを開く
2. File CollectionタブでFile UploadにRAGの対象にしたいファイルを指定する
3. Upload and Indexボタンをクリックする
   - しばらく待つとindexが作成される
4. Chatを開く
5. Chat inputにメッセージを書き込む
   - しばらくthinkingと表示されてから応答が返ってくる
   - 応答が返された後、しばらくolama_llama_serverのCPU使用率が高いままになっていて、その間は新しいチャットに応答してくれなくなる
   - Embeddingsにparaphrase-multilingual-minilmを指定するほうが既定のnomic-embed-textよりもマシな応答になった


## 開発者向けドキュメント
