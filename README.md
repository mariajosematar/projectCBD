# Project CBD
Este proyecto será una tienda E-commerce en Node.js usando plain JavaScript HTML y CSS.

## NOTE
You need to setup the `secret.js` file inside `server/` containing the following elements:
```
module.exports = {
    stripeSecret, // Stripe secret api key
    emailUsername, // This is the mailgun username
    emailPassword, // This is the mailgun password
    adminName,
    mongoUrl: 'mongodb://merlox:merlox1@ds145750.mlab.com:45750/merunas', // This can be public because it's just the user of the databas
}
```


## Objetivos

1. Crear la interfaz gráfica

- Página de login para acceder como administrador de la tienda y/o consumidores.
- Página para añadir productos.
- Crear widget imagenes.
- Crear widget permalink.
- Crear widget categorías.
- Crear widget atributos.
- Página inicial donde ver los productos como visitante.
- Página de compra del producto donde poder pagar.

2. Añadir la funcionalidad

 - Crear funcionalidad de login y registro.
 - Crear funcionalidad de ver los productos actualmente disponibles, la página inicial y página de detalles de productos.
 - Crear funcionalidad de dashboard.
 - Crear funcionalidad de pago. Pagar con paypal y con tarjeta authorize.net o stripe.
 - Crear widget del carrito.


3. Completar el proyecto

- Reparar bugs y actualizar diseño con funcionalidades.
- Toques finales.

## Tutorial de GIT como referencia para el proyecto

git --version
git config --global user.name "name" ||| git config --global user.email "email" ||| git config --globar user.username "username" (Your github username)
git init (To create a new repository on github)
git status
git diff (To compare versions with the last)

#### Commit in git
1. Check status
2. git add yourfile.txt OR . (To add all use . )
3. git commit -m "commit message"

#### To link a repository with your proyect in your pc
- git remote add origin urlfromgithub

#### To push changes to the repository
- git push origin master

#### To force push if it gives errors
- git push -f origin master

#### To see remote connections
- git remote -v

#### To change your origin remote:
- git remote set-url origin <urlnewrepository>

#### To save commit credentials
- git config remote.origin.url https://{{username}}:{{password}}@github.com/{{username}}/{{repository name}} (Para que no pidan los credenciales a cada push)

#### Clone repository
- First you fork it clicking in the top "fork" button on github to have a copy on your account.
- git clone <repositoryurl> (You can get the repository url copying it from github.com)/

#### To pull changes from a repository:
- Go inside your cloned repository folder and
- git remote add upstream <repositoryurl>
- Now you can take a look at the git remote -v

#### To create a branch (una nueva rama separada del master branch) use:
- git branch <branchaname>
- Cd to the branch with: git checkout <branchname>
- Then you can commit like usual

#### To push the changes to the branch do:
- git add .
- git commit -m "message"
- git push origin <branchname>

#### To rename branch use:
- git branch -M <branchname>

#### To pull changes from other contributors of your repository, use:
- git pull <repositoryURL> <branchaname>

#### To push the changes from your forked repository to the original use a pull request:
- Go to your forked repository
- Go to pull requests
- Select your branch at the end
- Click on new pull request and send a message

#### To join branch with master branch do:
- Move to main branch: git checkout gh-pages
- git merge <branch to merge>
- Then delete your branch locally: git branch -d <branchname>
- And remotely: git push origin --delete <branchname>

## CSS notes

#### Excellent resources for flexbox to create responsive menus
- https://paulund.co.uk/css-flexbox
- https://css-tricks.com/snippets/css/a-guide-to-flexbox/

#### To align items horizontally like in a menu
- Add a main class to the menu container
- Add the items
- Use css display: flex and align-items: center to the container

#### box-sizing: border-box
- Border box te permite sumar todos los paddings y margins para que el width que le pongas sea el exacto.
- Es decir, que si le poner un width de 30% a un elemento y un padding de 10px, el tamaño del elemento será 30% no matter what.
- Sin border-box el resultado sería mayor de 30% porque los paddings, margins & stuff se calculan aparte.
- Importante: las pseudoclases como before y after se deben aplicar aparte.
