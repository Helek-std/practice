## Подготовка к работе с проектом
Начну с создания виртуального окружения и его настройки:
```bash
mkdir practice
cd practice
python3 -m venv .
```
Активирую виртуальное окружение 
```bash
source bin/activate
```
Устанваливаю django и postgress
```bash
pip install django
sudo apt update
sudo apt install postgresql postgresql-contrib
```

**Дальше будет описание хода моей работы, установка всего необходимого завершена**
<br>
**Можно просто склонировать мой репозиторий**
```bash
git clone https://github.com/Helek-std/practice.git
```

## Начало работы с проектом
Дальше создам новый проект в django и в нем же новое приложение
```bash
django-admin startproject practiceproj
cd practiceproj
python3 manage.py  startapp practiceapp
```
Дальше необходимо зайти в аккаунт postgress, в котором создам нового пользователя
```bash
sudo -i -u postgres
```
создаю user и сразу делаю его super
```console
postgres=# CREATE USER myprojectuser WITH PASSWORD 'password';
CREATE ROLE
postgres=# GRANT ALL PRIVILEGES ON DATABASE myproject TO myprojectuser;
ERROR:  database "myproject" does not exist
postgres=# GRANT ALL PRIVILEGES ON DATABASE myproj TO myprojectuser;
GRANT
postgres=# \q
logout
```
Затем необходимо провести миграции:
```bash
python3 manage.py makemigrations
python3 manage.py migrate
```
Окружение настроено, теперь можно преступить непосредственно к заданию
Сначала необходимо подключить модели из base_models.py (Task) и из wifi_models.py (PassiveWiFiData, PassiveWiFiRecord, ActiveWiFiData)
И повторно провести миграцию
