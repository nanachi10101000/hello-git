#hello-git

Q:為何使用git與github? A:取代傳統以資料夾或檔案命名區分版本，紀錄最新版本、版本差異、誰撰寫、何時寫...等

<h1>設置環境變數</h1>
<ol>
<li>$ git config --global user.name "XXX"</li>
<li>$ git config --global user.email "XXX"</li>
</ol>

$git config --list檢視設定內容

<br>

$ git init 建立.git夾，管理資訊，不想管理則刪除$rm - r .git

<img src="https://i.imgur.com/iYbhwu4.png">

```
$git status 查看狀態

$git add XXX.XXX 加入檔案

$git commit -m "這次commit資訊"

$git diff 檢視修改差異

$git commit -am "XXX" 加入過檔案，又有修改使用

$git restore --staged login.html 反悔加入暫存

$git restore login.html 反悔修改

$git checkout <commit> XXX.XXX 讓XXX檔案回到特地版本

	      HEAD~2 XXX.XXX 回到前兩個版本

              HEAD	     回到現在版本


```

