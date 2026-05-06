# Infraestructura Cloud: Procesamiento de Imágenes Serverless

## 1. Resumen del Proyecto
Este proyecto implementa la configuración de Infraestructura como Código (IaC) para desplegar una arquitectura automatizada en Amazon Web Services (AWS). El sistema permite la ingesta de archivos mediante una API y su procesamiento asíncrono.

## 2. Arquitectura de Servicios
La solución utiliza los siguientes servicios de AWS para garantizar un flujo desacoplado:
* **Amazon API Gateway:** Interfaz REST para la recepción de solicitudes externas.
* **AWS Lambda:** Funciones encargadas de la carga (Upload) y el procesamiento (Crop).
* **Amazon S3:** Almacenamiento de objetos con disparadores de eventos configurados.
* **Amazon SQS:** Cola de mensajes para el desacoplamiento de los componentes de procesamiento.
* **AWS IAM:** Gestión de identidades y permisos bajo políticas de mínimo privilegio.

## 3. Implementación Multientorno
El despliegue está diseñado para soportar tres entornos distintos mediante el uso de archivos de variables específicos:
* **Desarrollo:** Envs/dev.tfvars
* **QA:** Envs/qa.tfvars
* **Producción:** Envs/prod.tfvars

## 4. Guía de Operación

### 4.1 Inicialización
Para preparar el entorno de trabajo y descargar los proveedores necesarios, ejecute:
```bash
cd Terraform
terraform init
