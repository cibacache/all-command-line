## Command:

### Global:
```
git config --global user.name “Camilo Ibacache”
git config --global user.name   // Para ver el nombre
git config --global user.email camiloibacache@gmail.com
git config --global --list
```

### Eliminar git de una carpeta:
```
//Eliminar git de una proyecto   
cd carpeta 		
rm -rf .git
```

### Iniciar, commit , checkout
```  
git init 		//comienza a monitorear
git status 	// estado del proyecto
git add  	
git add -A 	//Agrega todo
git commit -m “mensaje del commit”
git log		//registros de los commit
git checkout <id commit>
git commit --amend -m "un mensaje"
```

###  Ramas
```
git branch 	//muestra las ramas
git branch <nombre nueva rama> 	//crea la nueva rama
git checkout <nombre rama>		//cambia de rama
git branch -D <nombre rama>	//borra una rama
git merge <nombre rama>	//absorbe a una rama, posicionarse  en rama que absorbe
git checkout -b <nombre nueva rama> 	//creamos y nos movemos a una nueva rama

git stash                              //guarda en memoria los cambios y puedes cambiarte de rama (es como un commit pero sin nombre)
git stash list                         //muestra una lista de stash guardados
git stash pop                           //recupera un estado anterior de la lista, saca el {0} si no se especifica 
git stash drop                          //elimina un estado de la lista, saca el {0} si no se especifica 
```

### Repositorios Remotos
```
git clone <URL>
git remote add <nombre servidor> <URL>	//Se asigna un nombre al repositorio remoto
git remote -v 		//muestra las conexiones remotas
git remote set-url origin <URL> //Cambiar de repositorio remoto
git push <servidor> <rama> //Sube commit a repositorio
git push -u origin --all //Sube toda las ramas al repositorio remoto

git pull <servidor> <rama> // actualiza el repo
git remote show [nombre] //info del repositorio remoto
```

### Tags
```
git tag -a v1.0 -m “un mensaje” <id commit>
git push origin --tags //sube todos los tags
git tag -n // muestra un lista de los tags con mensaje
git tag -d <nombre del tag> // borra un tag localmente ejemplo:  git tag -d v0.1.0
```
### Arbol de nodos 
```
 git log --oneline --graph --decorate
// Se puede crear un alias para mas comodidas
// alias arbolito='git log --oneline --graph --decorate'
```