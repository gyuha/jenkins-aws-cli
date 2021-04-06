# jenkins-aws-cli

1. 폴더를 만들어 줍니다.
```
mkdir jenkins_home
chmod 777 jenkins_home
```

2. docker-compose를 실행 해 준다.
```
docker-compose up -d
```


3. 초기 암호를 입력하기 위해서 아래와 같이 실행 한다.
```
docker exec -it jenkins-awscli bash
cat /var/jenkins_home/secrets/initialAdminPassword
```

## jakins 컨테이너 root로 접근하기
```
docker exec --user root -it jenkins bash
```

## 시스템 상태 조회
http://[SERVER_ID]:8080/systemInfo

## Reference
* [Jenkins Docker with AWS CLI](https://gist.github.com/plecong/b07c900ce0aa99eac3e77de8b0d224f0)
