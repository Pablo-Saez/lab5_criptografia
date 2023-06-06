# Utiliza una imagen base de Ubuntu
FROM ubuntu:latest

# Actualiza el sistema y realiza la instalación de OpenSSH Server
RUN apt-get update && apt-get install -y openssh-server

# Establece una contraseña para el usuario root (cambia "tu_password" por una contraseña segura)
RUN 

# Abre el puerto 22 para conexiones SSH
EXPOSE 22

# Reinicia el servicio SSH
RUN service ssh restart
