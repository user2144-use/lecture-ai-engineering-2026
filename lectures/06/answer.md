# 第6回 解答

## 演習

<!-- [tool call] の行は、表示された行をそのまま貼り付けてください。終わらなかった STEP は、空欄のままでかまいません。 -->

- STEP 1 のツールの名前：search_glossary, get_lecture_summary, search_materials, make_quiz
- STEP 2 の [tool call]：glossary_search_glossary({'query': '3レベル'})
- STEP 3 の [tool call]：fetch_fetch({'url': 'https://modelcontextprotocol.io/'})
- STEP 4 の [tool call]：aws_aws___search_documentation({'search_phrase': 'Amazon S3 versioning overview', 'topics': ['general']})
- 気づき・疑問：安易にMCPサーバーを設定ファイルに記載してしまうと、プロンプトインジェクションやSSRFの脆弱性につながってしまうことが分かった。

## 宿題

<!-- 基礎・実装・発展のどれか1つに取り組めば完了です。 -->

- 取り組んだレベル：基礎
- やったこと：ツール（get_lecture_summary）を公開するためにapp/mcp_server.pyコードを追記した。
- 結果：追加したツールが呼び出されていることを確認した。
- 気づき・疑問：サーバー側の設定変更のみでツールを追加できることが確認できた。演習を通してプロンプトインジェクションやSSRFの脆弱性につながることが確認できたが、ツールを安易に追加することでツールポイズニングの脆弱性につながってしまうことも確認することができた。
