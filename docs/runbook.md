# Runbook

> Fill in every TODO with exact commands. / Попълнете всяко TODO с точни команди.

## Start locally / Локално стартиране

docker build -t notes-api:0.3.0 .
docker run -d -p 8000:8000 --name notes-app-safer notes-api:0.3.0

## Check that it works / Проверка, че работи

Open http://localhost:8000/health (or your codespace port 8000 link with /health) and you should see {"status":"ok"}

## Run the tests / Тестове

pytest

## When something breaks / Когато нещо се счупи

1. Check container status: docker ps -a
2. Check container logs: docker logs <container-name>
3. Check health status: docker inspect --format '{{.State.Health.Status}}' <container-name>
