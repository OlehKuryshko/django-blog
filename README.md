# to-do-app

To load data into Postgres DB use [this](https://dev.to/coderasha/how-to-migrate-data-from-sqlite-to-postgresql-in-django-182h) guide: 
```bash
python3 manage.py migrate --run-syncdb
python3 manage.py shell
```

```python
from django.contrib.contenttypes.models import ContentType
ContentType.objects.all().delete()
quit()
```

```bash
python3 manage.py loaddata dump.json
```
