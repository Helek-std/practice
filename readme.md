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

