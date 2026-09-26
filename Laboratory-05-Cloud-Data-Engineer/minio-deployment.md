 MinIO Object Storage Deployment Documentation

 Overview

This document details the configuration and execution steps for deploying an open-source, S3-compatible MinIO object storage server using Docker in a cloud environment.


 Deployment Configuration
 
 1. Docker Deployment Command

To launch the containerized MinIO server, the following command was executed in the KillerCoda terminal:
`bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
minio/minio server /data --console-address ":9001"

