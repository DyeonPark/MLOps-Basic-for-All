
# CM (Continuous Monitoring)
- DevOps 또는 MLOps 파이프라인의 각 단계마다 준수 이슈와 보안 위협을 관찰, 감지할 수 있는 자동화된 파이프라인

<br/>

### CM Tools in DevOps
- **Monitoring Tools**: 인프라와 응용 프로그램의 성능을 모니터링 (ex: Prometheus, Sensu, Nagios)
- **Alerting Tools:** 실행 가능 상태에 따른 알람 제공 → 너무 많은 알람을 보내지 않는 것에 유의해야 함 (ex: Slack, PagerDuty, Servicenow)
- **Metric Storage**: 분석용 데이터를 저장할 저장소 (ex: Splunk, AWS, influxdb)
- **Visualization Tools**: 저장소에 있는 데이터를 기반으로 데이터 분포 및 시간에 따른 형상을 실시간으로 볼 수 있는 대시보드 제공 (ex: Grafana)

### Why CM is Important
- **Prometheus** 활용한다면? → 회사 시스템 운영에 필요한 수치 데이터를 수집 및 제공 및 시스템 모니터링기능 제공
- **Grafana**를 활용한다면? → 어떤 시스템이든 쉽게 데이터를 읽어와서 시각화 기능을 제공함
- Prometheus로 수집한 메트릭을 이용해 Grafana로 대시보드를 만들어 **이해관계자들과 업무 및 메트릭 공유가 용이**해짐

