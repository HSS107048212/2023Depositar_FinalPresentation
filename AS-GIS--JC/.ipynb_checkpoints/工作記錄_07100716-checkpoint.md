# 7月第二週

## July 10 
* 建立[GitLab](https://gitlab.com/) 帳號，並開啟[Group](https://gitlab.com/2023sunmmersinica/JulyW2Homework)，以及在其中建立一個Project。
* 建立[GitHub](https://github.com/HSS107048212)帳號： ubo11185@gapp.nthu.edu.tw
* [Install Git](https://www.atlassian.com/git/tutorials/install-git#linux) (看 Debian / Ubuntu 小節) (先安裝 + 設定)
* [Ecosystem of tools](https://executablebooks.org/en/latest/tools/)
* [Jupyter Notebook Publishing](https://myst-nb.readthedocs.io/en/latest/index.html)
* 閱讀 [Pro Git](https://git-scm.com/book/en/v2) Ch.Getting Started
* 閱讀 Jupyter Book 與 MyST 相關介紹
    * https://executablebooks.org/en/latest/tools/
    * https://jupyterbook.org/
* [參與月聚會： OpenStreetMap x Wikidata Taipei 54](https://hackmd.io/@Jessy-NTHU-HSS-IEEM/BJy04Itt3)
* 出現Virtualbox does not run: NS_ERROR_FAILURE問題，重新裝設新的VM+Ubuntu，以及Git.


## July 11 

* 閱讀 [Pro Git](https://git-scm.com/book/en/v2) Ch.Git Basic
    * ![](https://git-scm.com/book/en/v2/images/lifecycle.png)
    * ![](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*aSFDaNod0F550ubGZ6DTOw.png)
    * Observing "diff, add, rm, mv"
    * Observing "log"
* 完成W3school：關卡至Git Pull from GitHub 


## July 12 
* https://jupyterbook.org/en/stable/start/create.html
* https://jupyterbook.org/en/stable/start/build.html
* https://jupyterbook.org/en/stable/start/new-file.html
* https://jupyterbook.org/en/stable/start/publish.html
* https://jupyterbook.org/en/stable/start/example-book.html


## July 13 
* [Build beautiful, publication-quality books and documents from computational content.](https://jupyterbook.org/en/stable/intro.html)
* Pelican圖片本機位置設定，完成可以輸出
    * ![](https://hackmd.io/_uploads/Hkgf_7pYn.png)
* JB可以輸出程式結果
    * ![](https://hackmd.io/_uploads/BkfZcmpK3.png)
* 參加實習生分享，發現大家近半數做簡報。


## July 14 
* 在錯誤的嘗試中，盤點出Local/GitHub工作流程
* 成功在虛擬機的Terminal操作工作流程。
* 成功在本機的JupyterLab的Terminal操作工作流程。
* 成功透過GitHub實現「虛擬機」與「本機JupyterLab」修正的Jybook資料相互下載、修改、上傳。
* [GitHub Alternatives (Free, Paid, Self-Hosted)](https://tutswiki.com/github-alternatives/)
* [Comparing confusing terms in GitHub, Bitbucket, and GitLab (2017)](https://about.gitlab.com/blog/2017/09/11/comparing-confusing-terms-in-github-bitbucket-and-gitlab/)

```sequence
Local Terminal->GitHub: #git clone
GitHub->Local Terminal: 傳給local前版資料
Local Terminal->Local Terminal: 文字編輯器進行內容增減
Local Terminal->JupyterBook: #jb build
JupyterBook->Web: 透過本機位置呈現
Local Terminal->Local Terminal: #git add --all
Local Terminal->Local Terminal: #git commit (Describe)
Local Terminal->GitHub: #git push
GitHub->GitHub: 顯示最新檔案
Local Terminal->GitHub: #ghp-import（生成公開網頁）
GitHub->Web: Setting/Pages（查看公開網頁）
```

## Addtional Helpers from Google
### Git in Terminal
* [Git clone](https://github.com/doggy8088/Learn-Git-in-30-days/blob/master/zh-tw/25.md)
* [Makefile教程](https://blog.csdn.net/weixin_38391755/article/details/80380786?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522168894642616800188523927%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=168894642616800188523927&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-80380786-null-null.142^v88^control_2,239^v2^insert_chatgpt&utm_term=makefile&spm=1018.2226.3001.4187)
* [Compiler error - msgfmt command not found](https://stackoverflow.com/questions/9500898/compiler-error-msgfmt-command-not-found)
* [Git Explained — not just commands — in Under 8 minutes!](https://towardsdatascience.com/git-help-all-2d0bb0c31483#:~:text=git%20status,not%20in%20index%20and%20repository)
* [Git Commands](https://docs.gitopia.com/category/git-commands)
* [After installing with pip, "jupyter: command not found"
](https://stackoverflow.com/questions/35313876/after-installing-with-pip-jupyter-command-not-found)
* [How To Fix "fatal: not a git repository" in Git?](https://timmousk.com/blog/fatal-not-a-git-repository/#:~:text=The%20fatal%3A%20not%20a%20git%20repository%20error%20happens%20because%20you,t%20initialize%20the%20Git%20repository.)


### GitHub
* [git push解决办法： ! [remote rejected] master -＞ master (pre-receive hook declined)](https://blog.csdn.net/daipianpian/article/details/108233365)
* [How to resolve "refusing to allow an OAuth App to create or update workflow" on git push](https://stackoverflow.com/questions/64059610/how-to-resolve-refusing-to-allow-an-oauth-app-to-create-or-update-workflow-on)


### Anaconda
* [Mac打不开Anaconda-Navigator的解决办法！](https://zhuanlan.zhihu.com/p/452685170)


### Jupyter Book
* [如何使用Jupyter-book制作电子书](https://www.bilibili.com/video/BV1eM411N7Xe/?spm_id_from=333.337.search-card.all.click&vd_source=1e128eb45caebcd5f923028b92a8f4c7)


