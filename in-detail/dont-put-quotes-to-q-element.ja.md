# `q`要素内へ引用符は置かない

引用符はブラウザーが提供します。

悪い例:

    <q>“For writing maintainable and scalable HTML documents”</q>

良い例:

    <q>For writing maintainable and scalable HTML documents</q>

同じく良い例:

    “For writing maintainable and scalable HTML documents”


## 解説

段落内で他のソースから引用を行う場合に使う`q`要素では、引用符は主にブラウザー（もしくはCSS）によって提供されます。仕様では明確に`q`要素の内部等に引用符が「現れてはならない」とされています。

    <p>漱石はその小説内で猫の鳴き声を<q>ニャーニャー泣いていた</q>としている。</p>

また、どのような引用符で括られるかは、ブラウザーによってもそうですが、HTML文書の言語指定によっても変化することがあります。例えばGoogle Chrome 43では言語指定が英語（en）の場合は“と”で、日本語（ja）の場合は「と」で括られます。この挙動は、日常生活で引用の時に使われる記号の言語間における差異を吸収してくれることになります。

もし、どうしても引用符を完全に制御したいと考えているのならば、*引用符を`q`要素の代わりに*直接記述します。

    <p>漱石はその小説内で猫の鳴き声を『ニャーニャー泣いていた』としている。</p>

仕様でもこのように`q`要素を使わず明示的に引用符を使用しても良いとされています。`q`要素を使うべきかどうかは判断が難しいところではありますが、間違った使い方だけはしないようにしましょう。
