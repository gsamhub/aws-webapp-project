# Networking Design / Diseño de Red

---

## ENG

This section explains the networking design implemented in AWS.

The architecture is based on a custom VPC with subnet segmentation across multiple Availability Zones to ensure high availability and isolation.

---

### VPC Design

- Custom VPC created for full network control
- CIDR block designed to allow subnet segmentation
- Clear separation between public and private subnets

---

### Subnet Strategy

**Public Subnets**
- Application Load Balancer (ALB)
- Internet Gateway access

**Private Subnets**
- EC2 application servers
- No direct internet exposure

---

### Routing Design

- Public route tables allow inbound/outbound internet traffic via Internet Gateway
- Private route tables route outbound traffic through NAT Gateway only

---

### Availability Zones

Resources are distributed across two Availability Zones to ensure high availability and fault tolerance.

---

## ESP

Esta sección explica el diseño de red implementado en AWS.

La arquitectura se basa en una VPC personalizada con segmentación de subredes en múltiples zonas de disponibilidad para garantizar alta disponibilidad y aislamiento.

---

### Diseño de VPC

- VPC personalizada para control total de red
- CIDR diseñado para permitir segmentación de subredes
- Separación clara entre subredes públicas y privadas

---

### Estrategia de subredes

**Subredes públicas**
- Application Load Balancer (ALB)
- Acceso a Internet Gateway

**Subredes privadas**
- Servidores EC2 de aplicación
- Sin exposición directa a internet

---

### Diseño de enrutamiento

- Las tablas públicas permiten tráfico desde/hacia Internet mediante Internet Gateway
- Las tablas privadas enrutan el tráfico saliente a través de NAT Gateway

---

### Zonas de disponibilidad

Los recursos están distribuidos en dos zonas de disponibilidad para garantizar alta disponibilidad y tolerancia a fallos

---

# Architecture Evidence / Evidencia de arquitectura

---

## VPC and Subnet Configuration
<img width="1669" height="891" alt="VPC" src="https://github.com/user-attachments/assets/3601fe92-c849-49ea-9724-739a223d0fcd" />

---

## Internet Gateway Configuration
<img width="1698" height="364" alt="IGW" src="https://github.com/user-attachments/assets/0d241851-bd2a-49b4-b0cc-6c29fa173548" />

---

## EC2 Instances across Availability Zones
<img width="1918" height="1031" alt="2InstanciasendiferentesSubRedes" src="https://github.com/user-attachments/assets/19bef8a7-8e19-491c-8d76-2c6f00ce1668" />
