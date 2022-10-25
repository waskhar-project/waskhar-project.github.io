---
title: "Análisis y diseño de Smart Contracts a partir de los procesos modelados con BPMN"
date: 2022-08-10T10:50:40+02:00
draft: false
authors: ["Carlos Ticla"]
layout: single_article
categories: [BPMN, Process Modeling, Smart Contract]
url: /2022/08/10/analisis-diseño-smart-contracts-a-partir-procesos-modelados-con-bpmn
---

## 1. Objetivo

Identificar los puntos (actividades) en los procesos de negocio que fueron modelados que son susceptibles de ser integrados o que requieren guardar información transaccional en la Red Blockchain.

## 2. Abreviaturas

* MINAGRI: Ministerio de Agricultura y Riego
* SERFOR: Servicio Nacional Forestal y de Fauna Silvestre
* MC-SNIFFS: Módulo de Control del Sistema Nacional Información Forestal y de Fauna Silvestre
* BPM: Business Process Management en inglés o Gestión de Procesos de Negocio
* GTF: Guia de Transporte Forestal
* ARFFS: Autoridad Regional Forestal y de Fauna Silvestre
* ARF: Autoridad Regional Forestal
* PO: Plan Operativo
* PMFI: Plan de Manejo Forestal Intermedio
* DEMA: Lineamientos para la elaboración de la Declaración de Manejo
* CTP: Centros de Transformación Primaria
* RUC: Registro Único de Contribuyentes

## 3. Situación actual

El mundo se está digitalizando y con nuevas formas de ver los contratos, los denominados “Smart Contracts” o Contratos Inteligentes que se define como “Programa informático que se programa para que ejecute de forma automática acuerdos que hayan determinado dos o más partes”. En ese sentido, durante el diseño de los procesos de negocio de la explotación de la madera, hemos identificado normas, reglas con una serie de documentos que bien pueden ser considerados como información irrefutable que reforzaría la veracidad de un contrato, además, hemos identificado los actores del procesos, que serían las partes que participarán en la celebración del contrato y así sucesivamente.  
En resumen, después de haber completado el modelado de los procesos de negocio más representativos de la explotación de la madera, y una vez analizado en detalle cada uno de ellos habremos identificado aquellos puntos importantes, sus reglas o normas, los participantes y los documentos o datos intercambiados en ese momento, para luego crear una nueva estructura de datos llamado Smart Contract, que será la que guardará en la Red Blockchain.

## 4. Problema

Desconocemos si las autoridades utilizan para modelar los procesos de negocio BPMN 2.0, ya que ello permitiría una fácil interpretación de lo que pasa en el ciclo de vida de la madera y que nos ayude a identificar esos puntos dentro del proceso susceptibles de ser llevados a la Red Blockchain. 
Como el MC-SNIFFS está aún en proceso de construcción e implementación y SERFOR está tomando acciones iniciales para abordar los temas de trazabilidad de la madera, todo este trabajo presentado en este Proyecto es el resultado de haber revisado aplicaciones legadas, haber revisado documentación pública y de haber asistido a varias reuniones donde se han explicado escenarios similares; por lo cual, es un trabajo que está siendo mejorado y adaptado cada día y puede que lo que hoy estamos añadiendo a la estructura de los Smart Contracts, mañana puede ser que no se considere.
 
## 5. Acciones

Hemos modelado todos los procesos con BPMN 2.0 y hemos definido las interfases de interacción humana llamadas SCREENs, gracias a ProcessMaker el modelamiento y la generación de esas interfases no ha sido un trabajo difícil. Los SCREENs nos permite definir la manera más fácil la representación de los documentos, reglas, formularios y estructura de datos que son usados en los procesos de manera real, pero en este caso, estos formularios serán nuestra estructura de datos que son susceptibles de ser registrados en la Red Blockchain.  
Ante ello, las principales acciones adoptadas fueron:
* Análisis al detalle de la información en la web relacionada al Manual de Usuario Sistema de Emisión y Registro de Guías de Transporte.
* Análisis y diseño de los SCREENs con sus respectiva estructura de datos, incluyendo las variables que ProcessMaker requiere.

## 6. Desarrollo

El uso de Blockchain en la trazabilidad de la cadena de explotación, podría permitir un seguimiento exhaustivo e identificación del recurso madera utilizada. Mejor aún, si el sistema de trazabilidad es más completo, preciso y responsable ofrece visibilidad sustancial del producto y ayudaría a que toda la cadena de explotación fuera más congruente, confiable y no repudiable.  

ProcessMaker nos permite incorporar información sobre la estructura de datos a través de los SCREENs y cuáles son los participantes en cada una de las actividades representadas en cualquier proceso. Muchos procesos requieren recopilar el mismo tipo de información, como el nombre y apellido, dirección, correo electrónico, etc. Por lo tanto, los diseñadores de procesos o analistas de negocio pueden crear SCREENs que sólo muestren información relevante a cada acción o actividad, y que finalmente será esa información la que se reflejará en la Red Blockchain a través de los Smart Contracts.  
 
Asimismo, se puede usar SCREENs de diferentes tipos con visualización que muestre información, descargar archivos, mostrar indicadores clave de rendimiento (KPI) e información de uso común para las partes interesadas.  

Después de emplear ProcessMaker, revisar la información disponible del MC-SNIFF, realizar entrevistas a los especialistas forestales, etc. hemos podido desarrollar 10 SCREENs, estos son:

* SCREEN 1: AS1-Titulares de Título Habilitante
* SCREEN 2: AS2-Crear Nuevo Titular
* SCREEN 3: AS3-Datos Generales
* SCREEN 4: AS4-Plan Operativo
* SCREEN 5: AS5-Establecimientos Registrados
* SCREEN 6: AS6-Nuevo Establecimiento
* SCREEN 7: AS7-GTF-Titulos Habilitantes
* SCREEN 8: AS8-GTF-PO-Planes de Manejo
* SCREEN 9: AS9-GTF-Especies y Volúmenes Aprobados
* SCREEN 10: AS91-GTF-Registrar GTF al Estado Natural

Ahora, el siguiente paso es identificar cuál de estos SCREENs puede ser usado para validar la estrategia de Integración entre procesos modelados BPMN con la Red Blockchain a través de los Smart Contracts.  

En el siguiente gráfico se muestra los 10 SCREENs diseñados con la herramienta ProcessMaker:

{{< image-resize "/assets/post20220810_art02/art2-graf1-lista-processmaker-screens.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 1: Lista de SCREENs identificados en los procesos de explotación de recursos maderables modelados con BPMN 2.0.
</center></i>
{{</ rawhtml >}}

### 6.1. SCREEN 1: AS1-Titulares de Titulo Habilitante
 
 {{< image-resize "/assets/post20220810_art02/art2-graf2-screen1-as1-titulares-de- titulo-habilitante.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 2: Diseño del SCREEN 1: AS1-Titulares de Título Habilitante.
</center></i>
{{</ rawhtml >}}

> Es un buscador que ubica a titulares de titulo habilitante que se encuentran registrados con sus datos como ruc, domicilio fiscal, departamento, provincia, distrito, título obtenido, modalidad de otorgamiento, fecha de inicio y final, área otorgada, ubicación, representante legal y estado situacional.
Se han elaborado 17 variables y label relacionados a sus nombres.

### 6.2. SCREEN 2: AS2-Crear Nuevo Titular

{{< image-resize "/assets/post20220810_art02/art2-graf3-screen2-as2-crear-nuevo-titular.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 3: Diseño del SCREEN 2: AS2-Crear Nuevo Titular.
</center></i>
{{</ rawhtml >}}

> Crea nuevos titulares de título habilitante que no se encuentran registrados. Desarrolla registro de datos como razón social, email, teléfono, rubro, giro, domicilio fiscal, departamento, provincia, distrito. Datos del representante legal. Asimismo, se elaboraron 13 variables para el titular y 12 variables para el representante legal.

### 6.3. SCREEN 3: AS3-Datos Generales
 
{{< image-resize "/assets/post20220810_art02/art2-graf4-screen3-as3-datos-generales.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 4: Diseño del SCREEN 3: AS3-Datos Generales.
</center></i>
{{</ rawhtml >}}

> Este SCREEN edita los datos generales número de título, contrato, permiso o autorización, ruc, nombre o razón social, modalidad de otorgamiento, actividad, propietario de la tierra, fecha de firma, fecha de vigencia. Datos de la ubicación del título habilitante y representante legal. Se ha desarrollado 23 variables.

### 6.4. SCREEN 4: AS4-Plan Operativo

{{< image-resize "/assets/post20220810_art02/art2-graf5-screen4-as4-plan-operativo.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 5: Diseño del SCREEN 4: AS4-Plan Operativo.
</center></i>
{{</ rawhtml >}}

> Este SCREEN registra datos del plan operativo: número de contrato, número de plan operativo, resolución, tipo de recurso, fecha de expediente, fecha de zafras, parcela de corte, área a aprovechar.
Registra datos del regente autorizado para elaborar el plan operativo, número de licencia y estado situacional de la licencia.
Se ha desarrollado 18 variables.

### 6.5. SCREEN 5: AS5-Establecimientos Registrados

{{< image-resize "/assets/post20220810_art02/art2-graf6-screen5-as5-establecimientos-registrados.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 6: Diseño del SCREEN 5: AS5-Establecimientos Registrados.
</center></i>
{{</ rawhtml >}}

> Este SCREEN es un buscador de los establecimientos registrados con el número, tipo, ruc, nombre y número de establecimiento, dirección, departamento, número de resolución, fecha de vencimiento y estado.
Asimismo, se ha desarrollado 12 variables con sus respectivos nombres.

### 6.6. SCREEN 6: AS6-Nuevo Establecimiento

{{< image-resize "/assets/post20220810_art02/art2-graf7-screen6-as6-nuevo-establecimiento.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 7: Diseño del SCREEN 6: AS6-Nuevo Establecimiento.
</center></i>
{{</ rawhtml >}}

> Este SCREEN registra los nuevos establecimientos como ruc, número asignado, nombre del representante legal, dirección con validación por Sunat. Referencias de la ubicación, coordenadas geográficas, departamento, provincia, distrito. Datos de la autorización o permiso de funcionamiento. Se ha desarrollado 21 variables con sus respectivos nombres.

### 6.7. SCREEN 7: AS7-GTF-Titulos Habilitantes
 
{{< image-resize "/assets/post20220810_art02/art2-graf8-screen7-as7-gtf-titulos-habilitantes.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 8: Diseño del SCREEN 7: AS7-GTF-Titulos Habilitantes.
</center></i>
{{</ rawhtml >}}

> Es un buscador los títulos habilitantes mediante Nro de ruc, razón social del titular o número del título habilitante esto permite obtener el Nro título habilitante, ruc del titular, razón social y la vigencia de inicio y fin. Se han desarrollado 06 variables con sus respectivos nombres.

### 6.8. SCREEN 8: AS8-GTF-PO-Planes de Manejo

{{< image-resize "/assets/post20220810_art02/art2-graf9-screen8-as8-gtf-po-planes-manejo.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 9: Diseño del SCREEN 8: AS8-GTF-PO-Planes de Manejo.
</center></i>
{{</ rawhtml >}}

> Este SCREEN ubica los planes de manejo mediante la búsqueda de los títulos habilitantes que se encuentran registrados con ruc, razón social o número de TH.
Reporta los Nro de plan operativo, Nro de resolución, zafra, fecha de inicio, fecha final, parcela, área asignada, tipo de plan, plan ID, estado situacional. Se han desarrollado 16 variables con sus respectivos nombres.

### 6.9. SCREEN 9: AS9-GTF-Especies y Volúmenes Aprobados
 
{{< image-resize "/assets/post20220810_art02/art2-graf10-screen9-as9-gtf-especies-vol-aprob.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 10: Diseño del SCREEN 9: AS9-GTF-Especies y Volúmenes Aprobados.
</center></i>
{{</ rawhtml >}}

> Este SCREEN ubica las especies y volúmenes aprobados mediante la búsqueda de los títulos habilitantes que se encuentran registrados con datos como ruc o razón social o Nro de TH. Se generan los datos de los planes de manejo con las especies y volúmenes autorizados del plan aprobado con zafra, descripción, nombre científico, árboles, volumen autorizado, unidad métrica, volumen movilizado, saldo, fecha del último movimiento. Se ha desarrollado 16 variables con sus respectivos nombres.

### 6.10. SCREEN 10: AS91-GTF-Registrar GTF al Estado Natural
 
{{< image-resize "/assets/post20220810_art02/art2-graf11-screen10-as91-gtf-reg-estado-nat.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 11: Diseño del SCREEN 10: AS91-GTF-Registrar GTF al Estado Natural.
</center></i>
{{</ rawhtml >}}

> Este SCREEN es el más importante pues es la información que registra la guía de transporte forestal al estado natural con mayor detalle. Se desarrollan 16 variables con sus respectivos nombres. A continuación se explica la secuencia de información muy relevante para la elaboración del Smart Contract.

Por la relevancia e importancia del documento “Registrar la Guía de Transporte Forestal (GTF) al estado natural” y al revisar todas las actividades del proceso, creemos que es el SCREEN candidato más apropiado a ser considerarlo como la estructura de datos base para el diseño del Smart Contract clave para la integración con la Red Blockchain.  
El registro de Guías de Transporte Forestal sirve para el ingreso de guías manuales emitidas previamente. Para acceder se deberá seguir con los siguientes pasos:

* Seleccionar la resolución del plan y registrar GTF al E. Natural.
* Se mostrará que debe ingresar el número de GTF a registrar, para verificar que no se haya registrado previamente.
* Se verificará y validará si ya está registrada la GTF.
* Si la validación no está registrada, se procederá con el registro de la GTF.
* El sistema mostrará que se deberá seleccionar la especie a movilizar.
* Se visualizará las trozas que fueron agregadas, donde se deberá ingresar el código de la troza, el D1 (siempre será el diámetro mayor), D2 y el largo.
* Ingresar a datos de la Guía de Transporte Forestal, se deberá ingresar todos los datos:
  - Fecha de emisión y vencimiento: fechas que fueron detalladas en la GTF Manual.
  - Propietario del producto: este podrá ser el mismo Titular, se deberá dar Propietario es el titular, en caso este propietario no figure en la lista del sistema. Se podrá ingresar los datos del propietario, el cual deberá ser validado con SUNAT o RENIEC.
  - Tipo de comprobante: en esta lista se deberá seleccionar de manera obligatoria entre Boleta y Factura como medio que comprueba la transacción económica en la compra de la madera movilizada e ingresar el número de este documento. Solo en casos en que, el mismo titular movilice la madera podrá seleccionar No Aplica.
  - Destinatario: en esta lista se deberá seleccionar al CTP o Depósito al cual irá la madera, cabe señalar que estos deben estar registrados previamente en el sistema.
  - Transportista: seleccionar al conductor que transportará la madera, en caso este no figure en la lista se podrá agregar a la lista. En esta ventana se podrá ingresar los datos del conductor, el cual deberá ser validado con RENIEC.
  - Luego de haber ingresado todos los datos solicitados se graba el Registro.

El sistema pedirá confirmar que se mantengan los datos de la lista registrada previamente, esto es con la finalidad de poder usar posteriormente los datos de la lista de trozas previamente generada.

## 7. Conclusiones

De los 10 SCREENs que forman parte de los procesos elaborados el más apropiado por el grado de importancia y relevancia es el ”registro de la guía de transporte forestal al estado natural” pues presenta información sobre fechas de emisión y vencimiento, propietario del producto, tipo de comprobante, destinatario y transportista que están relacionadas a la madera movilizada incluso en trozas y resolución del plan operativo de procedencia pues a través de este último registro responde una de las preguntas de investigación que era identificar a la autoridad forestal que autorizo y firmo dicho expediente.
