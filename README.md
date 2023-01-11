# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Entity Relationship Diagram](./ORM1.png)

## DESIGN STEPS

### STEP 1:
Push the changes in the branch to the Github repository

### STEP 2:
 Create a migration file that contains code for the database schema of a model

### STEP 3:
Apply all the migrations to the database

## PROGRAM

```
Model.py

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

Admin.py

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
 ```

## OUTPUT

![OUTPUT](./Out.png)


## RESULT

Program executed successfully