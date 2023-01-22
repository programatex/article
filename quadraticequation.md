# 二次方程式の実数解

二次方程式は
\(ax^2 + bx + c = 0\)
で表されます。  
いい感じに式変形すると、(*追記予定)  
\(\displaystyle x = \frac{-b±\sqrt{b^2-4ac}}{2a}\)  
になります。  
  
この記事では、
\(\displaystyle x = \frac{-b±\sqrt{b^2-4ac}}{2a}\)  
のプログラムを取り上げます  

## javascriptのプログラム例
引数\(a,b,c\)に二次方程式\(ax^2 + bx + c = 0\)の\(a,b,c\)の値を渡すと、解の配列が戻り値になります  
実数解がない場合はfalseが戻り値になります  
```js
function quadraticequation(a,b,c) {
    let d = b**2-4*a*c;
    let x;
    if (d==0) { x = [(-b)/(2*a)]; }
    else if (d<0) { return false; }
    else { x = [(-b+Math.sqrt(d))/(2*a),(-b-Math.sqrt(d))/(2*a)]; }
    return x;
}
```