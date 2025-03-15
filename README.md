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

sudo curl -L "https://github.com/docker/compose/releases/download/$COMVER/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose
![image](https://github.com/user-attachments/assets/72550e5c-4fb3-40ec-96c6-d8c99b29d53a)
Эта команда позволяет загрузить последнюю версию Docker Compose и заменить существующую, если она есть

sudo chmod +x /usr/bin/docker-compose
![image](https://github.com/user-attachments/assets/e5497e06-eb0f-41b4-a1b7-42bf2c254357)
Эта команда необходима, если при использовании утилиты возникают проблемы с правами на выполнение.

docker-compose –version
![image](https://github.com/user-attachments/assets/871ff733-5072-4bc7-96b5-39d83e9311f6)
Позволяет посмотреть версию команды docker-compose.

git clone https://github.com/skl256/grafana_stack_for_docker.git
![image](https://github.com/user-attachments/assets/15d4502c-f3e5-4ba4-afaf-73d243190702)
 Клонирует репозиторий по ссылке на компьютер. При клонировании на локальную машину копируются файлы и папки проекта, а также вся его история

Sudo yum install git
![image](https://github.com/user-attachments/assets/df8f78a8-8a58-483d-a12e-623b36cec565)
![image](https://github.com/user-attachments/assets/9fa562a1-5c0c-4db1-a624-149eb3dd17e6)
Устанавливает Git и его зависимости в системе

git clone https://github.com/skl256/grafana_stack_for_docker.git
![image](https://github.com/user-attachments/assets/7521a563-ac6e-45d5-ae89-d584cbcfe16f)
Создаём локальную копию репозитория по указанному URL.
cd grafana_stack_for_docker
![image](https://github.com/user-attachments/assets/f02817ea-1b21-46d1-b85c-d6ed2c4c58b9)
позволяет перейти в каталог с содержимым репозитория grafana_stack_for_docker

sudo mkdir -p /mnt/common_volume/swarm/grafana/config
![image](https://github.com/user-attachments/assets/0444a475-5273-4f9d-93c9-090160a22802)
Создаём папку с именем «config» в пути /mnt/common_volume/swarm/grafana.
sudo chown -R $(id -u):$(id -g) {/mnt/common_volume/swarm/grafana/config,/mnt/common_volume/grafana}
![image](https://github.com/user-attachments/assets/99ad189b-e8f8-4b5e-88b4-b82946a3933f)
 меняем владельца и группу для указанных папок и их содержимого
touch /mnt/common_volume/grafana/grafana-config/grafana.ini
![image](https://github.com/user-attachments/assets/97829281-3ab5-4f47-aff2-1b552be40386)
создаём файл grafana.ini в папке grafana-config в каталоге /mnt/common_volume.

cp config/* /mnt/common_volume/swarm/grafana/config/
![image](https://github.com/user-attachments/assets/e7f265ba-2dbe-46f7-b86d-3e05708979dd)
после выполнения этой команды все файлы из каталога config будут скопированы в каталог /mnt/common_volume/swarm/grafana/config/.

mv grafana.yaml docker-compose.yaml
![image](https://github.com/user-attachments/assets/db04fae1-5b0b-4973-8b52-fb758e4860ee)
после выполнения этой команды файл grafana.yaml будет переименован в docker-compose.yaml.

sudo docker compose up -d
![image](https://github.com/user-attachments/assets/0d922031-6943-4f10-87c2-8788f808d9ed)
Docker Compose начинает создавать и запускать все сервисы, указанные в docker-compose.yml файле. флаг -d: Ctrl + C: Прерывает (остановливает) выполнение текущей команды или процесса в терминале. Если запустили контейнеры без флага -d, использование Ctrl + C остановит их. Ctrl + Z: Приостанавливает выполнение текущего процесса и переводит его в фоновый режим. Это позволяе вернуться к терминалу и продолжить работу, но при этом процесс останется приостановленным. Чтобы вернуть процесс в активное состояние, можно использовать команду fg.
![image](https://github.com/user-attachments/assets/c5e08ad0-76f1-42cf-82e6-5e5960569437)

![image](https://github.com/user-attachments/assets/ae333ae7-c7d6-4cff-a702-4d2a5d6290be)

sudo docker-compose
![image](https://github.com/user-attachments/assets/c026aa83-9115-4081-b294-4dd842c84389)

sudo docker-compose stop
![image](https://github.com/user-attachments/assets/b674ea95-c5c1-472a-8cfb-515818f988ee)
используется для остановки запущенных контейнеров
sudo docker-compose down
![image](https://github.com/user-attachments/assets/1c4e88ff-820a-42a6-95d7-1d012e207e58)
остановил и удалили все контейнеры
sudo docker-compose up -d
![image](https://github.com/user-attachments/assets/ff7713d8-687e-42c1-95c6-d88415b3d615)
снова запустил контейнеры
sudo docker-compose ps
![image](https://github.com/user-attachments/assets/37229b19-7687-4709-8486-be069817937a)
 вывел список запущенных контейнеров с их статусами и портами
переход в папку cd grafana_stack_for_docker и выполнение комнады git clone https://github.com/Kokokii/alien.git
![image](https://github.com/user-attachments/assets/d14452b0-964c-4ade-93d6-b7b89ef26d72)

cp docker-compose.yaml docker-compose.yaml1
![image](https://github.com/user-attachments/assets/577fffcb-216a-4d3d-9fb2-ed0d68aec8f0)

cd /mnt/common_volume/swarm/grafana/config и cp prometheus.yaml prometheus.yaml1
![image](https://github.com/user-attachments/assets/9a2661dc-7bcd-4218-8fcf-94a9332b9090)








