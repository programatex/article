# 2進数文字列から数値型への変換

0と自然数のみの対応です  
補数や小数などは対応していません  

## プログラムの解説
2進数の文字列を引数strsとして渡す  
返り値用の変数result=0を用意  
strsは2進数を1桁ごとに取得  
1ならば、\(2^桁\)をresultに足す  

## 数学的な解説
2進数の\(n\)桁目は、\(2^n\) の位になっています  
それぞれの桁で、1ならば\(2^n\)を足していけば数値になります  
( 0の場合は \(0(2^n)\) を足すことになるので計算する必要がありません )  
| 8の位 | 4の位 | 2の位 | 1の位 |  10進数 |  
| - | -| - | - | - |  
| 1 | 1 | 1 | 0 |  14 |  

例) 1110(2) の場合は、 \(8×1+4×1+2×1+1×0 = 8+4+2 = 14 \)  

## javascriptのプログラム例
引数strsに文字列として二進数を渡すと数値が返り値になります  
```js
function bin_to_dec(strs) {
    let result = 0;
    for (let i = 0; i < strs.length; i++) {
        if (strs[i]=="1") {
            result += (2**(strs.length-i-1));
        }
    }
    return result;
}
```

## c#のプログラム例
引数strsに文字列として二進数を渡すと数値が返り値になります  
```cs
static int bin_to_dec(string strs) {
    int result = 0;
    for (int i=0; i < strs.Length; i++) {
        if (strs[i]=='1') {
            result += (int)Math.Pow(2,strs.Length-i-1);
        }
    }
    return result;
}
```

## pythonのプログラム例
引数strsに文字列として二進数を渡すと数値が返り値になります  
```py
def bin_to_dec(strs):
    result = 0
    for i in range(len(strs)):
        if (strs[i]=="1") :
            result += 2**(len(strs)-i-1)
    return result
```
