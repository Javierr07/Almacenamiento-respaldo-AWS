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

## Topic a utilizar para las alertas del bucket.
configuracion general del topic a utilizar, el ecual se muestra el email que recibira las notificaciones
![image](https://github.com/user-attachments/assets/f01df1eb-ea5c-4c52-aafe-c85e5d7784d8)


## politica de acceso
sele agrego la siguiente politica de acceso a nuestro topic de notificaciones para que permita recibir las notificaciones del bucket.
![image](https://github.com/user-attachments/assets/1dcbe4a1-3937-49a7-ba43-6901d44ff821)



arquitectura de almacenamiento y respando usando servicios de AWS
