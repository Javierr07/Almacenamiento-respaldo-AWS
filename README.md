# Arquitectura de Almacenamiento y Respaldo en AWS

## Servicios Utilizados 
- Amazon S3.
- S3 Glacier
- AWS CLI
- Politicas de Ciclo de vida.
- Amazon SNS

## Diagrama
muestra el diagrama del proyecto que estaremos desarrollando.
![image](https://github.com/user-attachments/assets/b690a69e-56b3-4dcc-9caa-a645ed7b6fea)

## Creacion de S3 y sus politicas de ciclo de vida

### creamos el bucket s3
![image](https://github.com/user-attachments/assets/77553df0-aa9d-441e-9700-507b99f6a09c)

### activamos el versionado 
![image](https://github.com/user-attachments/assets/25ed1a95-37b5-4550-85fa-7e051bbae4fd)

### politicas de ciclo de vida
se ha condifurado la politica de ciclo de vida en la cual todos los objetos dentro del bucket, se movenran automaticamente a glacier despues de 30 dias de no ser utilizado o frecuentado.
![image](https://github.com/user-attachments/assets/25bfdaf8-fdf1-4239-aa0b-91b21a163bab)




arquitectura de almacenamiento y respando usando servicios de AWS
