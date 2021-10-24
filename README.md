
# Práctica 1: IAAS

Esta práctica consiste en preparar la máquina virtual para poder trabajar a lo largo de la asignatura. 


# 1. Instalación de LINUXBREW
Homebrew es un sistema de gestión de paquetes especialmente diseñado para el sistema operativo Mac OS de Apple.Linuxbrew es una bifurcación de Homebrew.

Ejecutamos en la terminal de la máquina virtual:
    sudo apt install curl
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# 2. Instalación de GIT
Git esel sistema de control de versiones moderno más utilizado del mundo. 

Ejecutamos en la terminal:
    sudo apt install git 
También podemos comprobar cual es la versión que hemos descargado con el comando: 
    git --version 
![image](/Users/teresabonetcosta/Desktop/capt1git.png)

Para configurar git debemos realizar lo siguiente: 
    git config --global user.name "teresaull"
    git config --global user.mail "alu0101523644@ull.edu.es"
    

# 3. Rama actual en el Prompt de la terminal

Para hacer esto ejecutamos:
    wget https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh -O ~/.git-prompt.sh

Y ahora editamos ~/.bashrc con emacs añadiendo las siguientes líneas al fichero:
    source ~/.git-prompt.sh
    PS1="\n[\[\033[32m\]\w]\[\033[0m\]\$(__git_ps1)\n\[\033[1;33m\]\u\[\033[32m\]$ \[\033[0m\]"

Cosas que he hecho:
git clone https://github.com/magicmonty/bash-git-prompt.git ~/.bash-git-prompt --depth=1


# 4. Alias en git

Esta funcionalidad nos permite cambiar el nombre a comandos que utilicemos recurrentemente para que sea más rápido trabajar con ellos. 
Utilizando el comando:
    git config --global alias.{nombre que quieras para tu comando} {comando con el nombre actual}

Podemos crear un alias para el comando 
    gh api -X DELETE /repos/ULL-ESIT-DMSI-1920/pruebateresa

Lo que debemos escribir será:
    git config --global.delete ´gh api -X DELETE /repos/ULL-ESIT-DMSI-1920/pruebateresa´

 

# 5. Instalación de nvm
Node Version Manager es un script bash utilizado para administrar múltiples versiones lanzadas de Node. js. Permite realizar operaciones como instalar, desinstalar, cambiar de versión, etc.

Para instalar nvm ejecutamos el siguiente comando:
    wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash

Ahora podemos instalar nvm con el comando:
    nvm install --lts

# 6. Instalación de Jshint 
SHint es una herramienta de análisis de código estático utilizada en el desarrollo de software para verificar si el código fuente de JavaScript cumple con las reglas de codificación. JSHint

Ejecutamos el comando: 
    npm install -g jshint

# 7. Instalación de rvm  
De las siglas, Ruby Version Manager, es una plataforma de software para sistemas operativos tipo UNIX diseñada para administrar múltiples instalaciones de Ruby en el mismo dispositivo.
Ejecutamos el comando:
    sudo apt-get install software-properties-common

Acontinuación descargamos el paquete de instalación de rvm. 
    sudo apt-add-repository -y ppa:rael-gc/rvm
    sudo apt-get update
    sudo apt-get install rvm
Cambiamos de usuario de rvm a nuestro usuario: 
    sudo usermod -a -G rvm $USERç

# 9. Instalación de Ruby 
Ruby es un lenguaje de programación interpretado, reflexivo y orientado a objetos.
Para instalarlo, utilizamos rvm y los siguientes comandos:
    rvm user gemsets 
    rvm install ruby

# 8. Instalación de NERDTree para vim 
El complemento NERDTree le permite a vim ver el directorio y mostrarlo en una estructura de árbol.
Utilizamos el siguiente comando: 
    git clone https://github.com/preservim/nerdtree.git ~/.vim/pack/vendor/start/nerdtree
    vim -u NONE -c "helptags ~/.vim/pack/vendor/start/nerdtree/doc" -c q

# 9. Instalación de Express.js
Express.js es un marco de aplicación web de back-end para Node.js, lanzado como software gratuito y de código abierto bajo la licencia MIT. Está diseñado para crear aplicaciones web y API.
Para descargarlo escribimos en la terminal:
    npm install express-generator -g

# 10. Instalación de ctags
Ctags es una herramienta de programación que genera un archivo de índice de nombres que se encuentran en los archivos de origen y encabezado de varios lenguajes de programación para ayudar a la comprensión del código. 

Para instalar ctags utilizamos el comando:
    sudo apt install universal-ctags

# 11. SSH Keys
Debemos crear una clave ssh para poder acceder de forma segura y realizar todas las acciones que queramos en la máquina virtual desde nuestro ordenador.
Para crearla deberemos escribir en la terminal:             
    ssh-keygen -trsa 

Esto crea una clave pública y otra privada, cogemos la pública para añadirla a github, esta es la que acaba en pub.

