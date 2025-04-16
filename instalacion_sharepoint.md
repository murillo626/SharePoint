# Paso a Paso: Instalación de SharePoint en Máquina Virtual

## Autores:
- Isaac Murillo
- Renzo Aguirre 

---

## Requisitos Iniciales

- Windows Server 2019 (virtualizado)
- SQL Server 2022 Developer Edition
- SharePoint Server 2019
- RAM mínima: 10 GB
- Almacenamiento sugerido: 60 GB+

---

## Pasos Generales

### 1. Instalación y Configuración de Windows Server
- Instalar Windows Server 2019
- Asignar nombre estático al servidor (ej: `PROYECTO`)
- Configurar IP fija si se trabaja en red

### 2. Instalar y Configurar Active Directory (AD DS)
- Promover el servidor a controlador de dominio (`proyecto.local`)
- Reiniciar y confirmar ingreso como `proyecto\Administrator`

### 3. Instalar SQL Server 2022 Developer
- Elegir instalación personalizada
- Activar modo mixto (Windows + SQL Auth)
- Agregar usuarios `Administrator` y `spfarm` como `sysadmin`
- Verificar habilitación de TCP/IP

### 4. Instalar SharePoint Server 2019
- Ejecutar Prerequisite Installer
- Instalar SharePoint Server
- Ejecutar configuración de la granja
  - Crear nueva granja
  - Usar `PROYECTO0\spfarm` como cuenta de servicio
  - Conectarse a SQL Server
  - Elegir rol “Single-Server Farm”
  - Definir puerto de Central Administration
  - Finalizar instalación

---

## Resultado

- Sitio SharePoint funcional
- Módulo de Finanzas operativo según PDF
- Integración lista para entrega y evaluación

---

