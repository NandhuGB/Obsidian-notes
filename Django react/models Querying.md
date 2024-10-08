### Basics

	makemigrations and migrate 
	you need migrations if and only any changes to model elements and schema not 
	for the methods changes

creating table entries
```python
book = Books(title="my story",...)
book.save()
```

other way
```python
Book.objects.create(title="My story",...)
```

getting all
```python
Book.objects.all()
```

getting one element with filter
```python
Book.objects.get(title="my story") 
#get should return one item otherwise will through an error--> try with id 
```

getting all filtered element 
```python
Book.objects.filter(rating=3, author="some name") # you can use multiple queries
```

filtering elements (django filer making queries field look-ups)
```python
Book.objects.filter(reating__lt=3) # rating lower than 3
```

#### filtering with And , Or operators

```python
Book.objects.filter(title__contains = "worst", rating__lt = 4) # comma indicates the and operating between given two queries
```

to use OR operator between filtering queries we have to import Q
```python
from django.db.models import Q

Book.objects.filter( Q(rating__gt=3) |  Q(is_bestselling = False))

# | symbol indicates the or operation between two queries 
```

we can combine AND and OR operators as well with Q

```python
Book.objects.filter()
```
#### Blank vs Null = True


### Validators

```python
from django.core.validators import MinValueValidator, MaxValueValidator

rating = models.IntegerField(validators = [MinValueValidator(1), MaxValueValidator(5)])
```

#### deleting data
```python
obj =  Book.objects.all()[0]
obj.delete()
``` 