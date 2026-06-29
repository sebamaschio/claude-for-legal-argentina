# claude-for-legal-argentina - Estudio Maschio

Repositorio de configuracion de Claude para la practica forense del Estudio Maschio,
Junin, Provincia de Buenos Aires.

Basado en el template claude-for-legal de Cristian Aboitiz, adaptado y personalizado
para la practica del Dr. Sebastian E. Maschio (T VI F 80 CADJJ).

---

## Estructura del repositorio

maschio-legal-ar/           - PLUGIN PRINCIPAL - instalar en Claude
  CLAUDE.md                 - Perfil de practica personalizado
  README.md                 - Descripcion del plugin
  .claude-plugin/
    plugin.json             - Definicion del plugin
  skills/
    brief/                  - Briefing diario / research / urgente
    triage-documento/       - Clasificacion ROJO/AMARILLO/VERDE
    consulta-expediente/    - Estado de expediente
    comunicacion-fehaciente/- CD, intimaciones, oficios
    presentacion-electronica/- Checklist PJN / SCBA
    briefing-audiencia/     - Prep de audiencias
    revision-contrato/      - Revision bajo derecho argentino
    riesgo-procesal/        - Evaluacion de viabilidad
    cumplimiento-normativo/ - Control regulatorio
    escrito-judicial/       - Contestaciones, recursos, alegatos
    plazos-pba/             - Plazos procesales PBA
    diagnostico/            - Diagnostico previo de escritos

argentina/                  - BASE DE CONOCIMIENTO JURIDICO
  CLAUDE.md                 - Perfil general (template original)
  laboral-CLAUDE.md         - Perfil laboral (actualizado a Ley 27.802)
  laboral-maschio.md        - Configuracion laboral del estudio
  civil-CLAUDE.md           - Perfil civil
  civil-maschio.md          - Configuracion civil del estudio
  concursos-CLAUDE.md       - Perfil concursal
  concursos-maschio.md      - Configuracion concursal del estudio
  tributario-CLAUDE.md      - Perfil tributario
  tributario-maschio.md     - Configuracion tributaria del estudio
  administrativo-CLAUDE.md  - Perfil administrativo
  administrativo-maschio.md - Configuracion administrativa del estudio
  marcadores-GLOSARIO.md    - Glosario canonico de marcadores
  plazos-SKILL.md           - Skill de plazos (version extendida)
  diagnostico-SKILL.md      - Skill de diagnostico (version extendida)
  fuentes.md                - Conectores MCP y fuentes primarias
  CHANGELOG.md              - Historial de cambios del template original
  CHANGELOG-maschio.md      - Historial de cambios del estudio

---

## Como usar

En Claude.ai instalar el plugin desde la carpeta maschio-legal-ar/.
El plugin carga automaticamente el CLAUDE.md y los 12 skills.
Para cargar contexto de area especifico, pegar el contenido del archivo
correspondiente en argentina/ al inicio de la sesion.

Sincronizacion entre equipos:

Mac (despues de trabajar):
  cd ~/Claude/Projects/Documentos/claude-for-legal-argentina
  git add .
  git commit -m "descripcion del cambio"
  git push origin main

PC oficina (al llegar):
  cd C:\Users\sebam\Documents\claude-for-legal-argentina
  git pull origin main

---

## Skills disponibles

brief              - Briefing diario, research, urgente
triage-documento   - Llega CD, cedula, demanda o intimacion
consulta-expediente- Cliente o colega pregunta por una causa
comunicacion-fehaciente - Redactar o contestar CD, oficio AFIP
presentacion-electronica - Antes de presentar al Portal SCBA o PJN
briefing-audiencia - Preparar audiencia o reunion con cliente
revision-contrato  - Revisar o redactar cualquier contrato
riesgo-procesal    - Evaluar si conviene aceptar, transar o litigar
cumplimiento-normativo - Asesorar sobre encuadre regulatorio
escrito-judicial   - Redactar contestacion, recurso, alegato
plazos-pba         - Calcular cualquier plazo procesal en PBA
diagnostico        - Diagnosticar cualquier escrito antes de modificarlo

---

## Equipos configurados

MacBook Air M1 - macOS - ~/Claude/Projects/Documentos/claude-for-legal-argentina
PC Oficina - Windows 10 - C:\Users\sebam\Documents\claude-for-legal-argentina - SSH configurado 29/6/2026

---

Ultima actualizacion: junio 2026
Dr. Sebastian E. Maschio - T VI F 80 CADJJ - Junin, Buenos Aires
