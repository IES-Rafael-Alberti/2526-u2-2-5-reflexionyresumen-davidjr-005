# RESPUESTAS — Reflexión y Resumen (Plantilla genérica)

> **Actividad / ID: 2.a.e**  
> **Unidad / Tema: Unidad 2**  
> **Alumno/a: David Jimenez Ruiz**  
> **Fecha: 19/02/2026**  

---

## 1) Reflexión crítica (preguntas)
Responde con **lenguaje técnico** y **argumentos** (no solo opiniones). Si procede, usa ejemplos, riesgos y decisiones justificadas.

### 1.1) ¿Qué te han parecido los temas tratados en la unidad?
- En general, la unidad me ha parecido muy bien planteada porque combina teoría de un entorno SOC con prácticas que aterrizan esos conceptos a casos reales: monitorización (SIEM), investigación (OSINT) y gestión formal del incidente (clasificación, valoración y documentación).

- Lo que más he disfrutado ha sido la práctica de instalación y configuración del SIEM, porque te obliga a entender de verdad el flujo “log --> normalización --> correlación --> alerta”, y además es algo muy aplicable en un trabajo real.

- OSINT también me gustó mucho porque te das cuenta de la cantidad de información que se puede recopilar en fuentes abiertas y del riesgo que supone para una persona o empresa. Lo único que mejoraría es que algunos ejercicios (como el de la “jirafa”) porque es fácil encontrarse páginas con respuestas (literalmente buscando información sobre la jirafa aparecián webs con la solución).

- La parte de taxonomía de incidentes me parece importante porque da un “lenguaje común” para describir incidentes, priorizarlos y gestionarlos, como hace la taxonomía de INCIBE-CERT y la Guía Nacional con criterios de peligrosidad e impacto.

### 1.2) ¿Qué ha sido más útil para tu futuro puesto de trabajo? ¿Por qué?
- Lo más útil ha sido el SIEM, porque en cualquier puesto relacionado con SOC vas a trabajar con consolas, alertas, reglas de detección y revisión de eventos; saber montarlo y entender cómo se generan las alertas te da una base de conocimiento.

### 1.3) ¿Qué partes ya conocías y cuáles han sido nuevas para ti?
- Ya conocía conceptos generales como SIEM, IDS/IPS y nociones básicas de OSINT, pero de forma más teórica.

- Lo nuevo ha sido ver el enfoque “de ciclo completo”: no solo definir qué es un SIEM, sino instalarlo/configurarlo, plantear un caso de uso (ej. fuerza bruta) y documentar el proceso con incidencias reales de configuración.

- También me resultó nuevo el enfoque de taxonomía y criterios de severidad: entender que clasificar bien es parte del trabajo y no un trámite, porque condiciona la priorización y la forma de notificar y gestionar.

### 1.4) ¿Qué concepto/idea te ha llamado más la atención y por qué?
- Me parece muy interesante el enfoque de la Guía Nacional de usar niveles de peligrosidad e impacto, porque separa “lo peligrosa que es la amenaza” de “lo que realmente ha afectado al servicio/organización”, y eso ayuda a priorizar con criterio.

### 1.5) ¿Qué parte recortarías o simplificarías si hubiera menos tiempo? Justifica.
- Si hubiera menos tiempo, recortaría el ejercicio de OSINT (tipo “jirafa”) o lo sustituiría por un OSINT más actualizado, para que el objetivo sea aplicar metodología y no pelear contra páginas con respuestas.

- Mantendría sí o sí SIEM + documentación de incidentes + taxonomía, porque forman un bloque muy coherente.

### 1.6) ¿Qué tema has echado en falta o ampliarías? Justifica.
- Ampliaría la parte de triage y priorización en un SOC: cómo decidir qué alerta se atiende primero, cómo reducir falsos positivos y cómo definir un playbook mínimo.

### 1.7) ¿Qué aplicarías “mañana” en un entorno real con recursos limitados?
- Con recursos limitados aplicaría un “mínimo viable” de monitorización y respuesta: centralizar logs críticos, crear unas pocas reglas de detección (por ejemplo, fuerza bruta y accesos anómalos) y definir un procedimiento de respuesta corto con responsables y pasos.

- Y como medida rápida de reducción de riesgo, haría una revisión OSINT básica de la exposición pública de la organización (dominios, subdominios, perfiles, filtraciones visibles) para saber por dónde te pueden entrar.

### 1.8) ¿Qué duda, riesgo o punto crítico te queda abierto tras la unidad?
- La duda principal que me queda es cómo “aterrizar” la parte de clasificación y niveles (peligrosidad/impacto) en casos donde un incidente encaja en varias categorías; por ejemplo, un ataque que empieza con un phishing, continúa con acceso no autorizado a la cuenta (intrusión) y termina con exfiltración de correos o documentos (compromiso de la información), y cómo decidir de forma consistente cuál es la categoría principal.  

- También veo como punto crítico el equilibrio entre detectar mucho (muchas alertas) y detectar bien: si no se ajusta el SIEM, puedes saturarte de falsos positivos y perder lo importante.

## 2) Resumen esquematizado (obligatorio)
Incluye **todos los puntos** vistos en la unidad. Prioriza esquema/tabla/listas sobre párrafos largos.

### 2.1) Mapa/índice de la unidad (visión global)

| Apartado                               | Qué incluye (resumen)                                                                   |
| -------------------------------------- | --------------------------------------------------------------------------------------- |
| Gestión de incidentes                  | Clasificación, valoración y documentación de incidentes                                 |
| OSINT aplicado a investigación digital | Recopilación y análisis de información en fuentes abiertas con metodología y evidencias |
| SOC                                    | Concepto, componentes, roles y operación                                                |
| Tecnologías en un SOC                  | SIEM, SOAR, IDS e IPS                                                                   |
| Threat Intelligence y Threat Hunting   | Uso defensivo dentro del SOC: inteligencia de amenazas y búsqueda proactiva             |
| Incident Response y Forensics          | Respuesta ante incidentes, preservación/análisis de evidencias y aprendizaje posterior  |
| Taxonomía + Guía Nacional              | Taxonomía de INCIBE-CERT + criterios de peligrosidad/impacto de la Guía Nacional        |

### 2.2) Conceptos clave (lista breve)
- SOC, SIEM, IDS, IPS, SOAR.

- OSINT y huella digital.

- Threat Intelligence (CTI) y Threat Hunting.

- Incidente vs alerta vs evento.

- Clasificación/taxonomía de incidentes (categorías INCIBE-CERT).
​
- Peligrosidad e impacto (Guía Nacional).

### 2.3) Procesos / procedimientos (pasos o checklist)

Suponiendo que se trata de un ciberincidente, los procedimientos a seguir serián:

1. **Identificación:** detectar el evento, confirmar si es incidente, recopilar información.
​
2. **Clasificación y priorización:** etiquetar el incidente con una taxonomía y asignar prioridad según peligrosidad e impacto (para saber que se atiende primero).

3. **Contención:** frenar la propagación o el daño (aislar equipos, bloquear IPs/domínios, deshabilitar cuentas, etc.).

4. **Mitigación:** aplicar medidas correctivas para reducir el impacto y eliminar la causa (parches, cambios de credenciales).

5. **Recuperación:** restaurar servicios a operación normal y validar que el entorno vuelve a estar estable (verificaciones, monitorización reforzada).

6. **Actuaciones post-incidente:** documentar lecciones aprendidas, mejorar controles/procedimientos y actualizar reglas de detección para evitar recurrencias.

7. **Documentación continua:** timeline, evidencias, decisiones tomadas y comunicaciones realizadas.

### 2.4) Herramientas / técnicas (si aplica)
- SIEM tipo ELK (Elasticsearch + Logstash + Kibana)

- Técnicas OSINT: búsquedas avanzadas, análisis de perfiles y OSINT Framework

- Taxonomía INCIBE-CERT para clasificar incidentes por categorías

### 2.5) Buenas prácticas y errores típicos
- Ajustar el SIEM: reglas pequeñas pero útiles, y revisión periódica.

- Reducir superficie de exposición (OSINT como medida preventiva).

- Documentar desde el minuto 1

Errores típicos:

- Sobrecargar el SIEM de alertas sin priorización (fatiga de alertas).

- No guardar evidencias o no anotar timestamps

### 2.6) Glosario mínimo (términos y definiciones cortas)

| Término                 | Definición corta                                                              |
| ----------------------- | ----------------------------------------------------------------------------- |
| SOC                     | Centro/equipo que monitoriza, detecta y coordina la respuesta ante incidentes |
| SIEM                    | Plataforma que centraliza logs y genera alertas por correlación/reglas        |
| IDS / IPS               | Sistemas de detección (IDS) y prevención (IPS) de intrusiones                 |
| SOAR                    | Orquestación y automatización de respuesta (playbooks)                        |
| OSINT                   | Obtención de información a partir de fuentes abiertas                         |
| Threat Intelligence     | Inteligencia sobre amenazas para mejorar detección/prevención                 |
| Threat Hunting          | Búsqueda proactiva de señales de compromiso                                   |
| Taxonomía de incidentes | Sistema estandarizado para clasificar incidentes (INCIBE-CERT)                |
| Peligrosidad / Impacto  | Escalas para valorar amenaza potencial y afectación real (Guía Nacional)      |


## 3) (Opcional) Evidencias y recursos usados
Enlaza aquí evidencias (capturas, logs, configuraciones, salidas de comandos, etc.) si forman parte de tu trabajo.

### Evidencia 1
- Archivo: `evidencias/01_SIEM.png` [01_SIEM](evidencias/01_SIEM.png)
- Qué demuestra: La instalación y configuración de un SIEM tipo ELK (Elasticsearch + Logstash + Kibana), con la ingesta de logs y la visualización/correlación de eventos en dashboards.
- Qué he aprendido: A desplegar y dejar operativo un SIEM en un entorno de laboratorio, entendiendo el flujo completo de trabajo y a identificar problemas típicos de configuración.

### Evidencia 2
- Archivo: `evidencias/02_OSINT.png` [02_OSINT](evidencias/02_OSINT.png)
- Qué demuestra: Aplicación de una técnica OSINT de búsqueda inversa de imágenes con TinEye para identificar dónde aparece una imagen en Internet para localizar posibles fuentes originales.
- Qué he aprendido: A usar la búsqueda inversa como parte del proceso de investigación (verificación de contenido y contraste de fuentes).


## 4) Conclusión (cierre)

En esta **Unidad 2** he consolidado una visión bastante completa de cómo se trabaja en un entorno tipo SOC, desde el enfoque práctico de detectar, investigar y gestionar incidentes. 

La parte que más me aportó fue la instalación y configuración de un SIEM tipo ELK, porque me ayudó a entender el flujo real de los eventos (logs), la correlación y la generación de alertas.

Las prácticas de OSINT también fueron muy útiles para tomar conciencia de la huella digital y de lo fácil que es recopilar información desde fuentes abiertas si no se controla.

También, me quedo con la importancia de la taxonomía de incidentes y de valorar un incidente por criterios de peligrosidad e impacto, porque es lo que permite priorizar y comunicar de forma consistente.

Por último la importancia que es documentar bien lo ocurrido para aprender y mejorar los controles.