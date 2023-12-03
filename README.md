# بسم الله الرحمن الرحيم
Git is any tool that let you keep track of your code changes overtime

Github is a website that let's you upload your code files on it.

## Things you should do first
* install git
* create an ssh key on your local machine and assign it to your account on github so the website knows it's you and give you access to your repo's..
[ازاي بقى الكلام ده خش على الرابط ده وانت تعرف ](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

## Basic Commands needed to commit and push changes online
* `git clone "the ssh url"`
* `git status` : showes you all the files that have been updated or created or deleted but haven't been saved in a commit yet
* `git add .` tells git to track changes in all files in the cloned directory.. you can choose only one file to track and it will only track changes of that file
* if you use `git status` again after the previous step it will show you what files git is tracking and what not .. changes in both
&NewLine;
* Now we've specified to git with `git add` what files we want to commit , now to commit  'em you can simply type `git commit -m "some message to say"` -m means message and it can be one char but there must be a massege for the title of your commit to appear on github and you can add to messages one is a title and the other is a description
`git commit -m "title of my commit" -m "this is a description"`
* with that we've commited the changes on git localy
حاجة كدة زي جيت على الجهاز اعتمد التغييرات بتاعتك وعرف هي ايه ولو حبيت تسلم هتسلم انهي ملف وتسيب انهي ملف
&NewLine;
* But to commit changes online you do that using `git push origin main`
you can default the main branch by writing `git push -u origin main` for  the first time and from then you can just write `git push` and it will commit to the main branch automatically.
&NewLine;
### طب ليه فيه كوميت وبوش وادد
انت دلوقتي عندك تلت مراحل فلنفرض انك عندك فايل واحد في البروجكت كله وعملت git init  كدة انت عملت ريبو او تقدر تقول خليت البروجكت ده يكون متسطب فيهgit  &NewLine; 
الفايل بتاعك ده موجود في zone واحدة حاليا اللي هي الwindows directoy لو عملتله git add <filename> هيبقى منه نسختين،، النسخة العادية اللي عندك ع الويندوز ونسخة اتحفظت في الstaging zone اللي هي زون متوسطة بعتبرها مرحلة انتقالية باخد فيها لقطة من ملفات معينة ولو عجبتني اللقطة دي ممكن احفظها في الارشيف او في الهيستوري عشان ارجعلها بعدين تحفظهم عن طريق انك تعمل كوميت،، فابعد ماتاخد اللقطة من الملفات اللي انت عايزها ولتكن الملف الوحيد بتاعنا هنا، لو عملت commit بيبقى فيه تلت نسخ من الملف كدة نسخة في كل زون من التلاتة بس الفرق ان النسخة اللي اتحفظت في الكوميت زون عمرها ما هتروح وتقدر ترجعلها ف اي وقت لانها عاملة زي الهيستوري وباقي النسخ هتروح مجرد ما تغير مثلا في الملف بتاع الويندوز كدة النسخة بتاعة الويندوز راحت ومجرد ما عملت stage لفيرجن تاني من الملف كدة النسخة اللي اللي في الزوون الانتقالية اتغيرت فا كدة نقدر نقول:
ادد عشان تختار اللفات اللي هتتسلم | كوميت عشان تحفظ لوكالي الفيرجن من الملف اللي هيتسلم بحيث ممكن ترجع للكوميت دي بعد كدة | بوش عشان تسلم
---------------|-------------------------------------------------|-------------------------------------
&NewLine;
فمثلا ممكن تسلم ملف مش هو اللي موجود حاليا على جهازك بل اخر ملف انت عملتله كوميت لجيت

## to start a repo locally and submit it on a remote place like github
1. create a new dir
1. write your code files in it
1. after you finnish you need to make it a git dir.. how?
    1. first, open the terminal window
    1. navigate to the repo dir using `cd c:/blah/blah`
    1. write `git init`, now it's a git dir
1. Now you can stage files to commit using add and commit it using git but if you try to push it live to github it would give you an error since it's not cloned from any repo you have access to
1. we need to make it connected to any repo
1. so we go to github.com and create a new repo and copy the ssh url of it
1. back to the terminal write `git remote add origin "the ssh url"` for eg `git remote add origin git@github.com:Engsiddeq/new.git`
by that we added a reference to the remote repository on github or wherever it is because remote means somewhere else but not on this computer
1. we can check what remote repo's is connected to this local repo or dir by typing `git remote -v`
1. finally you can push your local repo live using `git push origin master`
Note that it's `git push origin master` NOT `git push origin main`

## Branch commands
* `git branch` shows you branches of the repo and puts a * beside the current branch
* `git checkout -b TheNameOfTheNewBranch` creates a new branch with the nam "TheNameOfTheNewBranch" and switch current branch to it
* To switch between branches you use ` git checkout TheNameOfTheBranch`
* now you can commit changes and push it to the new branch using `git push origin TheNameOfTheNewBranch`
* if your current branch is mastere and you want to compare it with the TheNameOfTheNewBranch branch you just type `git diff TheNameOfTheNewBranch`
* if you just typed `git diff` it will show you what have changed in your local repo since you last commited
* to merge both branches use ` git merge TheNameOfTheNewBranch`
* merging is done usually using the UI on the github website not on the cmd
* after merging two filies on  th website if you want to update your repo on your local machine you type `git pull origin master`
* to remove a branch `git branch -d TheNameOfTheNewBranch`

## other commands
* `git commmit -am "title"` you can ommit the add step by typing this command but it only works if you modified files and didn't create new ones
* stashing is beyond this tutorial but it's basically a way to save your changes of code temporally on some temporarlly place and retrieve them later but essentially you don't make a commit to git

## undoing in git
* to undo staging (adding).. say you staged a file to commit by writing down `git add file.md` and you want to undo that ..you can write `git reset`

* to undo a commit you write this command `git reset HEAD~1`
HEAD refers to the last commit and HEAD~1 refers to the commit that was before the last commit.. So that basically means to undo the last commit .. and with the same logic if you want to undo the last two commits and reset the commit that was before that you youse `HEAD~2`

* `git log` will log all of your commits with a unique hash key identifying every commit and you use the space key to go down the list, so if you want to go back to some commit you copy its hash table from the log and write `git reset the_Hash_number`
---------
Now it unstagd and uncommited all changes but if you also want your files to be changed to that commit you write `git reset --hard the_Hash_number`
