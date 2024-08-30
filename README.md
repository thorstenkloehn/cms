## CMS Django Inststallieren

CMS Django ist ein Content Management System, das auf dem Webframework Django basiert. Es ist ein Open-Source-Projekt, das von der Django-Community entwickelt wird. Es bietet eine einfache und benutzerfreundliche Benutzeroberfläche, mit der Sie Inhalte auf Ihrer Website verwalten können.   

In diesem Tutorial erfahren Sie, wie Sie CMS Django auf Ihrem Server installieren und konfigurieren können. Wir werden Schritt für Schritt durch den Prozess der Installation und Konfiguration von CMS Django gehen.

### Installieren von CMS Django

```bash
git clone https://github.com/thorstenkloehn/cms.git
cd cms
code .
python3.12 -m venv venv
source venv/bin/activate
pip install django-cms 
pip install -r requirements.in
```
### Konfigurieren Datei .env

```bash
sudo nano .env
```
Fügen Sie die folgenden Zeilen hinzu:

```bash
SECRET_KEY=django-insecure
DATABASE_NAME=your_database_name
DATABASE_USER=your_database_user
DATABASE_PASSWORD=your_database_password
DATABASE_HOST=your_database_host
DATABASE_PORT=your_database_port
DEBUG=True
ALLOWED_HOSTS=your_domain.com
```
Speichern und schließen Sie die Datei.
```
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```