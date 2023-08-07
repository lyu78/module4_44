# База знаний - группа №44
База знаний для группы №44 онлайн-школы MAXIMUM EDUCATION ("Код будущего").  

### Лекции №1-№5
Добавлен код по лекциям №1-№5 и ДЗ по лекциям №1-№4.

### Лекция №7
Создали свою первую модель и научились работать в Shell.

### Лекция №8
Настроили административную панель проекта. Научились добавлять записи через админку.


### Лекция №9
Наполнили шаблон главной страницы джанго-проекта. 


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