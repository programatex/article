# 数式のテスト

```math
<mtable><mtr><mtd><msup><mrow><mo>( </mo><mi>a </mi><mo>+ </mo><mi>b </mi><mo>) </mo></mrow><mn>2 </mn></msup></mtd><mtd><mo>= </mo></mtd><mtd><msup><mi>c </mi><mn>2</mn>
</msup><mo>+ </mo><mn>4 </mn><mo>⋅ </mo><mo>(</mo>
<mfrac><mn>1 </mn><mn>2 </mn></mfrac><mi>a </mi><mi>b </mi><mo>)</mo>
</mtd></mtr><mtr><mtd><msup><mi>a </mi><mn>2</mn>
</msup><mo>+ </mo><mn>2 </mn><mi>a </mi><mi>b </mi><mo>+ </mo><msup><mi>b </mi><mn>2</mn>
</msup></mtd><mtd><mo>= </mo></mtd><mtd><msup><mi>c </mi><mn>2</mn>
</msup><mo>+ </mo><mn>2 </mn><mi>a </mi><mi>b</mi>
</mtd></mtr><mtr><mtd><msup><mi>a </mi><mn>2</mn>
</msup><mo>+ </mo><msup><mi>b </mi><mn>2</mn>
</msup></mtd><mtd><mo>= </mo></mtd><mtd><msup><mi>c </mi><mn>2</mn></msup></mtd></mtr></mtable>
```
上記  
https://developer.mozilla.org/ja/docs/Web/MathML/Examples/MathML_Pythagorean_Theorem  
LICENSE: https://github.com/mdn/translated-content/blob/main/LICENSE.md  

- - - -

```math
<mi>a</mi>
<mo>+</mo>
<mi>b</mi>
<mo>-</mo>
<mn>3</mn>
```

文章中の \( a^2−b^2 \) 数式  
  
\(a^2 + b^2 = c^2\)  
\[a^2 + b^2 = c^2\]  

\begin{cases}
a^2 + b^2 = c^2 \\
b^2 + a^2 = c^2 \\
\end{cases}

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