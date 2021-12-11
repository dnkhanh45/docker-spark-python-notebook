# Base images from [bde2020](https://github.com/big-data-europe/docker-spark)

## Spark master:

### Base image:
[bde2020/spark-master:3.1.1-hadoop3.2](https://hub.docker.com/r/bde2020/spark-master)

### Docker Hub:
[khanhdn4500/spark-master-python-notebook](https://hub.docker.com/repository/docker/khanhdn4500/spark-master-python-notebook)

### Include:
- `hadoop-3.2.2`, `python3`
- `pip3`, `jupyter notebook`, `jupyter_http_over_ws`, `findspark`

### Start jupyter kernel
Publishing port `8888` beside `8080`, `7077`
```bash
jupyter notebook \
  --ip 0.0.0.0 \
  --port=8888 \
  --no-browser \
  --allow-root \
  --NotebookApp.allow_origin='https://colab.research.google.com' \
  --NotebookApp.port_retries=0
```
