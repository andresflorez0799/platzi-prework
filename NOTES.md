sudo apt-get upgrade
sudo apt install nodejs
sudo apt install npm

-   sudo apt install git
-   ssh-keygen -t rsa -b 4096 -C "[correo]"
-   eval "$(ssh-agent -s)"
-   ssh-copy-id "[correo]"
-   cd ~/.ssh
-   cat id_rsa.pub
    //Copia el contenido e ir a github.com y opcion SSH Keys y agregar la ssh key

git config --global user.email [correo]
git config --global user.name [usuario]

Ir a github.com y crear un repositorio nuevo

Ir a Settings > Developer Settings > pestaña Personal access tokens y luego
darle click a Generate new token y crear un token (guardarlo {token} porque se usara mas adelante).

…create a new repository on the command line
echo "# platzi-prework" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin [url del repo en git]

git remote set-url origin https://{token}@github.com/{usuariogit}/{nombrerepo}.git

git push -u origin main
