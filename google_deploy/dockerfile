FROM google/cloud-sdk

RUN mkdir -p /repo
WORKDIR /repo

# Install python and pip3
RUN apt-get update && apt-get install -y \
    python3.7 \
    wget \
    && rm -rf /var/lib/apt/lists/*

# Needed python packages
RUN pip3 install alembic pymysql

RUN wget https://dl.google.com/cloudsql/cloud_sql_proxy.linux.amd64 -O /repo/cloud_sql_proxy \
    && chmod +x /repo/cloud_sql_proxy
