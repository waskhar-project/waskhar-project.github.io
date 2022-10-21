---
title: "Evaluacion de herramientas BPM Open Source"
date: 2022-08-02T18:51:44+02:00
draft: false
authors: ["Roger Carhuatocto"]
#type: post
layout: single_article
categories: [BPM, DApp, Web3]
url: /2022/08/02/evaluacion-de-herramientas-bpm-open-source
---

## Qué es BPM, BPMS y BPMN

De acuerdo a [Wikipedia](https://es.wikipedia.org/wiki/Gesti%C3%B3n_de_procesos_de_negocio), _BPM_ (Business Process Management o Gestión de Procesos de Negocio) es una disciplina de gestión que tiene por objetivo mejorar el desempeño y la optimización de los procesos de una organización. Esto se alcanza siguiendo las etapas: (1) diseñar, (2) modelar, (3) organizar, (4) documentar y (5) optimizar de manera contínua.

_BPMS_ son las siglas de Business Process Management System, y es una herramienta que automatiza el BPM y asiste en todas sus etapas.

[_BPMN_](https://es.wikipedia.org/wiki/Business_Process_Model_and_Notation) son las siglas de Business Process Model and Notation, y es una notación gráfica estandarizada que permite el modelado de procesos de negocio, en un formato de flujo de trabajo (workflow). 

En resumen, _BPM_ es la metodología, _BPMS_ es la tecnología o software, mientras que _BPMN_ es el lenguaje gráfico con el que modelamos los procesos de negocio.

## Las ventajas del uso de BPM

Como hemos mencionado en el párrafo anterior, _BPM_ me permite modelar, organizar, documentar y optimizar los procesos de negocio, y cuando se trata de trazabilidad a lo largo de la _cadena de gestión de recursos maderables_, la mejor forma de entender el fondo del problema es analizando dicho proceso. 

- **Rápido análisis**. El modelamiento es la mejor forma de ver y entender los procedimientos, el intercambio de información, identificar las actividades críticas y cuáles son los puntos problemáticos que hacen que se cometan _ilegalidades_ a lo largo de la _cadena de gestión de recursos maderables_. En resumen, si quieres resolver un problema, primero analízalo usando metodología y herramientas relacionadas a BPM.
- **Rápida implementación y validación**. Las herramientas BPMS actuales son tan sofisticadas que permiten la generación rápida de aplicaciones a partir de proceso modelado con BPMN. No es necesario programar ni tener experiencia en tecnología informática para obtener una aplicación web. Con _BPMS_ puedo añadir cambios en el proceso modelado con _BPMN_ y obtener una aplicación actualizada, esto nos permite iterar tantas veces quiera hasta obtener el proceso final.
- **Integración**. Además de generar rápidamente la aplicación a partir del proceso BPMN, las herramientas BPMS proveen mecanismos para extender su funcionalidad y poder ser integrados con aplicaciones externas como ERP, ESB, CRM, etc. En nuestro particular, nuestro interés es poder integrarlo con Blockchain. 

Entonces, la pregunta final es ¿Qué BPMS debo usar?. En el siguiente apartado explicamos el criterio que hemos usado para la selección de la herramienta BPMS para Proyectos de Blockchain.

## Herramientas BPMS para Proyectos de Blockchain 

Hace [más de 10 años hice una revisión de herramientas BPMS muy similar](https://holisticsecurity.wordpress.com/2011/07/21/jbpm-bonita-intalio-processmaker-activiti-que-bpm-suite-uso/), el sector ha cambiado mucho y la tecnología ha evolucionado. Muchas de esas herramientas incluso han sido descontinuadas y otras han madurado mucho. Teniendo en cuenta todo esto, aquí explicamos el **criterio** que hemos usado para esta nueva selección:

1. **Open Source**.  
Que nos permita desgarla, probarla, experimentar y constribuir.
2. **BPMN 2.0**.  
Que permita que los procesos modelados puedan ser exportados y volver a importarlos en otro BPMS.
3. **Extensibilidad e Integración**.  
Que pueda ser fácil extender funcionalidades y conectar a otras aplicaciones externas. Esto en Blockchain es llamado [DApp (Distributed Application)](https://es.wikipedia.org/wiki/Aplicaci%C3%B3n_descentralizada).
4. **No Code**. Que formularios Web (front end), reglas de negocio y la complejidad de la integración puedan ser generados sin conocimiento de programación. 

Con este criterio y después de revisar varias soluciones comerciales y open source, las alternativas que tienen una versión open source o _community_ y que tienen las características que nuestro proyecto requiere son:

| Herramienta BPMS                                 | Observaciones |
|---                                               | ---           |
| 1. [ProcessMaker](https://www.processmaker.com/) |- Basada en tecnología PHP y es 100% web.                     |
| 2. [BonitaSoft](https://www.bonitasoft.com/)     |- Basada en Java, todo es web excepto el Editor de Procesos.  |
| 3. [Camunda](https://camunda.com/)               |- Basada en Java, 100% web, preparado para Kubernetes.        |

## Desplegando un BPMS en AWS

Hemos elegido [ProcessMaker](https://www.processmaker.com/), y desde que nuestro equipo de Proyecto es distribuído entre Perú (varias regiones, inclusive en Madre de Dios), España y Reino Unido, hemos instalado ProcessMaker en AWS. Las guías que hemos usado se encuentran aquí:

> Deployment and configuration of BPM ProcessMaker 4 on AWS.  
> https://github.com/chilcano/bpm-processmaker-aws

## Otras herramientas BPMS

Aunque este no es un proyecto 100% sobre procesos de negocio, creemos que es importante compartir nuestras investigaciones en este campo. Pues, a continuación tenéis una lista de herramientas BPMS muy interesantes que vale la pena considerarlos, estos son:

- https://www.imixs.org
- https://kogito.kie.org/ - Kogito (based on jBPM)
- https://www.activiti.org
- https://www.joget.org - Artículos de cómo Joget DX es integrado con Aplicaciones Blockchain:  
  * [What Everybody Ought to Know About Distributed Ledger Technology and Blockchain When Combined With No-Code - 2022/Oct/13](https://blog.joget.org/2022/10/distributed-ledger-technology-and-blockchain-with-no-code.html)    
  * [ Cardano and Joget: Building No-Code, Composable Blockchain Apps - 2021/Oct/05](https://blog.joget.org/2021/10/cardano-and-joget-building-no-code-composable-blockchain-apps.html)  
  * [ Want to Know Where Your Coffee Comes From? - 2022/Apr/01](https://blog.joget.org/2022/04/want-to-know-where-your-coffee-comes.html)  
