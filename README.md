### devops-netology

First string

В файле .gitignore описаны параметры, исключающие некоторые файлы или 
каталоги для тех или иных действий. В данном случае исключает commit
для некоторых файлов.

# Ex.1

![alt text](https://github.com/StepanovSA/devops-netology/blob/main/git%201.PNG)

# Ex.2

![alt text](https://github.com/StepanovSA/devops-netology/blob/main/git%202.PNG)

# Ex.3

![alt text](https://github.com/StepanovSA/devops-netology/blob/main/git%203.PNG)

*Где просят ввести после git push , Git запросит логин и пароль — вводить логин и пароль не от GitHub, а от репозитория  username и tocen

![alt text](https://github.com/StepanovSA/devops-netology/blob/main/git%204.PNG)

# git log

![alt text](https://github.com/StepanovSA/devops-netology/blob/main/git%205.PNG)

* В файле .gitignore использовал параметры из документации, для terraform уже отдельно сделаю, когда дойдем

# Ex.4

**/.terraform/* - позволит игнорировать директории .terraform любой степени вложенности вместе с вложенными в них директориями и файлами.

!*.tfstate - не исключать файлы c расширением .tfstate

crash.log и crash/**/*.log  - для игнорирования файлов с именем crash.log, также игнорировать все файлы, с расширением .log в дирректории crash/

*.tfvars и *.tfvars.json - для исключения файлов c расширением .tfvars и .tfvars.json

override.tf, override.tf.json, *_override.tf и *_override.tf.json - для исключения файлов с именем override.tf, override.tf.json, а также файлы, заканчивающиеся на _override.tf и _override.tf.json
.terraformrc и terraform.rc - позволит игнорировать файлы, которые заканчиваются на .terraformrc и любые файлы terraform.rc .
