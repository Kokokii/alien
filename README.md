alien
Ввел команду `sudo yum install wget`


![image](https://github.com/user-attachments/assets/bfed0a82-af35-41ed-b32f-342184affb0f)

Ввел команду su root, что бы зайти в командную строку от имени администратора  после этого ввел команду `vi /etc/sudoers`

Далее вылезли команды 
![image](https://github.com/user-attachments/assets/2846f04a-ac6e-43e5-82d0-ff7d611c290e)
Дал права администратора пользователю 

Что бы сохранить использовал команду `:wq!` что бы выйти без сохранения `:q!`

Скачал пакеты с помощью команды `sudo yum install wget`
Пакет: wget-1.21.1-8.el9_4.x86_64
![image](https://github.com/user-attachments/assets/d97ec8f8-0844-431f-8223-9a572e40a823)


Использовал команду `sudo yum install curl` 
![image](https://github.com/user-attachments/assets/c36754fa-150a-482e-a8bc-55aac4134f6a)
Для работы с веб-ресурсами через сетевые протоколы. Для установки утилиты curl в дистрибутивах Linux
Ввел команду `sudo wget -P /etc/yum.repos.d/ https://download.docker.com/linux/centos/docker-ce.repo`
![image](https://github.com/user-attachments/assets/bb1eb5e4-6fc1-4996-b39c-789829536491)
 Используется для скачивания конфигурационного файла репозитория Docker в CentOS. Это необходимо для установки Docker, чтобы получить наиболее актуальную версию программы.

Устанавливаем docker с помощью команды `sudo yum install docker-ce docker-ce-cli containerd.io`
![image](https://github.com/user-attachments/assets/9cf47f9a-bbcd-4e3c-b1dc-d83911051ea6)
После этого подверждаем установку 
![image](https://github.com/user-attachments/assets/7838738c-462c-49e6-9787-710e74ad639c)
После этого еще раз подверждаем установку 
![image](https://github.com/user-attachments/assets/946accc2-c756-4ab5-919b-85d8a0702117)
Вводим команду `sudo systemctl enable docker --now`
![image](https://github.com/user-attachments/assets/287a68d1-55c4-406e-825d-d5ac439f95ab)
Команда запускает службу Docker и настраивает её на автоматический запуск при загрузке системы.
