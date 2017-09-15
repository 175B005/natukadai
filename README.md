# natukadai
夏休みの簡単ゲーム制作についてのプレゼン
---
# ***EXシューター***

[!]()//画像

## レッツプレイ！

[![]()]()//画像とリンク
---
##　概要

とめどなく流れてくるボールを消していくゲームです。  
段によって得点と消しやすさが違うので、  
取れそうなボールをどんどんとっていきましょう。  

## 操作方法

クリックでゲームを始めます。 

[!]()//スタートシーン画像

マウスをボールに合わせ、 　
クリックでボールを消します。

[!]()//ゲームシーン画像
---
## 開発

ボールの動き、当たり判定、  
消える処理など作った。  
音楽をつけた。  
すべて授業内容内でやったことを使いました。  
---
##　参考資料

Instancieteのコードの書き方  
```cs

		Quaternion qua = new Quaternion ();
		qua = Quaternion.identity;
    //回転の角度

Instantiate (blockPrefab, pos, qua);	
//このコードの書き方。


```
## こだわり

### スコア
```cs
	public static void MaxScoreC(){
		_Resultscore = _score;

			if (_Maxscore < _Resultscore) {
			_Maxscore = _Resultscore;
			}
```
### 端につくと自動で消える
```cs
if (CompareTag ("mato")) {
			transform.position += new Vector3 (-0.03f, 0f, 0f);
			if (transform.position.x <= -4.56f) {
				BallCrate.countball -= 1;
				BallCrate.high = keyword1;
				GameParams.DeScore (1);
				Destroy (gameObject);
			}
		}
	
if (countball < 11) {
		switch (high) {
		case keyword1:
			Instantiate (blockPrefab, pos, qua);	
			countball += 1;
			//Debug.Log (countball);
			break;
		case keyword2:
			Instantiate (blockPrefab1, pos1, qua);	
			countball += 1;
		//	Debug.Log (countball);
			break;
		case keyword3:
			Instantiate (blockPrefab2, pos2, qua);	
			countball += 1;
			//Debug.Log (countball);
			break;
		}		
```
---
### リンク

[Instancieteのprefabからの生成](http://qiita.com/JunShimura/items/7e45fc6236cf97914041)  
[Unity3dスクリプトリファレンス](https://docs.unity3d.com/ja/540/ScriptReference/MonoBehaviour.OnMouseOver.html)  
[Unity3dスクリプトリファレンス](https://docs.unity3d.com/ja/540/ScriptReference/Transform.SetParent.html)  
[親子関係](http://qiita.com/YuwUnknown/items/69cf5bbe59452e645d92)   
[親子](https://increment-log.com/unity-instantiate-nesting/)  
[わかりやすい親子](http://sawalemounity.hatenablog.com/entry/2017/07/27/160636)  
[効果音ラボ](https://soundeffect-lab.info/)　　

---
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
---
