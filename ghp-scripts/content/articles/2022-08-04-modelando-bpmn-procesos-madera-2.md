---
title: "Modelado BPMN 2.0 de los Procesos de Explotación de Recursos Maderables en la Amazonía Peruana - Parte II"
date: 2022-08-04T10:50:40+02:00
draft: false
authors: ["Carlos Ticla"]
layout: single_article
categories: [BPMN, Process Modeling]
url: /2022/08/04/modelando-procesos-explotacion-recursos-maderables-amazonia-bpmn-2
---

> Para conocer el objeto y el contexto sobre la explotación de los recursos maderables, te recomendamos revisar la primera parte del artículo.  
[Modelado BPMN 2.0 de los Procesos de Explotación de Recursos Maderables en la Amazonía Peruana - Parte I](/2022/08/03/modelando-procesos-explotacion-recursos-maderables-amazonia-bpmn-1)


## 7. Modelado y análisis de los Procesos

Tener en cuenta que para el modelado se uso ProcessMaker como solución BPMS y se siguió el lenguaje BPMN 2.0. 
A continuación explicamos el desarrollo y análisis de cada uno de los procesos antes identificado.

{{< image-resize "/assets/post20220803-1y2/art1-01-lista-procesos-relacionado-trazabilidad.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 1: Lista de procesos relacionados a la trazabilidad de la recursos forestales maderables.
</center></i>
{{</ rawhtml >}}

### 7.1. Proceso 1: A1-Cadena Productiva-Madera-ctc 

Es el macroproceso de toda la cadena productiva de la madera que nos brinda un panorama  global desde el bosque hasta su comercialización descrita de la siguiente manera: 
* a. Planificación: es la aprobación del plan de manejo, contiene información del censo forestal  y detalla la ubicación del árbol, asignación del código e identificación de la especie. 
* b. Aprovechamiento forestal: representa las actividades de tala, trozado y despacho, es  determinante la codificación entre el árbol y todas las trozas que se generen de la misma. 
* c. Transporte primario: es la movilización con GTF de los productos forestales maderables  desde la extracción hacia la industria, depósitos o centros de comercialización. 
* d. Transformación primaria: es el procesamiento de los productos al estado natural en los  centros de transformación o también en las áreas de aprovechamiento utilizando equipos  móviles. 
* e. Transporte secundario: es la movilización de los productos forestales maderables entre  los centros de transformación primaria y secundaria, depósitos y centros de  comercialización. 
* f. Comercialización: se realiza a lo largo de la cadena productiva para abastecer el  mercado interno o externo 

{{< image-resize "/assets/post20220803-1y2/art1-02-proceso-a1-cadena-productiva-madera-ctc.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 2: Diseño de la cadena productiva de la madera.
</center></i>
{{</ rawhtml >}}

Para iniciar el aprovechamiento del recurso forestal se debe tener aprobado el plan de manejo  forestal y se registra en el libro de operaciones de los títulos habilitantes. En los procesos de  transformación primaria se relacionan los lotes de trozas con lotes de madera aserrada. En el  proceso de transformación secundaria, los productos que son despachados se movilizan con la  guía de remisión del remitente. 
En todo el proceso de la cadena productiva el instrumento Guía de Transporte Forestal adquiere  mayor relevancia pues relaciona los productos y subproductos con los títulos habilitantes. 

La primera pregunta de la investigación que surgió fue: 
__¿Es posible que la información contenida en la GTF sea relacionada a la Blockchain?__ 
Por otro lado un actor clave en la cadena es la _Autoridad Regional y de Fauna Silvestre (ARFFS)_ pues el mecanismo de trazabilidad del aprovechamiento forestal permite el registro de la  información de los árboles a aprovechar que han sido autorizados por la ARFFS que están  relacionados a los árboles censados e inventariados con los productos en su estado natural.  Asimismo, se puede conocer la procedencia del producto.

La segunda pregunta de la investigación es: 
__¿Contiene la GTF los datos de la Autoridad Regional y de Fauna Silvestre quien autoriza el aprovechamiento forestal?__
Dada la formulación de preguntas y la entrevista con especialistas forestales de SERFOR la  herramienta más apropiada a estudiar era el: 
- Aplicativos informáticos para la emisión y registro de GTF de títulos habilitantes y centros de transformación primaria.  

En ese sentido se analizó el siguiente procedimiento de dicha herramienta:  
- Emisión y Registro de Guías de Transporte Forestal del Módulo de Control del Sistema  Nacional de Información Forestal y de Fauna Silvestre. 

Este procedimiento contribuye a comprender el registro de las operaciones realizadas por los  titulares de títulos habilitantes, centros de transformación y depósitos. Entre las principales  funciones de este sistema, está el registro de documentos de gestión, como, por ejemplo:  
* Contratos 
* Permisos  
* Autorizaciones  
* Resoluciones de planes operativos  
* Autorizaciones y/o resoluciones de centro de transformación o depósitos.   

De igual forma, el sistema permite registrar las operaciones realizadas por los titulares de títulos  habilitantes, centros de transformación o depósitos mediante el registro de guías de transporte forestal:  
* Registro de Guías de Transporte Forestal al estado natural.
* Registro de Guías de Transporte Forestal de productos transformados El siguiente paso fue diseñar y describir los procesos más importantes. 

### 7.2. Proceso 2: A2-Documentos de Gestión-Autoridad-ctc 

Este proceso realiza el registro de información generada por la Autoridad Regional Forestal (ARF) como contratos, permisos, autorizaciones, resoluciones de planes operativos, PMFI,  DEMA y autorizaciones de centros de transformación primaria. Estos registros son la fuente de  información con la que los usuarios finales interactúan, siendo importante el correcto registro de la información. En el siguiente gráfico se muestra la interacción entre los actores. 

{{< image-resize "/assets/post20220803-1y2/art1-03-proceso-a2-documentos-gestion-autoridad-ctc.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 3: Documentos de Gestión-Autoridad.
</center></i>
{{</ rawhtml >}}

### 7.3. Proceso 3: A3-Título Habilitante-ctc 

En este proceso se realiza el registro de los títulos Habilitantes de la siguiente manera: 

#### a) Titular

Es la creación y registro del titular. 
* Buscar titular: permite la búsqueda por número de RUC, Título Habilitante o Razón Social. Si  no está registrado se procede a crearlo, caso contrario se editan los datos del titular. 
* Crear nuevo titular: si no se encuentra registrado el titular, deberá ingresar los datos: Tipo de  persona jurídica, RUC, representante legal, tipo y número de documento, dirección. 
* Editar datos del titular: permite modificar los datos ingresados previamente. 
* Ver datos del titular: permite visualizar los datos del titular. 

#### b) Títulos Habilitantes  

Una vez creado el titular se procederá a crear un nuevo título habilitante. 
* Crear nuevo título: se deberá ingresar los datos como número de título (contrato, permiso o  autorización) dato único generado al momento de aprobar el contrato, modalidad de  otorgamiento, actividad, propiedad de la tierra, fecha de firma, PGM, vigencia, departamento,  provincia, distrito y/o cuenca, área. 
* Editar título: permite modificar los datos ingresados previamente.  
* Ver título: permite visualizar los datos del titular. 
* Cargar el Título Habilitante (contrato, permiso o autorización) escaneado: primero visualiza los  documentos previamente subidos, carga nuevos documentos, ver, editar o eliminar, crear nuevo  documento, seleccionar y nombrar el contrato digitalizado. 

#### c) Documento de Gestión 

Representa los documentos que sustentan las operaciones 
* Registrar el PO, PMFI o DEMA que considera el contrato que desea agregar, ingresa los datos y número de PO. En caso de PMFI o DEMA con un plan, se ingresa el número 1. Se registra número y fecha de resolución, tipo de plan operativo, tipo de curso si es Maderable o No  Maderable, zafra, fecha inicio – fin, parcela, área y regente. 
* Editar documento de gestión, donde se podrá modificar los datos ingresados previamente. Se  selecciona el Documento de Gestión que se desea editar. Cabe señalar que una vez activado no  podrá ser editado. 
* Ver documento de gestion.

Una vez registrada la información, ésta debe ser revisada y validada por el usuario antes de la  activación. 
* Activar luego de ingresar todos los datos necesarios en el Plan Operativo, PMFI o DEMA y figure disponible en la base de datos, se deberá seleccionar el documento. 

Con la activación del documento se podrá usar para el registro de guías de transporte forestal y no se podrá agregar, editar o eliminar especies y/o volúmenes. 

Tener en cuenta que esta acción sólo podrá ser realizada en caso se haya terminado con el  registro de especies y volúmenes. 
* Activación parcial es una acción opcional, solo será utilizado en los casos que alguna especie  no se encuentre en la lista del sistema, el cual podrá ser agregado posteriormente. En el sistema  se encuentra cargada la lista de especies oficiales aprobadas por el SERFOR, solo se agregaran  las especies que sean acreditadas su existencia con una constancia de identificación botánica. 

Al haber activado parcialmente, el sistema permitirá agregar la especie faltante, siempre que este  haya sido acreditado su existencia. Tener en cuenta que esta acción sólo podrá ser realizada en  caso se haya ingresado por lo menos parte de las especies y volúmenes. 
* Activar documentos se deberá cargar la resolución escaneado que aprueba el Documento de  Gestión (Plan operativo, PMFI o DEMA).
* Agregar especies luego de haber registrado un documento de gestión (PO, PMFI o DEMA) se  deberá ingresar todas las especies y volúmenes aprobados en su resolución. Se deberá  seleccionar el documento registrado. 
* Editar especies en caso se desee modificar alguna especie o volúmenes, esta se podrá realizar  seleccionando el documento de gestión. El sistema podrá editar los datos ingresados  previamente. 
* Ver especies con la finalidad de validar las especies ingresadas.

En el siguiente gráfico (Gráfico 4) se observa el diseño del proceso. 

{{< image-resize "/assets/post20220803-1y2/art1-04-proceso-a3-titulo-habilitante-ctc.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 4: Titulo Habilitante.
</center></i>
{{</ rawhtml >}}

### 7.4. Proceso 4: A4-Aserraderos y Depósitos-ctc 

En este proceso se realiza el mantenimiento de Centros de Transformación Primaria y Depósitos con los siguientes subprocesos: 
* Buscar CTP o Depósito registrado previamente, se deberá ingresar el nombre o número de  RUC para identificarlo. Si no se encuentra se procede a registrarlo. 
* Registrar nuevos establecimiento para lo cual se debe ingresar todos los datos solicitados por  el aplicativo y el sistema permitirá realizar la edición de los datos del CTP o Depósito, para  realizar esta acción se selecciona y actualiza al titular. 
* Desactivar el establecimiento en caso el CTP o Depósito ya no cuente con una autorización  vigente o este ya no exista como empresa, la autoridad deberá realizar la búsqueda del titular  y desactivar. Al realizar esta acción, el titular ya no podrá ser utilizado como destino en las GTF. 
* Activar el establecimiento si el CTP o Depósito se encuentra en estado inactivo, este podrá ser  activado nuevamente por la autoridad. Para ello se deberá seleccionar al titular. • Ver detalle registrado si se desea ver los datos, se deberá realizar la selección del titular. • Cargar el Documento de Gestión (Plan operativo) escaneado, para lo cual se deberá  seleccionar y cargar la Autorización y Resolución digitalizado. 

En el siguiente gráfico (Gráfico 5) se observa el diseño del proceso. 

{{< image-resize "/assets/post20220803-1y2/art1-05-proceso-a4-aserraderos-depositos-ctc.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 5: Aserraderos y Depósitos
</center></i>
{{</ rawhtml >}}

### 7.5. Proceso 5: G1-Registro Guía de Transporte Forestal-Estado Natural 

Este proceso describe el registro y emisión de Guías de Transporte Forestal desde el bosque,  es decir todas las guías generadas para el titular de Título Habilitante.  
Aquí identificamos los componentes de la GTF que podría responder a la pregunta de investigación  y es materia de análisis para verificar la posibilidad de relacionarla a la tecnología Blockchain.  
El procedimiento se detalla a continuación: 

Acceder primero al Registro de Guía de Transporte Forestal al EstadoNatural.  
#### a) Títulos Habilitantes: 
- Buscar titular ingresando RUC, Razón Social o Número del TH y registrar los datos requeridos  del titular y su Título Habilitante 

#### b) PO – Planes de Manejo  
- Seleccionar un Título Habilitante, el sistema mostrará todas las resoluciones de PO, PMFI o  DEMA con sus respectivos datos. 

#### c) Especies y volúmenes autorizados del plan aprobado  
- Seleccionar una resolución de PO, PMFI o DEMA, el sistema mostrará las especies y  volúmenes aprobados. 
- Registrar GTF al estado natural, el registro de Guías de Transporte Forestal servirá para el  ingreso de guías manuales emitidas previamente. Para acceder se deberá seguir con: 
  * Seleccionar la resolución del plan y registrar GTF al E. Natural, se deberá ingresar el número  de GTF que se desea registrar, esto es para verificar que no se haya registrado previamente. 
  * Verificar, el sistema validará si está registrada la GTF. Caso contrario se procederá su registro. 
  * Seleccionar la especie a movilizar agregando items. 
  * Ingresar el código de la troza, el D1 (siempre será el diámetro mayor), D2 y el largo. 
  * Ingresar datos de la Guía de Transporte Forestal, con todos los datos solicitados por el sistema como fechas, propietario del producto, tipo de comprobante, destinatario y transportista. Esta  información será materia de análisis para los SCREEN que utiliza el Processmaker por su alto  grado de importancia para relacionarla con la nueva tecnología planteada. 

#### Opcional: 
Sobre la Madera Aserrada en Bosque: Para guías que cuenten con madera aserrada en bosque. 
- Registrar en el sistema la cantidad de trozas y volumen total usadas para la generación de  madera aserrada en bosque. 
- Ingresar el N° de lista de productos, cantidad de piezas, el tipo de producto. 
- Ingresar el código del paquete y el volumen total de la madera aserrada. 
- Calcular rendimiento utilizando el sistema. 
- Emitir GTF al estado natural: la emisión de Guías de Transporte Forestal servirá para el ingreso  de guías que no hayan sido emitidas previamente tanto manual o en sistema. Con esta acción  el sistema asignará un número único a la guía emitida desde el sistema. 
- Ver historial GTF sirve para generar un reporte detallado de las Guías de Transporte Forestal  generadas en el sistema desde el plan operativo seleccionado, para lo cual se deberá  seleccionar la resolución de plan operativo. 
- Elaborar Declaración Jurada (DJ) de Volúmenes Movilizados para cuando se desee regularizar  los saldos a los títulos habilitantes. Existirán casos en que los titulares ya hayan iniciado  operaciones antes del uso del sistema y se deberá seleccionar la resolución de plan operativo. 
- Crear Plantilla de Excel que será usada cuando el usuario desee trabajar desde un archivo  excel la lista de trozas, esto facilitará la creación de la mencionada lista de trozas.

{{< image-resize "/assets/post20220803-1y2/art1-06-proceso-g1-registro-guia-transporte-forestal-estado-natural.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 6: Registro Guía de Transporte Forestal-Estado Natural.
</center></i>
{{</ rawhtml >}}

### 7.6. Proceso 6: G2-Registro Guía de Transporte Forestal-Producto Transformado 

En este proceso se realizará el registro y emisión de las Guías de Transporte Forestal desde un Centro de Transformación Primaria. Es decir, será realizada en los Centros de Transformación  Primaria que no sean usuarios del sistema de Libro de Operaciones de CTP.  

Primero se deberá realizar lo siguiente: 
* Acceder al Registro de Guía de Transporte de Productos Transformados. 

#### a) Titulares de centros de transformación primaria y depósitos 
* Ingresar RUC o Razón Social para realizar la búsqueda, el sistema mostrará los datos del  titular, guías de transporte enviadas al CTP, especies y sus volúmenes disponibles. 

#### b) Guías de transporte y/o declaraciones juradas de inventario registradas a este destino
* Seleccionar la GTF con el número de registro para visualizar al detalle las guías enviadas al CTP, la cual ayudará a una validación previa a la recepción de la GTF. 
* Recepcionar GTF en destino que será utilizada luego de validar la GTF enviada al CTP, con  esta acción se da por recepcionada la GTF. 
* La GTF habrá cambiado de estado a GTF Recepcionada, eso quiere decir que las especies  y volumen pasaron al CTP. 

#### c) Volúmenes disponibles por especie donde se visualiza las especies y volúmenes  recepcionados hasta el momento, así como, el origen, volumen despachado y saldo. 

#### d) Registrar GTF de CTP El registro de Guías de Transporte Forestal servirá para el ingreso de  guías manuales emitidas previamente. Para acceder se deberá seguir los siguientes pasos: 
* Seleccionar el origen de la madera y especie que se desea aprovechar. • Seleccionar e ingresar el N° Lista Productos, cantidad, tipo de producto y agregar items. • Ingresar el código del paquete y volumen, en el caso de la madera aserrada no será  obligatorio detallar la medida de cada pieza, sólo se considerará el volumen total por cada  especie y tipo de producto. 
* Ingresar datos de la Guía de Transporte Forestal, en la que se deberá ingresar todos los datos  solicitados por el sistema como: Fecha de emisión y vencimiento, Tipo de comprobante y  Transportista. 

#### e) Registrar Declaración Jurada de centros de transformación primaria. 
* En esta caso existen dos opciones: Usar aplicativo ER-GTF-CTP o Solicitar a la ARF 

#### f) Emitir GTF a solicitud de propietario del producto: La emisión de Guías de Transporte Forestal  a solicitud de propietario del producto, solo será usado en casos que, el propietario desee  movilizar la madera y no cuente con una GTF, pero si con los documentos la acreditación del  origen y de compra. Para este caso debe seguir con: 
* Registrar GTF de CTP donde el sistema asignará un número único a la guía emitida. • Consultar Guía de Transporte Forestal registradas, se podrán visualizar todas las Guías de  Transporte Forestal emitidas o registradas desde el MC SNIFFS, las cuales podrán ser  impresas, reemitidas, etc. 
* Ver detalle GTF mediante búsqueda se podrá realizar de guías registradas en los sistemas  del MC SNIFFS, ingresando el número de RUC del emisor, N° de GTF, Destinatario o N° de  Registro. Para realizar la búsqueda de se deberá ingresar uno de los datos detallados. El  número de registro, es el número único que le asigna el sistema a cada GTF registrada o  emitida por el MC SNIFFS. Asimismo las siguientes acciones: 
* Lista de guías de transporte forestal se podrá observar todas las GTF emitidas o registradas  en los sistemas de MC SNIFFS, podrán filtrar por fechas e ingresar el rango de fechas. • Detalle del contenido de la guía de transporte si se desea ver el detalle de la GTF, se deberá  seleccionar la GTF en Ver Detalle del Registro N° “número de registro”. El sistema mostrará  los datos de la madera movilizada en la GTF.
Re emisión de GTF: Las GTF solo podrán ser re emitidos por los siguientes motivos: Periodo de  vigencia vencido, inmovilización parcial de la carga, cambio de destinatario, cambio de vehículo, cambio de transportista y distribución de la carga en varios vehículos. 
* Seleccionar el motivo y check en la troza o producto que será movilizado en la nueva GTF. Para la Distribución de la carga en varios vehículos, se deberá dar check solo en las trozas  que serán movilizadas en esta GTF. Asimismo, elegir el periodo de vigencia vencido. Para el  resto de casos, el sistema habilitará el cambio de datos.  
  - La nueva GTF se genera y figura con un nuevo número de registro y estado GTF reemitida.
  - La GTF de origen quedará como una GTF Fraccionada, el cual podrá ser utilizada para  generar una nueva GTF, solo en los casos que queden trozos o productos por movilizar. 
* Imprimir constancia de registro de GTF donde el sistema mostrará la GTF y lista de trozas  generada. Guardar como un archivo PDF. 
* Ver detalle de registro de GTF o emitida se deberá seleccionar la GTF donde el sistema  mostrará una ventana, en la que se podrá ver al detalle los datos de la GTF, así como, todas  las acciones realizadas por los usuarios del sistema con la GTF. 
* Generar orden de pago las cuales serán generadas en base al volumen movilizado por  especie en la GTF, para lo que se deberá seleccionar la GTF y generar Orden de Pago. - En caso no esté ingresado el precio, el usuario deberá hacerlo de forma manual y el  sistema hará el cálculo del monto a pagar por la GTF. 
* Ver inspecciones en el mapa Las guías de transporte forestal inspeccionadas en los puestos  de control figuran con el estado GTF validado, estas inspecciones podrán ser visualizadas  desde el sistema seleccionando la GTF y ver Inspecciones en el Mapa.  

Otros subprocesos que se estudiarán posteriormente: 
* Registro de Declaración Jurada de inventario de planta de transformación: en esta parte se  podrá visualizar todas las Declaraciones Juradas de Inventario registradas de los Centros de  Transformación Primaria, que servirán para la regularización de saldo actual en la planta.  
* Registro de Declaración Jurada de volúmenes movilizados: en esta parte se podrá visualizar  todas las Declaraciones Juradas de Volúmenes Movilizados, que servirán para la  regularización de saldo actual del Título Habilitante. Para acceder, ingresar a Registro de  Guías de Transporte Forestal, Registro de Declaración Jurada de Volúmenes Movilizados. 

{{< image-resize "/assets/post20220803-1y2/art1-07-proceso-g2-registro-guia-transporte-forestal-producto-transformado.png" 400x >}}
{{< rawhtml >}}
<i><center>
Gráfico 7: Registro Guía de Transporte Forestal-Producto Terminado
</center></i>
{{</ rawhtml >}}

## 8. Conclusiones 

1. Se logró diseñar 6 procesos utilizando la herramienta de gestión de procesos BPM  obteniéndose 2 macroprocesos que nos brinda una visión actual y normado de la  trazabilidad de la madera en nuestra Amazonía y 4 procesos detallados sobre la  interacción entre los actores y los registros respectivos. 
2. Se identifican 2 actores claves: Autoridad Regional Forestal y el usuario Titular de la  concesión. 
3. Se identifica que la Guía de Transporte Forestal adquiere mayor relevancia pues  relaciona los productos y subproductos con los títulos habilitantes para lo cual surgen  dos preguntas de investigación si es posible su integración a la tecnología planteada y si la autoridad también está registrada. 
4. La presente información facilita el estudio de los Smart Contract en los procesos de trazabilidad de la madera.

## 9. Bibliografia 

- a. Serfor 2019, “Resolución de Dirección Ejecutiva N.230–2019–MINAGRI–SERFOR-DE” 
- b. Serfor 2020, “Ley Forestal y de Fauna Silvestre, sus reglamentos, el Decreto Legislativo 1220  y 1319, la Resolución de Dirección Ejecutiva 104-2017 y 044-2020 del SERFOR” 
- c. Serfor 2019, “Manual de Usuario Sistema de Emisión y Registro de Guías de Transporte” d. ProcessMaker Inc. 2000-2022, “ProcessMaker Documentation” 
- e. José Luis Mela N. y Edwin J. Cedeño Herrera Vol.3, No.2: 110-126 Diciembre 2019 - Mayo  2020 Panamá ISSN 2520-9892- “tecnologías Blockchain y sus aplicaciones” 
- f. Ahmed Banafa -Julio 2020, “tecnología Blockchain y gestión de la cadena de Suministro”
