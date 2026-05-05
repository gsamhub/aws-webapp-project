# Security Design / Diseño de Seguridad

---

## ENG

This section describes the security design implemented in the AWS architecture.

The security model follows AWS best practices based on the principles of least privilege, network isolation, and controlled access between layers.

---

### Security Layers Overview

The architecture implements multiple security layers:

---

### 1. Network Security (VPC Level)

- Public and private subnet separation
- Private subnets are not directly accessible from the internet
- Internet-facing traffic is only allowed through the Application Load Balancer (ALB)
- NAT Gateway is used for controlled outbound internet access from private subnets

---

### 2. Security Groups (Instance-Level Security)

**ALB Security Group**
- Allows inbound HTTP/HTTPS traffic from the internet
- Acts as the only entry point to the architecture

**EC2 Security Group**
- Allows inbound traffic only from the ALB Security Group
- No direct public access to EC2 instances

---

### 3. IAM Roles (Access Control)

- EC2 instances use IAM roles for AWS service access
- No hardcoded credentials are used
- Access is granted based on least privilege policies

---

### 4. Traffic Control Model

- All inbound traffic flows through the ALB
- Private instances are isolated from direct internet exposure
- Outbound traffic from private instances is routed through NAT Gateway

---

## ESP

Esta sección describe el diseño de seguridad implementado en la arquitectura de AWS.

El modelo de seguridad sigue buenas prácticas de AWS basadas en el principio de mínimo privilegio, aislamiento de red y control de acceso entre capas.

---

### Capas de seguridad

La arquitectura implementa múltiples capas de seguridad:

---

### 1. Seguridad de red (nivel VPC)

- Separación entre subredes públicas y privadas
- Las subredes privadas no son accesibles directamente desde internet
- El tráfico entrante pasa únicamente por el Application Load Balancer (ALB)
- NAT Gateway se utiliza para salida controlada a internet desde subredes privadas

---

### 2. Security Groups (seguridad a nivel instancia)

**Security Group del ALB**
- Permite tráfico HTTP/HTTPS desde internet
- Es el único punto de entrada a la arquitectura

**Security Group de EC2**
- Solo permite tráfico desde el Security Group del ALB
- No existe acceso público directo a las instancias

---

### 3. Roles IAM (control de acceso)

- Las instancias EC2 utilizan roles IAM para acceder a servicios de AWS
- No se utilizan credenciales embebidas
- El acceso se basa en el principio de mínimo privilegio

---

### 4. Modelo de control de tráfico

- Todo el tráfico entrante pasa por el ALB
- Las instancias privadas están aisladas de internet directo
- El tráfico saliente de las instancias privadas se enruta mediante NAT Gateway

---

# Security Evidence / Evidencia de Seguridad

---

## Security Groups Configuration
### EC2
<img width="1372" height="445" alt="image" src="https://github.com/user-attachments/assets/c5a5422e-bd1b-4ce0-92d8-9117b8adb49b" />

### ALB

<img width="1439" height="480" alt="image" src="https://github.com/user-attachments/assets/7077b084-3c1d-4dbf-bcbf-73afdc158492" />

## EC2 without public IP

<img width="1719" height="905" alt="Ec2" src="https://github.com/user-attachments/assets/0ab8445f-e528-438e-849f-6ff90301c6e8" />

