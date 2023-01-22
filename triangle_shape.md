# 三角形の形状

## 内容
・三辺の長さから、三角形の形状(鈍角・直角・鋭角)を求める

## 使用する内容
最も長い辺をAとして、  
鋭角三角形  \( A^2 < B^2 + C^2 \)  
直角三角形  \( A^2 = B^2 + C^2 \)  
鈍角三角形  \( A^2 > B^2 + C^2 \)  

## プログラムの解説
3辺\(a,b,c\)の長さを引数として渡す  
1, 最も長い辺を求め、変数longestに代入  
2, その他の辺を求め、配列otherに追加  
3, 比較する  

## javascriptのプログラム例
引数lに配列として三辺の長さを渡すと数値が返り値になります
```js
function triangle_shape(l) {
    let longest = 0;
    let longest_i = 0;
    for (let i=0;i<3;i++) {
        if (l[i]>longest) {
            longest = l[i];
            longest_i = i;
        }
    }
    let other = [];
    for (let i=0;i<3;i++) {
        if (i!=longest_i) {
            other.push(l[i]);
        }
    }
    let ls = longest**2;
    let rs = other[0]**2+other[1]**2;
    if (ls==rs) { return 0 } // 直角三角形
    else if (ls>rs) { return 1 } // 鈍角三角形
    else if (ls<rs) { return 2 }; // 鋭角三角形
}
```
### 使い方の例
```js
let value = triangle_shape([5,4,3]);
console.log(value); // 0
```