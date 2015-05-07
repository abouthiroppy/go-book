# はじめに

## 文字コード

文字コードは、基本UTF-8でエンコードされたUnicodeです  
他の文字コードを扱いたい場合は変換する必要があります  

## コメント
一行に対しての場合は`//`を使います  
複数行をまたぐ場合は`/* */`を使います

## 予約語
```
break        default      func         interface    select
case         defer        go           map          struct
chan         else         goto         package      switch
const        fallthrough  if           range        type
continue     for          import       return       var
```

## 特殊なトークン
```
+    &     +=    &=     &&    ==    !=    (    )
-    |     -=    |=     ||    <     <=    [    ]
*    ^     *=    ^=     <-    >     >=    {    }
/    <<    /=    <<=    ++    =     :=    ,    ;
%    >>    %=    >>=    --    !     ...   .    :
     &^          &^=
```
