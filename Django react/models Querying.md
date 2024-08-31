
creating table entries
```
book = Books(title="my story",...)
book.save()
```

other way
```
Book.objects.create(title="My story",...)
```

getting all
```
Book.objects.all()
```

getting one element with filter
```
Book.objects.get(title="my story") 
#filter should return one item otherwise will through an error--> try with id 
```

getting all filtered element
```
Book.objects.filter(rating>3) # you can use multiple 
```
