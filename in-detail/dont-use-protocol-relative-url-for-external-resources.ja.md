# 外部リソースにはプロトコル相対URLを使わない

プロトコルを指定すると、外部リソースを確実かつ安全に読み込めます。

悪い例:

    <script src="//example.com/js/library.js">

良い例:

    <script src="https://example.com/js/library.js">


## 解説

かつて、古いブラウザーが安全なリソースとそうでないリソースが混在しているという警告を、モーダル・ダイアログで出していました。こういったモーダル・ダイアログはユーザーに深刻な状況を想起させてしまうだけでなく、煩わしいものです。ウェブページ制作者としてはなんとしても避けたい事態でしょう。

そのため悪い例で挙げたようなコードがベスト・プラクティスとされていました。こうすることでユーザーが閲覧している状況に応じて、外部リソースのプロトコルが適宜選択されるので、ブラウザーが警告が出さないからです。

しかし、外部リソースの読み込みは常に危険を伴います。しばらく前には[GitHubがダウンするような事態][1]も引き起こされています。できうる限りHTTPSで提供される外部リソースのみを読み込むべきです。プロトコルを省略しないという簡単なルールにより、`https:`ならば安全が保障され、`http:`ならば危険を伴うことが意識できるでしょう。


[1]: https://www.netresec.com/?page=Blog&month=2015-03&post=China%27s-Man-on-the-Side-Attack-on-GitHub