# Cloud-security-threat-monitoring-system
IBM

PROJECT STRUCTURE :

+-------------------------------------------------------------+
|                      Cloud Environment (AWS/IBM Cloud)      |
|                                                             |
|  +----------------+     +------------------------------+   |
|  | Cloud Services | --> |  CloudTrail / CloudWatch Logs |   |
|  | (EC2, S3, IAM) |     |  (Events, API calls, Access)  |   |
+--------------------     +------------------------------+   |
+-------------------------------------------------------------+

                         |
                         v
+-------------------------------------------------------------+
|                     Data Collection Layer                   |
|                                                             |
|  - Python Scripts (boto3 SDK) / AWS Lambda                  |
|  - Scheduled log fetching and storage                       |
+-------------------------------------------------------------+

                         |
                         v
+-------------------------------------------------------------+
|                    Data Processing Layer (ELK Stack)        |
|                                                             |
|  - Logstash: Parses and normalizes log data                 |
|  - Elasticsearch: Indexes logs for search & analysis        |
|  - Kibana: Visualizes logs and security metrics             |
+-------------------------------------------------------------+

                         |
                         v
+-------------------------------------------------------------+
|                    Threat Detection & Alerting              |
|                                                             |
|  - Python Scripts for Anomaly Detection                     |
|  - AWS CloudWatch Alarms for threshold alerts               |
|  - AWS SNS / Email / Slack Alerts                           |
+-------------------------------------------------------------+

                         |
                         v
+-------------------------------------------------------------+
|                    Automated Remediation Layer              |
|                                                             |
|  - AWS Lambda Functions for automated responses             |
|    (e.g., Disable IAM user, Block IP)                       |
|                                                             |
|  - Manual intervention suggestions for critical threats     |
+-------------------------------------------------------------+
