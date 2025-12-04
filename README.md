SHADOW BUCKET DETECTOR
------------------------------------

PROJECT TITLE:
Shadow Bucket Detector – A Tool for Identifying Misconfigured Cloud Storage Buckets

PROJECT DESCRIPTION:
This project detects shadow buckets (publicly exposed or misconfigured cloud buckets) using anonymous S3-compatible checks. The tool identifies bucket existence, public listing permissions, public object access, and sensitive file exposure. A JSON report is generated after scanning all target buckets.

TECHNOLOGIES & LIBRARIES USED:
• Python 3  
• boto3  
• botocore  
• concurrent.futures (ThreadPoolExecutor)  
• MinIO (for local S3-compatible demo testing)

PREREQUISITES:
• Python 3.9+  
• pip  
• MinIO (optional demo environment)  
• requirements.txt installed

INSTALLATION:
1. Create virtual environment  
   python3 -m venv shadow_env  
2. Activate environment  
   source shadow_env/bin/activate  
3. Install dependencies  
   pip install -r requirements.txt

FILES INCLUDED:
• README.txt  
• requirements.txt  
• targets.txt  
• report.json  
• src/main.py  
• src/enumerator.py  
• src/permission_check.py  
• src/sensitive_scan.py  
• src/report_gen.py  
• src/config.py  
• src/utils.py  
• src/cli.py  
• src/__init__.py

HOW TO RUN:
python3 src/main.py --file targets.txt --output report.json

DEMO (OPTIONAL – MINIO):
1. Start MinIO server  
2. Create test buckets  
3. Upload sample files  
4. Set anonymous download access  
5. Run the detector to identify exposed buckets

OUTPUT:
A JSON file “report.json” containing:  
• bucket name  
• existence status  
• public listing permission  
• exposed objects  
• severity rating  
• timestamp
------------------------------------
END OF README
