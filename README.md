# بسم الله الرحمن الرحيم
Git is any tool that let you keep track of your code changes overtime

Github is a website that let's you upload your code files on it.

## Things you should do first
* install git
* create an ssh key on your local machine and assign it to your account on github so the website knows it's you and give you access to your files..
[ازاي بقى الكلام ده خش على الرابط ده وانت تعرف ](http://github.com)

## دي الاوامر او الكوماندز اللي استخدمتها ف الgit
* `git clone "the ssh url"`
* `git status` : showes you all the files that have been updated or created or deleted but haven't been saved in a commit yet
* `git add .` tells git to track changes in all files in the cloned directory.. you can choose only one file to track and it will only track changes of that file
* if you use `git status` again after the previous step it will show you what files git is tracking and what not .. changes in both

* Now we've specified to git with `git add` what files we want to commit , now to commit  'em you can simply type `git commit -m "some message to say"` -m means message and it can be one char but there must be a massege for the title of your commit to appear on github and you can add to messages one is a title and the other is a description
`git commit -m "title of my commit" -m "this is a description"`
* with that we've commited (saved) the new changes on git localy, so if you and your friends use the same machine you can keep tracking of code using `commit`
* But to commit changes online specifically to github.com you do that using `git push origin main`


