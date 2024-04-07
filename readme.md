initial commit

- 本書をpythonで実装したレポジトリ(https://github.com/nekoumei/cibook-python/tree/master)を参考にしている

- 1章：セレクションバイアスとRCT

- 2章：介入効果を測るための回帰分析
    - 因果推論における回帰分析は，指定した変数の傾向が似ているサンプル同士を比較する．
    - よって，セレクションバイアスを発生させていると考えられる変数を指定することで，それらが似通った状態，つまりセレクションバイアスが軽減された状態で効果を検証できる

- 3章：傾向スコアを用いた分析
    - 回帰分析は共変量の選定が重要であり，非常に難しいプロセスである
        - 実際に分析をすると，目的変数Yがどのような仕組みで決定されているかについて，十分な情報が得られない場合ある
        - このような場合は，共変量の選択が難しい
    - また，ユーザーの行動ログなどを扱う場合，様々な種類のデータが得られるため，回帰分析ではどのような共変量を選択すればよいかを選択するプロセスは，時間を大量に消費する上に，非常に難しい
    - 介入の割り当て確率が同一のサンプルで行った比較は，セレクションバイアスを軽減できるという状況を利用した分析方法
        - しかし，介入の割り当て確率自体が手に入ることは珍しく，分析者が推定する必要がある