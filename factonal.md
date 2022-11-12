# 自然数階乗

## プログラムの解説
n! の n を引数nとして渡す  
返り値用の変数result=1を用意  
ループ用の変数iを用意  
iが 2からnまで 1づつ増える ループを用いて、resultにiを掛ける  
※ result=1によりi=1の場合は初めからあるので、ループで用いるiの初期値は2でよい (1を掛けても変わらないので初期値をi=1にしても良い)

## 数学的な解説
\(n!\) は 1からnまでの全ての整数の積のことです  
\(n!\) の形であらわされます  
例) \( 5! = 1\times2\times3\times4\times5 = 120 \)  

## javascriptのプログラム例
```js
function factonal(n) {
    let result = 1;
    for (let i = 2; i <= n; i++) {
        result *= i;
    }
    return result;
}
```