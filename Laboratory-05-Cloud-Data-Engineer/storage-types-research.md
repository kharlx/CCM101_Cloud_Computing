# Cloud Storage Types Research

## Comparison of Cloud Storage Types

| Storage Type       | Description                                                                                                                                         | Primary Use Case                                                                                        | Cloud Provider Example                     |
| :----------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------ | :----------------------------------------- |
| **Block Storage**  | Splitting data into fixed-size blocks with unique identifiers. Acts as a virtual raw disk drive attached directly to a compute instance.            | Operating system boot volumes, high-performance transactional databases (e.g., PostgreSQL, MySQL).      | Amazon EBS (Elastic Block Store)           |
| **File Storage**   | Organizes data in a hierarchical file system with folders and subfolders. Shared across multiple instances over a network protocol like NFS or SMB. | Shared network file systems, content management systems (CMS), legacy app data sharing.                 | Amazon EFS (Elastic File System)           |
| **Object Storage** | Stores data as discrete objects containing raw binary data, customizable metadata, and a unique key identifier within a flat address space.         | Unstructured data storage at scale (images, videos, backups, static web assets, big data repositories). | Amazon S3 (Simple Storage Service) / MinIO |

---

## Why Object Storage for User-Uploaded Photos?

Object storage is the ideal solution for storing user-uploaded images because of its flat address space and seamless scalability without traditional filesystem overhead. Unlike block or file storage, object storage decoupled storage size limits from individual server instances and enriches each image file with custom metadata. This allows application servers to scale infinitely while serving static photo assets directly over HTTP/S APIs at low cost and high availability.
