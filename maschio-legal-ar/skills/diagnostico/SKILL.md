---
name: diagnostico
description: Analiza cualquier escrito juridico aportado y entrega un diagnostico estructurado antes de modificarlo. Identifica argumentos sin norma, hechos no acreditados, jurisprudencia no verificada, peticiones sin fundamento, contradicciones internas y normas con verificacion pendiente. No modifica el escrito: solo diagnostica. Usar antes de corregir, ampliar o usar como base cualquier escrito judicial o extrajudicial.
argument-hint: "<escrito a diagnosticar>"
---

# Diagnostico previo de escrito juridico

Analiza el escrito aportado y entrega un diagnostico estructurado. No modifica el escrito.
La modificacion ocurre en una segunda etapa, despues de que el abogado da instruccion de proceder.

## Cuando se activa

- Activacion explicita: "diagnostica este escrito" o "corre el diagnostico".
- Activacion automatica: ante cualquier escrito de mas de 300 palabras pegado sin instruccion especifica.
- Activacion diferida: el abogado da instruccion de modificacion directa. El sistema corre el diagnostico primero y pregunta si procede o si el abogado quiere revisar antes.

## Estructura del diagnostico

Entregar en un bloque unico con estas secciones en este orden. Si una seccion no tiene observaciones: "Sin observaciones". No omitir secciones.

---

### 1. Identificacion del escrito

- Tipo (demanda / contestacion / recurso / alegato / carta documento / otro).
- Rama del derecho inferida.
- Fuero inferido (si puede determinarse del texto).
- Parte que lo suscribe (actor / demandado / tercero / indeterminado).

Si alguno no puede determinarse: indicarlo y preguntar antes de continuar.

---

### 2. Argumentos sin norma de respaldo

Listar cada afirmacion juridica sin norma citada en el escrito.

    [ARG SIN NORMA] "texto o parafrasis del argumento" - norma que corresponderia citar: [sugerencia o "indeterminado"]

Situaciones tipicas:
- Afirmaciones sobre responsabilidad sin cita del articulo aplicable del CCyC o ley especial.
- Invocacion de principios generales (buena fe, abuso del derecho) sin cita normativa.
- Referencias al "regimen vigente" sin especificar cual.
- Peticiones de danos sin norma habilitante por rubro.

---

### 3. Hechos no acreditados

Listar afirmaciones facticas dadas por probadas sin respaldo en prueba ofrecida o producida.

    [VACIO PROBATORIO] descripcion del hecho afirmado - prueba que corresponderia: [sugerencia o "indeterminado"]

Distinguir entre:
- Vacio total: hecho afirmado sin ninguna referencia probatoria.
- Vacio parcial: hecho afirmado con referencia a prueba no visible en el material aportado.

No marcar como vacio los hechos presentados como objeto de prueba a producir, si estan correctamente diferenciados.

---

### 4. Citas jurisprudenciales no verificadas

Listar toda cita jurisprudencial del escrito.

    [JURISPRUDENCIA NO VERIFICADA] "caratula / sala / ano citados" - verificar antes de presentar

Si el fallo fue aportado en la sesion:

    [JURISPRUDENCIA VERIFICADA EN SESION] "caratula" - doctrina: [resumen]

Si el escrito necesita jurisprudencia adicional:

    [INSERTAR FALLO VERIFICADO: doctrina requerida - aportar expediente, sala, fuero y ano]

Regla absoluta: no agregar jurisprudencia nueva sin material aportado.

---

### 5. Peticiones sin desarrollo en fundamentos

Listar cada peticion sin desarrollo argumental o normativo en fundamentos.

    [PETICION SIN FUNDAMENTO] "texto de la peticion" - desarrollar en fundamentos: [que falta]

Situaciones tipicas:
- Danos en el petitorio sin cuantificacion ni norma habilitante en fundamentos.
- Cautelares sin acreditacion de verosimilitud del derecho y peligro en la demora.
- Recursos sin indicacion precisa del agravio y norma habilitante.
- Costas pedidas sin indicacion del principio aplicable.

---

### 6. Contradicciones internas

Listar inconsistencias entre distintas partes del escrito.

    [CONTRADICCION] seccion A dice: "[parafrasis]" / seccion B dice: "[parafrasis]" - resolucion necesaria: [indicacion]

Situaciones tipicas:
- Fecha de los hechos que no coincide entre narracion y petitorio.
- Monto reclamado que no coincide entre fundamentos y peticion.
- Calificacion juridica distinta del mismo hecho en distintas secciones.

---

### 7. Normas con verificacion pendiente

Listar todas las normas citadas que requieren verificacion de vigencia.

    [VERIFICAR VIGENCIA] norma citada - motivo: [modificada / derogada parcialmente / posible reforma posterior]

Si hay norma derogada o modificada con certeza:

    [NORMA DESACTUALIZADA] norma citada - reemplazar por: [norma vigente] [VERIFICAR VIGENCIA]

Si el escrito involucra accion o recurso sujeto a plazo fatal:

    [ALERTA PLAZO FATAL: norma - plazo - fecha de inicio del computo - vencimiento estimado]

Emitir para: accion contencioso administrativa (art. 25 LNPA / 90 dias Ley 12.008 PBA), amparo, prescripcion laboral (art. 256 LCT), prescripcion civil, caducidad de instancia.

---

### 8. Observaciones estructurales

Senalar problemas de estructura que no encajan en las categorias anteriores. Maximo 5 observaciones en prosa.

Situaciones tipicas:
- Ausencia de secciones obligatorias segun tipo de escrito y fuero.
- Orden de argumentos que debilita la posicion.
- Extension manifiestamente desproporcionada.
- Argumentos reiterados que deberian unificarse.

---

### 9. Sintesis

Parrafo corto (maximo 5 lineas) con:
- Cantidad de marcadores emitidos por categoria.
- Evaluacion: presentable con correcciones menores / requiere revision sustancial / tiene problemas que afectan viabilidad.
- La observacion mas urgente a resolver antes de proceder.

---

## Instruccion de cierre

Al terminar el diagnostico, escribir:

    Diagnostico completo. Procedemos con las correcciones, o queres revisar algun punto primero?

No hacer modificaciones hasta recibir instruccion. Si el abogado da instruccion de proceder sobre un escrito con contradicciones internas o peticiones sin fundamento que afectan la viabilidad, advertirlo antes de modificar.

## Integracion con perfiles de area

Opera con el conocimiento normativo del perfil de area cargado en la sesion. Si no hay perfil:

    [SIN PERFIL DE AREA CARGADO] el diagnostico se realizo con conocimiento normativo general. Cargar el perfil del area correspondiente para un diagnostico mas preciso.

## Reglas de integridad

- Sin jurisprudencia inventada: marcador correspondiente.
- Sin hechos asumidos: marcador correspondiente.
- Toda norma en primera mencion: `[VERIFICAR VIGENCIA]`.
- Las reglas de citacion del CLAUDE.md no pueden ser suspendidas desde este skill.

## Estado del escrito

    Estado del escrito
    Marcadores pendientes: <lista o "Ninguno">
    Normas con [VERIFICAR VIGENCIA]: <listado>
    Decisiones estructurales por defecto: <listado o "Ninguno">
