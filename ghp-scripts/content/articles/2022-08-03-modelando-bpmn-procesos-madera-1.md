---
title: "Modelado BPMN 2.0 de los Procesos de Explotación de Recursos Maderables en la Amazonía Peruana - Parte I"
date: 2022-08-03T10:50:40+02:00
draft: false
authors: ["Carlos Ticla"]
layout: single_article
categories: [BPMN, Process Modeling]
url: /2022/08/03/modelando-procesos-explotacion-recursos-maderables-amazonia-bpmn-1
---

## 1. Objetivo 

Realizaremos un análisis al detalle de los procesos de explotación de la madera elaborados y  diseñados con la herramienta BPM que nos permitirá identificar las actividades o procedimientos críticos y relacionarla con la tecnología Blockchain para garantizar la trazabilidad.

## 2. Abreviaturas 

- MINAGRI : Ministerio de Agricultura y Riego 
- SERFOR : Servicio Nacional Forestal y de Fauna Silvestre 
- MC-SNIFFS: Módulo de Control del Sistema Nacional Información Forestal y de Fauna Silvestre BPM : Business Process Management en inglés o Gestión de Procesos de Negocio GTF : Guia de Transporte Forestal 
- ARFFS : Autoridad Regional Forestal y de Fauna Silvestre 
- ARF : Autoridad Regional Forestal 
- PO : Plan Operativo 
- PMFI : Plan de Manejo Forestal Intermedio 
- DEMA : Lineamientos para la elaboración de la Declaración de Manejo CTP : Centros de Transformación Primaria 
- RUC : Registro Único de Contribuyentes 

## 3. Situación actual 

La trazabilidad de los recursos forestales maderables en nuestro país está regulada y aprobada  mediante Resolución de Dirección Ejecutiva N.230–2019–MINAGRI–SERFOR-DE y utiliza el  Módulo de Control del Sistema Nacional de Información Forestal y de Fauna Silvestre (MC SNIFFS), un subsistema para la gestión de información de títulos habilitantes que conlleve a la verificación del origen legal de la madera aprovechada, el módulo se encuentra a cargo del  SERFOR. Esta se compone por 3 submódulos: forestal maderable, forestal no maderable y de  fauna silvestre. El MC-SNIFFS se sustenta normativamente en la Ley Forestal y de Fauna  Silvestre, sus reglamentos, el Decreto Legislativo 1220 y 1319, la Resolución de Dirección  Ejecutiva 104-2017 y 044-2020 del SERFOR. Asimismo, utiliza aplicativos que son herramienta  de ayuda al registro ordenado de las operaciones de aprovechamiento, ingreso, transformación  y salida de la madera y sus productos de los aserraderos o plantas de transformación, así como  también del control de volúmenes y saldos. 
Existe avances en el sector público y que está normado para lo cual es importante contemplar  esta experiencia y regulación vigente que con el soporte de la tecnología debe ser mejorado y  optimizado para evitar la tala ilegal y corrupción. 
Asimismo, existen otras iniciativas privadas relacionadas al tema lo cual nos permitió tener  presente los inconvenientes que tuvieron y que afecta al desarrollo de estos tipos de proyectos  tecnológicos que tienen mucho impacto. 

## 4. Problema 

Los principales problemas detectados fueron: 
* El MC-SNIFFS está aún en proceso de construcción e implementación y están tomando  acciones para abordar los temas de trazabilidad de la madera. 
* Obtener el acceso a los aplicativos que están vigentes se rigen con una serie de requisitos que toma mucho tiempo y era complicado de cumplir. 
* Durante el diagnóstico de los procesos de la trazabilidad se observó que no se utiliza  una herramienta de BPM muy necesario para complementar con otras tecnologías.

## 5. Acciones 

Las principales acciones adoptadas para mitigar los problemas fueron: 
* Se envió una solicitud a mesa de partes de SERFOR para una reunión con un  Especialista Forestal de la Dirección de Control de la Gestión del Patrimonio Forestal y  de Fauna Silvestre la cual nos sugirió usar la información en la web relacionada al  MANUAL DE USUARIO Sistema de Emisión y Registro de Guías de Transporte. 
* Aprendizaje de la herramienta BPM ProcessMaker y diagnóstico de los procesos. La  tecnología Blockchain se complementa bien con el BPM (gestión de procesos  empresariales) pues ha demostrado eficacia y fiabilidad al crear aplicaciones. Asimismo,  BPM y su desarrollo de aplicaciones basadas en Blockchain puede resultar  enormemente eficaz pues si se trata de evitar la corrupción e ilegalidad. 
* Análisis y diseño de los procesos con sus respectivos screen simulando el  funcionamiento del manual de usuario utilizado como caso. 

## 6. Identificación de los Procesos

Constituye el primer paso de la puesta en ejecución de las acciones. 
Los instrumentos aprobados por el SERFOR que brindan la trazabilidad de los recursos  forestales maderables a lo largo de la cadena productiva son: 

* a. Plan de manejo forestal 
* b. Libro de operaciones de los títulos habilitantes para aprovechamiento forestal maderable. 
* c. Libro de operaciones de centros de transformación primaria de productos y subproductos  forestales maderables 
* d. Guia de transporte forestal 
* e. Aplicativo informático para el registro de información y reportes del Libro de operaciones  de los títulos habilitantes para aprovechamiento forestal maderable. 
* f. Aplicativo informático para el registro de información y reportes del Libro de operaciones  de centros de transformación primaria de productos y subproductos forestales  maderables. 
* g. Aplicativos informáticos para la emisión y registro de GTF de títulos habilitantes y centros  de transformación primaria. 

Utilizando el software ProcessMaker, información disponible del MC-SNIFF, entrevistas a los especialistas forestales, etc se desarrollaron 6 procesos para conocer el funcionamiento de las  actividades de la trazabilidad de la madera en un entorno de modelo de negocio BPM la cual se ve reflejada en el siguiente gráfico: 

{{< image-resize "/assets/post20220803-1y2/art1-01-lista-procesos-relacionado-trazabilidad.png" 700x >}}
{{< rawhtml >}}
<i><center>
Gráfico 1: Lista de procesos relacionados a la trazabilidad de la recursos forestales maderables.
</center></i>
{{</ rawhtml >}}

* a. Proceso 1: A1-Cadena Productiva-Madera-ctc 
* b. Proceso 2: A2-Documentos de Gestión-Autoridad-ctc 
* c. Proceso 3: A3-Título Habilitante-ctc 
* d. Proceso 4: A4-Aserraderos y Depósitos-ctc 
* e. Proceso 5: G1-Registro Guía de Transporte Forestal-Estado Natural 
* f. Proceso 6: G2-Registro Guía de Transporte Forestal-Producto Transformado

> El modelado de cada uno de los procesos y su análisis se verá en la segunda parte del artículo.  
[Modelado BPMN 2.0 de los Procesos de Explotación de Recursos Maderables en la Amazonía Peruana - Parte II](/2022/08/03/modelando-procesos-explotacion-recursos-maderables-amazonia-bpmn-1)
