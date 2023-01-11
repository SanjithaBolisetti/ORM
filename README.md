# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Entity Relationship Diagram](./Ex02_ORM.png)

## DESIGN STEPS

### STEP 1:
Clone the repository from github

### STEP 2:
Create a new app using Django

### STEP 3:
Create programs for admin and modesl for creating employee database

## PROGRAM
```
models.py

from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()
class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

admin.py

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)

```
## OUTPUT
![OUTPUT](./san.png)


## RESULT
The program executed successfully