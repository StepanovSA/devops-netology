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

# Правила .gitignore

1) Комментарии доступны через решётку(#) в начале строки

2) Символ "/" в начале строки указывает, что правило применяется только к файлам и папкам, которые располагаются в той же папке, что и сам файл .gitignore

3) Доступно использовать спецсимволы: звёздочка(*) заменяет любое количество символов(ноль или больше)

4) Знак вопроса ( ? ) соответствует любому одиночному символу

5) Два символа звездочки соответствуют любому файлу или нулю или более каталогам

Если за ** следует косая черта /, соответствует только каталогам

6) Восклицательный знак(!) в начале строки означает инвертирование правила, необходим для указания исключений из правил игнорирования

7) Символ "\" используется для экранирования спецсимволов

8) Для игнорирования всей директории, правило должно оканчиваться на слэш(/), в противном случае правило считается именем файла












# Local .terraform directories
**/.terraform/*

Этот шаблон исключает все локальные директории `.terraform`, которые содержат временные файлы и кэшированные данные, используемые Terraform для хранения состояния и конфигураций.

# .tfstate files
*.tfstate
*.tfstate.*

Файлы состояния Terraform (`.tfstate`) содержат информацию о текущем состоянии инфраструктуры, управляемой Terraform. Эти файлы часто содержат чувствительные данные и не должны быть добавлены в систему контроля версий.

# Crash log files
crash.log
crash.*.log

Файл с логами ошибок (`crash.log`) генерируется в случае краха Terraform и не должен храниться в системе контроля версий.

# Exclude all .tfvars files, which are likely to contain sensitive data, such as
# password, private keys, and other secrets. These should not be part of version 
# control as they are data points which are potentially sensitive and subject 
# to change depending on the environment.
*.tfvars
*.tfvars.json

Файлы переменных (`.tfvars`) часто содержат чувствительные данные, такие как пароли и приватные ключи, и не должны быть добавлены в репозиторий.

# Ignore override files as they are usually used to override resources locally and so
# are not checked in
override.tf
override.tf.json
*_override.tf
*_override.tf.json

Файлы переопределения используются для локальных изменений ресурсов и обычно не должны быть включены в систему контроля версий.

# Ignore transient lock info files created by terraform apply
.terraform.tfstate.lock.info

Файл блокировки Terraform (`.terraform.lock.hcl`) обеспечивает детерминированность версий провайдеров. Этот файл может быть специфичным для локальной машины и не должен храниться в репозитории.

# Include override files you do wish to add to version control using negated pattern
!example_override.tf

Эта строка показывает, как можно включить конкретные файлы переопределения в систему контроля версий, используя отрицательный шаблон.

# Include tfplan files to ignore the plan output of command: terraform plan -out=tfplan
example: *tfplan*

Файлы плана (`tfplan`) содержат результаты выполнения команды `terraform plan` и не должны храниться в репозитории.

# Ignore CLI configuration files
.terraformrc
terraform.rc

Конфигурационные файлы Terraform CLI (`.terraformrc` и `terraform.rc`) могут содержать локальные настройки и не должны храниться в системе контроля версий.
