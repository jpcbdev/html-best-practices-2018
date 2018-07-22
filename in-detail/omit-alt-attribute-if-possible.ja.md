# 可能ならば`alt`属性は省略する

たまにどのような文字列が適切な`alt`属性の値かわからない場合もあります。

悪い例:

    <img alt="CAPTCHA" src="captcha.cgi?id=82174">

良い例:

    <img src="captcha.cgi?id=82174" title="CAPTCHA">
    (If you cannot see the image, you can use an <a href="?audio">audio</a> test instead.)


## 解説

必須であるはずの`alt`属性も、ごく限られた状況では使うべきではありません。というよりも適切な`alt`属性の値がどうやっても指定できない場合には指定できません。

例えばCAPTCHAの画像です。このサービスの仕組み上、その中身を機械的にたどれるようでは無意味になってしまうからです。こういった場合は良い例で挙げたように、何も指定せず、かつ別の方法でフォールバックするべきです。

他には、ユーザーがアップロードした画像をサービスがマークアップして表示する場合も指定すべきではありません。ユーザーからその画像について説明を受けない限り、どのような写真でどのような意図をもっているのかを確定できないからです。一部で画像を機械学習で処理することで`alt`属性の値を生成する試みもありますが、`alt`属性の値が画像の説明ではないことを考えると、あくまでも次善の策でしょう。画像の閲覧者に誤解させないようにするためにも空にするもの、と考えた方が無難です。