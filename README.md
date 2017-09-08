# natukadai
夏休みの簡単ゲーム制作についてのプレゼン

# ***EXシューター***

[!]()//画像

## レッツプレイ！

[![]()]()//画像とリンク

##　概要

とめどなく流れてくるボールを消していくゲームです。  
段によって得点と消しやすさが違うので、  
取れそうなボールをどんどんとっていきましょう。  

### ヒント

当たり判定が少なく、全体的に消えにくくなっています。  
連続したボールをねらい目として、連続クリック！！  
端にたどり着いてしまうと、減点１ポイント。  
どんどん減っていくので、得点をゲットしたからといって、  
油断しないように。

## 操作方法

クリックでゲームを始めます。 

[!]()//スタートシーン画像

マウスをボールに合わせ、 　
クリックでボールを消します。

[!]()//ゲームシーン画像

## 開発

ボールの動き、当たり判定、  
消える処理など作った。  
音楽をつけた。  
すべて授業内容内でやったことを使いました。  

##　参考資料

Instancieteのコードの書き方  
```cs

		Quaternion qua = new Quaternion ();
		qua = Quaternion.identity;
    //回転の角度

Instantiate (blockPrefab, pos, qua);	
//このコードの書き方。


```

### リンク

[]()//参考資料のリンク
[]()
[]()
[]()

##　反省（考察）

インスタンスが設定されていなかったり、
（NullRefarenceExeptionなど、、）

ボールの当たり判定、
if分の処理との、時間差によって、
ポジションを受け取るのが遅れているのか、
ボールの座標を受け取る時は
中心の座標一点しかうけとっていないので、
当たり判定が一点しかないのか、
たぶん後者でしょう。。

ちょっと試したコードが、、

```cs
//コメントアウトしたコードなど
```

もうちょっとで全部できたと思うので、
次回はがんばりたい。。
