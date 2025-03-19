# Despliegue de Recursos con Terraform en Azure

Este documento describe los pasos necesarios para desplegar una Azure Function y una máquina virtual Linux en Azure utilizando Terraform. Se incluyen comandos, imágenes de referencia y una breve explicación de cada paso.

## PARTE 1: Despliegue de AZURE FUNCTION

1. Inicializar Terraform

Antes de comenzar, debemos inicializar Terraform para descargar los proveedores necesarios y preparar el entorno.
```bash
terraform init
```
![Imagen 1. Terraform Init](images/image_1.png)

2. Validar la configuración

Verificamos que la configuración y sintaxis de nuestros archivos de Terraform sean correctas.
```bash
terraform validate
```
![Imagen 2. Terraform Validate](images/image_2.png)

3. Ver el plan de ejecución

Este comando nos permite ver un resumen de los cambios que Terraform realizará en la infraestructura antes de aplicarlos.
```bash
terraform plan
```
![Imagen 3. Terraform Plan](images/image_3.png)
![Imagen 3_1. Terraform Plan](images/image_3_1.png)

4. Aplicar los cambios

Ejecutamos el siguiente comando para desplegar la Azure Function en la nube.
```bash
terraform apply
```
![Imagen 4. Terraform Apply](images/image_4.png)
![Imagen 4_1. Terraform Apply](images/image_4_1.png)
![Imagen 4_2. Terraform Apply](images/image_4_2.png)
Confirmamos con `yes` cuando se nos solicite.

5. Destruir los recursos

Si necesitamos eliminar la infraestructura creada, utilizamos:
```bash
terraform destroy
```
![Imagen 5. Terraform Destroy](images/image_5.png)
![Imagen 5_1. Terraform Destory](images/image_5_1.png)

## PARTE 2: DESPLEGAR VM_LINUX CON TERRAFORM

1. Inicializar Terraform

Al igual que en el despliegue anterior, debemos inicializar Terraform.
```bash
terraform init
```
![Imagen 6. Terraform Init](images/image_6.png)

2. Validar la configuración

Revisamos que los archivos de configuración no contengan errores.
```bash
terraform validate
```
![Imagen 7. Terraform Validate](images/image_7.png)

3. Ver el plan de ejecución

Obtenemos un resumen de los cambios que se aplicarán en la infraestructura.
```bash
terraform plan
```
![Imagen 8. Terraform Plan](images/image_8.png)
![Imagen 8_1. Terraform Plan](images/image_8_1.png)

4. Aplicar los cambios

Ejecutamos el comando para desplegar la máquina virtual Linux.
```bash
terraform apply
```
![Imagen 9. Terraform Apply](images/image_9.png)
![Imagen 9_1. Terraform Apply](images/image_9_1.png)
![Imagen 9_2. Terraform Apply](images/image_9_2.png)
![Imagen 9_3. Terraform Apply](images/image_9_3.png)

Confirmamos con `yes` cuando se nos solicite.


5. Destruir los recursos

Si es necesario eliminar la máquina virtual y otros recursos asociados, ejecutamos:
```bash
terraform destroy
```
![Imagen 10. Terraform Destroy](images/image_10.png)
![Imagen 10_1. Terraform Destory](images/image_10_1.png)
