# to-do-app

Start app:
- Install requirements
```bash
pip install -r requirements.txt
```
- Install PostgresSQL locally or use official Docker image like this:
```bash
docker run -p 5532:5432 --name=postgres_12_py -e POSTGRES_PASSWORD=mysecretpassword -d postgres:12.4-alpine
```
- Create todolist Database
```postgresql
CREATE DATABASE todolist;
```
- load data into Postgres DB use [this](https://dev.to/coderasha/how-to-migrate-data-from-sqlite-to-postgresql-in-django-182h) guide: 
```bash
python3 manage.py migrate --run-syncdb
python3 manage.py shell
```
```python
# paste the following in shell
from django.contrib.contenttypes.models import ContentType
ContentType.objects.all().delete()
quit()
```
```bash
python3 manage.py loaddata dump.json
```

- Start server

```bash
python manage.py runserver
```
