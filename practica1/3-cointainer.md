# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
docker create --name srv-web nginx:latest
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
# COMPLETAR

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
```
docker create hello-world:latest
```

# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
docker start srv-web

```
Iniciar el contenedor srv-web 
# COMPLETAR

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

### Para detener un contenedor

```
docker stop <nombre contenedor>
docker stop srv-web
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
docker run --name srv-web2 nginx:alpine
```
![Ecosistema de Docker](imagenes/dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
# COMPLETAR

**¿Qué sucede luego de la ejecución del comando?**
![Result](Results/7.PNG)


# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
docker run -d --name srv-web2 nginx:alpine
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
# COMPLETAR

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
docker rm strange_austin
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
# COMPLETAR

Verificar que el contenedor que se eliminó
![Result](Results/8.PNG)
# COMPLETAR

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
docker rm -f srv-web3
```
Eliminar el contenedor **srv-web3** 
# COMPLETAR

Verificar que el contenedor que se eliminó
![Result](Results/9.PNG)
# COMPLETAR

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
![Result](Results/10.PNG)
# COMPLETAR
