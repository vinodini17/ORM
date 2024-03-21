# Ex02 Django ORM Web Application
## Date:18/03/24 

## AIM
To develop a Django application to store and retrieve data from a Train database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM
![alt text](<Screenshot 2024-03-19 171500.png>)

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM

admin.py
```
from django.contrib import admin

from .models import Train, TrainAdmin

admin.site.register(Train, TrainAdmin)
```

models.py
```
from django.db import models
from django.contrib import admin
class Train(models.Model):
    Train_code=models.CharField(max_length=20,primary_key=True)
    Train_name=models.CharField(max_length=100)
    start_time=models.DateTimeField()
    End_time=models.DateTimeField()
    start_station_code=models.CharField(max_length=20)
    End_station_code=models.CharField(max_length=20)
 
class TrainAdmin(admin.ModelAdmin):
    list_display=('Train_code','Train_name','start_time','End_time','start_station_code','End_station_code')
```
## OUTPUT
<img width="945" alt="Screenshot 2024-03-19 174858" src="https://github.com/vinodini17/ORM/assets/149347288/acc82b9e-8795-46d8-be8e-f076303a49e8">

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
