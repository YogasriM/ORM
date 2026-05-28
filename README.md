# Ex01 Django ORM Web Application
# Date:14/05/2026
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 cars

# PROGRAM

## ADMIN.PY 
```
from django.contrib import admin
from .models import FoodOrder

@admin.register(FoodOrder)
class FoodOrderAdmin(admin.ModelAdmin):
    list_display = (
        'order_id',
        'customer_name',
        'restaurant_name',
        'food_item',
        'quantity',
        'price',
        'order_status'
    )
```

## MODELS.PY 
```
from django.db import models

class FoodOrder(models.Model):
    order_id = models.AutoField(primary_key=True)
    customer_name = models.CharField(max_length=100)
    restaurant_name = models.CharField(max_length=100)
    food_item = models.CharField(max_length=100)
    quantity = models.IntegerField()
    price = models.FloatField()
    delivery_address = models.CharField(max_length=200)
    order_status = models.CharField(max_length=50)

    def __str__(self):
        return self.customer_name
```
# OUTPUT
Include the screenshot of your admin page.
<img width="1903" height="1032" alt="Screenshot 2026-05-14 204147" src="https://github.com/user-attachments/assets/8955bdfe-9bdb-4b8d-a17c-18d4b8e80faa" />
<img width="1754" height="960" alt="image" src="https://github.com/user-attachments/assets/51924bf2-642a-4c94-8fcb-8c705778b4e3" />


# RESULT
Thus the program for creating a database using ORM hass been executed successfully
