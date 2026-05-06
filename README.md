# Infraestructura Cloud: Procesamiento de Imágenes Serverless

## 1. Resumen del Proyecto
[cite_start]Este proyecto implementa la configuración de Infraestructura como Código (IaC) para desplegar una arquitectura automatizada en Amazon Web Services (AWS)[cite: 3, 4]. [cite_start]El sistema permite la ingesta de archivos mediante una interfaz API y su posterior procesamiento asíncrono[cite: 5].

## 2. Arquitectura de Servicios
[cite_start]La solución utiliza los siguientes servicios de AWS para garantizar un flujo desacoplado[cite: 6]:
* [cite_start]**Amazon API Gateway:** Interfaz REST para la recepción de solicitudes externas[cite: 7].
* [cite_start]**AWS Lambda:** Funciones encargadas de la carga (`upload-lambda`) y el procesamiento (`crop-lambda`)[cite: 8].
* [cite_start]**Amazon S3:** Almacenamiento de objetos con disparadores de eventos configurados[cite: 9].
* [cite_start]**Amazon SQS:** Cola de mensajes para el desacoplamiento de los componentes de procesamiento[cite: 10].
* [cite_start]**AWS IAM:** Gestión de identidades y permisos bajo políticas de mínimo privilegio[cite: 11].

## 3. Implementación Multientorno
[cite_start]El despliegue está diseñado para soportar tres entornos distintos mediante el uso de archivos de variables específicos[cite: 12, 13]:
* [cite_start]**Desarrollo:** `Envs/dev.tfvars` [cite: 14]
* [cite_start]**QA:** `Envs/qa.tfvars` [cite: 15]
* [cite_start]**Producción:** `Envs/prod.tfvars` [cite: 16]

## 4. Guía de Operación

### 4.1 Inicialización
[cite_start]Para preparar el entorno de trabajo y descargar los proveedores necesarios, ejecute[cite: 17, 18]:
```bash
cd Terraform
terraform init
