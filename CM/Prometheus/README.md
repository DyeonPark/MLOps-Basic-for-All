# Prometheus
- 오픈 소스 모니터링 솔루션
- 메트릭을 추적하고 그에 따른 알람 기능 제공
- 구글의 Borgman에서 영감을 받은 솔루션

<br/>

### Prometheus의 특징
- PromQL이라는 Filxible Query Language를 포함함 (READ only Language)
- Built-in expression Browser를 사용하여 시각화가 가능함
- Grafana와 함께 사용할 수도 있음
- 수집된 모든 메트릭은 메모리 혹은 로컬 디스크에 효율적인 형태로 저장됨
- Go언어로 작성되었음

<br/>

### Prometheus의 구조
![Alt text](Images/image.png)
* 프로메테우스 서버에서 end-point를 통해 클라이언트에서 데이터를 불러옴 (pull metrics)
* 불러온 데이터를 HDD/SDD에 저장
* Alertmanager를 활용하여 경고 및 알람을 보낼 수도 있음
* PromQL을 사용하여 데이터를 내보내 웹 UI 혹은 Grafana로 시각화된 결과를 보여줄 수 있음


<br/>

**Prometheus Server**
* 모니터링 타겟을 HTTP end-point를 통해 모니터링 "데이터"를 긁어옴 (각 타겟에서 필요한 데이터만!)
* 긁어온 데이터를 토대로 모니터링
* 초당 최대 백만개의 타임 시리즈 데이터를 긁어올 수 있음


**Prometheus PushGateway**
* 배치 혹은 단기로 이뤄짐으로써 짧게 존재하는 데이터를, 프로메테우스 서버가 긁어갈 수 있도록 데이터가 좀 더 오랫동안 존재할 수 있게 해줌
* 해당 데이터들을 프로메테우스 서버에 노출시켜 서버가 긁어가게 함


**Exporters and Intergrations**
* 서드파티 시스템을 통해 데이터를 프로메테우스 메트릭으로 수집할 수 있게 해줌
* 프로메테우스 서버가 직접적으로 계측할 수 없는 데이터들도 수집할 수 있게 함 (예: HAProxy, Linux System stats)

**Prometheus Alertmanager**
* 클라이언트 앱이 보내는 경고를 처리하거나, 프로메테우스 서버에서 보내는 알람을 전송시킬 수 있음
* 알람 복제, 그룹핑, 라우팅이 가능함

**Service Discovery**
* end-point를 찾아서 메트릭 데이터를 긁어가게 해줌
* prometheus.yaml 파일을 구성하여, 데이터를 긁어올 엔드포인트를 알려주고, 수행할 잡을 커스터마이징

**PromQL**
* Prometheus Querying Language
* 그래프로 결과를 내보내거나 HTTP API로 내보낼 수도 있음

<br/>

### Prometheus Metric and Type
* 4 core metric Type (Counter, Gauge, Histogram, Summary)

**Counter**
* cumulative metric (only increasing or zero)
* ex: number of requests, task completed, errors

**Gauge**
* singel numerical value (can up or down)
* ex: memory usgae, cpu temperatures

**Historgram**
* sample observation
* provide sum of all observerd value
* ex: request duration, reponse size

**Summary**
* summary samples observation (similary to histogram)
* total count of observations
* ex: request durations, reponse size

