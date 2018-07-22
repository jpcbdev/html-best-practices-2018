# 大文字・小文字を混ぜない

これも一貫性を与えてくれます。

悪い例:

    <a HREF="#general">General</A>

良い例:

    <a href="#general">General</a>

同じく良い例:

    <A HREF="#general">General</A>


## 解説

複数の開発者により書かれる場合に限らず、タグの書き方に一貫性がないHTML文書を見かけることはよくあります。その一貫性のなさは要素同士だけでなく、開始タグと終了タグ、要素名と属性名でもあります。

    <P>W3Cについて、より詳しくは
    <a Href="http://www.w3.org/">W3CのWebサイト</A>
    をご参照ください。</P>

仕様では大文字と小文字の区別はないので、文法としては決して間違いではありません。しかし大文字と小文字の違いは比較的目に止まりやすいため、HTMLコードの読みやすさに大きな影響を与えます。その影響は決して良いものではなく、違和感や不必要な強調として捉えられ、HTMLコードの把握に悪影響を与えることが多いでしょう。

    <p>W3Cについて、より詳しくは
    <a href="http://www.w3.org/">W3CのWebサイト</a>
    をご参照ください。</p>

より読みやすいHTMLソースのために、まずは大文字・小文字、そして引用符の統一から始めましょう。何に統一するからは自由です。一般的には小文字で書く人が増えているようですので、そうするのも悪くはありません。