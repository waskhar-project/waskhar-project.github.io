---
title: "El Proyecto Waskhar"
date: 2022-08-01T18:49:40+02:00
draft: false
#type: post
layout: single_article
#tags: [Amazon Forest]
categories: [Blockchain, Traceability, Supply Chain]
url: /2022/08/01/el-proyecto-waskhar
aliases: 
   - /2022/08/01/the-waskhar-project
---

> "Digitalización y mejora de la Trazabilidad a lo largo de la Cadena de Suministro de Madera de la Amazonía Peruana usando Blockchain."

![](/media/assets/post20221001/waskhar-logo-3-knots-color.png)
_Palabra Quechua que significa 'Cadena o cuerda o soga dura, difícil de romper.'_

## 1. Resumen ejecutivo

La cadena de suministro de madera es vulnerable a la ilegalidad y corrupción. Los agentes activos son mayormente organizaciones nacionales e internacionales que aprovechan la amplia informalidad, limitada capacidad de control y sanción, deficiente articulación e incompleta información, poca tecnificación de los procesos, entre muchos otros factores.
Frente a ello, las autoridades emplean diversas iniciativas TICs, aplicaciones y base de datos obsoletas. Asimismo, hay ausencia de tecnologías de última generación disuasivas. Este proyecto usará la tecnología blockchain para mejorar la capacidad del Estado a obtener información confiable en tiempo real de los recursos maderables: concesionados, en almacenes, en el campo, en tránsito y en el destino final. Esto facilitaría que los agentes en los puntos de control de la cadena de suministro generen registros que, al ser almacenados en una cadena de blockchain, serían únicos e inmutables. En este caso la aplicación estará en un proceso específico de la cadena de suministro de la madera
Con esta propuesta, esperamos desincentivar la tala ilegal de madera, pues se podría rastrear el origen de cualquier embarque en cualquier punto de control a cargo del Estado. Por otro lado, se desincentivaría la corrupción, pues al almacenar los datos en blockchain, no habría capacidad de los actores involucrados para alterar la información a reportar en cualquier punto de la cadena.


## 2. Contexto del Proyecto

__I. Obsolescencia__

Uno de los problemas es la individualidad y heterogeneidad de las iniciativas TIC que son emprendidas y usadas de manera aislada.

__II. MC-SNIFFS (Módulo de Control del Sistema Nacional de Información Forestal y de Fauna Silvestre)__

El SNIFFS, una iniciativa liderada por SERFOR iniciada hace 2 años, se alza como la solución de control y trazabilidad a lo largo del ciclo de vida de los recursos naturales forestales y de fauna silvestre. El MC-SNIFFS se rige por la Ley Forestal y de Fauna Silvestre, sus reglamentos, el Decreto Legislativo 1220 y 1319, la Resolución de Dirección Ejecutiva 104-2017 y 044-2020 del SERFOR.

En el rubro de recursos naturales maderables, el MC-SNIFFS provee 3 tipos de aplicaciones que [cubren todos los aspectos de control y trazabilidad](https://sniffs.serfor.gob.pe/control/):
1. Emisión y registro de guías de transporte forestal - perfil de autoridad regional forestal.
  * [ER-GFT](https://drive.google.com/file/d/1GnT3ftRAcHQpTcbm8ITYSrqeYtTOUe-S/view?ts=62150ea1) v2.0.125, actualizado el 2022/02/22 (Archivo binario ejecutable para Windows)
2. Libro de operaciones - perfil de titular de título habilitante.
  * [LIBRO-TH](https://drive.google.com/file/d/1TzrJ3It_WM3WqP9tZhlt069b8w4nOgCx/view?ts=61eedff8) v1.0.29, actualizado el 2022/01/24 (Archivo binario ejecutable para Windows)
3. Libro de operaciones de centros de transformación primaria.
  * Web: [http://web.serfor.gob.pe/ctp](http://web.serfor.gob.pe/ctp)

Cabe mencionar que blockchain no es mencionado en ninguna documentación técnica, manual de aplicación ni presentaciones realizadas hasta la fecha.

__III. Trazabilidad sin blockchain__

En simples palabras, blockchain es un libro digital contable y distribuído, usado para garantizar la autenticidad, integridad y no repudio de las transacciones. Es usado exitosamente en los llamados Neo-Banks, que permiten construir sistemas financieros en paralelo al sistema financiero tradicional. Tecnológicamente, blockchain puede ser utilizado en cualquier sector, no sólo en el financiero.

Aunque las aplicaciones o sistemas informáticos registran toda su actividad en archivos de eventos (logs) y en base de datos, esta información puede ser manipulada o no estar disponible, lo que cuando sucede la convierte en una fuente de datos de poca confianza.

__IV. Blockchain como una "caja negra"__

Por su naturaleza, introducir blockchain en el ecosistema gestionado por MC-SNIFFS podría traer incertidumbre, desorden y resistencia. En estas circunstancias, la estrategía de adopción de blockchain debería propender hacia la transparencia en la implementación. En otras palabras, debemos ver el uso de blockchain como una "caja negra" ("adaptador", "plugin" o "conector") que nos permita usarla e integrarla de manera amigable en cualquier punto que nuestro proceso lo requiera.

__V. Dónde y cómo empezar con blockchain: Partida del nacimiento del árbol__

Blockchain es una tecnología que suma valor a aplicaciones o sistemas informáticos existentes, no viene a reemplazar ninguna base de datos o aplicativo. Sin embargo, ¿cómo empezamos?. La respuesta viene de las Buenas Prácticas de Arquitectura Empresarial ([Enterprise Integration Patterns, EIP](https://www.enterpriseintegrationpatterns.com/toc.html)), según las cuales empezar con blockchain significa:
* Elaborar un adaptador y la lógica de blockchain que implemente tantos patrones de integración como se haya identificado en cada interacción de interés.
* Alojar y ejecutar el adaptador blockchain en un servidor intermedio (middleware) entre las aplicaciones de negocio (ERP, CRM, etc.) y la plataforma blockchain y que facilite la comunicación fluida entre ambas capas.

## 3. Solución propuesta

Como la integración del adaptador blockchain se hace sobre una transacción cuando dos componentes intercambian información, lo recomendable es hacerla en puntos o etapas iniciales del proceso de ciclo de vida de la madera. Consecuentemente, usaremos blockchain, preferentemente, en algún punto del proceso de la "partida de nacimiento" del árbol. 

__3.1. Arquitectura de alto nivel__

Nuestra propuesta no pretende implementar las 4 capas representadas arriba; considerar este como una referencia o mapa de alto nivel que ayuda a entender dónde estará, o debería estar, situado el adaptador blockchain y el middleware.

![](/media/assets/post20221001/waskhar-arch-01.png)
_Arquitectura de alto nivel de la solución propuesta_

A continuación describiremos cada una de las capas y sus componentes presentes en la arquitectura:   

__I. Blockchain Ledger Layer__

* __Consensus Module__: Confirma la autenticidad y la adecuada ejecución de las operaciones dentro de la red de blockchain. Es responsable de la validación y la verificación de las transacciones y el acuerdo general sobre el estado actual del Ledger entre los diferentes nodos que participan en la red de blockchain.
* __Transactions Handling Module__: Es el componente más importante de cualquier plataforma blockchain. Su principal objetivo es almacenar los datos de la transacción y todos sus eventos relevantes en el "Ledger" (Registro Contable). Cuando una transacción está siendo enviada a la red blockchain, toda esta información es registrada en el Ledger. Dicha información incluirá un identificador de la transacción, identificador de quién origina y quién recibe, la hora de la transacción (timestamp), el valor de la transacción, etc.

__II. Middleware Layer__

* __Upload Handler Module__: Regula la gestión (entrada, descarga, registro, emisión) de documentos (facturas, guías de transporte, planes operativos, etc.) asociados con cada etapa del proceso. Cuando un nuevo documento entra al proceso, ciertas operaciones necesitan ser seguidas para manejarlas a través de la plataforma de blockchain, para ello este módulo creará un Smart Contract y lo desplegará a través del Smart Contract Manager Module. Después de eso, el documento quedará almacenado en el correspondiente CMS (Gestor Documental).
* __Data Orchestrator Module__: Es responsable de almacenar eficientemente un documento de manera segura y distribuída, con baja latencia.
* __Smart Contract Manager Module__: En este módulo, muchas operaciones viajan a través de sus funcionalidades y mecanismos de aprobación. La creación automática, despliegue y disparos de Smart Contracts constituyen su principal responsabilidad. Él interactúa con el Upload Handler y el Transactions Handling. Cuando un actor, por ejemplo un concesionario o un comprador, carga una guía de transporte, ya sea "requerida" o "entregada", el Smart Contract Manager procesaría las entradas respectivas recolectadas desde Upload Handler Module.
* __Application Transaction Handler__: Este módulo regula las transacciones que se gestionan dentro de la plataforma blockchain. Es responsable de todas las interacciones entre el Application Layer y el Middleware Layer. En el Smart Contract Manager, cada funcionalidad relacionada con el smart contract crea una nueva transacción que está controlada por el Transactions Handling y es reenviada a la Blockchain Ledger Layer.

__III. Application Layer__

* __Application Server (Implementación de la Cadena de Suministro)__: Implementa la lógica de negocio. Es el equivalente digital del proceso físico. Si el proceso físico no está automatizado, es este componente el que debería implementarlo. Usará una base de datos; además, podría trabajar conjuntamente con el ERP y/o CMS existentes. En esta capa se ubicará la aplicación actualmente en uso y que se integrará con blockchain.
* __ERP y CMS__: Podrían ser aplicaciones existentes, puede ser que no existan, tengan otro nombre o simplemente son implementaciones Ad-hoc y/o están distribuidas.

__IV. Proceso Físico (Cadena de Suministro)__

Representa el proceso seguido por todos los actores involucrados en la cadena de suministro de los recursos maderables. En el largo plazo, el éxito de este proyecto radica en llevar todas las etapas identificadas en el proceso al mundo digital; concretamente, implementar en el Application Layer dicho proceso de inicio a fin.

![](/media/assets/post20221001/waskhar-arch-02.png)
_Diagrama de transición entre capas_

__3.2. Arquitectura de bajo nivel__

Representaremos las especificaciones técnicas del adaptador blockchain, el middleware y cómo éste se integrará con la capa de aplicaciones de negocio (SNIFFS y otros).

![](/media/assets/post20221001/waskhar-arch-03.png)
_Diagrama de interacciones_


![](/media/assets/post20221001/waskhar-arch-04.png)
_Descripción de las interacciones_

__3.3. Especificaciones técnicas del Middleware Layer y del Blockchain Adapter__

La escalabilidad de la solución propuesta se alcanzará por los siguientes motivos: 
* __Middleware__: Es la mejor forma de integrar sistemas heterogéneos (Databosque, MC-SNIFFS, etc.) con el Blockchain Ledger. En este caso, el Middleware traducirá los eventos originados en las aplicaciones de negocio (ERP, CRM, BPM, etc.) en llamadas que Blockchain Ledger entienda. Como Middleware podemos emplear un ESB (Enterprise Service Bus), BPM (Business Process Manager), EDA (Event-Driven Architecture) tool o usar un AS (Application Server) con la capacidad de integrar y orquestar asíncronamente aplicaciones heterogéneas.
* __Adapter__: Una forma de encapsular y ocultar la complejidad de las operaciones que hay que realizar en el Blockchain Ledger. En este caso, el Blockchain Adapter expondrá dichas operaciones a través de API RESTful seguro. El Blockchain Adapter puede ser usado tantas veces como actividades en los procesos de negocio requieran registrar información en Blockchain Ledger, inclusive si las actividades identificadas en los procesos pertenecen a aplicaciones totalmente diferentes y distribuidas geográficamente. 
* __Disponibilidad__: El Middleware hospedará una o muchas instancias del Blockchain Adapter y que el Middleware debe ser accesible de manera segura a todas las aplicaciones que quieran interactuar con el Blockchain Ledger. 
Interoperabilidad con Blockchain: La interoperabilidad en el lado de las aplicaciones de negocio es alcanzada gracias al uso de API RESTful y al intercambio de mensajes estructurados en JSON y XML. Mientras que la interoperabilidad en el lado de Blockchain se logra gracias al uso de estándares aceptados en el sector Crypto como ERC-20 (Ethereum Request for Comments #20 para Tokens fungibles) y ERC-721 (para Tokens no fungibles). 

![](/media/assets/post20221001/waskhar-arch-05.png)
_Escalabilidad de la solución_

## 4. Objetivos del Proyecto

Diseñar la plataforma de trazabilidad basada en blockchain siguiendo los principios de integridad, autenticidad y no repudio de las acciones, transacciones y/u operaciones aplicado en un proceso específico de la cadena de suministro de la madera.

Implementar un adaptador blockchain para facilitar la integración de las aplicaciones de negocio con una plataforma de blockchain de manera fácil, transparente y agnóstica a la tecnología usada. Este adaptador podrá ser usado tantas veces como puntos de control se quiera tener a lo largo de la cadena de suministro, lo que asegura su escalabilidad. Adicionalmente, al desarrollar un adaptador genérico, esta misma solución podría ser usada en otras cadenas de suministro para combatir problemas de corrupción similares como las de la producción y explotación del oro, la hoja de coca, marihuana, etc.

## 5. Entregables y recursos

Los entregables y recursos necesarios para diseñar, implementar y soportar esta Propuesta de Proyecto son:

| Actividad | Observación                            |
| ---       | ---                                    |
| Identificar los puntos de integración del adaptador blockchain en un proceso específico de la aplicación objetivo | Incluye: Análisis de datos a incluir en la transacción blockchain. Entrevistas a usuarios y otros interesados. |
| Diseñar y crear el adaptador de blockchain     | - |
| Implementar el middleware de integración       | Incluye: Licencias y hosting |
| Determinar la plataforma blockchain a utilizar | Incluye:  Acceso a un entorno de desarrollo y pruebas durante los 6 meses |
| Crear la guía de integración del adaptador     | - |
| Implementar un caso genérico de integración del adaptador | |
| Diseño del smart contract                      | - |
| Pruebas de integración y seguridad             | - |

## 6. Conclusiones

1. El Middleware permitirá integrar aplicaciones nuevas, existentes y heterogéneas entre sí, resolviendo así el problema de las obsolescencias.
2. El diseño e implementación de las operaciones de blockchain como un Adaptador o Plugin facilitará la integración, escalabilidad, repetibilidad y encapsula la complejidad de blockchain en la cadena de suministro.
3. Blockchain mejora la trazabilidad debido a que usa algoritmos criptográficos para garantizar la integridad, autenticidad y no repudio de la información. Así tenemos:
  * _Confianza_. Un proceso automatizado que usa elementos de control, de seguridad, de auditabilidad y de trazabilidad que proporciona blockchain inspirará mayor confianza que uno que no está automatizado ni usa blockchain.
  * _Seguridad de Activos_. Los recursos maderables en procesos automatizados que usan blockchain representan activos. Un recurso natural maderable tendrá una representación unívoca como si fuese "dinero digital". Gracias a Blockchain, esos activos serán cuantificables como recursos valiosos fungibles que estarán registrados en un registro contable (ledger). Así, un concesionario podrá valuar los recursos maderables en su equivalente digital en Blockchain, siendo incluso tratados como recursos financieros y potencialmente usados como garantía bancaria.
  * _Antifraude_. Todos los recursos maderables y sus  operaciones (eventos y transacciones) quedan siempre registrados en el registro contable (ledger) que provee la plataforma blockchain. Con ello, no será posible "blanquear" recursos maderables.
4. Esta solución abre puertas a nuevas oportunidades como:
  * _Minting_: podemos crear activos financieros a partir de recursos forestales, por ejemplo, crear la "moneda árbol" y usarlo como recurso financiero.
  * _Bonos de carbono_: a partir de la cuantificación de los árboles podemos inferir cuánto de gases de efecto invernadero (GEI) son capturados y percibir algún beneficio.
