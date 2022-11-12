# ベクトル

## 内容
・ベクトル同士の和  
・スカラー倍  

## ベクトルについて

幾何でのベクトルは、「向きと大きさをもつ量」を意味します。

## プログラムでの表現

配列を使って表現されます。
```js
vector2 = [x,y]
vector3 = [x,y,z]
```

## ベクトル同士の和
それぞれの値を足していくだけです。
```js
function add(vec1,vec2) {
    if (vec1.length!=vec2.length) {return false;} // error
    for (let i=0;i<vec1.length;i++) {vec1[i]+=vec2[i];}
    return vec1;
}
```
## ベクトルのスカラー倍
ベクトルの全ての値にスカラーを掛けます
```js
function scalarproduct(vec1,scalar) {
    for (let i=0;i<vec1.length;i++) {vec1[i]*=scalar;}
    return vec1;
}
```