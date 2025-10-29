# Taller 2 - Exploración de ChromaDB como Base de Datos Vectorial

**Estudiante:** John Alexander Chicaiza  
**Programa:** Especialización en Construcción de Software  
**Universidad:** Universidad de Nariño  
**Docente:** Dr. PhD Oscar Ceballos  
**Curso:** Bases de Datos Vectoriales  
**Fecha:** Octubre 2025

## 📋 Descripción del Proyecto

Este proyecto implementa y explora **ChromaDB** como base de datos vectorial alternativa a Pinecone, demostrando todas las operaciones CRUD fundamentales y análisis comparativo con otras soluciones del mercado.

## 🎯 Objetivos

- ✅ Instalar y configurar ChromaDB usando Docker
- ✅ Implementar operaciones CRUD completas para vectores
- ✅ Realizar consultas de similitud semántica
- ✅ Comparar ChromaDB con otras bases de datos vectoriales
- ✅ Documentar el proceso paso a paso

## 🛠️ Requisitos Previos

### Software Necesario
- **Python 3.8+** instalado en el sistema
- **Docker** y **Docker Compose** instalados
- **Git** para clonar el repositorio
- **Visual Studio Code** (recomendado) con extensión de Jupyter

### Verificar Instalaciones
```bash
python3 --version
docker --version
docker-compose --version
git --version
```

## 🚀 Instalación y Configuración

### 1. Configurar Entorno Virtual Python
```bash
# Crear entorno virtual
python3 -m venv chroma_env

# Activar entorno virtual
source chroma_env/bin/activate  # macOS/Linux
# chroma_env\Scripts\activate   # Windows

# Instalar dependencias
pip install -r requirements.txt
```

### 2. Iniciar ChromaDB con Docker
```bash
# Iniciar el servicio ChromaDB
docker-compose up -d

# Verificar que esté corriendo
docker-compose ps
```

### 3. Abrir el Notebook
```bash
# Con VS Code (recomendado)
code ChromaDB_OperacionesCRUD_Vectoriales.ipynb

# O con Jupyter
jupyter notebook
```

## 📁 Estructura del Proyecto

```
Bases de datos vectoriales/
├── ChromaDB_OperacionesCRUD_Vectoriales.ipynb  # Notebook principal
├── docker-compose.yml                          # Configuración Docker
├── requirements.txt                            # Dependencias Python
├── README.md                                   # Este archivo
├── .gitignore                                  # Archivos ignorados
├── chroma_env/                                 # Entorno virtual (no versionado)
└── chroma_data/                               # Datos ChromaDB (no versionado)
```

## 🔧 Configuración de ChromaDB

El archivo `docker-compose.yml` configura:
- **Puerto:** 8000 (http://localhost:8000)
- **Persistencia:** Datos guardados en `./chroma_data`
- **CORS:** Habilitado para desarrollo
- **Reset:** Permitido para pruebas

## 📝 Operaciones Implementadas

### 1. Conexión al Servidor
- Configuración del cliente HTTP
- Verificación de conexión

### 2. Creación de Colección
- Creación de colección "demo_vectores"
- Configuración de metadatos

### 3. Inserción de Vectores (CREATE)
- Inserción de vectores 3D con metadatos
- Validación de datos insertados

### 4. Consultas de Similitud (READ)
- Búsqueda por similitud coseno
- Filtrado por número de resultados
- Inclusión de distancias y metadatos

### 5. Actualización de Vectores (UPDATE)
- Modificación de embeddings existentes
- Actualización de metadatos

### 6. Eliminación de Vectores (DELETE)
- Eliminación por ID específico
- Verificación de eliminación

## 🔄 Ejecutar el Proyecto

1. **Activar entorno virtual:** `source chroma_env/bin/activate`
2. **Iniciar ChromaDB:** `docker-compose up -d`
3. **Abrir el notebook:** `code ChromaDB_OperacionesCRUD_Vectoriales.ipynb`
4. **Ejecutar las celdas** en orden secuencial

## 🆚 Análisis Comparativo

El proyecto incluye una comparación detallada entre:
- **ChromaDB** (implementado)
- **Pinecone** (SaaS)
- **Milvus** (Open Source)
- **Weaviate** (Open Source)
- **FAISS** (Biblioteca)

## 🛑 Detener el Proyecto

```bash
# Detener ChromaDB
docker-compose down

# Desactivar entorno virtual
deactivate
```

## � Detener el Proyecto

```bash
docker-compose down  # Detener ChromaDB
deactivate          # Desactivar entorno virtual
```

## 📊 Resultados Esperados

Al ejecutar el notebook completo, deberías ver:
- ✅ Conexión exitosa a ChromaDB
- ✅ Creación de colección "demo_vectores"
- ✅ Inserción de 3 vectores con metadatos
- ✅ Consulta que retorna 2 vectores más similares
- ✅ Actualización del vector "v1"
- ✅ Eliminación del vector "v3"
- ✅ Estado final con 2 vectores restantes

## 📚 Referencias

- [ChromaDB Documentation](https://docs.trychroma.com/)
- [Docker Compose Documentation](https://docs.docker.com/compose/)
- [Jupyter Notebook Documentation](https://jupyter-notebook.readthedocs.io/)

## 📧 Contacto

**John Alexander Chicaiza**  
Especialización en Construcción de Software  
Universidad de Nariño

---

**Fecha de última actualización:** Octubre 2025