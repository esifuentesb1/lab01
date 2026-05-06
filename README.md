Aquí tienes todo el contenido de tu PDF convertido a **Markdown limpio**, listo para pegar en tu `README.md`:

---

````markdown
# Infraestructura Cloud: Procesamiento de Imágenes Serverless

## 1. Resumen del Proyecto

Este proyecto implementa la configuración de **Infraestructura como Código (IaC)** para desplegar una arquitectura automatizada en AWS.  
El sistema permite la ingesta de archivos mediante una API y su procesamiento asíncrono.

---

## 2. Arquitectura de Servicios

- **Amazon API Gateway**: Interfaz REST para solicitudes externas.  
- **AWS Lambda**: Funciones de carga (Upload) y procesamiento (Crop).  
- **Amazon S3**: Almacenamiento con disparadores de eventos.  
- **Amazon SQS**: Cola para el desacoplamiento de componentes.  
- **AWS IAM**: Gestión de identidades bajo políticas de mínimo privilegio.  

---

## 3. Implementación Multientorno

Soporte para tres entornos mediante archivos `.tfvars`:

- **Desarrollo**: `Envs/dev.tfvars`  
- **QA**: `Envs/qa.tfvars`  
- **Producción**: `Envs/prod.tfvars`  

---

## 4. Guía de Operación

### 4.1 Inicialización

```bash
cd Terraform
terraform init
````

### 4.2 Despliegue (DEV)

```bash
terraform apply -var-file="../Envs/dev.tfvars"
```

### 4.3 Destrucción

```bash
terraform destroy -var-file="../Envs/dev.tfvars"
```

---

## 5. Estructura de Archivos

```
/Modules     # Lógica modularizada
/Envs        # Variables por entorno
/Terraform   # Código principal
```

---

## Información del Proyecto

* **Autor**: Anthony
* **Materia**: Computación en la Nube

```

---

Si quieres, puedo mejorarlo más (por ejemplo: agregar badges, diagramas, o hacerlo estilo GitHub pro con tablas y emojis).
```
