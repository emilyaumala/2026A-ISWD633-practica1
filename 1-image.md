# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**
# COMPLETAR

**¿Qué es nginx?**
NGINX es un software de código abierto para servidores web, proxy inverso, almacenamiento en caché, equilibrio de carga, transmisión de medios y más .

# COMPLETAR 

Descargar la imagen  **nginx** en la versión **alpine**
# COMPLETAR
<img width="2350" height="1225" alt="image" src="https://github.com/user-attachments/assets/417f8038-9aa0-4e80-97e6-136f329ead23" />

### Listar imágenes

```
docker images
```

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 

<img width="2880" height="1524" alt="image" src="https://github.com/user-attachments/assets/ebda9461-f07e-431a-a985-129156ceed1d" />


**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
<img width="2880" height="1524" alt="image" src="https://github.com/user-attachments/assets/716a9723-ee9b-4c91-9957-ec3fc6bb5365" />

# COMPLETAR

**¿Con qué algoritmo se está generando el ID de la imagen**
Con SHA-256 que es una función criptográfica unidireccional que convierte cualquier cantidad de datos en una huella digital única y fija de 256 bits

# COMPLETAR

### Filtrar imágenes

```
docker images | grep/findstr <termino a buscar>

<img width="2880" height="1524" alt="image" src="https://github.com/user-attachments/assets/d207e457-0f5e-4603-be6b-18c513752378" />


```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 
# COMPLETAR
<img width="1991" height="164" alt="image" src="https://github.com/user-attachments/assets/419ccf0c-9dc3-4132-8d40-99904753badc" />

-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
