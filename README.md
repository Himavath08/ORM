# Ex02 Django ORM Web Application
## Date: 20-03-2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![WhatsApp Image 2024-03-22 at 11 38 08_892ff4e5](https://github.com/Himavath08/ORM/assets/139110631/7a2029cb-a78e-4255-9054-8b63ec602a72)




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
#Model.py
```
from django.db import models
from django.contrib import admin
# Create your models here.

class Student(models.Model):
    referencenumber = models.CharField(max_length=10, help_text="Your Reference Nummber")
    name = models.CharField(max_length=100)
    age = models.IntegerField()
    email = models.EmailField()
    mobile_number = models.IntegerField()
    
class StudentAdmin(admin.ModelAdmin):
    list_display = ('referencenumber','name','age','email','mobile_number')

class Employee (models.Model):
    emp_id=models.CharField(primary_key=True,max_length=4,help_text=' Employee ID')
    ename=models.CharField(max_length=50)
    post=models.CharField(max_length=20)
    salary=models.IntegerField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('emp_id','ename','post','salary')
```
## Admin.py
```
from django.contrib import admin
from .models import Student,StudentAdmin,Employee,EmployeeAdmin

# Register your models here.
admin.site.register(Student,StudentAdmin)
admin.site.register(Employee,EmployeeAdmin)
```
## OUTPUT
![WhatsApp Image 2024-03-22 at 11 37 36_94090ec4](https://github.com/Himavath08/ORM/assets/139110631/c5a0446e-7840-4889-9b43-1e31b26c5f53)

![WhatsApp Image 2024-03-22 at 11 37 54_2f8a9837](https://github.com/Himavath08/ORM/assets/139110631/1a0de576-ca89-4eb2-a427-14ea67c59636)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
