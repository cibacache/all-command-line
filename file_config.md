 Si usas una versión de OSX superior a **Mac Sierra** (v10.12)
 debes crear o modificar un archivo **"config"** en la carpeta
 de tu usuario con el siguiente contenido (ten cuidado con
 las mayúsculas):
```
Host *
        AddKeysToAgent yes
        UseKeychain yes
        IdentityFile ruta-donde-guardaste-tu-llave-privada
```


 Añadir tu llave SSH al "servidor" de llaves SSH de tu
 computadora (en caso de error puedes ejecutar este
 mismo comando pero sin el argumento -K):

```bash
ssh-add -K ruta-donde-guardaste-tu-llave-privada
```
