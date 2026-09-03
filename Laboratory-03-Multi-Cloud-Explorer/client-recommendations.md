# Client Cloud Recommendations & Multi-Cloud Decision Matrix

## 1. Scenario Recommendations (Checkpoint 4)

### Client A – Startup Company
* **Recommended Platform:** Amazon Web Services (AWS)
* **Justification:** Amazon Web Services is the ideal platform for startups due to its flexible pay-as-you-go pricing and generous startup credits offered through programs like AWS Activate. AWS provides a low-barrier entry point for launching new mobile applications with minimal upfront costs while ensuring unmatched elasticity for rapid business expansion. Its fully managed cloud services allow small development teams to focus on app development rather than managing underlying server infrastructure. As user traffic spikes, AWS automatically scales resources dynamically without service interruptions.
* **Recommended Services:** Amazon Lightsail / EC2, Amazon S3, Amazon DynamoDB.

### Client B – University
* **Recommended Platform:** Microsoft Azure
* **Justification:** Microsoft Azure is the most natural fit for the university because of its deep native integration with existing Microsoft software stacks. Since the institution already utilizes Windows Server, Active Directory, and Microsoft 365, migrating to Azure allows seamless hybrid connectivity without changing core identity models. Through Microsoft Entra ID (formerly Azure AD), the university can implement unified single sign-on (SSO) across on-premises and cloud resources effortlessly. Additionally, the university can leverage Azure Hybrid Benefit to significantly cut cloud licensing costs for existing Windows Server setups.
* **Recommended Services:** Microsoft Entra ID, Azure Virtual Machines, Azure SQL Database.

### Client C – AI Research Company
* **Recommended Platform:** Google Cloud Platform (GCP)
* **Justification:** Google Cloud Platform is the industry leader for artificial intelligence, machine learning, and high-performance computing workloads. GCP features specialized Tensor Processing Units (TPUs) and custom GPU infrastructure designed specifically to accelerate complex deep learning and training pipelines. Its Vertex AI platform unifies data engineering, model training, and deployment into a single streamlined workspace. Furthermore, GCP's native heritage with TensorFlow and advanced big data tools ensures high efficiency for resource-intensive research applications.
* **Recommended Services:** Google Compute Engine (GPU/TPU instances), Vertex AI, Google Cloud Storage.

### Client D – Global E-Commerce Company
* **Recommended Platform:** Amazon Web Services (AWS)
* **Justification:** AWS possesses the world's most mature and expansive global infrastructure network, making it perfect for multinational online shopping platforms. Its multi-region availability zones and edge caching capabilities deliver minimal latency and high performance for global customers. AWS Auto Scaling groups dynamically handle sudden, massive traffic surges during global sales events without experiencing downtime. By combining robust managed database engines with content distribution networks, AWS ensures 99.99% operational availability for enterprise retail systems.
* **Recommended Services:** Amazon EC2 Auto Scaling, Amazon CloudFront (CDN), Amazon Aurora.

---

## 2. Multi-Cloud Decision Matrix (Checkpoint 6)

| Business Requirement | Recommended Platform | Justification |
| :--- | :--- | :--- |
| **Startup Company** | AWS | Offers vast startup credit programs (AWS Activate), low pay-as-you-go entry costs, and rapid scalability. |
| **Enterprise Organization** | Azure | Provides strong compliance coverage, high-availability SLAs, and extensive hybrid cloud integration tools. |
| **Microsoft Environment** | Azure | Features native Active Directory / Entra ID sync and cost-saving Azure Hybrid Benefit licensing options. |
| **AI / Machine Learning** | GCP | Delivers state-of-the-art Vertex AI pipelines, native TensorFlow support, and specialized TPU hardware. |
| **Kubernetes Deployment** | GCP | Built by the original creators of Kubernetes, offering unmatched managed performance via GKE. |
| **Global Web Application** | AWS | Leverages massive global edge networks, regional redundancy, and enterprise auto-scaling infrastructure. |