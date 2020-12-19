## docker 기본 명령어

### container 강제종료/삭제(-f 묻지 않고 삭제)
- docker rm -f [container name]

### image 강제종료/삭제(-f 묻지 않고 삭제)
- docker rmi -f [image name]

### 사용하지 않는 볼륨만 제거(-f 묻지 않고 제거)
 - docker volume prune -f

### 사용하지 않는 이미지 제거(-f 묻지 않고 제거)
 - docker rmi $(docker images -f "dangling=true" -q)
 - docker image prune -f

### docker volume list show
 - docker volume ls
 
### docker 컨테이너 삭제시 volume 같이 제거
 - docker rm -v <container id or name>
 - 컨테이너가 중지되면 고정 장치 볼륨이 자동으로 제거되지 않습니다. 컨테이너를 중지 할 때 연관된 볼륨을 제거하려면 다음과 같이하십시오.

### docker volume 상세보기
 - docker inspect volume [voumne name]
