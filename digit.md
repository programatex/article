# 整数の桁ごとの値を取得

## javascriptのプログラム例
引数num,nに整数numとn進数を渡すと、n進数として桁ごとに分割した整数の配列が返り値になります  
```js
function getdigits(num,n=10) {
    let dcnt = 0;
    while (true) {
        if (n**dcnt>num) { break; }
        dcnt++;
    }
    let ret = new Array(dcnt);
    for (let d=1;d<=dcnt;d++) {
        ret[dcnt-d] = num%(n**d)/(n**(d-1));
        num = num-num%(n**d);
    }
    return ret;
}
```