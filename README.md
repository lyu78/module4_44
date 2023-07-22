# База знаний для группы №44

### Обновления
20.07 Добавлен код с лекций №1-№5.  
22.07 Добавлен код с лекции №7.


### Код терминала с лекции №7
```
$ python manage.py shell
>>> from app_advertisements.models import Advertisement
>>> adv1 = Advertisement(title='Первое объявление', description=100, auction=True)
>>> adv1.save()
>>> adv1 = Advertisement(title='Второе объявление', description=200, auction=True)
>>> adv1.save()

>>> adv1.created_at
datetime.datetime(2023, 7, 22, 10, 26, 40, 428442, tzinfo=datet)

>>> adv1.title
'Второе объявление'

>>> Advertisement.objects.all()
<QuerySet [<Advertisement: Advertisement object (1)>, <Advertisct (2)>]>
>>> queryset = Advertisement.objects.all()
>>> first_obj = queryset[0]

>>> first_obj
<Advertisement: Advertisement object (1)>

>>> first_obj.title
'Первое объявление'

>>> first = Advertisement.objects.first()
>>> first.title
'Первое объявление'

>>> last = Advertisement.objects.last()
>>> last.title
'Второе объявление'

>>> from django.db import connection 
>>> connection.queries
```