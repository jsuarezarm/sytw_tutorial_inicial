# Instalación de Ruby (rvm) y Git

## Instalación de Ruby (rvm)
Instalaremos la versión rvm de Ruby. Podemos encontrar toda la documentación en http://rvm.io/

Para instalarlo ejecutaremos el comando siguiente (hay que hacerlo como usuario sin privilegios):
~~~
\curl -sSL https://get.rvm.io | bash -s stable
~~~

Si no tiene el programa curl instalado, deberá hacerlo antes.
~~~
sudo apt-get install curl
~~~

Después de haber instalado rvm, instalamos Ruby. En mi caso, la versión 2.0.0.
~~~
rvm install 2.0.0
~~~

![Instalación Ruby](images/rvm200.png "Instalación de la versión de Ruby 2.0.0")

Tenemos que añadir una línea al fichero ~/.bash_profile con el siguiente comando:
~~~
echo "source $HOME/.rvm/scripts/rvm" >> ~/.bash_profile
~~~

Ahora podemos indicar que se haga uso de la versión 2.0.0 de Ruby.
~~~
rvm use 2.0.0
~~~

Como vemos en la imagen siguiente, es probable que antes de ejecutar el comando anterior ejecutemos: `/bin/bash --login`

![rvm use](images/rvm_use.png "Configurar el uso de la versión 2.0.0")



## Instalación de Git
Para instalar git:
~~~
sudo apt-get install git
~~~

Una vez instalado procederemos a configurarlo.

Lo primero es añadir un nombre y un correo electrónico.
~~~
git config --global user.name "Nombre Apellido"
git config --global user.email "tu@correo.com"
~~~

Seguidamente, configuraremos git para que no sea necesario introducir la contraseña cada vez que hagamos una actualización.
~~~
git config --global credential.helper cache
~~~

También haremos que todos los cambios se empujen siempre en el repositorio git.
~~~
git config --global push.default "matching"
~~~

Y por último, configuraremos git para que se eviten los commits innecesarios.
~~~
git config --global branch.autosetuprebase always
~~~

Si queremos ver la configuración de git, ejecutaremos el comando siguiente:
~~~
git config --list
~~~

![Ejemplo](images/git_config.png "Ejemplo de configuración de Git")



## Instalación de gemas
Para instalar una gema, lo haremos con el comando:
~~~
gem install "nombre_gema"
~~~

### Instalación de la gema sinatra
Siguiendo el comando anterior, instalaremos la gema sinatra.
~~~
gem install sinatra
~~~

![Sinatra](images/sinatra.png "Instalación de la gema sinatra")

