## Simple Regex Engine

README(ja) is [here](./README_JP.md).

### Outline

+ Object
  - Developing an application of simplified regex engine. 
+ What does it do?
  - It finds longest matching partial string using specified Regex from target string , and outputs its length.

### Premise  

★ translating.. now



+ Target string  
  - S: `a-z` のアルファベット小文字のみを含む、1000文字以下の文字列  
+ Regex Pattern  
  - R: `a-z` のアルファベット小文字と, `.?*` のみを含む、1000文字以下の文字列  
+ Scope at Version 1.0  
  - 正規表現 `.`, `*`, `?` の機能に対応する。
+ Note  
  - 

### 制限事項

+ 正規表現では、`*` と`?` は先頭には現れない
  - それらの文字の前の文字は必ずアルファベット小文字または`.`とする。

### 仕様

+ 起動パラメータ
  - なし
+ 入力仕様  
  - 起動後、標準入力から2行の引数を受け取る。各行はEnterキーで確定する。
  - 1行目= 文字列 S
  - 2行目= 文字列 R  
+ 処理
  - Sの中で、Rが一致する箇所を求め、それらのうち最長となる文字数を取得する。  
+ 出力仕様  
  - 最長文字数を標準出力に出力する。  
  - 一致する部分が無い場合は、-1 を出力する。
  - 前提および制限事項を満たさない文字列が与えられた場合、メッセージを出力し異常終了する。

