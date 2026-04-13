## Docker Swarm node 추가 하기
- subnet 이 private 일 경우 외부 접속이 안되니, 무조건 public 으로 설정.
```bash
sudo dnf install -y docker
sudo systemctl enable docker
sudo cat <<EOF > /etc/cron.daily/docker-cleanup
#!/bin/bash
/usr/bin/docker system prune -af --filter "until=24h" || exit 1
/usr/bin/docker image prune -af --filter "until=24h" || exit 1
/usr/bin/docker volume prune -af || exit 1
EOF
sudo chmod +x /etc/cron.daily/docker-cleanup
sudo reboot
```

## NLB/ALB sg 관련
- NLB 의 sg 그룹 설정시 private ip 를 사용하지만, EC2에 사용자의 public ip로 접속이 들어 올수있음
- 내부 구현 문제일듯. TLS 설정 안된 TCP 는 그냥 bypass 된다고 생각하면 됨.