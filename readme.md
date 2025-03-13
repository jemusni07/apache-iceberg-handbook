This is a collection of notes, implementations and examples for Apache Iceberg table format. 

**Blogs:**
- [Data Modification Strategies](./learn/data-modification-strategies.md)
- [GDPR Compliance](./learn/gpdr-compliance.md)

**Notebooks:**
- [Iceberg Query Lifecycle](./notebooks/iceberg_query_lifecycle.ipynb)

**Docker Setup:**

To be able to run the notebooks, you need to download [Docker CLI](https://docs.docker.com/get-started/get-docker/) and [Docker Compose](https://github.com/docker-archive/compose-cli/blob/main/INSTALL.md).

Then start the docker containers with `docker-compose up` command.

This will give you an environment for running Spark on Iceberg Tables using Minio as the storage backend.