app.yaml:create pod app with labels app=demo, run=demo, for image us-central1-docker.pkg.dev/k8s-k3s-406919/demo/demo-image:v1.0.0, container name app, running on port 8080 named http:Creates a pod for DEMO image:https://raw.githubusercontent.com/sergeypashkov/AsciiArtify/main/yaml/app.yaml
app-livenessProbe.yaml:create pod app-livenessprob in demo namespace, for image us-central1-docker.pkg.dev/k8s-k3s-406919/demo/demo-image:v1.0.0, container name app, running on port 8080 named http, with liveness probe at path / on port 8000 (initial delay 5s, timeout 1s, period 10s, failure threshold 3s):Creates a pod in demo namespace for DEMO image with liveness probe:https://raw.githubusercontent.com/sergeypashkov/AsciiArtify/main/yaml/app-livenessProbe.yaml
app-readinessProbe.yaml:create pod app-readinessprob in demo namespace, for image us-central1-docker.pkg.dev/k8s-k3s-406919/demo/demo-image:v1.0.0, container name app, running on port 8080 named http, with liveness probe at path / on port 8000 (initial delay 5s, timeout 1s, period 10s, failure threshold 3s), with readiness probe at path /ready on port 8000 (initial delay 0s, success threshold 1s, period 2s, failure threshold 3s):Creates a pod in demo namespace for DEMO image with liveness and readiness probes:https://raw.githubusercontent.com/sergeypashkov/AsciiArtify/main/yaml/app-readinessProbe.yaml
app-volumeMounts.yaml:create pod app-volume, for image gcr.io/kuar-demo/kuard-amd64:1, container name app, running on port 8080 named http, with liveness probe at path /healthy on port 8080 (initial delay 5s, timeout 1s, period 10s, failure threshold 3s), with readiness probe at path /ready on port 8080 (initial delay 0s, success threshold 1s, period 2s, failure threshold 3s), with volume data, path on host /var/lib/app mounted to /data container directory, mount named data:Creates pod with "Kubernetes up and running" image with mounting volume from host:https://raw.githubusercontent.com/sergeypashkov/AsciiArtify/main/yaml/app-volumeMounts.yaml
app-cronjob.yaml:create cron job named app-cronjob with schedule at every 5th minute, restart on failure, API version batch/v1. Container name hello with image bash, execute command 'echo' 'Hello World':Creates Cron job executed each 5 minutes:https://raw.githubusercontent.com/sergeypashkov/AsciiArtify/main/yaml/app-cronjob.yaml
app-job.yaml:create job named app-job-rsync with volume data-input, gcePersistentDisk named glow-data-disk-200, filesystem ext4. Never restart. Backoff limit 0. Container ‘init' with image google/cloud-sdk:275.0.0-alpine, command to execute '/bin/sh' '-c' 'gsutil -m rsync -dr gs://glow-sportradar/ /data/input', volume data-input is mounted to /data/input container folder.:Creates rsync job:https://raw.githubusercontent.com/sergeypashkov/AsciiArtify/main/yaml/app-job.yaml
