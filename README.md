#hello-git 筆記

Q:為何使用git與github? A:取代傳統以資料夾或檔案命名區分版本，紀錄最新版本、版本差異、誰撰寫、何時寫...等

<h1>設置環境變數</h1>
<ol>
<li>$ git config --global user.name "XXX"</li>
<li>$ git config --global user.email "XXX"</li>
</ol>

$git config --list檢視設定內容

<br>

$ git init 建立.git夾，管理資訊，不想管理則刪除$rm - r .git

```
$git nano XXX.XXX 修改XXX檔案內容，如沒有會新建立一個

$git cat XXX.XXX 獲取XXX內容

$cd 切換位置

$pwd 檢視所在位置
```

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

```
$git log 查看提交紀錄

$git log README.md 查看REANDE

$git log -p README.md 查看修改細節

$git log --grep="XXX" 搜尋關鍵字XXX

$git blame README.md 查看誰寫的 //十十千

```

<h1>每個人的提交習慣不同，團隊最好要有一致性。</h1>


```
$git restore --staged XXX.XXX 從暫存中移除XXX檔案
r
$git rm XXX.XXX 在git中刪除XXX檔案

 
```

<h1>建立分支與合併</h1>

```
$nano ~/.gitconfig 

[init]

	defaultBranch = main //預設改為main

$git branch -m -master main 分支改為main


```

<h1>分支指令</h1>

$git branch 檢視分支

$	    XXX 建立XXX分支

$    switch  XXX 切換XXX分支


```

分支XXX功能用於開發其他功能，待功能完成後必須將分支XXX merge 回去主分支

```
$ git switch main 切換

      merge  XXX //XXX加入main
```

<h1>github repo</h1>
```
$git remote add origin https://github.com/nanachi10101000/hello-git.git 建立github repo

$git push -u origin main 推送程式碼 分支main
```

<p>錯誤發生頻率高且嚴重優先處理權高</p>

-a -> 全部

-f -> 強制

<hr>

<h1>NodeJS</h1>

簡單來說就是在瀏覽器以外環境執行JS

NodeJS暨不是程式語言，也不是框架

LTS: long-term support 長期維護版
- Current: 最新的、目前的 //平常自己測
- Active LTS: 正在積極維護跟升級中的版本　//建議安裝
- Maintenance LTS: 維護中的 LTS 直到生命週期結尾
- EOL: end of life

windows: https://github.com/coreybutler/nvm-windows/releases

//git Bash要以管理員身分開啟

```
# 列出可以安裝的版本
$ nvm ls-remote 14
# windows版本
$ nvm list available

# 安裝最新的 LTS
$ nvm install 14.17.6

# 切換版本
$ nvm use 14.17.6

# 確認目前 node 的版本
$ node -v

# 列出你電腦裡 node 的版本
$ nvm ls
# windows 用 list
$ nvm list

# 設定預設版本
$ nvm alias default 14.17.6
```

