
```bash
[Unit]
Description=My Custom Service
Documentation=https://example.com/docs
After=network.target
Wants=network-online.target

[Service]
# Service type
Type=simple

# User and group to run service under
User=myuser
Group=mygroup

# Working directory for the process
WorkingDirectory=/opt/my-service

# Main executable
ExecStart=/usr/bin/my-binary --config /etc/my-service/config.yaml

# Optional Exec settings
ExecReload=/bin/kill -HUP $MAINPID
ExecStop=/bin/kill -TERM $MAINPID

# Restart behavior
Restart=on-failure
RestartSec=5

# Logs
StandardOutput=append:/var/log/my-service/info.log
StandardError=append:/var/log/my-service/error.log

# Environment variables
Environment="ENV_VAR1=value1"
Environment="ENV_VAR2=value2"

[Install]
WantedBy=multi-user.target
```

