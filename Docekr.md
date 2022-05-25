1. Docker란?
- 가상화 기술. 가상화 컨테이너에 application 배포를 자동화시켜주는 오픈소스 엔전
- container 가상화 실행 환경 위에 application 배포 엔진을 더함으로서 사용자의 코드를 어디서든 빠르고 가볍게 실행시킬수 있는 기술을 제공

2. Hypervisor가상화 vs Container가상화

1) Hypervisor가상화
- 물리적인 서버에서 하나 혹은 그 이상의 독립적인 운영체제가 돌아가는 구조. 즉 물리적 서버의 OS 위에 여러 다른 독립적인 OS가 가상적(virtually)으로 돌아가는 구조
- 이러한 가상화의 장점은 물리적 서버의 리소스를 더 효율적으로 사용할수 있다는 것에 있다.
- hypervisor 가상화를 사용하여 하나의 서버에 여러 OS를 실행시키면 CPU를 idle 상태로 두지않고 필요한 OS나 서비스에 할당이 되어질 수 있음으로 리소스를 훨씬 효율적으로 쓰게 된다.
- 단점은 기술적으로 너무 무겁다(heavy-weight)는 것.

2) Container가상화
- hypervisor 가상화와 틀리게 OS의 커널 위의 유저 공간(user space)에서 실행된다. 즉 완전히 독립적인 운영체제를 가상화 하는 것이 아니라 독립적인 user space를 가상화 한다고 생각하면 쉽다.
- 즉 하나의 호스트 서버에서 여러 독립적인 user space 인스탄스들을 가상적으로 실행할 수 있게 되는 것
- hypervisor 가상화 보다 훨씬 가볍기 때문에 빠르고 쉽게 독립적인 가상 환경을 실행시킬수 있다
- 예를 들어 docker image만 있으면 어디서든 쉽고 빠르게 test 환경, sandbox 환경 및 production 배포를 할 수 있다. 그래서 최근에 널리 퍼져있는 MSA(Micro Service Architecture)와 CI/CD에 아주 잘 어울리는 가상화 기술로서 각광을 받고 있다.

3. Docker 구조

1) Docker client 와 server
- 클라이언트가 서버에 명령을 전달하고 서버가 실행시키는 구조
- docker binrary 커맨드가 docker 클라이언트 이고 dockerd 가 docker daemon 혹은 docker engine이다.

2) Docker 이미지
- Docker의 life cycle에서 docker 이미지는 “build”의 부분에 해당
- Docker container에서 실행시키고 싶은 application을 docker 이미지로 빌드해서 실행시키게 된다.

3) Docker registries
- docker 이미지를 저장하는 repository
- Source code를 github에 저장하여 관리하듯 docker 이미지는 dockerhub 같은 docker registries에 저장한다고 생각
- Github가 마찬가지로 public registry 가 있고 private registry가 있다.

4) Docker containers
- Docker container에서 docker 이미지가 실행
- docker 이미지를 실행시키는 가상화 공간
- Docker container는 하나 혹은 그 이상의 프로세스를 실행 시킬수 있다 (하지만 하나의 프로세스만 실행시키는 것을 권장).

5) Docker Compose And Swarm
- Docker에서는 여러 docker container들로 이루어진 stack이나 cluster를 관리 하는 서비스도 제공하는데 바로 docker compose 와 docker swarm
- Docker compose는 복수의 docker container들을 모아서 종합적인 application stack을 정의 하고 운영할수 있도록 해주는 서비스
- Compose 파일을 사용하여 전체적인 application 서비스를 설정한후, application을 이루고 있는 각각의 컨테이너들 (예를 들어, web 서버 컨테이너, api 서버 컨테이너 등등)을 따로 실행시킬 필요 없이 한번에 생성하고 실행할 수 있도록 해준다.
- Docker swarm은 docker containers 들로 이러우진 cluster를 관리할수 있도록 해주는 서비스이다. 즉 docker container를 위한 clustering tool

## 참고자료
https://cultivo-hy.github.io/docker/image/usage/2019/03/14/Docker%EC%A0%95%EB%A6%AC/
