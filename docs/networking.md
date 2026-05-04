Diseño de red

## CIDR

10.0.0.0/16

|   Subnet  |     CIDR      |     AZ      |   Type   |
|-----------|---------------|-------------|----------|
|  public-a |  10.0.0.0/20  | us-east-1a  |  Public  |
|  public-b |  10.0.16.0/20 | us-east-1b  |  Public  |
| private-a |  10.0.128.0/20| us-east-1a  |  Private |
| private-b |  10.0.144.0/20| us-east-1b  |  Private |


##Internet Gateway

Se habilitó un gateway para las subredes publicas con 0.0.0.0 para acceso a internet y las subredes privadas tienen acceso aislado entre sí.



