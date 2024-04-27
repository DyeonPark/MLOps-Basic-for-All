# Grafana
- 웹 어플리케이션을 상호작용 가능하게 시각화할 수 있도록 해주는 오픈소스

### Grafana의 특징
- 데이터를 잘 이해할 수 있도록 시각화해주는 다양한 옵션을 제공함
- 데이터에 대한 알람 기능을 제공
- 수백개의 공식 라이브러리를 제공함
- 데이터와 대시보드를 공유할 수 있도록 함 (팀 작업에 좋다!)
- 다양한 종류의 데이터베이스에 사용할 수 있도록 지원함 (프로메테우스의 데이터 소스도 가능!)

<br/>

### Grafana 설치방법
실습 참고 링크: [Prometheus-Grafana-Docs](https://github.com/manifoldailearning/Prometheus-Grafana-Docs/tree/main/scripts)
```shell
chmod u=rwx,g=r,o=r 3-install-grafana.sh
./3-install-grafana.sh
sudo service grafana-server status
```
- 로컬 호스트의 3000번 포트로 서비스됨
- 해당 주소에 접속하면 관리자 페이지를 볼 수 있음
- 기본 설정 admin / admin
- 관리자 페이지에서 Connections > Data sources > Prometheus
- 프로메테우스의 서비스 URL 포트를 입력하면 연결 가능!