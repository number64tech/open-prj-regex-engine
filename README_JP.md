## 簡易正規表現エンジン

英語版は[こちら](./README.md)  

### 概要

+ 目的  
  - 簡易正規表現エンジンの開発。  
+ 機能  
  - 検索対象文字列を正規表現で検索し、一致する部分文字列の最大の長さを出力する。

### 前提  

+ 検索対象文字列  
  - S: `a-z` のアルファベット小文字のみを含む、1000文字以下の文字列  
+ 正規表現文字列  
  - R: `a-z` のアルファベット小文字と, `.?*` のみを含む、1000文字以下の文字列  
+ Ver 1.0時点でのスコープ  
  - 正規表現 `.`, `*`, `?` の機能に対応する。
+ Javaの正規表現機能は使用しない

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


