# Prisma Vulnerabiltiies Export

This script uses the Prisma Cloud  APIs to get the unified vulernability dashboards and exports the data to csv. 

## Setup Instructions

### Prerequisites

- Python 3.x
- Prisma Cloud API credentials

### Installation

1. **Create Python Virtual Environment (If you haven't alread)y**:

```bash
python3 -m virtualenv venv && source venv/bin/activate  
```

2. **Install required packages**:

Install the dependencies listed in `requirements.txt`:

```bash
pip install -r requirements.txt
```

3. **Environment Variables**:

Create a `.env` file in the root directory of your project. You can copy the `.env.example` file and update it with your own credentials:

```bash
cp .env.example .env
```

Update the `.env` file with your Prisma Cloud API credentials and AWS SES credentials:

```ini
# Prisma Cloud API Credentials
PRISMA_API_URL=<your_prisma_cloud_api_url>
PRISMA_ACCESS_KEY=<your_prisma_access_key>
PRISMA_SECRET_KEY=<your_prisma_secret_key>
```

### Usage

Edit vuln-query-download.py first to create the query that matches your requirements. This is listed under def vuln_query.

-----*To Do: create the script to use json files*-----

Run the script as follows:

```bash
python vuln-query-download.py
```

### Output

The script will query the API, get a response, unzip and deliver a csv. 

