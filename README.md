
# Netflix Data Pipeline (ETL with Airflow, AWS S3, PostgreSQL)

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-2.5%2B-orange)](https://airflow.apache.org/)
[![AWS S3](https://img.shields.io/badge/AWS%20S3-Cloud%20Storage-ff9900)](https://aws.amazon.com/s3/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15%2B-336791)](https://www.postgresql.org/)

---

## 🚀 **Project Description**  
Automation of an ETL (Extract, Transform, Load) pipeline for Netflix movies and TV shows data.  
**Goal**: Learn workflow orchestration with Apache Airflow, AWS S3 integration, and relational databases.

---

## 🔧 **Technologies Used**  
- **Orchestration**: Apache Airflow.  
- **Cloud Storage**: AWS S3.  
- **Database**: PostgreSQL.  
- **Python Libraries**: Pandas, SQLAlchemy, Boto3.  
- **Dataset**: [Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows).

---

## 📂 **Repository Structure**

├── dags/                  
├── scripts/               
│   ├── extract.py       
│   ├── transform.py      
│   └── load.py           
├── sql/                  
│   └── schema.sql        
├── config/                
│   └── aws_credentials.py 
├── data/                  
│   ├── raw/               
│   └── processed/       
└── requirements.txt       
---

## ⚙️ **Installation Guide**  
1. **Clone the repository**:  
   ```bash
   git clone https://github.com/your-username/netflix-data-pipeline.git
   cd netflix-data-pipeline
2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
3. **Configure Airflow connections:**
- **AWS S3**: Access key and secret.
- **PostgreSQL**: Database URL.

4. **Run the DAG**:
- Enable the netflix_data_pipeline DAG in the Airflow UI.

## 🛠️ **Key Features**  
- **Automated Data Cleaning**:  
  - Handle missing values in critical columns (e.g., `director`, `country`).  
  - Standardize date formats (`date_added`) and categorical values.  
- **Incremental Load**:  
  - Efficient data upload to AWS S3 (Parquet/CSV formats).  
  - Optimized inserts into PostgreSQL to avoid duplicates.  
- **Workflow Orchestration**:  
  - Scheduled DAGs in Apache Airflow for end-to-end pipeline management.  
- **Error Handling**:  
  - Detailed logging and alerts for failed tasks.  
- **Modular Code**:  
  - Reusable scripts for extraction, transformation, and loading.
## 📚 **References**  
- **Tutorial**: [Build a Netflix Data Pipeline - YouTube](https://www.youtube.com/watch?v=ZnQwO6V7pec).  
- **Dataset**: [Netflix Movies and TV Shows - Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows).
## 📄 **License**  
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.  
