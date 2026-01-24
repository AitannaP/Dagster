FROM python:3.13

RUN pip install dagster \ dagster-webserver\
    dagster-docker \ 
    dagster-dg-cli 
    

# Add code location code
WORKDIR /opt/dagster/app
# COPY ../Dagster_etl_tutorial/etl-tutorial /opt/dagster/app

# Run dagster code server on port 4000
EXPOSE 3000

# HEALTHCHECK --timeout=1s --start-period=3s --interval=3s --retries=20 CMD ["dagster", "api", "grpc-health-check", "-p", "4000"]

# CMD allows this to be overridden from run launchers or executors to execute runs and steps
# CMD ["dagster", "code-server", "start", "-h", "0.0.0.0", "-p", "4000", "-f", "definitions.py"]
# CMD ["dg", "dev" ]

# CMD ["pwd","&&","dagster", "code-server", "start", "-h", "0.0.0.0", "-p", "3000","-f","src/etl_tutorial/definitions.py"]
