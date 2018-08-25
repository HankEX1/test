//桌面新增資料夾
//右擊，git bash
//初始化流程
git config --global user.name 'your_Github_id'
git config --global user.email 'your_email_address'
//配置成功，初始化一個新的Git倉庫
//創建文件夾 
mkdir test // 創建test 資料夾
//在文件內初始化git (創建git倉庫)，以上創建了test資料夾，我們想把這個當作我們的倉庫，於是先改目錄到test資料夾，then git init
cd test
git init

//向剛剛所新增的倉庫新增文件
touch a1.php//創建一個 a1.php的文件
git status //確認當前文件狀態，紅色代表未add的狀態，若完成add，則該文件名稱顯示綠色
// (use "git add <file>..." to include in what will be committed)
git add a1.php//將a1.php添加到倉庫暫存區
git status//再次確認狀態則顯示以下，已經移至unstage狀態
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
//將暫存區文件存至倉庫commit指令
$ git commit -m '此處為描述 add a1.php'
[master (root-commit) b67f30a] 此處為描述 add a1.php
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 a1.php
//再執行一次git status
$ git status
On branch master
nothing to commit, working tree clean
//提交成功
# 整理以上可知添加文件大致上為以下指令
  git add file_name.副檔名
  git status
  git commit -m '敘述'  //創帶一次帶message的提交，方便之後查詢
  
