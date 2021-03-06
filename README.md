# Python-DockerCompose


<img src="dock.jpeg">

<h3>  :octopus: What we talking about ? </h3>

<p>On this repository I let a structure ready to build and use with only two command.</p>
<p>That offer you to use a python environement with Django and Postgre.</p>
<p>I followed the link below to build this environement, so if your lost or confuse you may be should take a look on the documentation.</p>

<p> :link: <a href="https://docs.docker.com/compose/django/a" target="_blank">Docker compose. </a></p>

<br>

<hr>

<h3> :squirrel: What do we need ? </h3>

<p>This environement only need a working docker compose version, you can do the command : <br>
<br>
<code>docker-compose -v </code><br>
<i> Checkout if you already have a docker-compose installed on your system, if not, you can follow the guide below : </i><br><br>
<a href="https://docs.docker.com/compose/install/">Docker-compose documentation </a></p>

<h3> :bell: Let's begin !</h3>

<code>sudo docker-compose run web django-admin startproject "NameOfYourFutureApp"</code><br><br>
<code>sudo chmod 777 -R "FolderName"</code><br><br>


<p><i>In the folder you have created, you have to find the file named as settings.py and edit the array <b>DATABASES</b></i></p>

``` json

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}

```

<p><b>Note :  On certain platforms, you might need to edit  ALLOWED_HOSTS to  ALLOWED_HOSTS = ['*'] inside settings.py</b></p>

<p> Then now use <b>docker-compose up </b></p>
<img src="p1.png">
 
 <p>It's should return to you at the <a href="http://localhost:8000/" target='_blank'>localhost:8000</a> your django starter.</p>

