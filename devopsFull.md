# DevOps

## Linux and Bash

- The server is Linux. Bash is how you look at it before you change it.
- pwd, ls, cd move you. cat and less read a file. tail -f follows a log.
- ps and ss show processes and ports. A programme that is not listening is not a proxy problem.
- grep finds a line. Do not grep a secret into a shared screen if you can avoid it.
- A shell script has set -euo pipefail if you ship it, so a failed command does not continue.
- Linux is the building. Bash is walking the corridors with a torch before you call a builder.
- careful: Running a command you copied, as root, against production, because a forum said so.
- The site is down. What is the first command?
- I check whether the process is up and whether the port is listening, then the last lines of the nginx error log. I do not redeploy first.

```bash
ss -ltnp | head
tail -n 100 /var/log/nginx/error.log
```

- homework
```bash
ss -ltnp | head
tail -n 100 /var/log/nginx/error.log
```

## Networking basics

- You need the path of one request: name, address, port, proxy, process.
- DNS resolves the name. TCP connects to the address and port. TLS wraps it. HTTP is the message.
- curl -v shows the path. It is the tool I trust before I trust a theory.
- A firewall drop looks like a timeout. A refused connection means nothing is listening.
- Inside Docker, localhost is the container.
- Networking is the road, the gate, and the door. Say which one is shut.
- careful: Restarting Node when DNS is what failed.
- Timeout or connection refused?
- Refused: the host answered and nothing is on that port. Timeout: a firewall, a route, or a process that never accepts. They are different bugs.

```bash
curl -v https://vms.arrobin.com/health
```

- homework
```bash
curl -v https://vms.arrobin.com/health
```

## Git and GitHub

- Git is the history of the code. GitHub is the place the history is reviewed.
- A commit is a snapshot with a message that says why.
- A branch is a line of work. A pull request is the review.
- main is deployable. You do not push broken experiments straight to it.
- Rebase rewrites your unpushed commits. Do not rebase a branch other people have pulled, unless you have agreed.
- Git is a notebook you cannot quietly tear a page out of once it is shared.
- careful: A commit of node_modules, .env, or a database dump.
- What is in a good commit message?
- The why. 'Fix bug' is not a message. 'Ignore weather hours in the laytime window' is.

```bash
git checkout -b laytime-weekend-rule
git commit -m "Treat weather delays as exceptions in laytime"
```

- homework
```bash
git checkout -b laytime-weekend-rule
git commit -m "Treat weather delays as exceptions in laytime"
```

## Docker

- Docker runs a process in a filesystem you built, so the server and the laptop share the same libraries.
- A Dockerfile starts FROM a base image, copies the app, installs dependencies, and sets the command.
- An image is the recipe's result. A container is a running image.
- Layer order matters. Copy the lockfile and install before you copy the source, so a code change does not reinstall the world.
- Do not run as root inside the image if you can add a user. Do not copy secrets into the image.
- Docker is a shipping container. The crane does not care what is inside, as long as the doors match.
- careful: A latest tag in production, so Monday's build is not Tuesday's build.
- Image or container?
- The image is the packed box. The container is the box opened and running. I can start two containers from one image.

```docker
FROM node:22-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
```

- homework
```docker
FROM node:22-alpine
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm ci
COPY . .
CMD ["node", "dist/main.js"]
```

## Docker Compose

- Compose starts several containers with one file and one network.
- Services: api, db, redis. depends_on waits for the process to start, not for Postgres to be ready to accept queries. A health check or a retry in the app covers that.
- A named volume keeps the database across compose down. An anonymous volume does not, once it is removed.
- The service name is the DNS name. The API uses db:5432, not localhost.
- Compose is how you develop and how you might run a single server. It is not a multi-node cluster.
- Compose is one kitchen with several cooks who know each other by name.
- careful: Putting the database password in the file and committing it.
- Why did the API fail on the first second?
- Postgres was not ready. depends_on only waits for the start. I retry the connection, or I use a health check.

```yaml
services:
  api:
    build: .
    depends_on: [db, redis]
  db:
    image: postgres:16
    volumes: [pgdata:/var/lib/postgresql/data]
volumes:
  pgdata:
```

- homework
```yaml
services:
  api:
    build: .
    depends_on: [db, redis]
  db:
    image: postgres:16
    volumes: [pgdata:/var/lib/postgresql/data]
volumes:
  pgdata:
```

## Kubernetes

- Kubernetes runs containers across machines. It restarts them, rolls them out, and attaches services.
- A Pod is one or more containers. A Deployment keeps a number of Pods alive.
- A Service is a stable address in front of Pods that come and go.
- A ConfigMap is configuration. A Secret is a secret, and it is not magically safe just because of the name.
- You do not need a cluster for one VPS and PM2. Say that. Then show you know the nouns.
- Kubernetes is a harbour master for containers. A harbour master is a lot of staff for one boat.
- careful: Drawing a cluster for a project that fits on one box, and calling that senior.
- Have you run it in production?
- If you have not, say no. I know the objects, and on a single machine I use Compose and PM2. I would reach for Kubernetes when we have several machines and a need to roll Pods without a custom script.

```
Deployment keeps 2 API pods
Service routes to their labels
readiness probe hits /health
```

- homework
```
Deployment keeps 2 API pods
Service routes to their labels
readiness probe hits /health
```

## Helm

- Helm is a package manager for Kubernetes. A chart is a templated set of manifests.
- values.yaml is the settings: image tag, replica count, host name.
- The templates render Deployments and Services.
- A release is one install. You can roll it back.
- Without Kubernetes, Helm has nothing to sit on. Do not study the flags before the objects.
- Helm is a form letter. The values are the blanks you fill for each office.
- careful: Copy-pasting the rendered YAML into production and losing the chart.
- Why template at all?
- The staging host and the production host differ. The chart is the shared shape. The values are the difference.

```bash
helm upgrade --install vms ./chart --set image.tag=1.4.2
```

- homework
```bash
helm upgrade --install vms ./chart --set image.tag=1.4.2
```

## CI/CD pipelines

- CI checks every change. CD delivers a change that passed.
- On a pull request: install, lint, test. Fail the merge if tests fail.
- On main: build an image, run migrations carefully, restart the process.
- The pipeline uses the same commands you use locally, or it becomes a second source of truth.
- A red main is a stop. You do not deploy around it.
- CI is the door check. CD is the van that leaves only if the check passed.
- careful: A pipeline that always goes green because the tests are skipped.
- What is the smallest pipeline worth having?
- Tests on the pull request, and a deploy of main that a human can also run by hand. A pipeline you cannot run locally will fail at midnight in a way you cannot see.

```
pull request -> npm test
main -> build image -> deploy
```

- homework
```
pull request -> npm test
main -> build image -> deploy
```

## GitHub Actions

- GitHub Actions is the CI you already point at. A workflow is YAML. A job runs on a runner. Steps are commands.
- on: pull_request runs the tests. on: push to main can deploy.
- Use the lockfile. npm ci, not npm install, so the runner matches the repo.
- Secrets live in the repository settings, not in the YAML.
- Cache the npm directory if the install time hurts. Do not cache your way past a failing test.
- Actions is a robot that follows the checklist you were going to forget at midnight.
- careful: A secret echoed in a debug step.
- Why npm ci?
- It installs the lockfile exactly and fails if the lockfile is out of date. npm install may change versions and you will debug a ghost.

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

- homework
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

## Cloud basics

- A cloud server is someone else's machine with an API. The nouns are compute, disk, network, and identity.
- A VM is a computer. A managed database is Postgres you do not patch yourself, and you still design backups.
- A security group is a firewall: which ports, from where.
- Object storage is the blob store.
- The bill follows CPU, disk, and egress. A public video without a cache is an egress bill.
- The cloud is a rented building. You still lock the doors.
- careful: Opening port 5432 to the world so the laptop can connect.
- Which cloud do you use?
- Name the one in front of you, or say the site is a VPS you administer. Do not invent AWS services you have not opened. The ideas, firewall, disk, and object storage, transfer.

```
VM runs nginx and the API
managed Postgres, or Postgres on the VM if that is what you operate
object storage for video
```

- homework
```
VM runs nginx and the API
managed Postgres, or Postgres on the VM if that is what you operate
object storage for video
```

## Terraform

- Terraform describes servers and networks as code, and applies the difference.
- You write resources. terraform plan shows what would change. apply does it.
- The state file is the map of real ids. Lose it carelessly and Terraform wants to recreate the world.
- Do not commit secrets into the files. The state can contain secrets too, so the state is not a public bucket.
- For one VPS edited twice a year, a documented script may be enough. Say the threshold.
- Terraform is a shopping list the shop will fulfil, and a notebook of what you already bought.
- careful: Applying a plan you did not read, because it said 12 to destroy.
- What is drift?
- Someone changed the firewall in the console. The code no longer matches reality. plan shows the drift. I decide whether the code or the console is the mistake, then I make them match.

```
resource "server" "api" { image = "ubuntu-24" size = "2gb" }
```

- homework
```
resource "server" "api" { image = "ubuntu-24" size = "2gb" }
```

## Ansible

- Ansible configures machines over SSH from a list of tasks.
- A playbook installs nginx, copies a config, and restarts the service.
- It is idempotent when the modules are. Running it twice should be a no-op the second time.
- Inventory is the list of hosts.
- It complements images. Docker already has the app. Ansible might have the host: firewall, nginx, certificates.
- Ansible is a caretaker with a checklist. The second visit should find the house already in order.
- careful: A shell task that is not idempotent, so the second run appends the same line again.
- Ansible or a Dockerfile?
- The Dockerfile is the app. Ansible is the machine around it, if the machine is not rebuilt from an image every time. I do not configure application libraries both ways and hope.

```yaml
- name: install nginx
  apt: { name: nginx, state: present }
```

- homework
```yaml
- name: install nginx
  apt: { name: nginx, state: present }
```

## nginx reverse proxy

- nginx receives the public connection and passes it to Node.
- It terminates TLS, serves the static Next build, and proxies /api to 127.0.0.1:3000.
- proxy_set_header Host and the forwarded headers so the app knows the original scheme.
- client_max_body_size must allow a video upload, or Anemi fails with 413.
- WebSocket proxying needs the Upgrade headers, or Socket.IO falls over.
- nginx is the front door. Node is the office. A 502 means the office did not pick up.
- careful: Proxying sockets without the upgrade headers and debugging it as an application bug.
- What is a 502 from nginx?
- nginx is up and the upstream did not answer. Node is down, or the port is wrong, or the process is wedged. I look at the upstream, not at DNS.

```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000/;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
```

- homework
```nginx
location /api/ {
  proxy_pass http://127.0.0.1:3000/;
  proxy_set_header Host $host;
  proxy_set_header Upgrade $http_upgrade;
  proxy_set_header Connection "upgrade";
}
```

## Load balancers

- A load balancer is nginx, or a cloud box, spreading traffic across healthy copies.
- Round robin is the simple policy.
- Least connections helps when some requests are long, such as an upload.
- Health checks pull a bad copy out.
- On one machine, several Node processes behind nginx are already a small balancer.
- The balancer is the person at the door with a counter, sending the next guest to a free desk.
- careful: No health check, so a dead process still gets guests.
- Sticky or not?
- Not, if the process is stateless. Sticky hides a session stored in memory. I would rather put the session in Redis or use the JWT we already have.

```nginx
upstream api { least_conn; server :3000; server :3001; }
```

- homework
```nginx
upstream api { least_conn; server :3000; server :3001; }
```

## Prometheus

- Prometheus scrapes metrics: numbers your process exposes.
- A counter only goes up, such as http_requests_total.
- A histogram measures duration.
- A gauge is a level, such as queue depth.
- You add a label for the route, not for the user id. A label with unbounded values will exhaust the server.
- Prometheus is a clipboard of numbers taken every few seconds. It is not a diary of individual requests.
- careful: A label per user id or per port call id.
- Counter or gauge for queue depth?
- Gauge. Depth goes up and down. A counter is for events that accumulate, such as jobs completed.

```
http_requests_total{route="/port-calls",status="201"}
queue_depth{queue="laytime"}
```

- homework
```
http_requests_total{route="/port-calls",status="201"}
queue_depth{queue="laytime"}
```

## Grafana

- Grafana draws the Prometheus numbers and pages you when a rule fires.
- A dashboard for request rate, error rate, duration, and queue depth is enough to start.
- An alert on error rate over a threshold for five minutes beats an alert on every exception.
- Look at the deploy marker. A cliff at deploy time is the release.
- A dashboard nobody opens is decoration. Tie it to a question you have actually asked.
- Grafana is the glass on the clipboard. The alert is the person who rings you when the number is bad for long enough to be real.
- careful: An alert on a one-second spike that pages you every night.
- What do you alert on?
- Symptoms a user feels: errors and a stuck queue. Not CPU at 40 percent, which might be a healthy encode.

```
alert: 5xx ratio > 2% for 5 minutes
alert: laytime queue depth > 100 for 10 minutes
```

- homework
```
alert: 5xx ratio > 2% for 5 minutes
alert: laytime queue depth > 100 for 10 minutes
```

## ELK logging

- ELK is Elasticsearch, Logstash, and Kibana. Logs go in, and you search them. The idea matters more than the brand.
- A structured log, JSON, with a request id, is searchable. A pretty sentence is not.
- Kibana, or any UI, filters on the request id so one failed save shows every line.
- Keep retention finite. Disk fills.
- Sentry is for exceptions. The log is for the path. You can run both.
- ELK is a library of every note the building wrote, with a catalogue.
- careful: Logging the token so you can 'debug auth'.
- Sentry or ELK?
- Sentry when an exception needs a stack and a release. The log pipeline when I need to follow one request across nginx and the API. I do not pick one and throw away the other kind of question.

```json
{"requestId":"abc","msg":"port call created","ms":40}
```

- homework
```json
{"requestId":"abc","msg":"port call created","ms":40}
```

## Blue-green deploys

- Blue-green means two full environments. One serves traffic. You deploy the other, test it, and switch.
- Green is the idle copy. You deploy there. You smoke-test. You move the proxy.
- Rollback is moving the proxy back, if the database migration is compatible.
- A migration that deletes a column cannot roll back with the proxy alone.
- On one machine this may be two directories and a symlink nginx follows. The idea is the same.
- Blue and green are two stages. The audience hears one. You change which stage the speakers are plugged into.
- careful: A destructive migration in the same minute as the switch.
- Why is the migration the hard part?
- The old code and the new code share the database during the switch. The schema must work for both until the old one is gone. Expand, then contract.

```
proxy -> blue (live)
deploy green, test green, proxy -> green
```

- homework
```
proxy -> blue (live)
deploy green, test green, proxy -> green
```

## Auto scaling

- Auto scaling adds or removes machines from a signal, such as CPU or queue depth.
- Scale the API on CPU or request latency.
- Scale workers on queue depth. That is the signal that means laytime is waiting.
- Set a maximum. A bug that enqueues forever should not buy infinite machines.
- A scale-up that is faster than your boot time will flap. Add a cooldown.
- Auto scaling is hiring temporary staff when the queue at the door is long, and sending them home when it is short, with a cap so you do not hire the whole town.
- careful: Scaling on CPU during a backup and doubling the fleet every night.
- What happens if you scale the API and not the database?
- You add clients to a tired Postgres. Latency gets worse. The scaler then adds more API. I scale the thing the metric says is saturated, and I watch the database.

```
queue depth high for 5 minutes -> one more worker
maximum workers = 4 until you know the database can take them
```

- homework
```
queue depth high for 5 minutes -> one more worker
maximum workers = 4 until you know the database can take them
```

## Secrets management

- A secret is a password, a key, or a token. It does not belong in git.
- .env is local. Production reads the environment from the host, or from a secret store.
- GitHub Actions secrets are for the pipeline. They are not printed in logs.
- Rotate a key that leaked. Assume the old one is public.
- The database password, the JWT signing key, the Stripe secret, and the TOTP encryption key are the list for your products.
- A secret is a house key. You do not photocopy it into the group chat or the repository.
- careful: A private repository treated as a safe. Private only means fewer readers, not none, and forks and logs exist.
- You committed a key. What now?
- I revoke it at the provider, issue a new one, put the new one in the environment, and remove the file from git. Deleting the commit is not enough if it was pushed. The old key is burned.

```
process.env.DATABASE_URL
never: git add .env
```

- homework
```
process.env.DATABASE_URL
never: git add .env
```
