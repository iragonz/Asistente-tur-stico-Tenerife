# Asistente Turístico de Tenerife con RAG y LLM

**Autor:** Iván Ramos González  
**Asignatura:** Large Language Models  
**Máster:** Inteligencia Artificial, Cloud Computing y DevOps - Pontia Tech  

## Descripción del Proyecto

Asistente turístico conversacional basado en LLM (Google Gemini) que combina:
- **RAG (Retrieval-Augmented Generation)** sobre una guía turística de Tenerife
- **Diálogo multiturno** con gestión de memoria conversacional
- **Function calling** con la función `get_weather()` para consultas meteorológicas

## Tecnologías Utilizadas

- **LLM:** Google Gemini 2.5 Flash
- **Embeddings:** HuggingFace Sentence Transformers (paraphrase-multilingual-MiniLM-L12-v2)
- **Vector Store:** FAISS
- **Framework:** LangChain
- **Document Processing:** PyPDF
- **Entorno:** Google Colab

## 📁 Estructura del Proyecto
```
asistente-turistico-tenerife/
├── notebook.ipynb              # Notebook principal con todo el código
├── data/
│   └── TENERIFE.pdf           # Guía turística (fuente de datos)
├── README.md                  # Este archivo
├── requirements.txt           # Dependencias
└── informe_final.pdf          # Documento con análisis y resultados
```

## 🚀 Instalación y Ejecución

### En Google Colab (Recomendado)

1. Abre el notebook en Google Colab
2. Crea y sube el archivo `TENERIFE.pdf` a la carpeta `data/`
3. Configura tu API key de Google Gemini en la Celda 2
4. Ejecuta todas las celdas en orden

### Requisitos
```bash
langchain
langchain-google-genai
langchain-community
pypdf
faiss-cpu
sentence-transformers
```

## Características Principales

### 1. RAG sobre Guía Turística
- Chunking inteligente (1000 caracteres, overlap 200)
- Búsqueda semántica con FAISS
- Citación de fuentes (páginas del PDF)

### 2. Function Calling - `get_weather()`

- Valida formato de fecha (YYYY-MM-DD)
- Simula datos climáticos realistas por zonas (Norte/Sur/Teide)
- Gestión de errores con try/except
- Logging de todas las llamadas

### 3. Gestión de Memoria
- Mantiene últimas 5 interacciones (10 mensajes)
- Control automático de límite de tokens
- Contexto conversacional en cada respuesta

### 4. Experiencia de Usuario
- Chat interactivo con comandos especiales
- Comandos: `salir`, `limpiar`, `historial`
- Respuestas amigables y contextualizadas
- Información del clima integrada naturalmente

## 👨‍💻 Autor

**Iván Ramos González**  
Máster en IA, Cloud Computing y DevOps - Pontia Tech
