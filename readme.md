# Apache Iceberg Handbook

This is a collection of notes, implementations and examples for Apache Iceberg table format. 

## Repository Contents

### 📚 Learning Resources (`/learn/`)
- **[Data Modification Strategies](./learn/data-modification-strategies.md)** - Deep dive into Copy-on-Write (CoW) vs Merge-on-Read (MoR) strategies, performance characteristics, and hybrid approaches
- **[GDPR Compliance](./learn/gpdr-compliance.md)** - Implementation guide for "right to be forgotten" compliance using Apache Iceberg's ACID guarantees and retention policies

### 📓 Interactive Notebooks (`/notebooks/`)
- **[Iceberg Query Lifecycle](./notebooks/iceberg_query_lifecycle.ipynb)** - Comprehensive walkthrough of table creation, data insertion, MERGE operations, and metadata inspection with practical SQL examples

### 🖼️ Visual Resources (`/images/`)
- `copy_on_write.png` - Visual representation of Copy-on-Write strategy
- `merge_on_read.png` - Visual representation of Merge-on-Read strategy

### 🐳 Docker Environment
- `docker-compose.yml` - Complete containerized environment setup

## Getting Started

To run the notebooks and examples, you need [Docker CLI](https://docs.docker.com/get-started/get-docker/) and [Docker Compose](https://github.com/docker-archive/compose-cli/blob/main/INSTALL.md).

Start the environment:
```bash
docker-compose up
```

This provides a complete Spark environment with Iceberg tables using MinIO as the storage backend.