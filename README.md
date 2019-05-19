# gott
gott script use fetch

```
必要なコマンド
ep [string]：開始ヘッダ
＠名前「[string]」：会話文
＠数字「[string]」：分岐
g[[string]]：変数
ef[[string]]：エフェクトコマンド
goto [string or url]：スクリプト遷移
```
# example
```
set mean the definition.
put mean the apply the set command
got mean the goto label
del mean set definition clear
log mean debug command like a console.log
```

```txt
set:<= any lines shortcut
xyz imageload('xyzeeeaaa').effect('grayscale');

---<= reset block
set zzz imageload('pppp')

set https://gnjo.github.io/use.js
put xyz
put zzz
got https://gnjo.github.io/ep1.got
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
got https://gnjo.github.io/ep1.got

`)
```
