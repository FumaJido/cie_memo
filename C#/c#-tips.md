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
