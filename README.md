# Arquitectura de Almacenamiento y Respaldo en AWS

## Servicios Utilizados 
- Amazon S3.
- S3 Glacier
- AWS Lambda
- Politicas de Ciclo de vida.
- Amazon SNS

## Diagrama
muestra el diagrama del proyecto que estaremos desarrollando.
![image](https://github.com/user-attachments/assets/4055d1d1-0c0a-40e9-b60a-1c8193d2257a)


## Creacion de S3 y sus politicas de ciclo de vida

### creamos el bucket s3
![image](https://github.com/user-attachments/assets/77553df0-aa9d-441e-9700-507b99f6a09c)

### activamos el versionado 
![image](https://github.com/user-attachments/assets/25ed1a95-37b5-4550-85fa-7e051bbae4fd)

### politicas de ciclo de vida
se ha configurado la politica de ciclo de vida en la cual todos los objetos dentro del bucket, se movenran automaticamente a glacier despues de 30 dias de no ser utilizado o frecuentado.
![image](https://github.com/user-attachments/assets/25bfdaf8-fdf1-4239-aa0b-91b21a163bab)

## Topic SNS AlertaS3
Informacion del topic.
![image](https://github.com/user-attachments/assets/a40ce992-98a2-4b1a-a1f4-99c2bc9a05d9)

## politica de acceso
sele agrego la siguiente politica de acceso a nuestro topic AlertaS3 de notificaciones para que permita recibir las notificaciones del bucket.
![image](https://github.com/user-attachments/assets/25adca50-e292-49cd-be63-a64fa4526e37)

este primer topic recibira las ntificaciones desde Amazon S3 con el siguiente formato
![image](https://github.com/user-attachments/assets/9797a101-7d2a-4888-88a1-1113836389bd)

## Funcion Lambda Email-s3
esta funcion recibe la notificacion desde el topic AlertaS3 para reformatear la notificacion y darle una mejor legilibilidad.
![image](https://github.com/user-attachments/assets/bd05b6ed-aa73-4343-9316-2f0b469d51f9)

## Topic Email-Usuario
este topic recibira las notificaciones desde la funcion Lambda la cual formateara la notificacion, el cual se encargara de reenviarlo al Email correspondiente.
![image](https://github.com/user-attachments/assets/21691cba-263c-4ecc-81db-a3410dc39a44)

Este es el nuevo formato de las notificaciones la cual resalta los datos importante de la notificacion como lo es el evento realizado, el bucket, y la fecha en que se realizo el evento.
![image](https://github.com/user-attachments/assets/f8a62186-e43d-4b53-acdd-58a905c198a3)








arquitectura de almacenamiento y respando usando servicios de AWS
