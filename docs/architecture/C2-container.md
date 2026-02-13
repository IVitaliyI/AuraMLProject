### WEB UI
Responsibility:
- принимает запросы от пользователей
- отображает результаты поиска и метаданные
- взаимодействует с Retrieval API и IAM Service
Technology:
- React + TypeScript + Tailwind
Interfaces:
- REST / HTTP

### Retrieval API
Responsibility:
- принимает поисковые запросы от UI
- выполняет поиск по Vector DB
- ранжирует и возвращает релевантные документы
Technology:
- Python + FastAPI
Interfaces:
- REST / HTTP JSON
- gRPC / SQL к Vector DB

### Ingestion Service
Responsibility:
- принимает и обрабатывает новые документы (PDF, TXT, MD)
- строит эмбеддинги и сохраняет их в Vector DB
- сохраняет оригиналы в Object Storage
Technology:
- Python + Haystack + Pandas
Interfaces:
- REST / gRPC
- S3 API для Object Storage

### Vector DB
Responsibility:
- хранение векторов документов
- быстрый семантический поиск
Technology:
- Milvus / FAISS
Interfaces:
- gRPC / REST API

### Object Storage
Responsibility:
- хранение исходных документов и метаданных
Technology:
- MinIO / S3
Interfaces:
- S3 API

### IAM Service Light
Responsibility:
- проверка авторизации пользователей и API ключей
- управление ролями и разрешениями
Technology:
- Python + FastAPI + SQLite
Interfaces:
- HTTP REST



