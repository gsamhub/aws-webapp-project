# Networking Design / Diseño de Red

## 🇺🇸 English

This section explains the networking design implemented in AWS.

The architecture is based on a VPC with subnet segmentation across multiple Availability Zones.

### VPC Design

- Custom VPC created for full network control
- CIDR block designed to allow subnet segmentation
- Separation between public and private subnets

### Subnet Strategy

- **Public Subnets**
  - ALB deployment
  - Internet Gateway access

- **Private Subnets**
  - EC2 application servers
  - No direct internet access

### Routing

- Public route tables allow internet traffic via Internet Gateway
- Private route tables route outbound traffic through NAT Gateway

### Availability Zones

Resources are distributed across two AZs to ensure high availability.


## 🇪🇸 Español

Esta sección explica el diseño de red implementado en AWS.

La arquitectura se basa en una VPC con segmentación de subredes en múltiples zonas de disponibilidad.

### Diseño de VPC
- VPC personalizada para control total de red
- CIDR diseñado para permitir segmentación
- Separación entre subredes públicas y privadas


### Estrategia de subredes


**Subredes públicas**
- Despliegue del ALB
- Acceso a Internet Gateway


**Subredes privadas**
-Servidores EC2 de aplicación
-Sin acceso directo a internet

### Enrutamiento
- Las tablas públicas permiten tráfico a Internet vía Internet Gateway
- Las privadas usan NAT Gateway para salida controlada


### Zonas de disponibilidad
Los recursos están distribuidos en dos AZs para alta disponibilidad

---

## Screenshots/Capturas:

### VPC/Subnet Config:
<img width="1669" height="891" alt="VPC" src="https://github.com/user-attachments/assets/3601fe92-c849-49ea-9724-739a223d0fcd" />

### Internet Gateway
<img width="1698" height="364" alt="IGW" src="https://github.com/user-attachments/assets/0d241851-bd2a-49b4-b0cc-6c29fa173548" />

### Ec2 in different availability zones

<img width="1918" height="1031" alt="2InstanciasendiferentesSubRedes" src="https://github.com/user-attachments/assets/19bef8a7-8e19-491c-8d76-2c6f00ce1668" />


