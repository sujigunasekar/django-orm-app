# Django ORM Web Application

## AIM:
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram:

![orm](https://user-images.githubusercontent.com/119559822/210796279-fef02f3b-20b9-42d7-a142-f73ac595d6a2.png)


## DESIGN STEPS

### STEP 1: 
Create a new Django project using "django-admin startproject",get into the project terminal and use


### STEP 2:
Define a model for the student_id "python3 manage.py startapp" command.in the models.py.Allow host access and add the app
name under installed apps in settings.py


### STEP 3:
Register the models with the Django admin site. In admin.py under app folder,register the models
with Django admin site.



## PROGRAM:
```
Admin.py
from django.contrib import admin
from .models import Student,StudentAdmin

# Register your models here.
admin.site.register(Student,StudentAdmin)

Models.py
from django.db import models
from django.contrib import admin

# Create your models here.
class Student(models.Model):
    student_id = models.CharField(max_length=8,primary_key=True)
    name =models.CharField(max_length=100)
    phone_number = models.IntegerField()
    email = models.EmailField()
    class_number = models.CharField(max_length=100)

class StudentAdmin(admin.ModelAdmin):
    list_display = ('student_id','name','phone_number','class_number','email')

```

## OUTPUT:
![django admin](https://user-images.githubusercontent.com/119559822/210796370-5cce7acf-2b22-4c1e-9cbf-ec716311ee3f.png)




## RESULT:
Successfully developed a Django application to store and retrieve data from a database using Object
Relational Mapping(ORM).

