# DVC Commands Cheatsheet

```bash
dvc init
dvc add data/raw/customer_churn.csv
dvc remote add -d course-storage /tmp/dvc-storage
dvc push
dvc pull
dvc checkout
dvc status
dvc repro
dvc dag
dvc metrics show
dvc metrics diff
dvc cache dir
```

# Git Commands Cheatsheet

```bash
git status --short
git diff --stat
git switch -c feature/name
git diff
git add <files>
git commit -m "type(scope): message"
git push -u origin feature/name
git log --oneline --graph --decorate --all
git fetch
git pull --rebase
git branch --show-current
```

# Linux commands

```bash
mkdir <-p> <paht>
touch <path/file.ext>
cat <path/file.ext>
cat > <path/file.ext> 
cat <path/file.ext> << <content to write>
tail <-n> <number of lines> <file.ext>
curl -sS -i http://localhost:8000
curl -sS -i -X POST <endpoint> -H "..." -d '{key:value}' echo
curl -sS -X POST  <http://localhost:8000/predict/batch>  -F "file=@<data/external/api_batch_sample.csv>"   -o <batch_predictions.csv>
'SEP' <CONTENT> SEP
rm <file.ext>
curl -sG  http://localhost:9090/api/v1/query --data-urlencode 'query=churn_predictions_total' echo
curl -sS http://localhost:8000/metrics  | grep -E "churn_predictions_total|churn_prediction_latency"
```

# Python commands

```bash
pip install -r <requirements.txt>
python - <<'PY'
<python code to execute>
PY
pytest -q
python -m py_compile <path/file.py>
uvicorn api.main:app --host 0.0.0.0 --port 8000
```

# Docker Commands
```bash
docker --version
docker compose version
docker buildx version
docker build -t <name-for-image> .
docker images <name-for-container>
docker run -d  --name <container-name> -p 8000:8000 <container-name>
docker logs <container-name>
docker stop <container-name>
docker rm <container-name>
docker ps -a
docker compose config (para el yaml)
docker compose build <api-name>
docker compose up -d
docker compose ps
docker compose logs --tail 20 prometheus  (http://localhost:9090/-/ready)
```