# csai382_lab_2_4_stefany_peixoto
ETL pipeline for restaurant data using Python, Pandas, and Databricks. Focused on reproducibility, logging, and data integrity for AI model training.

## Ethics in AI Reflection

**What information should not be logged?**
Two examples of data that should never be logged are **Personally Identifiable Information (PII)**, such as customer names or emails, and **Security Credentials**, like API keys or passwords. Logging PII violates privacy regulations like GDPR, and logging credentials creates a massive security vulnerability if the logs are ever intercepted.

**How does reproducibility support accountability?**
Reproducibility ensures that a model's results can be audited and verified by others. If a model affects people's lives (like in hiring or lending), being able to recreate the exact environment and data flow allows teams to identify biases and ensure the process is fair and transparent.