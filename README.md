⚙️ Flujo del sistema RAG
Carga del documento
Se utiliza PyPDFLoader para leer el PDF.
División del texto
Se divide el contenido en fragmentos (chunks) con RecursiveCharacterTextSplitter.
Generación de embeddings
Cada fragmento se convierte en vectores usando HuggingFaceEmbeddings.
Almacenamiento
Los vectores se guardan en una base vectorial con FAISS.
Consulta
El usuario hace una pregunta.
Se buscan los fragmentos más relevantes.
Generación de respuesta
Se construye un prompt con el contexto.
Un modelo genera la respuesta basada en ese contexto.
