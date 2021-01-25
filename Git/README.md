# Git 설정 및 명령어

1. ssh로 접속하기

+ step1 키 생성
```bash
# ssh키 생성
$ ssh-keygen -t rsa -b 4096 -C "git@email"

> Enter file in which to save the key: id_rsa_사용할 키 이름

# ssh-agent 실행 여부 확인
$ eval "(ssh-agent -s)"

$ ssh-add ~/.ssh/id_rsa_사용할 키 이름
```

+ github 사이트 가서 setting > SSH and GPG keys에 New SSH key 클릭
+ 만들어진 ssh키 중 id_rsa_사용할 키 이름.pub의 내용을 그대로 복사해서 만들기
+ remote 원격 저장소 ssh주소로 변경

2. submodule 등록
```bash
$ git submodule add << url >>
```

3. submodule 제거
```bash
$ git submodule deinit -f <<app>>

$ rm -rf .git/modules/<<app>>

$ git rm -f <<app>>
```

4. refusing to merge unrelated histories 에러(원격 저장소에 readme만들고, 기존 로칼에서 관리하던 log가 충돌나는 경우 자주발생함)

```bash

$ git pull origin 브런치명 --allow-unrelated-histories

```