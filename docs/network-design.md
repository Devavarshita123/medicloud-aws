# VPC CIDR : 10.0.0.0/16

Public Subnet A → 10.0.1.0/24
Public Subnet B → 10.0.2.0/24
Private App Subnet A → 10.0.11.0/24
Private App Subnet B → 10.0.12.0/24
Private DB Subnet A → 10.0.21.0/24
Private DB Subnet B → 10.0.22.0/24

## Network Layout

VPC
├── Public Subnet A
│   ├── Application Load Balancer
│   ├── NAT Gateway
│   └── Bastion Host
│
├── Public Subnet B
│   └── Application Load Balancer
│
├── Private App Subnet A
│   └── ECS/EC2 Application
│
├── Private App Subnet B
│   └── ECS/EC2 Application
│
├── Private DB Subnet A
│   └── Amazon RDS
│
└── Private DB Subnet B
    └── Amazon RDS


## Internet Connectivity

Internet
    │
Internet Gateway
    │
Public Route Table
    │
Public Subnets
    │
Application Load Balancer
    │
Private Application
    │
Amazon RDS
