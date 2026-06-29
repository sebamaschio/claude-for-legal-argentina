### Junio 2026 - Plugin maschio-legal-ar + configuracion del estudio

**Archivos nuevos:**
- `maschio-legal-ar/.claude-plugin/plugin.json` - definicion del plugin personalizado del estudio Maschio
- `maschio-legal-ar/README.md` - descripcion del plugin
- `maschio-legal-ar/CLAUDE.md` - perfil de practica personalizado (matriculas, fueros, areas, causas activas)
- `maschio-legal-ar/skills/brief/SKILL.md` - briefing forense diario / research / urgente
- `maschio-legal-ar/skills/triage-documento/SKILL.md` - clasificacion ROJO/AMARILLO/VERDE de documentos recibidos
- `maschio-legal-ar/skills/consulta-expediente/SKILL.md` - estado de expediente (Lex Doctor + PJN + SCBA)
- `maschio-legal-ar/skills/comunicacion-fehaciente/SKILL.md` - CD, intimaciones, oficios AFIP
- `maschio-legal-ar/skills/presentacion-electronica/SKILL.md` - checklist PJN / SCBA / firma
- `maschio-legal-ar/skills/briefing-audiencia/SKILL.md` - prep de audiencias
- `maschio-legal-ar/skills/revision-contrato/SKILL.md` - revision bajo derecho argentino
- `maschio-legal-ar/skills/riesgo-procesal/SKILL.md` - evaluacion de viabilidad y exposicion
- `maschio-legal-ar/skills/cumplimiento-normativo/SKILL.md` - control regulatorio AR
- `maschio-legal-ar/skills/escrito-judicial/SKILL.md` - contestaciones, recursos, alegatos PBA
- `maschio-legal-ar/skills/plazos-pba/SKILL.md` - calculo martes/viernes, ferias, acordadas SCBA
- `maschio-legal-ar/skills/diagnostico/SKILL.md` - diagnostico previo de escritos judiciales
- `argentina/laboral-maschio.md` - configuracion laboral del estudio (fuero, rol, CCTs)
- `argentina/civil-maschio.md` - configuracion civil del estudio (fuero, areas)
- `argentina/concursos-maschio.md` - configuracion concursal del estudio (fuero, roles)
- `argentina/tributario-maschio.md` - configuracion tributaria del estudio (fuero, perfil, tributos)
- `argentina/administrativo-maschio.md` - configuracion administrativa del estudio (fuero, areas)
- `.gitattributes` - normalizacion de saltos de linea LF/CRLF entre Mac y PC

**Archivos modificados:**
- `maschio-legal-ar/skills/plazos-pba/SKILL.md` - agregados: distincion tipos de plazo (hábiles judiciales / administrativos / corridos), marcador A10 ALERTA PLAZO FATAL con sintaxis canonica, exclusiones AFIP/ARBA/ANSES, tabla de plazos administrativos PBA (Dec-Ley 7647/70)

**Infraestructura:**
- SSH GitHub configurado en PC oficina (Windows 10, DESKTOP-8AV3M6N)
- Repo claude-for-legal-argentina clonado en C:\Users\sebam\Documents\
- Push funcionando desde PC con identidad git configurada

