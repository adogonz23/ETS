<h1>Ejercicio de  casos de Usos</h1>

Adonay González Gutiérrez

<h2>Indice</h2>

- [Ejercicio](#ejercicio)
- [Diagrama](#diagrama)
- [Especificacion Actores](#especificacion-actores)
  - [Paciente](#paciente)
  - [Recepcionista](#recepcionista)
  - [Administrador](#administrador)
  - [Enfermero](#enfermero)
  - [Medico](#medico)
- [Especificación Casos de Uso](#especificación-casos-de-uso)
  - [Se registra](#se-registra)
  - [Programa Citas](#programa-citas)
  - [Actualizaciones](#actualizaciones)
  - [Configuraciones](#configuraciones)
  - [Gestion de recursos](#gestion-de-recursos)
  - [Realaizan tareas](#realaizan-tareas)
  - [Aceden al historial](#aceden-al-historial)
  - [Prescribe tratamientos](#prescribe-tratamientos)
  - [Realiza Diagnosticos](#realiza-diagnosticos)
  - [Asigna tareas](#asigna-tareas)





## Ejercicio
Sistema de Gestión Hospitalaria

El sistema de gestión hospitalaria tiene como objetivo mejorar la eficiencia y coordinación de los procesos dentro de un hospital. En el sistema participan distantas personas, como son: Paciente, Médico, Enfermero, Administrador del Sistema y Recepcionista. A continuación, se presentan algunos casos de uso para este sistema:

**La información que se posee de cada uno de ellos es la siguiente:**

- Paciente: Un individuo que busca servicios médicos en el hospital.
- Médico: Profesional médico encargado de diagnosticar y tratar a los pacientes.
- Enfermero: Encargado de asistir a los médicos y cuidar a los pacientes.
- Administrador del Sistema: Responsable de la configuración y administración del sistema.
- Recepcionista: Encargado de la recepción de pacientes y asignación de citas.

**Las acciones que se realizarán en el sistema son las que siguen:**

- El paciente se registra en el sistema proporcionando información personal y médica.
- El paciente o la recepcionista programa citas médicas para los pacientes. (Debe autenticado)
- El médico realiza diagnósticos, prescribe tratamientos y registra la información médica del paciente.(Debe autenticado)
- El médico y el enfermero pueden acceder y actualizar el historial médico del paciente.(Debe autenticado)
- El médico asigna tareas específicas a los enfermeros relacionadas con la atención del paciente.(Debe autenticado)
- El administrador del sistema realiza configuraciones y actualizaciones del sistema.(Debe autenticado)
- El personal administrativo realiza tareas relacionadas con la facturación y el procesamiento del seguro médico.(Debe autenticado)
- El administrador del sistema gestiona los recursos hospitalarios, como camas, equipos médicos y suministros.(Debe autenticado)

## Diagrama

<img src="EjercicioCU1.png"/>

## Especificacion Actores

### Paciente
|  Actor | Paciente |
|---|---|
| Descripción  | Persona que busca servicios medicos|
| Características  |  |
| Relaciones | se relaciona con el recepcionista, el enfermero y el medico  |
| Referencias |Se registra en el sistema, programa citas, debe autenticarse|   
|  Notas |  _ |
| Autor  | Adonay Gonzalez Gutierrez |
|Fecha | 2023-11-15 |

### Recepcionista

|  Actor | Recepcionista |
|---|---|
| Descripción  | Encargado de recibir a los clientes y asignar citas  |
| Características  ||
| Relaciones | Se relaciona con el cliente   |
| Referencias |Programa citas y debe autenticarse|   
|  Notas |No las hay|
| Autor  | Adonay González Gutiérrez |
|Fecha | 2023-11-15|

### Administrador
|  Actor | Administrador |
|---|---|
| Descripción  | Responsable de la Configuracion del sistema  |
| Características  |  |
| Relaciones | no se relaciona con el resto de Actores |
| Referencias | Actulizaciones y configuracion de sistema, gestiona rescursos ( camas, equipos medicos, suministros), realizatareas de facturacion y de seguros medicos |   
|  Notas |  |
| Autor  | Adonay González Gutiérrez |
|Fecha | 2023-11-15|

### Enfermero
|  Actor | Enfermero |
|---|---|
| Descripción  | Encargados de asisitir a los medicos y cuidar a los pasientes |
| Características  |  |
| Relaciones | realiza las tareas asignadas por los medicos, cuida los pacientes   |
| Referencias | accede al historial, actualiza historial, debe autenticarse. |   
|  Notas |  |
| Autor  | Adonay González Gutiérrez |
|Fecha | 2023-11-15|

### Medico 
|  Actor | Medico |
|---|---|
| Descripción  | Profesional encargado de diagnosticar y tratar a los pacientes  |
| Características  |  |
| Relaciones | diagnostica y trata a los pacientes, asigna tareas a los enfermeros y pueden acceder al historial medico del paciente y actualizar sus datos |
| Referencias | diagnostica y trata, actualiza historial, asigna tareas, debe atenticarse |   
|  Notas |   |
| Autor  | Adonay González Gutiérrez |
|Fecha | 2023-11-15|

## Especificación Casos de Uso

### Se registra
 |  Caso de Uso	CU | Se registra  |
  |---|---|
  | Fuentes  | [Ejercicio](#ejercicio) |
  | Actor  |  Paciente |
  | Descripción | Registr sus datos en el sistema  |
  | Flujo básico | |
  | Pre-condiciones |  |  
  | Post-condiciones  | |  
  |  Requerimientos |   |
  |  Notas |  _Notas adicionales_ |
  | Autor  | Adonay González Gutiérrez |
  |Fecha | 2023-11-15 |

### Programa Citas
   |  Caso de Uso	CU | Programa Citas |
  |---|---|
  | Fuentes  |  [Ejercicio](#ejercicio) |
  | Actor  | El Cliente y el Recepcionista |
  | Descripción | El cliente o el recepcionista programan una cita   |
  | Flujo básico | _Descripción paso a paso de la ejecución. (1->2->3.)_ |
  | Pre-condiciones |  |  
  | Post-condiciones  |  |  
  |  Requerimientos | Autenticar |
  |  Notas |  _Notas adicionales_ |
  | Autor  | Adonay González Gutiérrez |
  |Fecha | 2023-11-15 |


### Actualizaciones
   |  Caso de Uso	CU | Actualizaciones  |
  |---|---|
  | Fuentes  | [Ejercicio](#ejercicio) |
  | Actor  |  Administrador |
  | Descripción | el administrador actuliza la base de datos  |
  | Flujo básico |  |
  | Pre-condiciones | debe autenticarse antes |  
  | Post-condiciones  |   |  
  |  Requerimientos | debe autenticarse |
  |  Notas |  _Notas adicionales_ |
  | Autor  | Adonay González Gutiérrez|
  |Fecha | 2023-11-15 |


### Configuraciones
   |  Caso de Uso	CU | Configuraciones |
  |---|---|
  | Fuentes  | [Ejercicio](#ejercicio)  |
  | Actor  | Administrador |
  | Descripción | Configura la base de datos  |
  | Flujo básico |  |
  | Pre-condiciones | _debe estar atenticado  |  
  | Post-condiciones  |  |  
  |  Requerimientos | debe estar autenticado  |
  |  Notas |  _Notas adicionales_ |
  | Autor  | Adonay González Gutiérrez |
  |Fecha | 2023-11-15 |

### Gestion de recursos
   |  Caso de Uso	CU | Gestiona recursos |
  |---|---|
  | Fuentes  |[Ejercicio](#ejercicio)  |
  | Actor  |  Administrador|
  | Descripción | gestiona los recursos del hospital |
  | Flujo básico | se Autentica realiza las gestiones, que pueden ser sobre las camas , los equipos medicos y suministros  |
  | Pre-condiciones | autenticar |  
  | Post-condiciones  |  |  
  |  Requerimientos | debe auntenticarse  |
  |  Notas |  _Notas adicionales_ |
  | Autor  | Adonay González Gutiérrez |
  |Fecha | 2023-11-15 |

### Realaizan tareas
   |  Caso de Uso	CU | realiza tareas  |
  |---|---|
  | Fuentes  | [Ejercicio](#ejercicio)  |
  | Actor  |  Administrador|
  | Descripción | _el administrador puede realizar diferentes tareas |
  | Flujo básico | _se autentica luego realiza las tareas que pueden ser la facturacion y procesamiento de seguros medicos|
  | Pre-condiciones | autenticarse  |  
  | Post-condiciones  |  |  
  |  Requerimientos | debe atenticarse |
  |  Notas |  _Notas adicionales_ |
  | Autor  | Adonay González Gutiérrez |
  |Fecha | 2023-11-15 |

### Aceden al historial
   |  Caso de Uso	CU | accede al historial  |
  |---|---|
  | Fuentes  | [Ejercicio](#ejercicio) |
  | Actor  | Enfermero y medico |
  | Descripción | el enfermero y el medico puede acceder al historial del paciendo y actilaizarlo  |
  | Flujo básico | debe autenticarse, accede al historial, puede actualizarlo |
  | Pre-condiciones |  |  
  | Post-condiciones  |  |  
  |  Requerimientos |debe autenticarse  |
  |  Notas |  _Notas adicionales_ |
  | Autor  |Adonay González Gutiérrez |
  |Fecha | 2023-11-15 |

### Prescribe tratamientos
   |  Caso de Uso	CU | Prescribe tratamientos |
  |---|---|
  | Fuentes  | [Ejercicio](#ejercicio)  |
  | Actor  |  Medico |
  | Descripción | prescribe tratamientos al paciente  |
  | Flujo básico |  |
  | Pre-condiciones |   |  
  | Post-condiciones  |   |  
  |  Requerimientos | Debe autenticar |
  |  Notas |  _Notas adicionales_ |
  | Autor  | Adonay González Gutiérrez |
  |Fecha | 2023-11-15 |

### Realiza Diagnosticos
   |  Caso de Uso	CU | Realiza Diagnosticos  |
  |---|---|
  | Fuentes  | [Ejercicio](#ejercicio) |
  | Actor  | Medico |
  | Descripción | realiza diagnosticos a los pacientes |
  | Flujo básico |  |
  | Pre-condiciones |  |  
  | Post-condiciones  |   |  
  |  Requerimientos | Debe autenticar |
  |  Notas |  _Notas adicionales_ |
  | Autor  | Adonay González Gutiérrez |
  |Fecha | 2023-11-15 |

### Asigna tareas
   |  Caso de Uso	CU | Asigna tareas |
  |---|---|
  | Fuentes  | [Ejercicio](#ejercicio) |
  | Actor  |  Medico |
  | Descripción | Asigna tareasa los enfermeros |
  | Flujo básico |  |
  | Pre-condiciones |   |  
  | Post-condiciones  |   |  
  |  Requerimientos |   |
  |  Notas |  _Notas adicionales_ |
  | Autor  | Adonay González Gutiérrez |
  |Fecha | 2023-11-15 |
   