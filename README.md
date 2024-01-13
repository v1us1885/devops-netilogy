# devops-netilogy


1. Local .terraform directories:   
Игнорируются все подкаталоги .terraform внутри текущего каталога и всех его подкаталогов.   
```
**/.terraform/*
```
2. .tfstate files:   
Игнорируются файлы состояния Terraform (.tfstate и .tfstate.*), которые могут содержать конфиденциальные данные и не предназначены для хранения в репозитории.
```
*.tfstate
*.tfstate.*
```
3. Crash log files:   
Игнорируются файлы логов аварий (crash.log и crash.*.log).
```
crash.log
crash.*.log
```
4. .tfvars files:   
Игнорируются файлы переменных Terraform (.tfvars и .tfvars.json), которые могут содержать чувствительные данные.
```
*.tfvars
*.tfvars.json
```
5. Override files:   
Игнорируются файлы, связанные с переопределением ресурсов в Terraform (override.tf, override.tf.json, *_override.tf, *_override.tf.json).   
```
override.tf
override.tf.json
*_override.tf
*_override.tf.json
```
6. Include override files:   
Можно добавить конкретные файлы переопределения, которые хотим включить в репозиторий, то добавить их с использованием отрицательного шаблона:   
```
!example_override.tf
```
7. Include tfplan files:   
Игнорируются файлы планов Terraform (*tfplan*), которые могут содержать выходные данные от команды terraform plan.
```
*tfplan*
```
8. Ignore CLI configuration files:   
Игнорируются файлы конфигурации CLI Terraform (.terraformrc и terraform.rc).
```
.terraformrc
terraform.rc
```
