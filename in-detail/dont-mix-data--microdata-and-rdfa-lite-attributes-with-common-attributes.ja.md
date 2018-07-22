# `data-*`とMicrodata、RDFa Lite用の属性と通常の属性を混ぜない

タグ文字列はとても複雑になりえます。こういった簡単なルールによってタグ文字列を読みやすくできるでしょう。

悪い例:

    <img alt="HTML Best Practices" data-height="31" data-width="88" itemprop="image" src="/img/logo.png">

良い例:

    <img alt="HTML Best Practices" src="/img/logo.png" data-width="88" data-height="31" itemprop="image">


## 解説

現在のHTML仕様では、MicrodataやRDFa Liteのための属性や、ユーザーが独自に定義することのできるカスタムデータ属性を、前置きなしで（`head`要素の`profile`属性を使って定義したりせずに）そのまま書けるようになりました。具体的な使い方については触れませんが、漫然と追加すれば良いというわけではありません。

例えば良くあるコーディング規約として*属性をアルファベット順に記述する*というものがあります。それに忠実に従ってカスタムデータ属性やMicrodataの属性を要素に追加すると、悪い例で挙げたようなコードになります。カスタムデータ属性は`data-`で必ず始まり、Microdataの属性は`item`で必ず始まるので、このように要素ごとの属性の間に挟まってしまうでしょう。ある程度はまとまっていますが、要素ごとの属性が分断されてしまっていると、どのような属性が指定されているのか把握しづらくしてしまいます。

良い例で挙げたように、まずはそれぞれの要素ごとに定義されている属性を書くと、そこでその要素がどういう振る舞いをするのかが概ね決定できるので、どのような意図を持った要素なのかが明確になります。続けてカスタムデータ属性はカスタムデータ属性でまとめ、Microdataの属性もMicrodataの属性でまとめて書くようにするのが良いでしょう。