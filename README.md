
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

Para instalar nvm ejecutamos el siguiente comando:
    wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash

Ahora podemos instalar nvm con el comando:
    nvm install --lts

# 6. Instalación de Jshint 
Ejecutamos el comando: 
    npm install -g jshint

# 7. Instalación de rvm  
Esto nos servirá para intalar, manejar y trabajar con ruby. 
Ejecutamos el comando:
    sudo apt-get install software-properties-common

Acontinuación descargamos el paquete de instalación de rvm. 
    sudo apt-add-repository -y ppa:rael-gc/rvm
    sudo apt-get update
    sudo apt-get install rvm
Cambiamos de usuario de rvm a nuestro usuario: 
    sudo usermod -a -G rvm $USER
# 9. Instalación de Ruby 
    rvm user gemsets 
    rvm install ruby

# 8. Instalación de NERDTree para vim 
    git clone https://github.com/preservim/nerdtree.git ~/.vim/pack/vendor/start/nerdtree
    vim -u NONE -c "helptags ~/.vim/pack/vendor/start/nerdtree/doc" -c q

# 9. Instalación de Express.js
    npm install express-generator -g

# 10. Instalación de ctags

    sudo apt install universal-ctags



