# aws-examen-web-Andres-MartinezMartinez
## Examen AWS: Creación de una VPC con Máquinas Virtuales y Despliegue Web
### Paso 1: Crear una VPC en AWS
```bash
   - Crear una VPC llamada: mi-vpc-TuNombre-Apellidos.
   - CIDR Block: 10.0.0.0/16
``` 
![alt text](./img/img1.png)
```bash
   - Crea dos subredes:
        - subnet-linux: CIDR 10.0.1.0/24
        - subnet-windows: CIDR 10.0.2.0/24
``` 
![alt text](./img/img2.png)
![alt text](./img/img3.png)
```bash
    - Crea una Internet Gateway asociada a la VPC
``` 
![alt text](./img/img4.png)
![alt text](./img/img5.png)
```bash
    - Añade una regla en la tabla de rutas (0.0.0.0/0) hacia el Internet Gateway
``` 
![alt text](./img/img6.png)
![alt text](./img/img7.png)
### Paso 2: Creación de instancias EC2
#### 1. Instancias EC2 Windows
```bash
    - Windows Server 2022 en la subnet-windows.
``` 
![alt text](./img/img8.png)
![alt text](./img/img13.png)
```bash
    - Tipo: t3.medium.
``` 
![alt text](./img/img9.png)
```bash
    - Crea las llaves.
``` 
![alt text](./img/img10.png)
```bash
    - Security Group Entrante: HTTP (80), Vite (5173), RDP (3389).
``` 
![alt text](./img/img11.png)
![alt text](./img/img12.png)
#### 2. Instancias EC2 Linux(Ubuntu)
```bash
    - Ubuntu 22.04 en la subnet-linux.
``` 
![alt text](./img/img14.png)
![alt text](./img/img15.png)
```bash
    - IP pública asignada.
``` 
![alt text](./img/img16.png)
```bash
    - Security Group Entrante: HTTP (80), Vite (5173), SSH (22)
``` 
![alt text](./img/img17.png)
![alt text](./img/img18.png)
```bash
    - Acceso mediante clave privada SSH.
``` 
![alt text](./img/img24.png)
### Paso 3: Instalación y despliegue web
```bash
    - Linux (Ubuntu SSH)
``` 
![alt text](./img/img29.png)
![alt text](./img/img19.png)
![alt text](./img/img20.png)
![alt text](./img/img21.png)
![alt text](./img/img22.png)
![alt text](./img/img23.png)
![alt text](./img/img25.png)
![alt text](./img/img26.png)
![alt text](./img/img27.png)


### Paso 4: Pull request
![alt text](./img/pullrequest.png)
![alt text](./img/img28.png)
