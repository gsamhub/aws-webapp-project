Architecture Overview / Vista de Arquitectura

## 🇺🇸 English

This document describes the overall architecture of the AWS Highly Available Web Architecture project.

The system is designed to ensure high availability, fault tolerance, and scalability using a multi-AZ deployment model.

### Key Components

- Application Load Balancer (ALB)
- EC2 instances deployed across multiple Availability Zones
- Public and private subnets
- NAT Gateway for controlled outbound internet access
- VPC with segmented network design

### High-Level Design

The architecture follows a layered approach:

1. Internet-facing load balancer (ALB)
2. Public subnets hosting the ALB
3. Private subnets hosting application servers (EC2)
4. NAT Gateway for outbound traffic from private instances

---

## 🇪🇸 Español

Este documento describe la arquitectura general del proyecto AWS Highly Available Web Architecture.

El sistema está diseñado para garantizar alta disponibilidad, tolerancia a fallos y escalabilidad mediante un modelo de despliegue multi-AZ.

Componentes principales
- Application Load Balancer (ALB)
- Instancias EC2 distribuidas en múltiples zonas de disponibilidad
- Subredes públicas y privadas
- NAT Gateway para salida controlada a internet
- VPC con segmentación de red

### Diseño general

La arquitectura sigue un enfoque por capas:

1. Balanceador de carga público (ALB)
2. Subredes públicas donde reside el ALB
3. Subredes privadas con servidores EC2
4. NAT Gateway para tráfico saliente
