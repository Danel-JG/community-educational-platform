# Community Educational Platform

Sistema educativo comunitario desplegado automáticamente usando AWS, Terraform, Ansible y Docker.

## Descripción

Este proyecto implementa una plataforma educativa accesible desde una red comunitaria local o infraestructura cloud. El objetivo es automatizar completamente el despliegue del entorno utilizando herramientas DevOps e Infrastructure as Code (IaC).

La plataforma permite:

- Acceso a cursos educativos
- Recursos académicos
- Evaluaciones
- Navegación web local
- Despliegue reproducible y portable

El sistema fue diseñado pensando en posibles escenarios de redes comunitarias y conectividad limitada.

---

# Tecnologías utilizadas

## Cloud & Infraestructura

- AWS EC2
- Terraform
- Security Groups
- SSH

## Automatización

- Ansible

## Contenedores

- Docker
- Docker Compose

## Frontend

- HTML5
- CSS3

---

# Arquitectura del proyecto

```bash
community-educational-platform/
│
├── ansible/
│   ├── ansible.cfg
│   ├── inventory.ini
│   └── playbook.yml
│
├── docker/
│   ├── docker-compose.yml
│   └── website/
│       ├── index.html
│       ├── css/
│       └── pages/
│
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
│
├── docs/
│   ├── architecture.md
│   ├── deployment.md
│   └── network-design.md
│
├── scripts/
│
├── .gitignore
└── README.md
```

---

# Objetivos del proyecto

- Automatizar infraestructura cloud
- Automatizar despliegue de servicios
- Implementar contenedores Docker
- Aplicar principios DevOps
- Comprender redes comunitarias
- Crear una plataforma educativa accesible
- Implementar infraestructura reproducible

---

# Despliegue Cloud

## Componentes AWS

La infraestructura crea automáticamente:

- Instancia EC2
- Security Groups
- Acceso SSH
- Configuración de red básica

## Terraform

Terraform se utiliza para:

- Provisionar infraestructura
- Gestionar estado de infraestructura
- Automatizar creación de EC2
- Configurar puertos y acceso

### Inicializar Terraform

```bash
cd terraform
terraform init
```

### Verificar infraestructura

```bash
terraform plan
```

### Crear infraestructura

```bash
terraform apply
```

### Ver outputs

```bash
terraform output
```

---

# Automatización con Ansible

Ansible automatiza:

- Actualización del sistema
- Instalación de Docker
- Instalación de Docker Compose
- Configuración del entorno
- Copia de archivos web
- Despliegue de contenedores

## Ejecutar playbook

```bash
cd ansible
ansible-playbook -i inventory.ini playbook.yml
```

## Verificar conectividad

```bash
ansible all -i inventory.ini -m ping
```

---

# Docker

El servicio principal se ejecuta usando contenedores Docker.

## Ventajas del uso de Docker

- Portabilidad
- Aislamiento
- Reproducibilidad
- Facilidad de despliegue
- Escalabilidad

## Levantar contenedores manualmente

```bash
cd docker
docker compose up -d
```

## Ver contenedores activos

```bash
docker ps
```

---

# Acceso a la plataforma

Abrir en navegador:

```text
http://PUBLIC_IP
```

---

# Entorno local

El proyecto también puede ejecutarse localmente.

## Requisitos

- Docker
- Docker Compose

## Instalación

```bash
sudo apt update
sudo apt install docker.io docker-compose -y
```

## Ejecutar localmente

```bash
cd docker
docker compose up -d
```

## Acceso local

```text
http://localhost
```

---

# Redes comunitarias

## Aplicación en redes mesh

La plataforma podría utilizarse en:

- Redes educativas rurales
- Redes mesh comunitarias
- Entornos con conectividad limitada
- Laboratorios locales
- Centros comunitarios

## Beneficios

- Acceso local a recursos educativos
- Reducción de dependencia de internet
- Compartición de contenido local
- Bajo consumo de ancho de banda
- Infraestructura autónoma

## Retos

- Escalabilidad
- Sincronización de contenido
- Administración distribuida
- Seguridad de red
- Disponibilidad energética

---

# Puertos utilizados

| Servicio | Puerto |
|---|---|
| HTTP | 80 |
| SSH | 22 |

---

# Seguridad

## Buenas prácticas aplicadas

- Uso de llaves SSH
- Exclusión de credenciales del repositorio
- Automatización reproducible
- Separación de infraestructura y aplicación

## Archivos excluidos

NO se deben subir:

- `.pem`
- llaves privadas
- Access Keys
- tokens
- credenciales

---

# Problemas encontrados

## Problemas durante el desarrollo

- Errores de imágenes Docker inexistentes
- Problemas con Docker Compose v1/v2
- Cambios dinámicos de IP pública AWS
- Problemas de permisos Docker
- Conflictos de contenedores huérfanos

## Soluciones aplicadas

- Actualización de imágenes Docker
- Migración a Docker Compose v2
- Reconfiguración de inventarios Ansible
- Limpieza de contenedores
- Uso de SSH keys

---

# Verificación del sistema

## Verificar Terraform

```bash
terraform output
```

## Verificar Ansible

```bash
ansible all -i inventory.ini -m ping
```

## Verificar Docker

```bash
docker ps
```

---

# Integrantes

- Daniel Guerra

---

# Conclusiones

El proyecto permitió aplicar conceptos de:

- DevOps
- Automatización
- Infrastructure as Code
- Contenedores
- Redes
- Cloud Computing

La solución implementada demuestra cómo automatizar completamente el despliegue de una plataforma educativa utilizando herramientas modernas de infraestructura y configuración.

---

# Licencia

Proyecto académico.
