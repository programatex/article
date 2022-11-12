# 自然数累乗

## プログラムの解説
\(x^n\)を引数x,nとして渡す  
返り値用の変数result=1を用意  
ループを用いて1にxをn回掛ける  

## 数学的な解説
\(x^n\) は xをn回掛けたもの  

例) \(2^3\) の場合は、\(2\times2\times2=8\)  

## javascriptのプログラム例
引数x,nに整数としてx^nを渡すと結果の整数が返り値になります  
```js
function exponentiation(x,n) {
    let result = 1;
    for (let i = 0;i < n;i++) {
        result *= x;
    }
    return result;
}
```

## Cのプログラム例
引数x,nに整数としてx^nを渡すと結果の整数が返り値になります  
```c
int exponentiation(int x,int n) {
    int result = 1;
    for (int i=0;i<n;i++) {
        result *= x;
    }
    return result;
}
```