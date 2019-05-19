# gott
gott script use fetch
コマンドプロンプトの為のスクリプト言語。
```
必要なコマンド
ep [string]：開始ヘッダ
＠名前「[string]」：会話文
＠数字「[string]」：分岐
g[[string]]：変数
ef[[string]]：エフェクトコマンド
goto [string or url]：スクリプト遷移
```

```
分岐構文。
(x)?goto xyz:goto ppp
```
# example
```
set mean the definition.
put mean the apply the set command
mes mean the message command
got mean the goto label
wai mean the wait, if press any key to go 
//log comment
/*slice comment*/
```

```txt
set:
imageload https://gnjo.github.io/use.js
xyz imageload('xyzeeeaaa').effect('grayscale');
zzz imageload('pppp')
---

xyz
zzz
got https://gnjo.github.io/ep1.got
```

```
//inner process
gott.g['xyz']=void 0
gott.g['xyz'] =imageload('xyzeeeaaa').effect('grayscale').bind(this);
gott.g['zzz'] =imageload('pppp').bind(this);

gott.g['xyz'].call(this)
gott.g['zzz'].call(this)
gott.got.call(this,url)
```

# first command
```js
gott(`
set:
xyz imageload('xyzeeeaaa').effect('grayscale');

---
set zzz imageload('pppp')

set https://gnjo.github.io/use.js
put xyz
put zzz
:loop1
this is a command
1 or 2
?flg
1:got loop2
2:got loop1
:got loop1
---
:loop2

got https://gnjo.github.io/ep1.got

`)
```

command
```js
gott(query,script,debugflg)
//gott('.disp',``,true)
```

