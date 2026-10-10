# BioAlert

**BioAlert** es una aplicación móvil para Android orientada a la detección temprana y evaluación del riesgo de Infecciones Respiratorias Agudas (IRA), mediante el análisis de información clínica y señales de audio relacionadas con la tos.

El proyecto integra inteligencia artificial, procesamiento de audio y servicios de backend para apoyar la evaluación del riesgo respiratorio y facilitar el seguimiento de los resultados por parte de ciudadanos y especialistas.

## Objetivo del proyecto

Desarrollar una herramienta móvil que contribuya a la identificación temprana del riesgo respiratorio, proporcionando una experiencia accesible para el registro de información, la evaluación mediante inteligencia artificial y la consulta de resultados.

BioAlert busca complementar los procesos de evaluación y seguimiento, sin sustituir el diagnóstico ni el criterio de los profesionales de la salud.

## Funcionalidades principales

- **Registro e inicio de sesión:** acceso para ciudadanos y especialistas.
- **Recuperación de contraseña:** flujo de recuperación mediante códigos de verificación OTP, sujeto al estado de configuración del servicio de correo.
- **Formulario respiratorio:** recopilación de información clínica relevante para la evaluación del riesgo.
- **Grabación de audio:** captura y envío de grabaciones de tos para su procesamiento.
- **Evaluación mediante inteligencia artificial:** análisis de información clínica y características de audio para estimar el riesgo respiratorio.
- **Procesamiento local:** ejecución de componentes del modelo de inteligencia artificial directamente en el dispositivo Android.
- **Visualización de resultados:** presentación de los resultados de la evaluación.
- **Auditoría por especialistas:** revisión de formularios y resultados para apoyar el seguimiento de los casos.
- **Reportes PDF:** generación de documentos con información relevante de las evaluaciones.
- **Actualización de la aplicación:** consulta de versiones publicadas en un repositorio público de GitHub para identificar nuevas versiones y facilitar su descarga e instalación.

## Inteligencia artificial

BioAlert incorpora componentes de inteligencia artificial para la evaluación del riesgo respiratorio.

El procesamiento local utiliza un modelo que combina información clínica con características derivadas del audio. También integra **YAMNet**, un modelo de aprendizaje automático para el análisis de audio, empleado en funciones relacionadas con la identificación de sonidos de tos y la extracción de características acústicas.

La evaluación utiliza la información disponible en el dispositivo y los componentes configurados para el análisis. La ejecución local de estos componentes permite realizar determinadas operaciones sin depender de una llamada a un servicio externo de aprendizaje automático.

Los resultados son estimaciones de apoyo y deben interpretarse dentro del contexto clínico correspondiente.

## Arquitectura y tecnologías

La solución está compuesta por una aplicación móvil Android y un backend independiente.

### Aplicación móvil

- **Kotlin:** lenguaje principal de desarrollo.
- **Android Studio:** entorno de desarrollo.
- **Jetpack Compose:** construcción de la interfaz de usuario.
- **Material Design:** componentes y lineamientos visuales.
- **Retrofit:** comunicación con los servicios de la API.
- **TensorFlow Lite:** ejecución de modelos de inteligencia artificial en el dispositivo.
- **YAMNet:** análisis y extracción de características de audio.

### Backend

El backend de BioAlert está desarrollado con **FastAPI** y utiliza **PostgreSQL** como sistema de gestión de base de datos.

Proporciona servicios para las operaciones de la aplicación, el almacenamiento de información y las funciones de seguimiento y administración que requieren comunicación con el servidor.

Entre las tecnologías utilizadas se encuentran:

- Python
- FastAPI
- Uvicorn
- PostgreSQL
- SQLAlchemy
- TensorFlow y Keras
- Librosa para el procesamiento de audio

## Sistema de actualización

BioAlert dispone de un mecanismo de actualización que consulta un archivo público de metadatos alojado en GitHub. Este archivo informa la versión publicada, su número de versión, la dirección de descarga del APK, las notas de la versión y si la actualización está marcada como obligatoria.

Repositorio de actualizaciones: [bioalert-updates](https://github.com/IlthonAliaga/bioalert-updates)

El sistema está diseñado para detectar versiones nuevas, facilitar la descarga del APK y ofrecer al usuario la posibilidad de iniciar su instalación. La instalación de una actualización requiere la autorización del usuario mediante los mecanismos de seguridad de Android.

La disponibilidad de una actualización depende de la publicación correcta de los metadatos y del APK correspondiente, así como de la implementación del mecanismo de comprobación en la aplicación.

## Privacidad y tratamiento de la información

BioAlert trabaja con información clínica y grabaciones de audio que pueden ser sensibles. Su tratamiento debe realizarse conforme a los consentimientos, avisos legales y medidas de protección aplicables al proyecto.

El uso de la aplicación debe respetar la confidencialidad de la información y limitar su utilización a los fines previstos.

## Alcance y limitaciones

BioAlert es una herramienta de apoyo para la evaluación del riesgo respiratorio. Sus resultados no constituyen por sí solos un diagnóstico médico y no reemplazan una evaluación profesional.

La disponibilidad de determinadas funciones depende de la configuración del backend, los servicios externos y el estado de desarrollo de cada componente.

## Autores

**Ilthon Aliaga y Diego Bravo**

