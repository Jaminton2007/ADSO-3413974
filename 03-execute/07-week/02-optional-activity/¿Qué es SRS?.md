# Ingeniería de Requerimientos — Proyecto MercaGo  
**Basado en la app desarrollada en el proyecto grupal: MercaGo**



## 1. Introducción

La ingeniería de requerimientos es una fase fundamental dentro del desarrollo de software, ya que permite identificar, analizar y documentar las necesidades de los usuarios para construir soluciones tecnológicas efectivas.

En el presente trabajo se aplica el proceso completo de ingeniería de requerimientos tomando como base el proyecto **MercaGo**, una aplicación orientada a la comparación de precios en supermercados. Para ello, se parte de la recolección de información mediante un cuestionario, seguido del análisis de los datos obtenidos y la definición de los requerimientos del sistema.



## 2. Aplicación del instrumento

El instrumento de recolección de información utilizado fue un cuestionario cerrado enfocado en los hábitos de compra de los usuarios y su disposición frente al uso de una aplicación comparadora de precios.

El cuestionario fue aplicado de manera simulada a una muestra de **50 personas**, con el objetivo de identificar patrones de comportamiento y necesidades relacionadas con el proceso de compra en supermercados.



## 3. Resultados del cuestionario

### 3.1 Rango de edad
- 18 – 25 años: 40%  
- 26 – 40 años: 35%  
- 41 – 60 años: 20%  
- Mayor de 60 años: 5%  

### 3.2 Frecuencia de compra
- Semanalmente: 60%  
- Cada 15 días: 25%  
- Mensualmente: 15%  

### 3.3 Responsable de compras
- Yo mismo/a: 55%  
- Compartido: 30%  
- Pareja: 10%  
- Otro: 5%  

### 3.4 Supermercados más usados
- D1: 70%  
- Ara: 65%  
- Éxito: 40%  
- Olímpica: 30%  

### 3.5 Comparación de precios
- Sí: 80%  
- No: 20%  

### 3.6 Cómo comparan precios
- Visitan varios supermercados: 50%  
- Consultan apps/webs: 25%  
- No comparan: 15%  
- Preguntan a conocidos: 10%  

### 3.7 Tiempo dedicado a comparar
- 15 – 30 minutos: 40%  
- 30 min – 1 hora: 30%  
- Menos de 15 min: 20%  
- Más de 1 hora: 10%  

### 3.8 Percepción de variación de precios
- Sí: 85%  
- No: 15%  

### 3.9 Principal problema
- No saber dónde es más barato: 55%  
- Falta de tiempo: 25%  
- Falta de información de ofertas: 20%  

### 3.10 Uso de una app como MercaGo
- Sí: 90%  
- No: 10%  

### 3.11 Funcionalidades más útiles
- Comparar precios: 75%  
- Ver ofertas: 60%  
- Crear listas: 45%  
- Carrito virtual: 20%  

### 3.12 Importancia de ahorrar dinero
- Nivel 5: 60%  
- Nivel 4: 25%  
- Nivel 3: 10%  
- Nivel 2 o menor: 5%  

### 3.13 Utilidad de precios en tiempo real
- Nivel 5: 65%  
- Nivel 4: 20%  
- Nivel 3: 10%  
- Nivel 2 o menor: 5%  

### 3.14 Dispositivo de acceso
- Celular Android: 70%  
- Computador: 20%  
- iPhone: 10%  

### 3.15 Preferencia de uso
- Aplicación móvil: 65%  
- Ambas: 20%  
- Web: 10%  
- Indiferente: 5%  



## 4. Análisis de la información

A partir de los resultados obtenidos en el cuestionario, se identifican patrones claros en los hábitos de compra de los usuarios.

En primer lugar, la mayoría de los encuestados realiza sus compras de manera semanal o quincenal, lo que indica que el proceso de compra es frecuente y relevante en su rutina.

Se evidencia que el 80% de los usuarios compara precios antes de realizar el mercado, lo que demuestra una alta preocupación por optimizar el gasto. Sin embargo, el 50% de estos usuarios realiza la comparación visitando físicamente varios supermercados, lo cual implica un proceso ineficiente en términos de tiempo y esfuerzo.

El principal problema identificado es la falta de información clara sobre en qué supermercado se encuentran los productos más económicos, señalado por el 55% de los encuestados. A esto se suma la falta de tiempo (25%) y la dificultad para acceder a ofertas (20%), lo que evidencia una necesidad de centralizar la información.

Adicionalmente, el 85% de los usuarios percibe que los precios varían significativamente entre supermercados, lo que refuerza la importancia de contar con herramientas que permitan comparar dicha información de forma rápida.

En cuanto a la viabilidad del sistema, el 90% de los encuestados manifestó que utilizaría una aplicación como MercaGo, lo que indica una alta aceptación del producto propuesto.

Finalmente, se observa que la mayoría de los usuarios prefiere el uso de dispositivos móviles, principalmente Android, lo que sugiere que la solución debe priorizar este tipo de plataforma.



## 5. Hallazgos principales

- Los usuarios comparan precios, pero el proceso actual es manual e ineficiente.  
- Existe pérdida de tiempo al visitar múltiples supermercados.  
- No hay una fuente centralizada de información de precios.  
- Los usuarios perciben una alta variación de precios entre supermercados.  
- Existe alta disposición al uso de una aplicación como solución.  
- El acceso se realiza principalmente desde dispositivos móviles.  



## 6. Requerimientos funcionales

- RF1: El sistema debe permitir al usuario buscar productos por nombre.  
- RF2: El sistema debe mostrar una comparación de precios del mismo producto en diferentes supermercados.  
- RF3: El sistema debe mostrar ofertas y promociones disponibles por supermercado.  
- RF4: El sistema debe permitir al usuario crear y gestionar listas de mercado personalizadas.  
- RF5: El sistema debe permitir visualizar el precio total estimado de una lista de compras.  
- RF6: El sistema debe actualizar la información de precios en tiempo real o en intervalos definidos.  
- RF7: El sistema debe permitir filtrar productos por supermercado.  
- RF8: El sistema debe permitir el acceso desde dispositivos móviles.  



## 7. Requerimientos no funcionales

- RNF1: El sistema debe tener un tiempo de respuesta menor a 3 segundos.  
- RNF2: El sistema debe ser accesible desde dispositivos móviles Android.  
- RNF3: La interfaz debe ser intuitiva y fácil de usar.  
- RNF4: El sistema debe estar disponible las 24 horas del día.  
- RNF5: El sistema debe garantizar la seguridad de los datos del usuario.  
- RNF6: El sistema debe ser escalable para soportar múltiples usuarios simultáneamente.  



## 8. Caso de uso: Comparar precios

**Actor:** Usuario  

**Descripción:** El usuario desea consultar el precio de un producto en diferentes supermercados para tomar una decisión de compra.  

**Flujo principal:**
1. El usuario ingresa el nombre del producto.  
2. El sistema procesa la solicitud.  
3. El sistema muestra una lista de precios en diferentes supermercados.  
4. El usuario analiza la información.  

**Resultado esperado:**  
El usuario identifica el supermercado con el mejor precio disponible.  



## 9. Conclusión

El desarrollo de este trabajo permitió aplicar de manera práctica el proceso de ingeniería de requerimientos, partiendo de la recolección de información hasta la definición de requerimientos del sistema.

Los resultados evidencian la necesidad de una herramienta como MercaGo, que permita optimizar el proceso de compra mediante la comparación de precios y la centralización de la información. Asimismo, se identificó una alta aceptación por parte de los usuarios, lo que respalda la viabilidad del proyecto.

En conclusión, la ingeniería de requerimientos permitió transformar datos en decisiones concretas para el desarrollo de una solución tecnológica alineada con las necesidades reales de los usuarios.
