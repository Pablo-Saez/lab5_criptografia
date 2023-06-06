# Utiliza una imagen base de Ubuntu 20.10
FROM ubuntu:20.10
RUN sed -i 's/archive.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list 
RUN sed -i 's/security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list 

RUN apt-get update && apt-get install -y apt-transport-https

RUN useradd --create-home --shell /bin/bash test
RUN echo 'test:test' | chpasswd
# Actualiza el sistema y realiza la instalación de OpenSSH Server
RUN apt-get update && apt-get install -y openssh-server
RUN apt-get install -y openssh-client
# Copia el archivo de configuración del servidor SSH
# COPY sshd_config /etc/ssh/sshd_config

# # Crea un directorio para los archivos de autenticación
# RUN mkdir /var/run/sshd

# # Establece una contraseña para el usuario root (cambia "tu_password" por una contraseña segura)
# RUN echo 'root:password' | chpasswd

# # Abre el puerto 22 para conexiones SSH
# EXPOSE 22

# # Reinicia el servicio SSH
# RUN service ssh restart

# # Establece el comando para iniciar el servidor SSH
# CMD ["/usr/sbin/sshd", "-D"]
