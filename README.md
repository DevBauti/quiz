# FastQuiz: Interactive Quiz Generation Tool

FastQuiz is an innovative tool designed to generate educational quizzes dynamically from uploaded documents. It supports a variety of file formats, including PDFs, text files, and CSVs, providing an intuitive interface for users to generate questions and answers based on the content of their documents.

---

## Features

1. **Dynamic Quiz Generation:** Generate questions and answers directly from uploaded files.
2. **Multi-format Support:** Handles PDFs, text files, and CSVs.
3. **Educational Focus:** Specifically tailored to create content in Spanish for educational purposes.
4. **AI Integration:** Utilizes OpenAI's GPT technology for natural language understanding and structured output.

---

## Workflow Overview

### 1. **Input Stage**

* Users upload documents via a **Webhook**.
* The tool determines the file type using a **Switch** node and processes it accordingly.

![Input Stage](images\FQuizWF.jpg)

---

### 2. **Data Manipulation**

* Extract content from files using nodes like:

  * **Extract from File** for PDFs.
  * **Extract from File1** for text files.
  * **Extract from File2** for CSVs.
* The extracted data is aggregated and prepared for quiz generation.

![Data Manipulation Workflow](.\images\FQuizWF.jpg)

---

### 3. **Quiz Creation**

* The AI Agent uses GPT to generate quizzes based on the extracted content.
* Questions and answers are structured in JSON format:

```json
{
    "quiz": [
        {
            "id": 1,
            "pregunta": "¿Texto de la pregunta?",
            "respuesta": "Texto de la respuesta"
        }
    ]
}
```

![Quiz Creation Interface](.\images\WindowsFQuiz.jpeg)

---

### 4. **Output Stage**

* The generated quizzes are sent back to the user through the **Respond to Webhook** node.
* The user interface displays the quizzes in an interactive format with options to reveal answers and navigate through questions.

---

## Screenshots

### Workflow Diagram

![Workflow Overview](.\images\FQuizWF.jpg)

### User Interface

![FastQuiz UI](.\images\WindowsFQuiz.jpeg)

---

## Installation and Usage

### Requirements

* **n8n** installed and configured.
* API key for OpenAI.

### Steps to Use

1. Clone the repository and import the workflow JSON file into n8n.
2. Configure the OpenAI API key in the AI Agent node.
3. Run the workflow.
4. Upload a file through the webhook endpoint to generate quizzes.

---

# FastQuiz: Herramienta Interactiva de Generación de Cuestionarios

FastQuiz es una herramienta innovadora diseñada para generar cuestionarios educativos de manera dinámica a partir de documentos subidos por los usuarios. Soporta varios formatos de archivo, incluidos PDFs, archivos de texto y CSVs, ofreciendo una interfaz intuitiva para generar preguntas y respuestas basadas en el contenido de los documentos.

---

## Características

1. **Generación Dinámica de Cuestionarios:** Genera preguntas y respuestas directamente de los archivos subidos.
2. **Soporte para Múltiples Formatos:** Maneja PDFs, archivos de texto y CSVs.
3. **Enfoque Educativo:** Específicamente adaptado para crear contenido en español con fines educativos.
4. **Integración con IA:** Utiliza la tecnología GPT de OpenAI para comprensión del lenguaje natural y salida estructurada.

---

## Resumen del Flujo de Trabajo

### 1. **Etapa de Entrada**

* Los usuarios suben documentos mediante un **Webhook**.
* La herramienta determina el tipo de archivo utilizando un nodo **Switch** y lo procesa en consecuencia.

![Etapa de Entrada](.\images\FQuizWF.jpg)

---

### 2. **Manipulación de Datos**

* Se extrae el contenido de los archivos mediante nodos como:

  * **Extract from File** para PDFs.
  * **Extract from File1** para archivos de texto.
  * **Extract from File2** para CSVs.
* Los datos extraídos se agregan y preparan para la generación del cuestionario.

![Flujo de Manipulación de Datos](.\images\FQuizWF.jpg)

---

### 3. **Creación de Cuestionarios**

* El Agente de IA utiliza GPT para generar cuestionarios basados en el contenido extraído.
* Las preguntas y respuestas se estructuran en formato JSON:

```json
{
    "quiz": [
        {
            "id": 1,
            "pregunta": "¿Texto de la pregunta?",
            "respuesta": "Texto de la respuesta"
        }
    ]
}
```

![Interfaz de Creación de Cuestionarios](.\images\WindowsFQuiz.jpeg)

---

### 4. **Etapa de Salida**

* Los cuestionarios generados se envían de vuelta al usuario mediante el nodo **Respond to Webhook**.
* La interfaz de usuario muestra los cuestionarios en un formato interactivo con opciones para revelar respuestas y navegar por las preguntas.

---

## Capturas de Pantalla

### Diagrama del Flujo de Trabajo

![Resumen del Flujo de Trabajo](.\images\FQuizWF.jpg)

### Interfaz de Usuario

![Interfaz FastQuiz](.\images\WindowsFQuiz.jpeg)

---

## Instalación y Uso

### Requisitos

* **n8n** instalado y configurado.
* Clave API para OpenAI.

### Pasos para Usar

1. Clonar el repositorio e importar el archivo JSON del flujo de trabajo en n8n.
2. Configurar la clave API de OpenAI en el nodo del Agente de IA.
3. Ejecutar el flujo de trabajo.
4. Subir un archivo a través del endpoint del webhook para generar cuestionarios.
