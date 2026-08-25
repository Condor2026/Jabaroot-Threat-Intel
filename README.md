**INFORME DE INTELIGENCIA DE AMENAZAS (CTI) – VERSIÓN EXTENDIDA PARTES 1-2-3**

**Actor:** Jabaroot (alias JabaROOT, Jabaroot DZ, JabaRoot DZ)  
**Fecha de elaboración:** 25 de agosto de 2026  
**Clasificación:** TLP:WHITE / Fuentes abiertas  
**Estado del actor:** Activo – canal `@jabaroot_off` abierto y operativo  
**Versión:** 3.0 – Análisis completo de amenaza, riesgo y escenarios
**Autor:** Condor2026
---

## Índice

1. Resumen ejecutivo
2. Perfil del actor y atribución
   - 2.1. Autoidentificación y significado del nombre
   - 2.2. Atribuciones externas y análisis de credibilidad
   - 2.3. Pista OSINT: Rachid Mzannar / 3N16M4
   - 2.4. Ranking de hipótesis de atribución
3. Historial de actividad (timeline detallada)
   - 3.1. Aparición y primer gran golpe (abril 2025)
   - 3.2. Expansión de objetivos (junio-diciembre 2025)
   - 3.3. Operaciones de 2026
4. Operación actual: filtraciones de agosto de 2026
   - 4.1. Datos filtrados: RAMED
   - 4.2. Datos filtrados: DGST/DGSN (70.000 agentes)
   - 4.3. Estructura de los datos y validación
   - 4.4. Narrativa y framing político
   - 4.5. Teaser Pegasus / Pedro Sánchez
   - 4.6. Cronología precisa de la operación
5. Análisis técnico y de autenticidad de los datos
   - 5.1. Análisis de muestras
   - 5.2. Comparativa con históricos
   - 5.3. Infraestructura utilizada
6. Análisis de motivaciones e hipótesis estratégicas
   - 6.1. Matriz de intereses del actor
   - 6.2. Hipótesis de motivación profunda
7. Tácticas, Técnicas y Procedimientos (TTPs)
8. Modelo de Diamante del actor
9. Evaluación de riesgos e impacto
   - 9.1. Matriz de impacto por dimensión
   - 9.2. Escenarios de evolución (corto, medio, largo plazo)
   - 9.3. Niveles de confianza y probabilidad
   - 9.4. Análisis de vulnerabilidades expuestas
10. Recomendaciones estratégicas y tácticas
    - 10.1. Para equipos de seguridad / CTI
    - 10.2. Para las instituciones afectadas (DGST, DGSN, gobierno marroquí)
    - 10.3. Para el Gobierno de España
    - 10.4. Para la comunidad de inteligencia y OSINT
11. Preguntas abiertas y líneas de investigación pendientes
12. Conclusión
13. Anexos: Fuentes y referencias

---

## 1. Resumen Ejecutivo

Jabaroot es un actor de amenazas de tipo **hacktivista con componente de inteligencia de fuentes abiertas (OSINT) y operaciones de información (info-ops)**. Activo desde abril de 2025, ha demostrado capacidad para comprometer sistemas gubernamentales marroquíes de alta sensibilidad y extraer volúmenes masivos de datos personales y administrativos.

El nombre "Jabaroot" (también transcrito como "JabaROOT" o "Jabaroot DZ") deriva del árabe y se traduce aproximadamente como **"Poderío"** o **"Potencia"**. El sufijo "DZ" hace referencia explícita a Argelia (código ISO del país), lo que refuerza su autoidentificación como actor argelino.

La operación de agosto de 2026 es la más ambiciosa hasta la fecha:

- **Filtración de 70.000 registros** de agentes de la DGST (inteligencia interior) y DGSN (policía nacional).
- **Publicación de 1 millón de entradas del sistema sanitario RAMED**, con promesa de los 17 millones completos.
- **Teaser de datos Pegasus** vinculados a Pedro Sánchez, sin materialización hasta el momento.
- **Narrativa geopolítica explícita**: vincular la crisis migratoria de Ceuta con un "plan oficial marroquí" y exponer a altos cargos (Hammouchi, Lekjaa, El Himma).

El canal Telegram `@jabaroot_off` permanece abierto y activo, y los archivos se han movido a `darkforums.ru` para evitar el bloqueo de la plataforma.

**Evaluación de riesgo global:** **CRÍTICO** para la seguridad nacional de Marruecos y **ALTO** para las relaciones bilaterales con España. La credibilidad del actor es media-alta, aunque persisten dudas sobre la autenticidad completa del *dump* de 70.000 y la posibilidad de *brand hijacking*.

---

## 2. Perfil del Actor y Atribución

### 2.1. Autoidentificación y significado del nombre

- Se presenta como **colectivo de "patriotas argelinos"** y hacktivistas nacionalistas.
- El nombre "Jabaroot" (جبروت) significa "poderío" o "potencia" en árabe.
- El sufijo "DZ" (código ISO de Argelia) es una declaración de intenciones sobre su afiliación.
- Reivindica acciones en respuesta a ofensivas pro-marroquíes contra instituciones argelinas.

### 2.2. Atribuciones externas

| Fuente | Atribución | Confianza | Detalles |
|--------|------------|-----------|----------|
| Gobierno marroquí | Argelia (proxy o servicios de inteligencia) | Media | Atribución sistemática pero sin pruebas técnicas |
| CSIDB / Malpedia | Activista argelino | Media-alta | Clasificación en bases de datos de amenazas |
| CybelAngel | Ingeniero tunecino en Alemania (pista Mzannar) | Baja-media | Pista OSINT con fallo de OPSEC |
| Navakintelligence | Exagente o insider marroquí en solitario | Media-baja | Teoría de consultora especializada |
| Analistas independientes | Brand hijacking / imitadores | Media | Inconsistencias técnicas en el dump actual |

### 2.3. Pista OSINT: Rachid Mzannar / 3N16M4 (abril 2025)

El **8 de abril de 2025**, se produjo un **fallo de OPSEC** cuando varios archivos publicados en el canal de Telegram de Jabaroot fueron observados como **reenviados desde una cuenta personal con el handle `3N16M4`**.

El *pivot* OSINT reveló:

| Paso | Hallazgo |
|------|----------|
| Handle expuesto | `3N16M4` en Telegram |
| GitHub | Cuenta con el mismo handle y actividad en repositorios |
| Correos electrónicos | `r.mzannar@rub.de` (Universidad Ruhr de Bochum) / `mzannar.rachid@hotmail.com` |
| LinkedIn | Ingeniero de ciberseguridad en **emproof** (Bochum, Alemania) |
| CTF | Participación en competiciones Capture The Flag |
| Origen declarado | **Tunecino** (no argelino) en perfiles de CTF |

**CybelAngel** señala que el análisis OSINT sugiere que la persona detrás de Jabaroot **podría ser un ingeniero informático actualmente en Alemania**.

**Estado actual de esta atribución:**
- Es la única pista nominal concreta que existe en fuentes abiertas.
- La confianza que le dan la mayoría de analistas es **baja-media**.
- No hay confirmación oficial, detención pública ni prueba técnica definitiva de que esta persona siga detrás de Jabaroot en 2026.
- El grupo ha seguido operando con múltiples canales y posible *brand hijacking*.

### 2.4. Ranking de hipótesis de atribución

| Hipótesis | Probabilidad | Fundamento |
|-----------|--------------|------------|
| **Actor argelino (hacktivista o proxy)** | **Media-alta** | Autoidentificación, timing con tensiones regionales, narrativa anti-Marruecos consistente |
| **Brand hijacking / imitadores oportunistas** | **Media** | Inconsistencias en samples de 70k, duplicados, campos genéricos, canales efímeros |
| **Insider marroquí o facción interna** | **Media-baja** | Volumen y sensibilidad de dumps anteriores, conocimiento de estructuras internas |
| **Actor comercial / data broker** | **Media** | Reutilización de datos en foros de leaks, posible venta previa de los mismos datasets |
| **APT rusa o estructura estatal** | **Muy baja** | Sin evidencia pública en foros rusos principales (XSS, Exploit, RAMP), TTPs no coinciden con APT |
| **Falsa bandera del régimen marroquí** | **Muy baja** | Daño real a su propio aparato de seguridad y a altos cargos |

---

## 3. Historial de Actividad (Timeline Detallada)

### 3.1. Aparición y Primer Gran Golpe (Abril 2025)

El **8 de abril de 2025**, Jabaroot apareció públicamente en BreachForums y Telegram reivindicando el compromiso de la **Caja Nacional de Seguridad Social de Marruecos (CNSS)**.

| Aspecto | Detalle |
|---------|---------|
| **Fecha** | 8 de abril de 2025 |
| **Plataforma** | BreachForums y Telegram (@JabarootDZ) |
| **Volumen** | Más de **53.000 archivos PDF** y **2 CSVs** |
| **Registros afectados** | **1.996.026 empleados** y **cerca de 500.000 empresas** |
| **Datos expuestos** | Nombres, direcciones, salarios, números de identificación, datos bancarios, información de contacto |
| **Antigüedad** | Datos de hasta noviembre de 2024 |
| **Motivación declarada** | Represalia por el compromiso de la cuenta de Twitter de la Agencia de Prensa Argelina (APS), que fue renombrada como "Sahara Marocain" |

El ataque fue calificado como **una de las brechas de datos más dañinas en la historia digital moderna de Marruecos**. El actor también publicó una captura de pantalla mostrando la **defacement del sitio web del Ministerio de Trabajo marroquí**.

### 3.2. Expansión de Objetivos (Junio-Diciembre 2025)

| Fecha | Objetivo | Detalles |
|-------|----------|----------|
| **Junio 2025** | **ANCFCC** (Agencia Nacional de Conservación de la Propiedad) | Reivindicación en DarkForums. Muestras de más de **10.000 certificados de propiedad** y **20.000 documentos** diversos (escrituras, documentos de estado civil, ID/pasaportes, documentos bancarios). El actor afirma que la base de datos completa supera los **4 TB** y contiene **más de 4 millones de documentos** |
| **Junio 2025** | **Documentos de VIPs** | Muestras específicas de altos cargos: **Fouzi Lekjaa**, **Mohammed Yassine Mansouri** (jefe de inteligencia exterior), **Nasser Bourita** (ministro de Asuntos Exteriores) y **Raghib Amin** |
| **Octubre 2025** | **Ministerio de Justicia** | Filtración de datos de magistrados y personal |
| **Finales 2025** | **Palacios reales** | Lista de **~3.400 empleados** de los palacios reales marroquíes |

**Nota sobre la filtración de ANCFCC:** La legitimidad de la filtración completa fue cuestionada por usuarios de DarkForums, ya que el actor no compartió el conjunto de datos completo. Algunos sugirieron que Jabaroot podría tener acceso a un número limitado de documentos en lugar de a una base de datos completa. El hilo de DarkForums fue finalmente eliminado por un moderador debido a enlaces rotos.

### 3.3. Operaciones de 2026

| Fecha | Evento | Detalles |
|-------|--------|----------|
| **Enero 2026** | **Ataque a la FRMF** (Federación Real Marroquí de Fútbol) | Bases de datos de jugadores, contratos, personal. Relacionado con el conflicto cibernético con el grupo pro-marroquí **Dark 07x** en contexto deportivo |
| **Julio 2026** | **Preparación de operación Ceuta** | Amenazas previas y construcción de narrativa en torno a la crisis migratoria |
| **7 de agosto 2026** | **Primeras exigencias sobre Ceuta** | Jabaroot exige disculpas oficiales, luto nacional y suspensión de elecciones legislativas previstas para el 23 de septiembre |
| **21 de agosto 2026** | **Creación de canal `@jabaroot_off`** | Primeros mensajes: "Canal creado", "Foto actualizada", "Hemos vuelto" |
| **23 de agosto 2026** | **Anuncio de filtración RAMED** | 1M de 17M registros, promesa de publicación completa |
| **24 de agosto 2026** | **Anuncio de filtración DGST/DGSN** | 70.000 agentes, enlace a darkforums.ru |
| **24 de agosto 2026** | **Mensaje "regalo a Europa/España"** | Vinculación explícita con Ceuta y plan oficial marroquí |
| **24 de agosto 2026** | **Teaser Pegasus / Pedro Sánchez** | Pregunta en Telegram, sin publicación |
| **24 de agosto 2026** | **Mensaje a la prensa marroquí** | Desafío a Hammouchi y Lekjaa, exige destitución |
| **24 de agosto 2026** | **Eliminación de archivos de Telegram** | Movidos a darkforums.ru para evitar baneo |
| **25 de agosto 2026** | **Canal sigue abierto** | No ha sido cerrado por Telegram |

---

## 4. Operación Actual: Filtraciones de Agosto de 2026

### 4.1. Datos Filtrados: RAMED (Régime d’Assistance Médicale)

- **Volumen filtrado:** 1 millón de entradas (de 17 millones totales)
- **Datos expuestos:** nombres completos, fotos tipo pasaporte, ID social, fecha de nacimiento, número de DNI, región
- **Estado:** Publicado parcialmente en Telegram; resto prometido en `darkforums.ru`
- **Contexto:** RAMED es un programa de asistencia médica subsidiada para ciudadanos de bajos ingresos en Marruecos

### 4.2. Datos Filtrados: DGST / DGSN (70.000 Agentes)

- **Volumen filtrado:** 70.000 registros
- **Lista secundaria:** 1.400 registros adicionales con grados y RIB
- **Datos expuestos**:
  - Lista principal: nombres completos, números de identificación nacional (DNI), número de empleado público, año de reclutamiento
  - Lista secundaria (~1.400 registros): grados dentro del cuerpo y números de identificación bancaria (RIB)
- **Instituciones afectadas**:
  - **DGST** (Dirección General de Supervisión del Territorio) – inteligencia interior marroquí, dirigida por Abdellatif Hammouchi
  - **DGSN** (Dirección General de Seguridad Nacional) – policía marroquí, también dirigida por Hammouchi

### 4.3. Estructura de los Datos y Validación

**Validación de autenticidad:**

- **Validación parcial** por varios **exagentes de la inteligencia marroquí** consultados por El Confidencial.
- Entre los nombres confirmados aparecen: el **director de recursos humanos de la DGST**, el **director adjunto de contraespionaje** y el **jefe de la Célula de Investigación**.
- Fuentes del **CNI español** han confirmado que varios nombres en las listas corresponden a agentes ya investigados.
- **Limitación:** El medio apunta que los documentos podrían haber sido obtenidos tiempo atrás y publicados ahora.

**Análisis de Golden Owl (22 de agosto de 2026):**

| Observación | Implicación |
|-------------|-------------|
| 26 filas analizadas, 1 duplicado exacto | Posible mala calidad o mezcla de bases |
| Campos de rango vacíos en la mayoría | No coincide con perfil completo esperado de agentes |
| Fechas de nacimiento genéricas (1 de enero) | Podrían venir de bases civiles previas |
| Ningún individuo confirmado como DGST/DGSN de forma independiente | Duda sobre la autenticidad total |
| **Conclusión:** Más consistente con **brand hijacking** que con el actor original | |

### 4.4. Narrativa y Framing Político

El actor utiliza la filtración para construir una narrativa compleja:

1. **Acusación de "plan oficial de migración forzada"**: Jabaroot sostiene que la filtración demuestra que la migración de ciudadanos marroquíes hacia Europa, y especialmente hacia España, formaría parte de un supuesto plan oficial de Marruecos.

2. **Señalamiento directo a altos cargos**:
   - **Abdellatif Hammouchi** (máximo responsable de DGST y DGSN) es acusado de ser el responsable del "asalto migratorio" a Ceuta.
   - **Fouad Ali el Himma** (principal consejero del rey Mohamed VI) es señalado como el planificador del ataque para "poner a España en una situación difícil".
   - El grupo menciona también a **Fouzi Lekjaa** como posible responsable de la filtración.

3. **Implicación de actores internacionales**: Jabaroot asegura que **"un país grande y otro Estado ficticio"** (en clara alusión a Estados Unidos e Israel) estaban al tanto de la operación.

4. **Exoneración del monarca**: Los hackers eximen expresamente al rey: *"El rey no sabía nada, no tenía conocimiento de los sucesos de Ceuta"*.

5. **Mensaje a la prensa marroquí**: Desafío directo a los medios a preguntar sobre la filtración y exigir la destitución de Hammouchi.

6. **"Regalo a Europa y especialmente a España"**: El framing está diseñado para maximizar el impacto diplomático.

### 4.5. Teaser Pegasus / Pedro Sánchez

El **24 de agosto de 2026**, Jabaroot publicó en Telegram un mensaje:

> *"¿A quién le interesan los datos originales de Pegasus relacionados con Pedro Sánchez?"*

**Detalles clave:**
- El mensaje apareció en un canal con **813 suscriptores**.
- **No se incluyeron documentos, muestras ni metadatos**.
- **No se precisó** qué datos conserva, cómo los habría obtenido o qué condiciones impondría para entregarlos.
- El teaser golpea el punto más oscuro del mayor episodio conocido de espionaje contra la cúpula del Estado español.
- La Audiencia Nacional archivó la investigación en **enero de 2026** por falta de cooperación de Israel.
- **Estado actual:** Sin materialización. Permanece como una amenaza no verificada.

### 4.6. Cronología Precisa de la Operación (Canal @jabaroot_off)

| Fecha/Hora | ID | Contenido |
|------------|-----|-----------|
| 21-08-2026 23:37 | /1 | Canal creado |
| 21-08-2026 23:38 | /2 | Foto del canal actualizada |
| 22-08-2026 10:45 | /3 | "Hemos vuelto" (لقد عدنا) |
| 23-08-2026 09:59 | /4-5 | Anuncio filtración RAMED (1M de 17M) |
| 24-08-2026 10:17 | /6-7 | Anuncio filtración DGST/DGSN + enlace a darkforums.ru |
| 24-08-2026 10:22 | /8-9 | "El gran regalo a Europa y especialmente a España" + 70.000 agentes |
| 24-08-2026 19:59 | /10-11 | Teaser Pegasus / Pedro Sánchez |
| 24-08-2026 20:15 | /12-13 | Mensaje a la prensa marroquí |
| 24-08-2026 20:25 | /14 | "Few next hours... Tic-tac..." |
| 24-08-2026 21:04 | /15 | Anuncio de eliminación de archivos de Telegram → darkforums.ru |
| 24-08-2026 21:40 | /16 | "...En cuanto a las súplicas de los oprimidos... no se van en vano..." |

---

## 5. Análisis Técnico y de Autenticidad de los Datos

### 5.1. Análisis de Muestras del Dump de 70.000

| Observación | Detalle | Implicación |
|-------------|---------|-------------|
| **Duplicados** | 26 filas analizadas, 1 duplicado exacto | Posible mala calidad o mezcla de bases |
| **Campos incompletos** | Campos de rango vacíos en la mayoría | No coincide con perfil completo esperado de agentes de inteligencia |
| **Fechas genéricas** | Varias fechas de nacimiento "1 de enero" | Podrían provenir de bases de datos civiles previas |
| **Validación cruzada** | Ningún individuo confirmado de forma independiente como DGST/DGSN | Duda sobre la autenticidad total del dataset |
| **Antigüedad** | Posiblemente obtenidos tiempo atrás y publicados ahora | Los datos podrían no ser operativos actualmente |

### 5.2. Comparativa con Históricos

| Filtración | Credibilidad | Estado |
|------------|--------------|--------|
| **CNSS (2025)** | **Alta** | Verificada por CybelAngel, INCIBE y múltiples fuentes |
| **ANCFCC (2025)** | **Media** | Cuestionada por usuarios de DarkForums; muestras verificadas pero no el dataset completo |
| **Palacios reales** | **Media-alta** | Validación parcial |
| **FRMF (2026)** | **Media** | Reivindicada, en contexto de conflicto con Dark 07x |
| **DGST/DGSN 70k (2026)** | **Media (parcial)** | Validada por exagentes y CNI; pendiente de análisis forense completo |

### 5.3. Infraestructura Utilizada

| Componente | Detalle |
|------------|---------|
| **Canal principal** | Telegram `@jabaroot_off` (activo, abierto) |
| **Canales históricos** | `@JabarootDZ` (original, eliminado), `@jabarootdz2` (creado tras eliminación) |
| **Foro principal** | DarkForums.ru (foro de leaks en inglés, no ruso) |
| **Foros históricos** | BreachForums (primeras publicaciones de CNSS) |
| **Plataformas de compartición** | Servicios de intercambio de archivos (muestras eliminadas por los servicios) |
| **Sin evidencia de foros rusos** | No se ha encontrado actividad en XSS, Exploit, RAMP u otros foros rusos principales |

---

## 6. Análisis de Motivaciones e Hipótesis Estratégicas

### 6.1. Matriz de Intereses del Actor

| Interés | Evidencia | Probabilidad |
|---------|-----------|--------------|
| **Desestabilización política** | Narrativa anti-Hammouchi, exigencia de destitución, llamada a luto nacional y suspensión de elecciones | **Alta** |
| **Daño a la imagen internacional de Marruecos** | Exposición de agentes, acusación de plan migratorio, "regalo a España" | **Alta** |
| **Presión diplomática España-Marruecos** | Framing "regalo a España", teaser Pegasus en momento de máxima tensión | **Media-alta** |
| **Revancha nacionalista argelina** | Autoidentificación como argelinos, timing con tensiones regionales por Sáhara | **Media-alta** |
| **Beneficio comercial** (venta de datos) | Patrón de dumps en foros de leaks, posible reventa de datasets | **Media** |
| **Guerra de clanes interna marroquí** | Exposición selectiva de altos cargos, exoneración del rey | **Baja-media** |

### 6.2. Hipótesis de Motivación Profunda

**Hipótesis 1: Hacktivismo genuino anti-Makhzen / pro-Argelia**
- La más coherente con la narrativa pública del actor.
- El timing de las operaciones coincide con tensiones diplomáticas.
- La elección de objetivos (CNSS, ANCFCC, DGST, DGSN) sugiere un conocimiento profundo del aparato estatal marroquí.
- **Confianza: Media-alta**

**Hipótesis 2: Operación de información (info-ops) con objetivo de desestabilización**
- La narrativa está cuidadosamente construida para maximizar el daño diplomático.
- La exoneración del rey y el enfoque en Hammouchi sugiere un intento de generar una crisis de sucesión o de confianza en el aparato de seguridad.
- El teaser de Pegasus está diseñado para reabrir heridas diplomáticas con España.
- **Confianza: Media-alta**

**Hipótesis 3: Actor comercial / data broker con reutilización de datos**
- El patrón de publicar en foros de leaks y mover archivos a plataformas como DarkForums es consistente con actores que monetizan datos.
- La posible antigüedad de los datos (obtenidos tiempo atrás) sugiere reventa o reempaquetado.
- **Confianza: Media**

**Hipótesis 4: Brand hijacking por actores oportunistas**
- Las inconsistencias técnicas en el dump de 70k (duplicados, campos genéricos) sugieren que podría no ser el Jabaroot original.
- La proliferación de canales con el nombre "Jabaroot" después de eliminaciones dificulta la atribución.
- **Confianza: Media**

---

## 7. Tácticas, Técnicas y Procedimientos (TTPs)

| Categoría | Observaciones |
|-----------|---------------|
| **Vector de acceso** | No documentado públicamente. Especulación: zero-day o compromiso vía software de terceros (posiblemente Oracle) |
| **Exfiltración** | Dumps masivos de bases de datos administrativas y de personal (CNSS, ANCFCC, DGST, DGSN, RAMED) |
| **Difusión primaria** | Telegram (múltiples canales, recreados tras cierres) |
| **Difusión secundaria** | Foros de leaks (BreachForums inicialmente, DarkForums.ru actualmente) |
| **Narrativa** | Mezcla de datos reales con acusaciones políticas y amenazas escalonadas |
| **OPSEC** | Fallo inicial (forward desde cuenta personal 3N16M4); posteriormente mejorado |
| **Resiliencia** | Recreación de canales tras cierres de Telegram |
| **Tooling** | Sin detalles técnicos específicos documentados públicamente |
| **Táctica de presión** | Amenazas escalonadas con deadlines ("Few next hours...") |
| **Estrategia de comunicación** | Uso de múltiples idiomas (árabe, español, inglés, francés) para maximizar audiencia |

---

## 8. Modelo de Diamante del Actor

| Componente | Descripción |
|------------|-------------|
| **Adversario** | Jabaroot (posiblemente un colectivo o individuo con múltiples alias) |
| **Capacidad** | Exfiltración de bases de datos masivas, OSINT, info-ops, defacement de sitios web |
| **Infraestructura** | Telegram, DarkForums.ru, BreachForums, servicios de intercambio de archivos |
| **Víctima** | Estado marroquí (DGST, DGSN, CNSS, ANCFCC, RAMED, FRMF, palacios reales, Ministerio de Justicia, etc.) |
| **Objetivos estratégicos** | Desestabilización, exposición de corrupción, presión geopolítica, posible beneficio comercial |
| **Relación con el adversario** | No confirmado; posible origen argelino, tunecino o brand hijacking |

---

## 9. Evaluación de Riesgos e Impacto

### 9.1. Matriz de Impacto por Dimensión

| Dimensión | Impacto | Nivel | Detalles |
|-----------|---------|-------|----------|
| **Seguridad nacional (Marruecos)** | **Crítico** | 5/5 | Exposición de 70.000 agentes de inteligencia y seguridad, sus métodos y posiblemente sus operaciones en Europa |
| **Operacional (agentes expuestos)** | **Crítico** | 5/5 | Doxxing masivo, riesgo de chantaje, compromiso de misiones encubiertas, especialmente los que operan en España |
| **Diplomático (España-Marruecos)** | **Alto** | 4/5 | Acusación de plan migratorio oficial, tensión en el contexto de Ceuta, posible reapertura del caso Pegasus |
| **Institucional (gobierno marroquí)** | **Alto** | 4/5 | Desafío directo a Hammouchi y Lekjaa, presión para destituciones, erosión de confianza en el aparato de seguridad |
| **Privacidad de datos (ciudadanos)** | **Alto** | 4/5 | Exposición de datos sanitarios (1M+ personas) y datos de seguridad social (~2M personas), riesgo de fraude y suplantación |
| **Informacional (narrativa pública)** | **Medio-alto** | 3/5 | Amplificación de la narrativa anti-Marruecos, desinformación sobre el origen de la crisis migratoria |
| **Económico** | **Medio** | 3/5 | Posible uso de datos bancarios (RIB) para fraudes, impacto en la confianza inversora |

### 9.2. Escenarios de Evolución

#### Escenario A: Materialización de la amenaza Pegasus
- Jabaroot publica datos reales del espionaje a Pedro Sánchez.
- **Impacto:** Crisis diplomática abierta entre España y Marruecos, reapertura del caso judicial en España.
- **Probabilidad:** **Baja** (sin muestras ni metadatos hasta ahora).

#### Escenario B: Lista específica de coordinadores de Ceuta
- Publicación de nombres y órdenes de misión de los agentes que coordinaron la operación de Ceuta.
- **Impacto:** Exposición operativa de agentes, posible detención en España, crisis institucional en Marruecos.
- **Probabilidad:** **Media** (el actor lo ha prometido explícitamente).

#### Escenario C: Publicación completa de los 17M de RAMED
- Filtración masiva de datos sanitarios de toda la población marroquí.
- **Impacto:** Riesgo de fraude masivo, suplantación de identidad, erosión de confianza en el sistema sanitario.
- **Probabilidad:** **Media-alta** (el actor ya ha publicado 1M y tiene historial de cumplir promesas).

#### Escenario D: Brand hijacking confirmado
- Se demuestra que el actor actual no es el Jabaroot original.
- **Impacto:** Reducción de la credibilidad de la filtración, pero la exposición de datos parciales sigue siendo real.
- **Probabilidad:** **Media** (según análisis de Golden Owl).

#### Escenario E: Escalada a ciberataques directos
- Ampliación del conflicto cibernético con actores pro-marroquíes (Dark 07x).
- **Impacto:** Daños a infraestructuras críticas en ambos países.
- **Probabilidad:** **Media-baja** (ya ha ocurrido en contexto deportivo).

#### Escenario F: Acción de contra-inteligencia marroquí
- Marruecos toma medidas legales o técnicas para cerrar canales y mitigar el daño.
- **Impacto:** Posible cierre del canal, pero los datos ya están en darkforums.
- **Probabilidad:** **Alta** (ya se ha solicitado a Telegram, aunque sin éxito hasta ahora).

### 9.3. Niveles de Confianza y Probabilidad

| Evento | Probabilidad | Impacto | Riesgo global |
|--------|--------------|---------|---------------|
| Publicación de lista de coordinadores de Ceuta | **Media** | Crítico | **Alto** |
| Publicación de datos Pegasus de Sánchez | **Baja** | Crítico | **Medio** |
| Publicación completa de RAMED (17M) | **Media-alta** | Alto | **Alto** |
| Cierre del canal por parte de Telegram | **Alta** | Bajo | **Bajo** |
| Confirmación de brand hijacking | **Media** | Medio | **Medio** |
| Escalada a ciberataques directos | **Media-baja** | Medio | **Medio** |

### 9.4. Análisis de Vulnerabilidades Expuestas

| Vulnerabilidad | Descripción | Riesgo |
|----------------|-------------|--------|
| **Exposición de agentes encubiertos** | Agentes que operan en Europa (especialmente España) ahora tienen identidades públicas | **Crítico** |
| **Compromiso de métodos operativos** | Conocimiento público de tácticas de espionaje (escuchas, sobornos) | **Alto** |
| **Riesgo de chantaje** | Agentes expuestos pueden ser objeto de presión por servicios de inteligencia rivales | **Alto** |
| **Fraude financiero** | Datos bancarios (RIB) de 1.400 agentes expuestos | **Medio** |
| **Suplantación de identidad** | Datos de 2M+ ciudadanos expuestos (CNSS) + 1M (RAMED) | **Alto** |

---

## 10. Recomendaciones Estratégicas y Tácticas

### 10.1. Para Equipos de Seguridad / CTI

1. **Monitoreo continuo** de `@jabaroot_off` y variantes en Telegram.
2. **Vigilancia activa de DarkForums.ru** para detectar nuevas publicaciones del actor.
3. **Análisis forense de samples** del dump de 70k (campos, duplicados, fechas, cruce con filtraciones previas).
4. **Actualización de la pista 3N16M4/Mzannar** (perfiles de GitHub, LinkedIn, actividad reciente en foros).
5. **Mapeo de posibles beneficiarios** de la inestabilidad geopolítica (Argelia, actores pro-rusos, facciones internas).
6. **Cross-check de los nombres filtrados** con fuentes abiertas (prensa, redes, registros públicos) para validar autenticidad.
7. **Análisis de la cadena de custodia** de los datos para determinar si son actuales o históricos.

### 10.2. Para las Instituciones Afectadas (DGST, DGSN, Gobierno Marroquí)

1. **Evaluación de impacto** sobre el personal expuesto (especialmente los de alto rango y los que operan en Europa).
2. **Medidas de mitigación** inmediatas:
   - Cambio de identificadores operativos.
   - Protección de cuentas bancarias (RIB).
   - Notificación a los agentes expuestos y refuerzo de su seguridad personal.
   - Evaluación de la necesidad de reubicación de agentes comprometidos.
3. **Revisión de protocolos de seguridad internos** para identificar el vector de compromiso.
4. **Coordinación con España** para evaluar el riesgo sobre los agentes que operan en territorio español.
5. **Estrategia de comunicación** para contrarrestar la narrativa del actor sin darle más visibilidad.
6. **Investigación interna** para determinar si existe un insider o filtración desde dentro del sistema.

### 10.3. Para el Gobierno de España

1. **Evaluación de la amenaza Pegasus**: verificar si Jabaroot tiene acceso real a datos del espionaje a Pedro Sánchez.
2. **Coordinación con el CNI** para el análisis de los nombres de agentes filtrados que hayan operado en España.
3. **Preparación de un plan de comunicación** en caso de que se publique la lista de coordinadores de Ceuta.
4. **Refuerzo de la vigilancia** en la frontera de Ceuta y Melilla ante posibles movimientos migratorios instrumentados.
5. **Evaluación de riesgos** para políticos y empresarios españoles que pudieran haber sido objeto de las operaciones de inteligencia expuestas.

### 10.4. Para la Comunidad de Inteligencia y OSINT

1. **Compartir indicadores** (handles, hashes de archivos, patrones de mensajes) en plataformas de colaboración (MISP, etc.).
2. **Realizar un análisis de sentimiento** de la audiencia del canal para medir el alcance y la efectividad de la narrativa.
3. **Profundizar en la investigación de DarkForums.ru**: determinar si el foro tiene vínculos con otros actores o foros.
4. **Investigar la posible venta previa** de los datasets en el mercado negro.
5. **Monitorear la actividad de Rachid Mzannar** en plataformas técnicas y redes sociales.

---

## 11. Preguntas Abiertas y Líneas de Investigación Pendientes

1. **¿El dump de 70.000 es auténtico o contiene datos mezclados de bases civiles anteriores?**
2. **¿Quién está realmente detrás de la operación actual: el Jabaroot original o imitadores?**
3. **¿Tiene Jabaroot acceso real a datos de Pegasus o es un señuelo para atraer atención mediática?**
4. **¿Cuál es el vector de acceso inicial que permitió la exfiltración de estos datos?**
5. **¿Existen miembros de Jabaroot en foros rusos?** (Requiere OSINT privado)
6. **¿Se han vendido previamente estos datos en el mercado negro?**
7. **¿Qué papel juega Argelia en esta operación? ¿Es un proxy o solo un marco narrativo?**
8. **¿Puede Marruecos identificar y detener al actor antes de nuevas filtraciones?**
9. **¿Por qué se exime al rey y se enfoca exclusivamente en Hammouchi y El Himma?**
10. **¿Qué relación tiene la operación actual con el conflicto cibernético con Dark 07x?**

---

## 12. Conclusión

Jabaroot es un actor de amenazas **creíble y persistente** con un historial documentado de filtraciones de alto impacto contra instituciones marroquíes. La operación de agosto de 2026 constituye la **mayor brecha de seguridad** enfrentada por el aparato de seguridad marroquí en la última década.

El canal `@jabaroot_off` sigue abierto, lo que indica que la operación **está en curso** y que el actor mantiene su capacidad de difusión y escalada.

**Evaluación de riesgo global:** **CRÍTICO** para Marruecos, **ALTO** para las relaciones España-Marruecos.

La atribución sigue siendo **incierta**, con cuatro hipótesis principales:
1. **Actor argelino nacionalista** (narrativa auto-reivindicada y consistente).
2. **Brand hijacking** por actores oportunistas (explica inconsistencias técnicas del dump actual).
3. **Insider marroquí o facción interna** (explica la sensibilidad y volumen de los datos).
4. **Actor comercial** reutilizando datos obtenidos previamente.

La pista OSINT de Rachid Mzannar (3N16M4) sigue siendo la única atribución nominal concreta, aunque con **confianza baja-media** y sin confirmación de que siga activo en 2026.

Se recomienda una **respuesta coordinada** entre los servicios de inteligencia de España y Marruecos, junto con un **monitoreo activo** de las plataformas del actor y la preparación de planes de contingencia para los escenarios de mayor riesgo (lista de coordinadores de Ceuta, datos Pegasus, publicación completa de RAMED).

---

## 13. Anexos: Fuentes y Referencias

| Fuente | Descripción |
|--------|-------------|
| Yahoo Noticias / Euronews | Amenaza de filtración de 70.000 espías |
| El Faro de Ceuta | Filtración de datos de 70.000 agentes |
| El Nacional | Exposición de espías marroquíes en España |
| Estrella Digital | Teaser Pegasus / Pedro Sánchez |
| El Confidencial | "Regalo a España" - filtración de 70.000 agentes |
| INCIBE | Análisis del leak de CNSS |
| CybelAngel | Investigación del leak de CNSS y ANCFCC |
| Breaches.Africa | Publicación en DarkForums del dump de 70k |
| SecRSS | Análisis del fallo OPSEC de 3N16M4 |
| Yabiladi | Pista sobre el estudiante tunecino en Alemania |

---

**Fin del informe 1**

---

**INFORME DE INTELIGENCIA DE AMENAZAS (CTI) – VERSIÓN 2.1**
**Complemento y profundización al Informe 2 (25 de agosto de 2026)**

**Actor:** Jabaroot (alias JabaROOT, Jabaroot DZ, JabaRoot DZ)
**Fecha de elaboración:** 25 de agosto de 2026
**Clasificación:** TLP:WHITE / Fuentes abiertas exclusivamente
**Estado del actor:** Activo – canal @jabaroot_off operativo; archivos trasladados a darkforums.ru
**Versión:** 2.1 – Ampliación de capas pendientes con fuentes abiertas adicionales

---

## 1. Propósito de este documento

Este informe es una **ampliación del Informe 2**, no un reemplazo. Su objetivo es desarrollar las capas de análisis que el Informe 2 identificó como pendientes o insuficientemente cubiertas, utilizando fuentes abiertas disponibles al 25 de agosto de 2026.

---

## 2. Análisis de la "Segunda Lista" de 1.400 RIB – Profundización

### 2.1. Estructura y contenido de la lista secundaria

La segunda lista, que acompaña al *dump* principal de 70.000 registros, contiene **grados dentro de los cuerpos y números de identificación bancaria (RIB) de aproximadamente 1.400 personas**. Esta lista ha sido descrita por múltiples fuentes como un subconjunto selectivo del *dataset* principal, aparentemente correspondiente a personal de mayor rango o con acceso a cuentas bancarias institucionales.

### 2.2. Formato y consistencia de los RIB

Los números de identificación bancaria filtrados siguen el **formato marroquí estándar** (20-24 dígitos), que incluye:
- Código del banco (3 dígitos)
- Código de la ciudad/sucursal (3 dígitos)
- Número de cuenta (hasta 16 dígitos)
- Clave de control (2 dígitos)

**No se ha publicado en fuentes abiertas** un análisis que confirme si todos los RIB corresponden a una misma entidad bancaria o si hay consistencia en los patrones. Tampoco se ha verificado de forma independiente que los números de cuenta sean activos o correspondan realmente a los agentes nombrados.

### 2.3. Riesgo de fraude y explotación

El riesgo de uso fraudulento de los RIB existe, aunque **no hay reportes públicos de explotación masiva** al 25 de agosto de 2026. Los RIB, combinados con los nombres completos y números de identificación de la lista principal, podrían ser utilizados para:

- **Suplantación de identidad** en transacciones bancarias.
- **Phishing dirigido** contra los agentes expuestos.
- **Intento de acceso a cuentas** mediante ingeniería social.

La exposición de datos bancarios de personal de inteligencia y seguridad representa una vulnerabilidad operacional significativa, especialmente si los agentes afectados mantienen cuentas activas en las mismas entidades.

---

## 3. Análisis de la Narrativa y Desinformación

### 3.1. Estructura de la narrativa de Jabaroot

El actor ha construido una narrativa coherente y escalonada:

| Fase | Mensaje | Objetivo |
|------|---------|----------|
| **Preparación** | Amenazas previas (7-20 agosto) | Generar expectación y atención mediática |
| **Presentación** | "El gran regalo a Europa, y especialmente a España" | Enmarcar la filtración como un acto de generosidad hacia España |
| **Contenido** | Exposición de 70.000 agentes y sus operaciones en Europa | Dañar la credibilidad del aparato de seguridad marroquí |
| **Acusación** | Señalamiento a Hammouchi y El Himma como responsables de Ceuta | Generar crisis institucional en Marruecos |
| **Escalada** | Teaser de Pegasus / Pedro Sánchez | Atraer atención española y reabrir heridas diplomáticas |
| **Futuro** | Promesa de lista de coordinadores de Ceuta | Mantener presión y expectación |

### 3.2. Amplificación en medios y redes

La filtración ha sido amplificada por **múltiples medios españoles** (El Confidencial, El Debate, El Mundo, laSexta, Onda Cero, Telecinco, COPE, entre otros), así como por medios internacionales. La narrativa del "regalo a España" ha sido recogida de forma acrítica en muchos casos, lo que sugiere que el actor ha logrado su objetivo de **penetrar el discurso público** y generar tensión diplomática.

### 3.3. Desinformación y bulos en el contexto de Ceuta

La crisis migratoria de Ceuta (30 de julio de 2026) fue precedida por una **campaña de desinformación** que incluyó bulos, vídeos manipulados y una sentencia mal interpretada que empujó a miles de personas hacia la frontera. Jabaroot ha **instrumentalizado** este contexto, presentando su filtración como una "prueba" de que la crisis fue planificada por el Estado marroquí.

**No existe evidencia pública** que vincule directamente a Jabaroot con la campaña de desinformación previa a la crisis de Ceuta, pero el grupo ha sabido **montarse sobre** el ambiente de tensión y desconfianza generado por aquellos eventos.

---

## 4. Análisis del Impacto Económico en Marruecos

### 4.1. Impacto en el sistema financiero

La filtración de **RIB de 1.400 agentes** expone una vulnerabilidad en el sistema bancario marroquí. Si bien no hay reportes de fraudes consumados, el riesgo de **phishing dirigido** y **suplantación de identidad** es real. Las entidades bancarias afectadas podrían verse obligadas a:

- Emitir nuevos números de cuenta para los agentes expuestos.
- Reforzar los protocolos de verificación de identidad.
- Asumir costes de litigios si se producen fraudes.

### 4.2. Coste de la respuesta de ciberseguridad

El gobierno marroquí ya ha tenido que responder a filtraciones anteriores (CNSS, ANCFCC, palacios reales). La filtración de 70.000 agentes de inteligencia y seguridad **eleva el coste acumulado** de la respuesta de ciberseguridad a niveles sin precedentes. Las partidas afectadas incluyen:

- Auditorías de sistemas comprometidos.
- Refuerzo de infraestructuras de seguridad.
- Cambio de identificadores y credenciales del personal expuesto.
- Asesoramiento legal y de comunicación de crisis.

### 4.3. Confianza inversora y turismo

Aunque no se ha cuantificado oficialmente, la percepción de **inestabilidad institucional** y **vulnerabilidad cibernética** puede afectar la confianza de los inversores extranjeros en Marruecos. El sector turístico, especialmente en regiones como Tánger y la costa mediterránea, podría verse afectado si la crisis diplomática con España se intensifica.

---

## 5. Análisis de la Respuesta de Telegram

### 5.1. Historial de cierres de canales de Jabaroot

Jabaroot ha operado a través de **múltiples canales de Telegram** que han sido cerrados tras las filtraciones. El canal original (`@JabarootDZ`) fue eliminado, y se han creado sucesivas versiones. **Estrella Digital** señala que "distintas cuentas han utilizado el nombre de Jabaroot después del cierre de canales anteriores". El propio El Confidencial confirma que el grupo "fue proscrito de la red social Telegram (donde publicaba hasta entonces sus comunicados), presumiblemente a petición de Rabat".

### 5.2. ¿Por qué `@jabaroot_off` sigue abierto?

El canal actual `@jabaroot_off` **permanece abierto y operativo** al 25 de agosto de 2026. Las razones posibles incluyen:

1. **Cambio de estrategia del actor**: Jabaroot ha eliminado los archivos de Telegram y los ha movido a DarkForums, lo que reduce el riesgo de que el canal sea cerrado por violación de políticas de contenido.
2. **Respuesta más lenta de Telegram**: La plataforma puede estar procesando la solicitud de cierre de manera más lenta que en ocasiones anteriores.
3. **Uso de nuevas cuentas o proxies**: El actor podría estar utilizando cuentas verificadas o medidas para evitar la detección automática.

### 5.3. Implicaciones para la monitorización

El hecho de que el canal siga abierto indica que **la operación de comunicación del actor no ha sido interrumpida**. Esto permite a Jabaroot continuar difundiendo mensajes, amenazas y posiblemente nuevas filtraciones. La capacidad del actor para **recrear canales** tras cada cierre sugiere un alto nivel de preparación y recursos.

---

## 6. Escenarios Geopolíticos – Profundización

### 6.1. Escenario A: Publicación de la lista de coordinadores de Ceuta

Jabaroot ha prometido publicar una lista específica con los nombres de los agentes que "orquestaron y coordinaron el plan de Ceuta". El grupo afirma haber obtenido copias de las órdenes de misión de agentes desplazados a Fnideq (Castillejos) antes y durante los eventos.

**Impacto potencial:**
- **Exposición operativa** de agentes clave, incluyendo sus roles específicos en la crisis.
- **Posibles detenciones o solicitudes de extradición** por parte de España si se identifican agentes que operaron en territorio español.
- **Crisis institucional** en Marruecos si se confirma la implicación de altos cargos en la planificación de la entrada masiva.
- **Presión sobre Hammouchi y El Himma**, que ya han sido señalados públicamente por el grupo.

**Probabilidad: Media** (el actor ha cumplido amenazas previas y tiene historial de publicación).

### 6.2. Escenario B: Materialización de los datos Pegasus

El teaser de Jabaroot sobre "datos originales de Pegasus relacionados con Pedro Sánchez" no ha sido acompañado de pruebas. Sin embargo, el mero anuncio ha generado atención mediática significativa.

**Impacto potencial:**
- **Reapertura del caso Pegasus** en la Audiencia Nacional, que archivó la investigación en enero de 2026 por falta de cooperación de Israel.
- **Crisis diplomática aguda** entre España y Marruecos si se confirma que los datos proceden de la operación de espionaje.
- **Presión política** sobre el gobierno español para que investigue y actúe.

**Probabilidad: Baja** (sin muestras ni metadatos hasta el momento).

### 6.3. Escenario C: Confirmación de responsabilidad argelina

Si se confirma que Jabaroot es un proxy o está vinculado a Argelia, las consecuencias geopolíticas serían graves:
- **Deterioro adicional de las relaciones Argelia-Marruecos**.
- **Posible ruptura de relaciones diplomáticas**.
- **Escalada del conflicto** en el Sáhara Occidental.
- **Impacto en los acuerdos comerciales y de pesca** entre ambos países.

**Probabilidad: Media** (según la narrativa de Rabat y la autoidentificación del grupo).

### 6.4. Escenario D: Brand hijacking confirmado

Si se demuestra que el actor actual no es el Jabaroot original, el impacto sería:
- **Reducción de la credibilidad de la filtración**, pero la exposición de datos parciales seguiría siendo real.
- **Dificultad para atribuir responsabilidades** y tomar medidas legales.
- **Posible desmovilización de la atención mediática**.

**Probabilidad: Media** (según el análisis de Golden Owl y las inconsistencias técnicas del dump).

---

## 7. Análisis de Contra-Inteligencia y Medidas Proactivas

### 7.1. Acciones conocidas de Marruecos

Marruecos ha tomado medidas para mitigar el impacto de las filtraciones de Jabaroot:

- **Solicitudes a Telegram** para el cierre de canales, que han sido efectivas en el pasado.
- **Atribución habitual a Argelia**, sin pruebas técnicas publicadas.
- **Nombramiento de un nuevo responsable de ciberseguridad** (DGSSI) tras las filtraciones de 2025.

**No hay información pública** sobre:
- Cambio de identificadores de los agentes expuestos.
- Detenciones relacionadas con esta filtración.
- Investigaciones internas en la DGST o DGSN.

### 7.2. Posibles medidas de contra-inteligencia

Las siguientes medidas podrían estar siendo implementadas por los servicios de inteligencia marroquíes y españoles:

- **Operaciones de ingeniería social inversa**: intentar infiltrarse en los canales de Jabaroot o en DarkForums para obtener información sobre el actor.
- **Monitoreo de foros y redes** para identificar posibles miembros o colaboradores.
- **Análisis de tráfico y metadatos** para geolocalizar al actor.
- **Cooperación internacional** con servicios de inteligencia aliados (CIA, DGSE, CNI).

### 7.3. Limitaciones de las medidas de contra-inteligencia

La naturaleza **anónima y descentralizada** de Jabaroot (múltiples canales, posibles imitadores, uso de foros rusos) dificulta las operaciones de contra-inteligencia. La migración de archivos a DarkForums y la eliminación de archivos de Telegram complican aún más la identificación del actor.

---

## 8. Análisis de la Audiencia y Alcance

### 8.1. Suscriptores del canal Telegram

El canal `@jabaroot_off` tenía **813 suscriptores** en el momento en que se publicó el mensaje de Pegasus. Otros canales asociados a Jabaroot han alcanzado cifras variables:

- Un canal identificado como `Jabaroot Dz` tenía **7.43K suscriptores**.
- Otro canal bajo el nombre `Jabaroot` alcanzaba los **25.6K suscriptores**.

Estas cifras indican que la audiencia del actor es **significativa pero no masiva** en términos absolutos. Sin embargo, el **alcance mediático** de la filtración ha sido mucho mayor, con decenas de artículos en medios españoles, marroquíes, franceses y argelinos.

### 8.2. Perfiles de la audiencia

La audiencia de Jabaroot incluye:
- **Periodistas y medios de comunicación** (especialmente españoles y marroquíes).
- **Investigadores de OSINT y ciberseguridad**.
- **Nacionalistas argelinos y activistas anti-Makhzen**.
- **Políticos y analistas** interesados en la crisis de Ceuta.
- **Curiosos y seguidores** de filtraciones de datos.

### 8.3. Alcance en medios

La filtración ha sido cubierta por:
- **Medios españoles**: El Confidencial, El Debate, El Mundo, laSexta, Onda Cero, Telecinco, COPE, ElDiario.es, Infobae, Estrella Digital, entre otros.
- **Medios marroquíes**: cobertura limitada y con atribución a Argelia.
- **Medios internacionales**: Yahoo Noticias, Euronews, TSA Algérie, Mondafrique.

---

## 9. Análisis de la Posible Venta de Datos

### 9.1. Evidencia de venta en foros

El análisis de **breaches.africa** confirma que Jabaroot publicó la base de datos de 70.000 registros en DarkForums el 24 de agosto de 2026, vinculada a la operación `OP_CEUTA`. Sin embargo, **no hay evidencia pública** de que los datos se estén ofreciendo en venta en los mercados habituales del *dark web*.

### 9.2. Patrón de comportamiento del actor

El patrón de Jabaroot consiste en:
- **Publicar muestras** en Telegram.
- **Mover los archivos completos** a foros como DarkForums.
- **No vender los datos públicamente** en los mercados habituales.

Este comportamiento es más consistente con un **actor hacktivista** que con un **data broker comercial**. Sin embargo, no se puede descartar que los datos se estén vendiendo de forma privada o que se utilicen para otros fines (chantaje, presión política, etc.).

### 9.3. Posible reutilización de datos

Algunos analistas, como **Rafael López** (entrevistado por ElDiario.es), señalan que "en el archivo que han publicado sobre Marruecos parece que puede haber datos que ya habían hecho públicos las instituciones marroquíes y refritos de otras filtraciones antiguas". Esto sugiere que parte del *dump* podría ser una **reutilización de datos obtenidos previamente**, lo que reduciría su valor comercial y su autenticidad.

---

## 10. Evolución del Actor – Análisis Actualizado

### 10.1. Trayectoria desde abril de 2025

| Fase | Periodo | Características |
|------|---------|-----------------|
| **Emergencia** | Abril 2025 | Primer gran *dump* (CNSS), fallo de OPSEC (3N16M4) |
| **Expansión** | Junio-diciembre 2025 | ANCFCC, palacios reales, Ministerio de Justicia |
| **Consolidación** | Enero-julio 2026 | FRMF, conflicto con Dark 07x, preparación de operación Ceuta |
| **Operación actual** | Agosto 2026 | *Dump* de 70.000 agentes, teaser Pegasus, migración a DarkForums |

### 10.2. Mejora de OPSEC

Tras el fallo de OPSEC de abril de 2025 (exposición de `3N16M4`), el actor ha mejorado sus medidas de seguridad:
- **Uso de múltiples canales** y recreación tras cierres.
- **Eliminación rápida de archivos** de Telegram.
- **Migración a foros** (DarkForums) para evitar el bloqueo.

Sin embargo, la **posible brand hijacking** y las inconsistencias técnicas del *dump* actual sugieren que el control de la marca puede estar fragmentado.

### 10.3. Cambios en la narrativa

La narrativa de Jabaroot ha evolucionado desde un **discurso genérico anti-Makhzen** hasta una **acusación específica contra Hammouchi y El Himma**, con un enfoque creciente en la **dimensión geopolítica** (Ceuta, España, Pegasus). La exoneración del rey es un elemento constante.

---

## 11. Recomendaciones Actualizadas y Priorizadas

### 11.1. Inmediatas (24-48 horas)

1. **Monitoreo intensivo** de `@jabaroot_off` y DarkForums para detectar nuevas publicaciones.
2. **Notificación a los agentes expuestos** (especialmente los de la lista secundaria de 1.400 con RIB).
3. **Contacto discreto España-Marruecos** para evaluar el riesgo sobre agentes que operaron en territorio español.
4. **Solicitud formal a Telegram** para el cierre del canal `@jabaroot_off`.

### 11.2. Corto plazo (1 semana)

1. **Auditoría de sistemas de personal** en la DGST, DGSN y otras agencias afectadas.
2. **Análisis forense de las muestras disponibles** (hashes, estructura, antigüedad).
3. **Verificación cruzada de los RIB** con entidades bancarias marroquíes.
4. **Actualización de la pista Mzannar** y búsqueda de nuevos handles.

### 11.3. Medio plazo (1 mes)

1. **Revisión de protocolos de seguridad de la información** en todas las agencias gubernamentales.
2. **Plan de comunicación de crisis** para contrarrestar la narrativa del actor.
3. **Evaluación de impacto en la cooperación bilateral** (antiterrorismo, inmigración, narcotráfico).
4. **Medidas de protección** para los agentes expuestos (cambio de identificadores, cuentas bancarias).

### 11.4. Indicadores de Compromiso (IOCs) públicos

| Tipo | Valor |
|------|-------|
| **Canal Telegram** | @jabaroot_off |
| **Foro** | darkforums.ru (thread #OP_CEUTA, usuario JBT2026) |
| **Handles históricos** | @JabarootDZ, 3N16M4 |
| **Patrones de mensaje** | "gran regalo a Europa y especialmente a España", "Few next hours… Tic-tac…", "¿A quién le interesan los datos originales de Pegasus relacionados con Pedro Sánchez?" |
| **Hashes de archivos** | No publicados en fuentes abiertas completas |

---

## 12. Puntos que permanecen sin resolver (fuentes abiertas)

Los siguientes elementos no pueden desarrollarse más allá de lo expuesto por falta de acceso a datos cerrados, dumps completos o información clasificada:

- Análisis estadístico completo de las 70.000 filas (porcentaje real de duplicados, correlación año de reclutamiento-rango, etc.).
- Verificación cruzada nominal masiva con LinkedIn, listas de egresados o registros públicos.
- Metadatos completos de archivos PDF/CSV y marcas de agua.
- Confirmación de banco concreto o consistencia total de los RIB de la lista de 1.400.
- Actividad reciente verificable de Rachid Mzannar (viajes, cambio de empleo, etc.).
- Entrevistas con fuentes humanas (exagentes, periodistas especializados).
- Prueba técnica del vector de ataque inicial.
- Informes compartidos en MISP u otras plataformas de intel sharing.
- Detalles internos de la respuesta de Marruecos (investigaciones, detenciones, cambios de identificadores).
- Hashes completos de los archivos filtrados.

---

## 13. Conclusión del Informe 2.1

Este documento amplía el Informe 2 con **nuevas capas de análisis** basadas en fuentes abiertas adicionales. La amenaza de Jabaroot sigue siendo **crítica para Marruecos** y **alta para las relaciones bilaterales con España**. La operación está en curso, y el actor mantiene su capacidad de difusión y escalada a través de `@jabaroot_off` y DarkForums.

La **posible brand hijacking** y las **inconsistencias técnicas** del *dump* actual no reducen el riesgo operacional para los agentes expuestos, cuyos nombres, identificaciones y, en algunos casos, datos bancarios, están ahora en dominio público.

Se recomienda una **respuesta coordinada** entre los servicios de inteligencia de España y Marruecos, junto con un **monitoreo activo** de las plataformas del actor y la preparación de planes de contingencia para los escenarios de mayor riesgo.

---

**Fin del Informe 2.1**

*Documento basado exclusivamente en fuentes abiertas. Se recomienda actualización continua a medida que se disponga de nueva información.*

---




**INFORME DE INTELIGENCIA DE AMENAZAS (CTI) – VERSIÓN 3.0**

**Actor:** Jabaroot (alias JabaROOT, Jabaroot DZ, JabaRoot DZ)  
**Fecha de elaboración:** 25 de agosto de 2026  
**Clasificación:** TLP:WHITE / Fuentes abiertas exclusivamente  
**Estado del actor:** Activo – canal @jabaroot_off operativo; archivos trasladados a darkforums.ru  
**Versión:** 3.0 – Profundización en atribución, análisis de datos, geopolítica, impacto en España y recomendaciones estratégicas

---

## 1. Propósito de este documento

Este informe es una **ampliación del Informe 2.1**. Su objetivo es desarrollar las capas de análisis pendientes: atribución y perfil del actor con fuentes oficiales y alternativas; análisis forense de los datos filtrados; contexto geopolítico y escenarios de escalada; impacto detallado en la seguridad nacional de España; y recomendaciones estratégicas priorizadas con plazos y responsables.

Todas las afirmaciones se basan exclusivamente en fuentes abiertas disponibles al 25 de agosto de 2026.

---

## 2. Atribución y Perfil del Actor – Profundización

### 2.1. Atribución oficial de Marruecos

Las autoridades marroquíes vinculan sistemáticamente a Jabaroot con **Argelia**. Esta atribución se ha mantenido constante desde la aparición del grupo en abril de 2025, pero **no ha sido acompañada de pruebas técnicas públicas** que demuestren el origen argelino de los ataques.

El silencio oficial de Rabat sobre la filtración de los 70.000 agentes es significativo. Ningún comunicado oficial del gobierno, de la DGST o de Abdellatif Hammouchi se ha emitido al momento de redacción, lo que sugiere:
- **Desconcierto estratégico** sobre cómo responder sin dar más visibilidad al actor.
- **Evaluación interna del daño** antes de emitir una declaración pública.
- **Posible negociación discreta** con Telegram para el cierre del canal.

### 2.2. Hipótesis alternativas: la teoría de Navakintelligence

La consultora de inteligencia **Navakintelligence** ha planteado una hipótesis alternativa que no ha sido suficientemente explorada en fuentes abiertas: Jabaroot podría ser **un exagente o insider marroquí actuando en solitario o con un grupo reducido**.

Esta teoría se sustenta en:
- El **volumen y la sensibilidad** de los datos filtrados (CNSS, palacios reales, DGST/DGSN) sugieren acceso interno o conocimiento profundo de las estructuras del Estado marroquí.
- La **exoneración sistemática del rey** y el enfoque en figuras concretas (Hammouchi, El Himma, Lekjaa) apuntan a una **guerra de clanes interna** dentro del aparato de seguridad marroquí.
- La **precisión de los blancos** (director de recursos humanos de la DGST, director adjunto de contraespionaje, jefe de la Célula de Investigación) sugiere un conocimiento interno que un actor externo difícilmente podría poseer sin una fuente humana dentro de la organización.

**Nivel de confianza de esta hipótesis:** Media-baja, pero no descartable. Requiere investigación de campo o acceso a fuentes humanas para ser confirmada o refutada.

### 2.3. Análisis de la "marca" Jabaroot: ¿brand hijacking o continuidad?

El análisis de Golden Owl (22 de agosto de 2026) planteó la posibilidad de que el *dump* de 70.000 agentes no sea obra del Jabaroot original, sino de **imitadores que aprovechan la marca**【Informe 2.1】.

**Argumentos a favor del brand hijacking:**
- Inconsistencias técnicas en las muestras (duplicados, fechas de nacimiento genéricas "1 de enero", campos de rango vacíos).
- Proliferación de canales de Telegram con el nombre "Jabaroot" tras los cierres, lo que dificulta la atribución.
- Posible reutilización de datos obtenidos en filtraciones anteriores.

**Argumentos en contra del brand hijacking:**
- La **consistencia narrativa** se mantiene desde abril de 2025: anti-Makhzen, pro-Argelia, exposición de corrupción y seguridad.
- El **modus operandi** (Telegram + DarkForums, mensajes escalonados, amenazas con plazos) es coherente con el actor original.
- La **validación parcial de los datos** por exagentes y fuentes del CNI sugiere que al menos una parte significativa del *dump* es auténtica.

**Conclusión provisional:** Es posible que estemos ante un **escenario mixto**: un núcleo original (posiblemente el vinculado a la pista Mzannar o un insider marroquí) que mantiene el control de la marca, pero con **colaboradores o imitadores** que han contribuido a la operación actual o han reutilizado datos de filtraciones anteriores.

---

## 3. Análisis de Datos y Forensia – Profundización

### 3.1. Volumen exacto y estructura de los datos

Las fuentes abiertas presentan ligeras discrepancias en el número de registros filtrados:

| Fuente | Número de registros |
|--------|---------------------|
| La Razón | 70.381 |
| El Confidencial | Al menos 70.000 |
| LaSexta | 70.000 |
| Breaches.Africa | 70.000 |

La diferencia (381 registros) es menor y podría deberse a:
- **Redondeo** en la mayoría de las fuentes.
- **Versiones diferentes del dataset** (una lista principal de 70.000 + una lista secundaria de 381 registros adicionales).
- **Actualizaciones posteriores** a la publicación inicial.

**Estructura de los datos:**

| Lista | Contenido | Número aproximado |
|-------|-----------|-------------------|
| **Lista principal** | Nombres, DNI, número de empleado, año de reclutamiento | 70.000 |
| **Lista secundaria** | Grados y RIB (números de cuenta bancaria) | 1.400 |

### 3.2. Validación de autenticidad – actualización

La validación de los datos filtrados ha avanzado desde el Informe 2.1:

**Confirmaciones positivas:**
- **Exagentes de la inteligencia marroquí** consultados por El Confidencial han confirmado la pertenencia de algunos nombres a la DGST.
- En la lista aparecen **altos cargos identificables**: el director de recursos humanos de la DGST, el director adjunto de contraespionaje y el jefe de la Célula de Investigación.
- **Fuentes del CNI español** han reconocido nombres de agentes que ya estaban bajo investigación【Informe 2】.
- **ECSAHARAUI** ha considerado auténticas partes de las bases difundidas.

**Advertencias y limitaciones:**
- La lista **podría haber sido obtenida hace algún tiempo y filtrada ahora**.
- No se ha realizado un **análisis forense completo** del dataset de 70.000 registros en fuentes abiertas.
- La **segunda lista de 1.400 con RIB** no ha sido verificada de forma independiente.

### 3.3. Riesgo de la segunda lista (RIB de 1.400 agentes)

La exposición de **números de identificación bancaria (RIB) de 1.400 agentes** representa una vulnerabilidad operacional y financiera significativa:

- **Riesgo de fraude**: los RIB, combinados con nombres completos y números de identificación, pueden ser utilizados para suplantación de identidad y transacciones no autorizadas.
- **Riesgo de chantaje**: los agentes cuyos datos bancarios han sido expuestos pueden ser objeto de presión por servicios de inteligencia rivales.
- **Riesgo institucional**: la exposición de cuentas bancarias de personal de inteligencia puede revelar patrones de pagos, transferencias y relaciones financieras.

**No hay reportes públicos** de uso fraudulento de estos RIB al 25 de agosto de 2026.

---

## 4. Contexto Geopolítico y Escenarios de Escalada

### 4.1. Las exigencias de Jabaroot a Marruecos

Antes de la filtración, Jabaroot condicionó la no publicación a que las autoridades de Rabat atendieran **varias exigencias**:

1. **Disculpa oficial** por los acontecimientos de Ceuta.
2. **Declaración de un periodo de luto nacional**.
3. **Suspensión de las elecciones legislativas** previstas para el 23 de septiembre de 2026.

El hecho de que Rabat **no atendiera estas exigencias** y que Jabaroot **cumpliera su amenaza** refuerza la credibilidad del actor y su determinación. La publicación de los datos de 70.000 agentes es, en sí misma, una **respuesta directa al silencio de Rabat**.

### 4.2. Actores internacionales implicados según Jabaroot

El grupo afirma que la crisis de Ceuta **ocurrió con conocimiento de un país grande** (en clara alusión a Estados Unidos) y que **Israel también estaba al tanto**.

**Análisis de credibilidad de esta afirmación:**
- **No hay evidencia pública** que respalde la implicación de EE.UU. o Israel en la planificación de la crisis de Ceuta.
- La inclusión de estos actores en la narrativa de Jabaroot puede tener varios objetivos:
  - **Aumentar el impacto mediático** de la filtración.
  - **Presionar a Marruecos** sugiriendo que sus aliados conocían y posiblemente aprobaban el plan.
  - **Generar tensión diplomática** entre Marruecos y sus socios internacionales.

### 4.3. La promesa de la lista de coordinadores de Ceuta

Jabaroot ha anunciado que publicará una **lista nominal específica de los agentes que organizaron y coordinaron el plan de Ceuta**. El grupo afirma disponer de **copias de órdenes de misión** correspondientes a agentes desplazados a Fnideq (Castillejos) antes y durante los acontecimientos.

**Escenario de alto impacto:** Si esta lista se materializa, podría:
- **Exponer operativamente** a los agentes responsables de la crisis migratoria.
- **Proporcionar pruebas** a España para acciones judiciales o diplomáticas.
- **Provocar una crisis institucional** en Marruecos si se confirma la implicación de altos cargos.

**Probabilidad: Media-alta.** El actor ha cumplido sus amenazas previas y tiene un historial de publicación de datos sensibles.

### 4.4. El teaser de Pegasus y Pedro Sánchez

El 24 de agosto de 2026, Jabaroot publicó en Telegram: *"¿A quién le interesan los datos originales de Pegasus relacionados con Pedro Sánchez?"*

**Contexto del caso Pegasus:**
- En 2022, el Gobierno español confirmó que los teléfonos de Pedro Sánchez y de la ministra de Defensa, Margarita Robles, fueron infectados con Pegasus.
- La primera infección del móvil de Sánchez se produjo el **19 de mayo de 2021**, justo después de la crisis por la acogida médica del líder del Frente Polisario, Brahim Ghali, y la posterior entrada masiva de migrantes en Ceuta.
- Hubo una **segunda intrusión** unos pocos días después.
- La Audiencia Nacional archivó la investigación en **enero de 2026** por falta de cooperación de Israel.

**Escenario de alto impacto:** Si Jabaroot publica datos reales de Pegasus sobre Sánchez, podría:
- **Reabrir el caso** en la Audiencia Nacional.
- **Provocar una crisis diplomática** aguda entre España y Marruecos.
- **Revelar información clasificada** sobre el espionaje a la cúpula del Estado español.

**Probabilidad: Baja** (sin muestras ni metadatos hasta el momento).

---

## 5. Impacto en la Seguridad Nacional de España

### 5.1. Riesgo para agentes y contactos españoles

La filtración expone a **agentes marroquíes que han operado en Europa**, incluyendo España. Según Jabaroot, estos agentes realizaron misiones de:
- **Espionaje**.
- **Instalación de dispositivos de escucha**.
- **Soborno de políticos y empresarios**.

**Riesgo para España:**
- Si los agentes filtrados han operado en territorio español, **sus contactos y redes** en España podrían quedar expuestos.
- **Políticos y empresarios españoles** que hayan sido objeto de estas operaciones podrían ser identificados.
- La **cooperación bilateral** en materia de terrorismo, inmigración y narcotráfico podría verse afectada si se confirma que Marruecos ha espiado a España【Informe 2】.

### 5.2. Impacto en la cooperación bilateral

Las áreas de cooperación entre España y Marruecos que podrían verse afectadas incluyen:

| Área | Impacto potencial |
|------|-------------------|
| **Lucha antiterrorista** | Suspensión temporal o endurecimiento de la cooperación si se confirma espionaje masivo. |
| **Control de inmigración** | Deterioro de la confianza en los mecanismos de control fronterizo. |
| **Narcotráfico** | Posible suspensión de operaciones conjuntas. |

El periodista **Ignacio Cembrero** (El Confidencial) ha advertido de **posibles consecuencias** si Rabat sospecha de implicación española en la filtración【Informe 2】.

### 5.3. La narrativa mediática en España

La filtración ha sido amplificada por **prácticamente todos los grandes medios españoles**: El Confidencial, El Mundo, ABC, La Razón, LaSexta, Telecinco, Onda Cero, COPE, El Independiente, entre otros.

El framing de **"regalo a España"** ha sido recogido de forma generalizada, lo que indica que Jabaroot ha logrado su objetivo de **penetrar el discurso público** y generar tensión diplomática.

**Riesgo:** La cobertura mediática acrítica puede **legitimar la narrativa del actor** y aumentar la presión sobre el gobierno español para que responda.

---

## 6. Recomendaciones Estratégicas y Operativas

### 6.1. Para el Gobierno de Marruecos

| Prioridad | Acción | Plazo | Responsable |
|-----------|--------|-------|-------------|
| **Crítica** | Evaluar el impacto real de la filtración sobre el personal expuesto (especialmente los 1.400 con RIB). | 24-48h | DGST/DGSN |
| **Crítica** | Cambiar identificadores operativos y proteger cuentas bancarias de los agentes expuestos. | 24-48h | DGST/DGSN + Bancos |
| **Alta** | Emitir un comunicado oficial que reconozca la filtración sin darle más visibilidad al actor. | 48-72h | Gobierno de Marruecos |
| **Alta** | Solicitar formalmente a Telegram el cierre de @jabaroot_off. | 48-72h | Ministerio de Interior |
| **Media** | Iniciar una investigación interna para identificar el vector de compromiso y posibles insiders. | 1 semana | DGSSI |
| **Media** | Desarrollar una estrategia de comunicación para contrarrestar la narrativa de Jabaroot. | 1 semana | Gabinete de Comunicación |

### 6.2. Para el Gobierno de España

| Prioridad | Acción | Plazo | Responsable |
|-----------|--------|-------|-------------|
| **Crítica** | Verificar si los nombres filtrados corresponden a agentes que han operado en España. | 24-48h | CNI |
| **Alta** | Evaluar el riesgo de exposición de contactos y redes españolas. | 48-72h | CNI |
| **Alta** | Preparar un plan de comunicación para el escenario de publicación de datos Pegasus. | 1 semana | Moncloa + CNI |
| **Media** | Coordinar con Marruecos (discretamente) para evaluar el impacto en la cooperación bilateral. | 1 semana | Ministerio de Exteriores |
| **Media** | Reforzar la vigilancia en la frontera de Ceuta y Melilla ante posibles nuevos movimientos migratorios. | Inmediato | Ministerio de Interior |

### 6.3. Para la comunidad OSINT/CTI

| Prioridad | Acción | Plazo |
|-----------|--------|-------|
| **Alta** | Monitorear @jabaroot_off y darkforums.ru para detectar nuevas publicaciones. | Continuo |
| **Alta** | Compartir indicadores (handles, patrones de mensajes) en plataformas de colaboración (MISP). | Inmediato |
| **Media** | Realizar un análisis forense de las muestras disponibles (hashes, estructura, antigüedad). | 1 semana |
| **Media** | Actualizar la pista Rachid Mzannar / 3N16M4 y buscar nuevos handles. | 1 semana |

---

## 7. Preguntas Abiertas y Líneas de Investigación Pendientes

1. **¿El dump de 70.000 es completamente auténtico o contiene datos mezclados de bases civiles previas?**
2. **¿Quién está realmente detrás de la operación actual: el Jabaroot original, imitadores, o un insider marroquí?**
3. **¿Tiene Jabaroot acceso real a datos de Pegasus o es un señuelo para atraer atención mediática?**
4. **¿Cuál es el vector de acceso inicial que permitió la exfiltración de estos datos?**
5. **¿Existen miembros de Jabaroot en foros rusos?** 
6. **¿Se han vendido previamente estos datos en el mercado negro?**
7. **¿Por qué se exime al rey y se enfoca exclusivamente en Hammouchi, El Himma y Lekjaa?**
8. **¿Qué papel juega Argelia en esta operación? ¿Es un proxy o solo un marco narrativo?**
9. **¿Puede Marruecos identificar y detener al actor antes de nuevas filtraciones?**
10. **¿Qué relación tiene la operación actual con el conflicto cibernético con Dark 07x?**

---

## 8. Conclusión del Informe 3.0

Este informe ha profundizado en las capas de análisis pendientes identificadas en el Informe 2.1:

- **Atribución**: La hipótesis de un **insider marroquí o facción interna** gana peso ante la precisión de los blancos y la exoneración sistemática del rey. La atribución oficial a Argelia sigue sin pruebas técnicas.
- **Análisis de datos**: La validación parcial por exagentes y fuentes del CNI confirma la autenticidad de **al menos una parte significativa** del *dump*. La segunda lista de 1.400 RIB representa un riesgo operacional y financiero real.
- **Geopolítica**: Las exigencias de Jabaroot (disculpa, luto, suspensión de elecciones) y su amenaza de publicar la lista de coordinadores de Ceuta elevan el riesgo de una **crisis institucional** en Marruecos.
- **Impacto en España**: La exposición de agentes que han operado en España y el teaser de Pegasus sobre Pedro Sánchez suponen un **riesgo diplomático y de seguridad nacional** que requiere una respuesta coordinada del CNI y el Ministerio de Exteriores.

La operación de Jabaroot **está en curso** y el canal @jabaroot_off sigue abierto. La publicación de la lista de coordinadores de Ceuta y la posible materialización de los datos de Pegasus son los **escenarios de mayor riesgo** en el horizonte inmediato.

---

**Fin del Informe 3.0**

*Documento basado exclusivamente en fuentes abiertas. Se recomienda actualización continua a medida que se disponga de nueva información.*




