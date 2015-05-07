# リテラル

リテラルとは特定の型による値を直接表記する際の書式のことです

## 整数リテラル
10進数以外の数字を表すには接頭語をつける必要があります  
8進数は`0`をつけます  
16進数は`0x`か`0X`をつけます
```
100
080
0xaaaaaa
0Xbbbbbb
```
## 浮動小数点リテラル
指数部を`e`か`E`で表記します
```
100.0
0.
.12
0123.0 // 123
12.3
5.21e-8
12.4E+11
2E5
.23e+23
```
## 虚数リテラル
小文字の`i`で表記します
```
0i
02i // 2i
0.i
1.e+0i
12.3e-2i
2E3i
.21i
```

## ルーンリテラル
Unicodeコードポイントに一致する整数値のことです  
一文字以上の文字をシングルクォートでくくって表現します  
アスキーエンコードされた文字はバックスラッシュによるエスケープを使い表します
```
\a   U+0007 alert or bell
\b   U+0008 backspace
\f   U+000C form feed
\n   U+000A line feed or newline
\r   U+000D carriage return
\t   U+0009 horizontal tab
\v   U+000b vertical tab
\\   U+005c backslash
\'   U+0027 single quote  (ルーンリテラル内で有効)
\"   U+0022 double quote  (文字リテラル内で有効)
```

## 文字リテラル
文字シーケンスからできる文字列定数のことです  
二種類存在します
- raw(未加工)  
バッククオートで囲みます  
UTF-8エンコードにおいて解釈しない  
この中ではバックスラッシュも意味を持ちません  
- interpreted(解釈有)  
ダブルクオートで囲みます  
バックスラッシュによるエスケープを解釈します

以下はすべて同じ文字列を示します  
```
"日本語"                                 // UTF-8 input text
`日本語`                                 // UTF-8 input text as a raw literal
"\u65e5\u672c\u8a9e"                    // the explicit Unicode code points
"\U000065e5\U0000672c\U00008a9e"        // the explicit Unicode code points
"\xe6\x97\xa5\xe6\x9c\xac\xe8\xaa\x9e"  // the explicit UTF-8 bytes
```
