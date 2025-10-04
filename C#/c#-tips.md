# C#のTips集

## swich文とreturnの併用について
```swich```は基本的に以下の形で使用される。
```
swich(式)
{
  case リテラル1:
    ~~~
    break;
  
  case リテラル2:
    ~~~
    break;
  
  case リテラル3:
    ~~~
    break;
}
```
一方で、```return```を使う場合は```break```は不要である。
```
swich(式)
{
  case リテラル1:
    ~~~
    return ~~~;
  
  case リテラル2:
    ~~~
    return ~~~;
  
  case リテラル3:
    ~~~
    return ~~~;
}
```

## 文字列の扱いについて
Stringクラスを使用した文字列操作を行う。
### 前後の空白文字を取り除く
```.Trim()```を使う。
```
var str = "　　オブジェクト指向　　";
var str2 = str.Trim();
Console.WriteLine($"[{str}]");
Console.WriteLine($"[{str2}]");
============================
[　　オブジェクト指向　　]
[オブジェクト指向]
```

## 配列の扱いについて
### 要素が配列の何番目かを取得する
```Array.IndexOf(array, input)```
```
static int GetIndex(string input, string[] array)
{
return Array.IndexOf(array, input);
}
###（例）
string[] letters = {"a", "b", "c"};
GetIndex("a", letters); // 出力0

```
