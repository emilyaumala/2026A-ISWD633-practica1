# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
# COMPLETAR
<img width="2465" height="293" alt="image" src="https://github.com/user-attachments/assets/63069f11-098e-413b-8f6b-499b4c6a0a8b" />

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
# COMPLETAR
<img width="2622" height="675" alt="image" src="https://github.com/user-attachments/assets/2f3c054e-d411-42c6-9964-04a2e767406d" />


### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
# COMPLETAR
<img width="2667" height="330" alt="image" src="https://github.com/user-attachments/assets/9e38039e-544b-4142-bd8b-9d21b704e6bb" />


### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```
<img width="2166" height="97" alt="image" src="https://github.com/user-attachments/assets/a29c7a1a-bd22-445b-8a39-02337aa242c0" />

### Para detener un contenedor

```
docker stop <nombre contenedor>
```
<img width="1061" height="207" alt="image" src="https://github.com/user-attachments/assets/b446a3dc-342a-46c4-a691-25832bb5a2fc" />

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
# COMPLETAR
<img width="2281" height="1394" alt="image" src="https://github.com/user-attachments/assets/a287ec4f-d26b-42e0-9e31-64a3935a953c" />

**¿Qué sucede luego de la ejecución del comando?**
Se esta ejecutando el proceso.

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
# COMPLETAR
<img width="2232" height="300" alt="image" src="https://github.com/user-attachments/assets/fb075279-6da7-412e-a2f4-955ae7d6fbeb" />

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
# COMPLETAR
<img width="2583" height="696" alt="image" src="https://github.com/user-attachments/assets/669073cc-335c-459c-ac31-f175dc1041b3" />

Verificar que el contenedor que se eliminó
# COMPLETAR
<img width="2583" height="696" alt="image" src="https://github.com/user-attachments/assets/08cc37d4-13f9-4f69-b1d0-e03791f6e310" />

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
# COMPLETAR
<img width="2214" height="264" alt="image" src="https://github.com/user-attachments/assets/cb7138ef-396f-487f-ac60-dd8c1903557f" />

Verificar que el contenedor que se eliminó
# COMPLETAR
<img width="2356" height="133" alt="image" src="https://github.com/user-attachments/assets/db220829-d18c-4f8e-b535-05d71b785673" />

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
# COMPLETAR
<img width="2468" height="1377" alt="image" src="https://github.com/user-attachments/assets/cf991912-61a3-46d7-abf0-b7ba8861bf20" />
