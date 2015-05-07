# gofmt

規約に沿うようにコードを整形してくれるコマンド  

```
$ gofmt --help
usage: gofmt [flags] [path ...]
  -cpuprofile="": write cpu profile to this file
  -d=false: display diffs instead of rewriting files
  -e=false: report all errors (not just the first 10 on different lines)
  -l=false: list files whose formatting differs from gofmt's
  -r="": rewrite rule (e.g., 'a[b:len(a)] -> a[b:]')
  -s=false: simplify code
  -w=false: write result to (source) file instead of stdout
```

- ディレクトリ指定をしない場合はカレントディレクトリの`.`で始まる
ファイル以外をすべてに対して実行します
- `-w`を付けない限りは上書きされません

## Option

| flags | description |
|:-------|:------------|
| -cpuprofile | ファイルにcpu profileを書き込む|
| -d | 適応前後の差分を表示 |
| -e | すべてのエラーを表示 |
| -l | gofmtでのフォーマット対象ファイルを表示 |
| -r | 指定したルールを適応した結果を表示 |
| -s | コードをシンプルにした場合の結果を表示 |
| -w | 結果を上書き |


### -r
小文字一文字はワイルドカードとして使用されます  
`pattern -> replacement` のように書く

- 余計なカッコがついているものを確認する  
`gofmt -r '(a) -> a' -l *.go`
- 余計なカッコを消す  
`gofmt -r '(a) -> a' -w *.go`
- `array[0:len(arrays)] -> arrays[0:]` のように簡略化する  
`a[b:len(a)] -> a[b:]`

### -s
自動的にコードをシンプルにする
- リテラルの簡略化  
`[]T{T{}, T{}}` -> `[]T{{}, {}}`  

- コードのシンプル化  
`s[a:len(s)]` -> `s[a:]`  
`for x, _ = range v {...}` -> `for x = range v {...}`


---
### 参照  
https://golang.org/cmd/gofmt/
