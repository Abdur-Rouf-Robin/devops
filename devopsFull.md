# DevOps

## chapter 1 Linux and Bash

- the shell = a program that runs commands. Bash is the usual one on a server
- a process we start in the shell is a child of the shell
- `pwd` prints the folder. `ls` lists it. `cd` moves
- a pipe `|` sends the output of one command into the next
- redirect `>` writes a file. `>>` appends
- permissions are read, write, execute, for owner, group, and others
- `chmod` changes them. a private key is not world-readable
- a unit file or PM2 keeps a process running after we log out. a command in an SSH session dies when we disconnect, unless we used a process manager
- we edit on the laptop and deploy. we do not hotfix production by typing into a live file and forgetting

```bash
ls -la
ps aux | grep node
tail -n 100 /var/log/nginx/error.log
```

- `tail` shows the end of a log. that is the first place a 502 sends us
- `grep` filters lines. the pipe is why `ps` and `grep` are one thought

- homework of chapter 1
```bash
# 1a  list files with their permissions
# 1b  the last 50 nginx error lines
# 1c  why a private key is not chmod 644
```

## chapter 2 Networking basics

- an interface has an address. the public one is how the internet reaches the box. a private one is how the box reaches the database on the same network
- a port is the number of the program. 22 SSH, 80 HTTP, 443 HTTPS, 5432 Postgres
- we do not publish 5432 to the world
- DNS turns the name into the address. the firewall decides if the port is open
- `curl` from the server tells us if the API is up without the browser
- inside Docker, localhost is the container. the database host is the service name

```bash
curl -I https://vms.arrobin.com
ss -lntp | head
```

- `-I` fetches headers. a 200 or a 301 is the front door answering
- `ss` shows who is listening. the Nest port should be local if nginx is the public door

- homework of chapter 2
```bash
# 2a  which port is public, 443 or 5432
# 2b  why curl to localhost from the API container does not reach Postgres
# 2c  what DNS answers, and what a firewall answers
```

## chapter 3 Git and GitHub

- a commit = a snapshot with a message and a parent
- a branch = a name for a commit we are building on
- `status` shows what changed. `diff` shows the lines
- `add` stages. `commit` records. `push` sends the branch
- a pull request is a branch we ask to merge. the conversation and the checks live there
- `main` is the branch we deploy. we do not rewrite its history after it is shared
- a merge commit joins two lines. a rebase replays our commits on top. we rebase only branches that are not shared
- `.gitignore` keeps `node_modules` and `.env` out of the repo

```bash
git status
git diff
git add backendFull.md
git commit -m "Describe the HTTP status codes with examples."
git push
```

- the message says why. the diff already says what
- a secret in a commit stays in the history. we do not commit `.env`

- homework of chapter 3
```bash
# 3a  the three commands from a changed file to a recorded commit
# 3b  what a pull request is for
# 3c  a file that must stay in .gitignore
```

## chapter 4 Docker

- an image = a packed filesystem and a start command
- a container = a running image. it has its own files and its own network namespace
- a Dockerfile builds the image in layers. a layer is cached when the lines above it did not change
- we copy the lockfile and install dependencies before we copy the source, so a code change does not reinstall every package
- the process in the container is PID 1. it should handle a stop signal and exit
- we do not run as root if the process does not need to
- localhost inside the container is the container

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
RUN npm run build
CMD ["node", "dist/main.js"]
```

- `npm ci` installs from the lockfile. it does not update it
- the image does not contain `.env`. we pass environment at run time

- homework of chapter 4
```dockerfile
# 4a  why package files are copied before the rest of the source
# 4b  what localhost means in this container
# 4c  where the database password comes from, if it is not in the image
```

## chapter 5 Docker Compose

- Compose starts several containers and gives them a network
- the service name is the DNS name. the API reaches Postgres at `postgres`, not at localhost
- a volume keeps the database files when the container is replaced
- `depends_on` waits for the process to start. it does not wait for Postgres to accept connections. the app retries
- VMS and Bracket compose files include Redis. Anemi's does not need Redis

```yaml
services:
  api:
    build: .
    environment:
      DATABASE_URL: postgres://app:app@postgres:5432/app
    depends_on:
      - postgres
  postgres:
    image: postgres:16
    volumes:
      - pgdata:/var/lib/postgresql/data
volumes:
  pgdata:
```

- the URL host is `postgres` because that is the service name
- the volume name `pgdata` is what survives `docker compose down` without `-v`

- homework of chapter 5
```yaml
# 5a  the host in DATABASE_URL, and why not localhost
# 5b  what we lose if we remove the volume
# 5c  which product's compose file has no Redis service
```

## chapter 6 Kubernetes and Helm

- we have not operated a Kubernetes cluster. the notes still name the parts
- a pod = one or more containers that share a network and are scheduled together
- a deployment = the desired number of pods, and how to replace them
- a service = a stable name and address in front of the pods
- an ingress = the HTTP front door, the role nginx plays for us today
- a configmap is configuration. a secret is a secret. both are mounted or injected as env
- Helm = a package of those YAML files, with values we fill in
- a chart is the package. a release is one install
- the idea we already use is the same: more than one process, a front door, env for config, a restart when it dies
- we do not draw pods on a diagram of the system we run today

```text
today: nginx -> node process managed by PM2 -> postgres
the kubernetes words: ingress -> service -> deployment -> pod
```

- a liveness probe restarts a stuck process. a readiness probe takes it out of the service until it can answer
- those map to "PM2 restarts it" and "nginx stops sending traffic to a dead upstream"

- homework of chapter 6
```text
# 6a  pod, deployment, service, in one line each
# 6b  the thing we run today that is closest to an ingress
# 6c  what we say if we are asked whether we operate a cluster
```

## chapter 7 CI, GitHub Actions, and cloud

- CI = every push runs the tests. a red check is not merged
- CD = a green main can deploy. we still know which commit is on the server
- GitHub Actions is the runner we use. a workflow file in `.github/workflows` lists the steps
- a job checks out the repo, installs, and runs the test script
- a secret in the workflow comes from the repo settings, not from the file
- a cloud server is someone else's machine with an API. the nouns are compute, disk, network, and identity
- a VM is a computer. a managed database is Postgres we do not patch ourselves, and we still design backups
- a security group is a firewall. which ports, from where
- object storage is the blob store for video
- the bill follows CPU, disk, and egress
- we name the machine in front of us. we do not invent a list of AWS products we have not opened
- the picture's cloud line was under the play button. the ideas are the VM, the firewall, the disk, and the object store

```yaml
name: test
on: [pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: npm ci
      - run: npm test
```

- `npm test` is Vitest or node:test, whichever the repo uses
- the workflow does not print the database password

- homework of chapter 7
```yaml
# 7a  when this workflow runs
# 7b  the step that must fail the pull request if a test fails
# 7c  a cloud noun for "who may open port 443"
# 7d  why a public video without a cache shows up on a bill
```

## chapter 8 Terraform and Ansible

- Terraform = a file that describes infrastructure. we plan, then we apply
- the state file remembers what Terraform created. we do not edit the cloud by hand and also let Terraform own it, or they drift
- state often contains secrets. it is not a public file
- Ansible = SSH and a list of tasks that make a server match a description. install nginx, copy a unit file, restart
- Terraform is better at "create the VM and the disk". Ansible is better at "the packages and the config files on that VM"
- we may not have either in the current deploy. the deploy we have is Docker, nginx, PM2, and GitHub Actions
- the words still have to be precise

```hcl
resource "local_file" "example" {
  filename = "hello.txt"
  content  = "hello"
}
```

```yaml
- name: nginx is installed
  apt:
    name: nginx
    state: present
```

- `plan` shows the change. `apply` does it. we read the plan
- an Ansible task should be safe to run twice. install "present" is. a blind append to a file is not

- homework of chapter 8
```text
# 8a  what Terraform state remembers
# 8b  why we do not commit a state file full of secrets
# 8c  a task that is safe to run twice, and one that is not
# 8d  the deploy tools we have actually used
```

## chapter 9 nginx and load balancers

- nginx is the front door. TLS, the static build, and `/api` proxied to Nest
- Caddy can do the same with automatic certificates. Anemi's notes include Caddy
- a load balancer spreads connections across healthy upstreams
- one upstream is still a front door. two upstreams are a balancer
- `proxy_pass` is the hop to Node
- we send the original host and the client IP if the app needs them
- WebSocket needs the upgrade headers
- a 502 means nginx could not get a valid answer from upstream

```nginx
server {
  listen 443 ssl;
  location /api/ {
    proxy_pass http://127.0.0.1:3000;
    proxy_set_header Host $host;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection "upgrade";
  }
  location / {
    root /var/www/app;
    try_files $uri /index.html;
  }
}
```

- `try_files` sends unknown paths to the single-page app
- the API location is a proxy. the page location is files
- least-connections versus round robin matters when some requests are long sockets and some are quick reads

- homework of chapter 9
```nginx
# 9a  which location is files, which is the API
# 9b  what a 502 points at
# 9c  the headers a WebSocket upgrade needs
```

## chapter 10 Prometheus, Grafana, and ELK

- Prometheus scrapes a metrics URL on an interval
- a counter only goes up. requests total. a gauge can go down. queue depth, memory
- a histogram is for duration. we can ask for a percentile later
- Grafana draws the Prometheus data
- a useful board is HTTP duration and queue depth, not a chart nobody opens
- ELK = Elasticsearch, Logstash or an agent, and Kibana. logs go in, we search them
- we may ship logs to a file and to Sentry for exceptions. ELK is the search stack when the files are not enough
- a log line has a request id. it does not have a password or a token
- Sentry is the exception with a release id. Prometheus is the number over time. they answer different questions

```text
http_requests_total{route="/port-calls",status="500"}
queue_depth{name="laytime"}
```

- a 500 rate and a rising queue depth are the two pictures that page someone
- a log without a request id cannot be tied to the metric spike

- homework of chapter 10
```text
# 10a  counter or gauge: queue depth
# 10b  counter or gauge: requests total
# 10c  what Sentry has that Prometheus does not
# 10d  two fields that never go in the log line
```

## chapter 11 Blue-green, autoscaling, and secrets

- blue-green = two copies of the app. one is live. we deploy the other, test it, then move the front door
- if the new copy is bad, the front door moves back
- a database migration has to work on both copies during the switch, or we migrate in a way the old code still understands
- rolling deploy = replace one process at a time. PM2 and a second upstream can do a small version of this
- autoscaling = add or remove machines from a metric. CPU, request count, queue depth
- scale the thing that is busy. API CPU is not a reason to add Postgres replicas by magic
- a scale-in that kills a worker mid-job needs the job to be retryable
- a secret = a password, a token, a key. it lives in the environment or a secret store, not in git
- the app reads `process.env`. the file `.env` is local and ignored
- rotate a secret by adding the new one, deploying, then removing the old one. a JWT signing key needs a moment where both verify

```text
blue: live, old release
green: new release, not in the upstream yet
test green
point nginx at green
keep blue until the graphs look normal
```

- we have shipped nginx, PM2, Docker, and GitHub Actions. blue-green is the pattern. a second upstream is the small version
- autoscaling on queue depth fits the laytime worker. autoscaling the API does not fix a slow query

- homework of chapter 11
```text
# 11a  what has to be true of a migration during blue-green
# 11b  a metric that should add a worker, not an API process
# 11c  where a database password lives, and where it does not
# 11d  why a signing-key rotation has an overlap
```

## chapter 12 A deploy we can walk

- a pull request runs GitHub Actions
- merge to main builds an image or a Node build
- the server pulls it. PM2 reloads the process
- nginx keeps the public port
- Postgres stays up. we run a migration as its own step, before the new code expects the column
- Sentry gets the release id so an exception names the deploy
- Anemi's box may be Caddy instead of nginx. the hop is the same idea

```text
pull request -> tests
main -> build
server -> migrate -> reload process -> watch errors and latency
```

- rollback is the previous image and, if the migration was backward compatible, the previous process
- a migration that deletes a column is not in the same minute as the code that stops writing it. stop writing first, deploy, then delete

- homework of chapter 12
```text
# 12a  the order: migrate, or reload, and why
# 12b  what we watch for ten minutes after
# 12c  the tools in this path we have actually run
# 12d  Anemi's front door if it is not nginx
```
