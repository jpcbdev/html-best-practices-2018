# `apple-touch-icon`へのリンクを書く

デフォルトでリクエストされるタッチ・アイコンのパスは突然変わりました。

Bad:

    <!-- Hey Apple! Please download `/apple-touch-icon.png`! -->

Good:

    <link href="/apple-touch-icon.png" rel="apple-touch-icon">


## 解説

iOSで最初にサポートされたタッチ・アイコンは、長らく暗黙的に探すパスが決まっていました。つまりファビコンと同じようにわざわざリンクを追加する必要はなかったわけです。しかしiOS 8でその挙動に変更が加わりました。今はまた変わっているかもしれませんし、こういった変更がもうないとは言い切れない状況に変化しました。

リンクがない場合に探しに行くようになっているため、リンクしないことはパフォーマンスの面でもメリットはありません。良い例で挙げたように素直に指定すると良いでしょう。後方互換性を意識して、パスは`/apple-touch-icon(-precomposed).png`にしておくのも悪くありません。
