# WSL 부팅 시 postgresql 자동 실행
```bash
$ sudo visudo

sungminyou ALL=(ALL) NOPASSWD: ALL 추가

$ echo sudo service postgresql start >> ~/.bashrc
```
