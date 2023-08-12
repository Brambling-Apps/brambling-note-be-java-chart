# Brambling Note Backend Java Helm Chart

## Install
See [Brambling-Apps/helm-chart-actions](https://github.com/Brambling-Apps/helm-chart-actions)

## values.yaml
```yaml
global:
  postgresql:
    auth:
      username: "brambling-note"
      password: "mH7Ah0u7WgosNm1g"
      database: "brambling-note"
# Send verification email to user
smtp:
  host: ""
  port: "587"
  starttls: "true"
  ssl: "false"
  auth:
    enabled: "false"
    email: ""
    password: ""
verification_email:
  subject: "Verify your account"
  # %s is the placeholder of verification codes from verification email
  content: "Click this link to verify your account: http://brambling-note.local/verification/%s"
```

## Usage
```
kubectl port-forward services/brambling-note-frontend-service <port-you-want>:8080
```
