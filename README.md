# Bower 基本使用教學:memo:
因為小弟覺得這東西非常實用，所以就簡單寫個教學文，順便記錄一下:memo:，希望能幫助想學的人:smile:

如果教學有誤再請糾正:sweat_smile:

相信大家一定常遇到 js 套件一更新，就要重新再去網路上抓，然後再放回自己的專案中，

其實，這是一個非常沒有效率的方法 :persevere:

今天，和大家介紹一個管理套件的好工具  [Bower](https://bower.io/)

## Bower 介紹

[Bower](https://bower.io/) 官網

## 前置安裝作業 - 安裝 node.js

因為我們需要使用 npm ( Node Package Manager )，而他是 Node.js 的套件（package）管理工具，

所以我們必須先安裝 <b>node.js</b>，請先到 [Node.js](https://nodejs.org/en/) 官網，下載後安裝即可，如何確認是否安裝成功呢 ?

在 cmd (命令提示字元) 輸入

```
node -v
```

如果有跑出 node.js 版本號代表安裝成功，如下圖

![alt atg](http://i.imgur.com/EQ7MnfL.png)

然後也請安裝 [git](https://git-scm.com/)


## 開始安裝 Bower

參考 [Bower](https://bower.io/) 官方教學

使用 cmd (命令提示字元) 輸入以下指令

```
npm install -g bower
```

## 開始使用 Bower

接著在目標資料夾底下使用 cmd (命令提示字元) 輸入以下指令
```
bower install <package>
```

例如我們安裝 jquery

```
bower install jquery
```
![alt atg](http://i.imgur.com/5zn388m.png)
 
預設安裝的資料夾是 <b>bower_components</b>
 
另外，因為不一定每一個套件都會在 Bower 之上，所以我們也可以透過 Bower 安裝 Github 上面的套件，

例如，我們從 Github 上安裝 bootstrap
```
bower install https://github.com/twbs/bootstrap.git
```

![alt atg](http://i.imgur.com/mvCsemA.png)


可以使用以下指令，觀看目前資料夾下有安裝的套件
```
bower list
```
![alt atg](http://i.imgur.com/g4tPZUq.png)

不知道大家有沒有發現呢 ?

每次安裝我們都要

```
bower install jquery
bower install bootstrap
```

雖然很簡單，但很煩 :scream:

有沒有一次安裝我們需要的全部套件呢 ?

有的 ! 

讓我們來建立 Bower 設定檔 bower.json 吧~

## 建立 Bower 設定檔 bower.json

如何建立 Bower 設定檔 bower.json 呢 ?

在目標資料夾底下使用 cmd (命令提示字元) 輸入以下指令

```
bower init
```
如果說明不想打，直接按 Enter 即可

![alt atg](http://i.imgur.com/RYGxqoj.png)

執行完成後，你會發現資料夾底下多出 <b>bower.json</b>

接著在目標資料夾底下使用 cmd (命令提示字元) 輸入以下指令

```
bower install jquery-validation --save
```

再去打開 <b>bower.json</b>  ，你會發現多出一些東西 ( 如下圖紅色框起來的地方 )
![alt atg](http://i.imgur.com/AlZuIZb.png)

假如今天我們需要安裝  jquery-validation 以及 bootstrap ， 我們可以打開 bower.json 輸入套件名稱

![alt atg](http://i.imgur.com/czgJeNi.png)

接著在目標資料夾底下使用 cmd (命令提示字元) 輸入以下指令

```
bower install 
```
![alt atg](http://i.imgur.com/Iyx48YC.png)

一次就幫你安裝全部套件 :blush:


## 如何修改預設 Bower 安裝路徑資料夾

剛剛前面有提到，bower 預設安裝的資料夾是 <b>bower_components</b>，

那我們該怎麼修改他的默認路徑呢 ?

首先，先建立一個  <b>.bowerrc</b> 檔案

P.S 因為 Windows 無法直接建立一個沒有名稱卻只有副檔名的檔案

所以，我們必須在 cmd (命令提示字元) 輸入以下指令
```
touch .bowerrc
```
![alt atg](http://i.imgur.com/QE4t7J6.png)

路徑底下就會多出一個  <b>.bowerrc</b> 檔案

接著在 <b>.bowerrc</b> 檔案裡輸入以下文字
```
{
  "directory": "js/javascript" 
}
```
以後使用 bower 安裝套件，默認就會安裝到路徑底下的 <b>js/javascript</b>

