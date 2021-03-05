<h1>
Read me for this django template
</h1>

Django version= 3.1

This is a django template for the ones just starting with django to follow to run their first app. 
This is a step by step guide to have their app successfully run to serve static and media files locally. 
 
Steps: 
<h3> starting project and first app </h3>
1-Create a new folder for your django project

2- Open your new folder in any IDE or code editor you like and run python
#make sure you have installed django using <b>pip install django</b>

3- Open terminal and run <b>django-admin startproject //name of project//</b>
to start a new django project 

4- from termianl run <b>python manage.py startapp //name of your first app//</b> to have your first app in django.

to this point you have successfully started a django project with one app
fun fact!
you can check your django app's default UI by running <b>python manage.py runserver</b> and it should look ike this 
![runserver](https://user-images.githubusercontent.com/56789675/110047380-99cb2000-7d6f-11eb-9fa5-8df4a1cdccd2.png)

<h3> Static, Media files setting </h3>

Every project have some type of static and media files in it and there are some settings you need to cinfigue to tell django the location to follow

Base directory ( BASE_DIR ) is the root folder of your django project which contains the <b>manage.py</b> file and other django files of your project
![base dir](https://user-images.githubusercontent.com/56789675/110048443-af414980-7d71-11eb-90d6-7f4ddd5dc581.png)


<b> you need to create static and media folders to have your files in there to be used in project.</b>

After creating these folders, you need to tell django about these folders in the settings.py file of your project folder
<h4> Configuring Static files</h4>
  
  </b>

<b> add this after the static_URL line in settings.py file  
  
  Use this setting to confiure your Static files
considering your foilder name is 'static' 

Static_ROOT= os.path.join(BASE_DIR, 'static')<br>
STATICFILES_DIRS=[
    os.path.join(BASE_DIR,'static')]
    
in this code you are telling django that this is the root folder for static and this is the base directory of static files
</b>
![static files](https://user-images.githubusercontent.com/56789675/110048873-8bcace80-7d72-11eb-86fe-f1ad146d000e.png)

<h4> Configuring Media files</h4>
  
 </b>
 do this similar process for media files as well
 
 Use this code to configure media files, condidering your media folder name is media</b>
 
MEDIA_ROOT=os.path.join(BASE_DIR, 'media')<br>
MEDIA_URL='/media/'
![media files](https://user-images.githubusercontent.com/56789675/110049063-e532fd80-7d72-11eb-8e13-458a3debe993.png)
to have media files setup for this project 

<h3> Configuring Templates </h3>
 In order to configure templates in django, add a folder in base dir named <b>template</b>
 
 and configure this setting in settings.py of your project
 
 In the template line in settings.py, in dir dictionary  add
 <b> [os.path.join(BASE_DIR, 'template')] </b> as value and you have successfully configured the templates
 
 ![templates](https://user-images.githubusercontent.com/56789675/110049538-d862d980-7d73-11eb-95db-b1195e22517e.png)
 
 

