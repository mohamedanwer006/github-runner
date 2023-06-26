# github-runner

- setup new self hosted runner  


Create runner service on ubuntu

`sudo vim /etc/systemd/system/github_runner.service`

```
[Unit]
Description=Example Service
After=network.target
StartLimitIntervalSec=0

[Service]
Type=simple
Restart=always
RestartSec=1
User=ubuntu
ExecStart=/home/ubuntu/actions-runner/run.sh

[Install]
WantedBy=multi-user.target
```

