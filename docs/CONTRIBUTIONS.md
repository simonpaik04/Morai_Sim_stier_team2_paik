# 기여 근거와 작성 커밋

검토일: 2026-10-08. 팀 main `42fdefa812747820b635231a0ab36845d58cdb7e`, paik `45ded67d34008c57b43f793ce3825c29f32e5d66`를 기준으로 기록했습니다.

작성자 이름과 이메일이 `simonpaik04 <simonpaik04@gmail.com>`인 비병합 커밋을 추출하고 대표 변경은 GitHub의 작성자 계정 연결과 diff·현재 코드·검증 문서로 대조했습니다. 병합 커밋은 제외했으며, main 포함 커밋과 paik에만 있는 커밋을 분리해 중복 없이 기록했습니다.

## 대표 변경과 현재 상태

| 분야 | 대표 커밋 | 확인 대상 | 상태 |
| --- | --- | --- | --- |
| 중앙 아키텍처·통신 | [0e59ed4](https://github.com/Team-Stier/Morai_Sim_team2/commit/0e59ed44ac0ffb96711ce221528897fd9159425c) | [TF·timestamp 계약과 UDP 브리지](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/ros_architecture_pkg/config/interface_contract.yaml) | main 반영 |
| HD Map | [014f9f1](https://github.com/Team-Stier/Morai_Sim_team2/commit/014f9f1203613b988251cc074ff78646626cb72f) | [MGeo/Lanelet2 변환·지도 뷰어](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/hd_map_pkg/README.md) | main 반영 |
| RDDF 연결 | [c494db8](https://github.com/Team-Stier/Morai_Sim_team2/commit/c494db8771b9af663afce11d25bf763ad90168a7) | [고주로 차선 RDDF 연속 연결](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/hd_map_pkg/docs/lane_rddf.md) | main 반영 |
| 체크포인트 합류 | [bef648c](https://github.com/Team-Stier/Morai_Sim_team2/commit/bef648c80afc949ea36df462e3f0247e83950924) | [CP11 통과 경로 수정](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/hd_map_pkg/docs/lane_rddf.md) | main 반영 |
| 위치 재배치 복구 | [ed31781](https://github.com/Team-Stier/Morai_Sim_team2/commit/ed317818186e74c8fd2a74e298683a2573dcf8d1) | [GPS·IMU 재초기화 연결](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/localization_pkg/README.md) | main 반영 |
| LiDAR 수평화 | [ecc0503](https://github.com/Team-Stier/Morai_Sim_team2/commit/ecc0503156e1204df0c0030356606e37f65d69a4) | [측정시각 자세 보간과 실시간 C++ 전처리](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/lidar_perception_pkg/src/horizontalization.cpp) | main 반영 |
| 자차 반사점 제외 | [656f280](https://github.com/Team-Stier/Morai_Sim_team2/commit/656f2800e595f7f7d2d51cbdb435526426118557) | [센서 좌표 자차 영역 필터](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/lidar_perception_pkg/README.md) | main 반영 |
| 지면 제거 | [e9fae2d](https://github.com/Team-Stier/Morai_Sim_team2/commit/e9fae2dc89166a27da9e1457872b69290c96196e) | [구역별 지면 처리](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/lidar_perception_pkg/docs/ground_filter.md) | main 반영 |
| 객체 추적 | [75cf54c](https://github.com/Team-Stier/Morai_Sim_team2/commit/75cf54c47ca3896bd8d21fe45822ff43ea21de06) | [map 변환·track ID·수명 관리](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/world_model_pkg/src/world_model_pkg/tracking.py) | main 반영 |
| 점군 속도 추정 | [b132c8a](https://github.com/Team-Stier/Morai_Sim_team2/commit/b132c8a49a60bee16e750bbabb59938299ed3f30) | [연속 클러스터 정합](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/world_model_pkg/README.md) | main 반영 |
| 경로 발행·reset | [6ecdc5a](https://github.com/Team-Stier/Morai_Sim_team2/commit/6ecdc5a77d8acbfe9cf42b78895ef7f10ffab1de) | [형상 보존·reset 결과 폐기](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/path_planning_pkg/docs/frenet_rddf.md) | main 반영 |
| 경로 최소 유지 | [f325c70](https://github.com/Team-Stier/Morai_Sim_team2/commit/f325c701b3327ef23aaa787b20b8361ffe54aa75) | [활성 경로·최신 대기 결과 관리](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/path_planning_pkg/docs/frenet_rddf.md) | main 반영 |
| RDDF 평활화 | [b4e650d](https://github.com/Team-Stier/Morai_Sim_team2/commit/b4e650d860a8b804dbbaa17c7a5a19703807b398) | [Gaussian 평균·이동 상한](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/path_planning_pkg/docs/frenet_rddf.md) | main 반영 |
| 평활화 상한 축소 | [cbcd937](https://github.com/Team-Stier/Morai_Sim_team2/commit/cbcd9375bec4c26c85c19bb8397f066c0f817107) | [현재 기본값 0.15m](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/path_planning_pkg/config/frenet_planner.yaml) | main 반영 |
| 제어 코어 통합 | [4573ac4](https://github.com/Team-Stier/Morai_Sim_team2/commit/4573ac4df76aadbc22fcdc14ebdd010fb34bca32) | [Closedteam2 제어 코어의 ROS 경계 연결](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/vehicle_control_pkg/docs/closedteam2_import.md) | main 반영 |
| RViz 진단 | [4ca0500](https://github.com/Team-Stier/Morai_Sim_team2/commit/4ca0500e11e3cb0d390bfd541c85803d7c01328f) | [현재 플래너·구간 표시](https://github.com/Team-Stier/Morai_Sim_team2/blob/42fdefa812747820b635231a0ab36845d58cdb7e/src/ros_architecture_pkg/docs/rviz_planner_status.md) | main 반영 |
| 터널 벽 지도 | [a8918cc](https://github.com/Team-Stier/Morai_Sim_team2/commit/a8918cc360f3e3ed8420a10b0056727e3ea830d5) | [벽선 HD Map·RViz 표시](https://github.com/Team-Stier/Morai_Sim_team2/blob/45ded67d34008c57b43f793ce3825c29f32e5d66/src/hd_map_pkg/docs/tunnel_walls.md) | paik만 반영 |
| 터널 벽 정합 | [a06cbe4](https://github.com/Team-Stier/Morai_Sim_team2/commit/a06cbe4bbd7da2606c31afdf8cd4a2802723ec1e) | [위치 추정기 연결](https://github.com/Team-Stier/Morai_Sim_team2/blob/45ded67d34008c57b43f793ce3825c29f32e5d66/src/localization_pkg/docs/tunnel_wall_matching.md) | paik만 반영 |

## 이식·통합과 이전 실험의 구분

- 팀의 기존 LiDAR 검출부를 가져온 작업(`e0cc454`)은 검출 알고리즘 전체를 처음부터 구현한 작업과 구분합니다. 수평화·자차 제거·지면 처리·추적 변경을 개인 기여로 설명합니다.
- 제어는 Closedteam2 코어를 중앙 ROS 경계에 연결한 이식·통합과 후속 파라미터 조정으로 소개합니다.
- 2026-09-22에는 Frenet의 정적 장애물 우회·복귀 후보를 실험했지만 `49e80e6`에서 해당 전용 기능을 삭제했습니다. 현재 Frenet 기능으로 소개하지 않습니다.
- 터널 벽 횡보정은 구현·연결·진단 확인 범위이며, 전체 터널 위치 유지의 성공 사례는 아닙니다.

## 팀 main에 포함된 작성 커밋 (85개)

| 날짜 | 커밋 | 수행 내용 |
| --- | --- | --- |
| 2026-09-03 | [1a3d067](https://github.com/Team-Stier/Morai_Sim_team2/commit/1a3d06747e7c961b41dd4ae80c0eb478eee3b33b) | Initial commit |
| 2026-09-03 | [a823228](https://github.com/Team-Stier/Morai_Sim_team2/commit/a823228ba7e37c5541ca6e6c3250d02166d739ac) | 문서: 대회 규정 베이스라인과 참고자료 추가 |
| 2026-09-03 | [417cd03](https://github.com/Team-Stier/Morai_Sim_team2/commit/417cd03dd9f3678f59f49d77f505986e58566806) | 문서: 대회 규정과 초기 아키텍처 기준 정리 |
| 2026-09-03 | [3c2e1f7](https://github.com/Team-Stier/Morai_Sim_team2/commit/3c2e1f7c3e73d7b829e45bf76deb983f1f31771b) | 구조: 자율주행 전체 아키텍처와 패키지 골격 추가 (#2) |
| 2026-09-05 | [de5a2b6](https://github.com/Team-Stier/Morai_Sim_team2/commit/de5a2b666d941d80d00cc1f9525f8bf47d010244) | 구조: 자율주행 시스템 패키지 골격과 중앙 계약 추가 (#3) |
| 2026-09-05 | [0e59ed4](https://github.com/Team-Stier/Morai_Sim_team2/commit/0e59ed44ac0ffb96711ce221528897fd9159425c) | 기능: TF·시간 계약과 MORAI UDP 수신 브리지 추가 (#4) |
| 2026-09-05 | [aa230c1](https://github.com/Team-Stier/Morai_Sim_team2/commit/aa230c18365242b8d7195d8ae431ca678c95dfd4) | 구조: 중앙 ROS 계약과 패키지 I/O 문서 정리 (#5) |
| 2026-09-11 | [0e99952](https://github.com/Team-Stier/Morai_Sim_team2/commit/0e999521feef74f7432ae68f4d803936994a618d) | chore: 기존 로컬리제이션 개발 작업 보존 |
| 2026-09-11 | [ed31781](https://github.com/Team-Stier/Morai_Sim_team2/commit/ed317818186e74c8fd2a74e298683a2573dcf8d1) | feat: GPS와 IMU 연속 관측으로 위치 재배치 자동 복구 |
| 2026-09-11 | [abe8b1a](https://github.com/Team-Stier/Morai_Sim_team2/commit/abe8b1af435e4640ee5cc8cf23251d2dcd616680) | fix: GPS 오차 기준 초과 시 해당 위치로 즉시 재초기화 |
| 2026-09-11 | [ec1a130](https://github.com/Team-Stier/Morai_Sim_team2/commit/ec1a1300fb30f1e8748b2b3b11d42db870b11c83) | 수정: 라이다 장착 위치를 2.0 0.0 1.5미터로 정정 |
| 2026-09-11 | [a2a4ff7](https://github.com/Team-Stier/Morai_Sim_team2/commit/a2a4ff75a1f1a4dc8917e32685b57dfb3770ae1e) | Paik (#13) |
| 2026-09-11 | [e0cc454](https://github.com/Team-Stier/Morai_Sim_team2/commit/e0cc454915ea87d11dd620b2f8c1d5efae2ba9ef) | 기능: 라이다 검출 브랜치의 인식 패키지를 원본 그대로 이식 |
| 2026-09-14 | [a84c676](https://github.com/Team-Stier/Morai_Sim_team2/commit/a84c676f0d821ab90982b18c0dd79e8ff5667d84) | Feature/public interface contract lidar visualization (#14) |
| 2026-09-14 | [db18684](https://github.com/Team-Stier/Morai_Sim_team2/commit/db1868401027164c13df969d7a9a4d6ec9cd7c0b) | LiDAR 사전학습 분류와 RViz 진단 연결 |
| 2026-09-14 | [bfe2ac4](https://github.com/Team-Stier/Morai_Sim_team2/commit/bfe2ac4d181025b4773165218518ed36c95545e9) | 외부 호환 패치의 원본 문맥 공백 보존 |
| 2026-09-14 | [ecc0503](https://github.com/Team-Stier/Morai_Sim_team2/commit/ecc0503156e1204df0c0030356606e37f65d69a4) | 라이다 퍼셉션에 스캔 시각 기반 롤·피치 수평화 적용 |
| 2026-09-14 | [de832e5](https://github.com/Team-Stier/Morai_Sim_team2/commit/de832e5640ec0f18f7170bf5d24da52f27264547) | 라이다 수평화 정량 평가와 전후 비교 보고서 추가 |
| 2026-09-14 | [d31b69c](https://github.com/Team-Stier/Morai_Sim_team2/commit/d31b69cdf2b0fd043f49a9c273ce0cbac92d90b4) | 라이다 원본 군집 점을 측정시각 TF로 HD맵에 표시 |
| 2026-09-14 | [370bbd8](https://github.com/Team-Stier/Morai_Sim_team2/commit/370bbd89a2658767af69759dd144f9885609180b) | 라이다 X ROI를 확장하고 RViz 점 표시를 굵게 조정 |
| 2026-09-15 | [75cf54c](https://github.com/Team-Stier/Morai_Sim_team2/commit/75cf54c47ca3896bd8d21fe45822ff43ea21de06) | 월드모델 map 좌표 객체 추적 구현 |
| 2026-09-21 | [667d0ca](https://github.com/Team-Stier/Morai_Sim_team2/commit/667d0caaff6050605d9a5594b8517863cdfaf286) | 라이다 검출 전 자세 보정의 제동 회귀 검증과 계약 정리 |
| 2026-09-21 | [656f280](https://github.com/Team-Stier/Morai_Sim_team2/commit/656f2800e595f7f7d2d51cbdb435526426118557) | 라이다 검출 전 자차 영역 반사점 제외 |
| 2026-09-21 | [e9fae2d](https://github.com/Team-Stier/Morai_Sim_team2/commit/e9fae2dc89166a27da9e1457872b69290c96196e) | 라이다 수평화 뒤 구역별 지면 제거 추가 |
| 2026-09-21 | [c6265ad](https://github.com/Team-Stier/Morai_Sim_team2/commit/c6265ad73d5b1e35bf8595ce121ebb479a87244c) | MORAI 검출과 표시의 일시 지연 허용 범위 완화 |
| 2026-09-21 | [4573ac4](https://github.com/Team-Stier/Morai_Sim_team2/commit/4573ac4df76aadbc22fcdc14ebdd010fb34bca32) | Closedteam2 제어 코어를 중앙 ROS 경계에 연결 |
| 2026-09-21 | [d3ec7b9](https://github.com/Team-Stier/Morai_Sim_team2/commit/d3ec7b99b1d181171e41ec948ba25a4a9d65f313) | 전역경로 추종 개발 실행을 MORAI에 연결 |
| 2026-09-21 | [34f4ca0](https://github.com/Team-Stier/Morai_Sim_team2/commit/34f4ca03724ee266592025412175dcb16034ed7f) | 동일 방향 추가 차로 RDDF 추출과 RViz 표시 추가 |
| 2026-09-21 | [7722e70](https://github.com/Team-Stier/Morai_Sim_team2/commit/7722e70f1093299ea6b378d313c6bb8f237b996e) | 필수 교차로 진입을 우회하는 추가 RDDF 제외 |
| 2026-09-21 | [c9622d3](https://github.com/Team-Stier/Morai_Sim_team2/commit/c9622d3b7144d95acabcf826956162ddda97b647) | 고주로 목표 100과 일반 구간 50 제한을 주행·RDDF에 적용 |
| 2026-09-21 | [fa339ad](https://github.com/Team-Stier/Morai_Sim_team2/commit/fa339add065c00b84b01a2652a6665a4640dc176) | 일반 구간 상한 58과 고주로 순항 목표 150 적용 |
| 2026-09-21 | [6528191](https://github.com/Team-Stier/Morai_Sim_team2/commit/6528191b98ac04c0654b059febaf89760cb8a3da) | 울트라실패작 |
| 2026-09-22 | [6dd21d4](https://github.com/Team-Stier/Morai_Sim_team2/commit/6dd21d484a76d031da3a265efa9926fed0061af8) | 전역경로 제어에 Q 전환과 기존 라이다 보정 복원 |
| 2026-09-22 | [84e9350](https://github.com/Team-Stier/Morai_Sim_team2/commit/84e9350eaed2467b62718869440f02f7385b8182) | Frenet RDDF 후보 생성과 클러스터 점 기반 비용 평가 개발 상태 저장 |
| 2026-09-22 | [567f15e](https://github.com/Team-Stier/Morai_Sim_team2/commit/567f15eb03ce669386a5a95a77097a49ec1b8811) | Frenet 계획 보관 시간을 입력 신선도와 분리 |
| 2026-09-22 | [6ed7598](https://github.com/Team-Stier/Morai_Sim_team2/commit/6ed7598cc12cca58b48ac17ec5c307c1950cf993) | RViz에 Frenet 출력 경로와 정지 지점 표시 |
| 2026-09-22 | [5da592c](https://github.com/Team-Stier/Morai_Sim_team2/commit/5da592c2e44a05a19f567bbd0093c1be9acb0ea5) | 정적 HD맵 캐시로 Route 진행 메시지 경량화 |
| 2026-09-22 | [4fbc3e4](https://github.com/Team-Stier/Morai_Sim_team2/commit/4fbc3e4c6edce6eb7fbc5325c64074a6ed6098a5) | Frenet 시험 속도 상한 해제 및 기존 구간 속도 복원 |
| 2026-09-22 | [a94098f](https://github.com/Team-Stier/Morai_Sim_team2/commit/a94098fd4af546776f5d772e8a9c013c5db0a736) | RDDF 형상 전용 주행과 기하 기반 차선변경 후보 적용 |
| 2026-09-22 | [a9a611b](https://github.com/Team-Stier/Morai_Sim_team2/commit/a9a611b25f83b3f02779cd47e82808e84ab5cda1) | 프레넷 계획 지연과 순간 정지를 줄임 |
| 2026-09-22 | [9dce693](https://github.com/Team-Stier/Morai_Sim_team2/commit/9dce693ae2c6bbe060ff1a389e39e2a42a2edeb0) | 새 결과까지 활성 경로를 계속 유지함 |
| 2026-09-22 | [c537453](https://github.com/Team-Stier/Morai_Sim_team2/commit/c537453a7734fc0ac53b105267dd93a109e038cf) | RDDF 종점 완주 허용거리를 적용함 |
| 2026-09-22 | [f4ba314](https://github.com/Team-Stier/Morai_Sim_team2/commit/f4ba314b6ef8df88ede7826c69082f48a9b318d7) | 현재 위치의 최근접 RDDF에서 주행을 재개하도록 수정 |
| 2026-09-22 | [8fa3d3d](https://github.com/Team-Stier/Morai_Sim_team2/commit/8fa3d3dfdb337ab236c589857511888f857561db) | 충돌 시간 샘플링을 실제 예측 범위로 제한 |
| 2026-09-22 | [7690dc4](https://github.com/Team-Stier/Morai_Sim_team2/commit/7690dc41456ccab43fc26e7ffa01f21e15bda8e4) | 현재 위치에서 RDDF로 연결하는 복귀 곡선을 완만하게 조정 |
| 2026-09-22 | [38b9121](https://github.com/Team-Stier/Morai_Sim_team2/commit/38b91213d4960edeeba9cb441ece8da2744c7e48) | 종점 접근 시 짧은 잔여 경로를 추종하도록 개발 설정 조정 |
| 2026-09-22 | [cf1c7de](https://github.com/Team-Stier/Morai_Sim_team2/commit/cf1c7deee5f90d476afb6bec5d66fb57b1613a57) | 닫힌 RDDF를 종점 정지 없이 연속 순환하도록 변경 |
| 2026-09-22 | [b5d421d](https://github.com/Team-Stier/Morai_Sim_team2/commit/b5d421dbcdf10f52d88bef3c4ed5efea9267ffca) | 고주로 RDDF를 시작점 분기와 전역경로 합류로 연결 |
| 2026-09-22 | [b132c8a](https://github.com/Team-Stier/Morai_Sim_team2/commit/b132c8a49a60bee16e750bbabb59938299ed3f30) | 클러스터 점군 정합으로 이동 속도 추정 개선 |
| 2026-09-22 | [df6e55b](https://github.com/Team-Stier/Morai_Sim_team2/commit/df6e55b22cb9358e2757e97103dc85ac3a0bc220) | 유한 RDDF 끝점 반복 대신 전역경로 복귀 궤적 생성 |
| 2026-09-22 | [80e11c9](https://github.com/Team-Stier/Morai_Sim_team2/commit/80e11c90359c35ea607da3bc9d19e1f8b25024e9) | 최신 차량 위치에 맞춰 프레넷 시작 진행값 정렬 |
| 2026-09-22 | [6ecdc5a](https://github.com/Team-Stier/Morai_Sim_team2/commit/6ecdc5a77d8acbfe9cf42b78895ef7f10ffab1de) | 프레넷 발행 경로의 형상 보존과 위치 재설정 처리 수정 |
| 2026-09-22 | [aea8929](https://github.com/Team-Stier/Morai_Sim_team2/commit/aea8929ac5c4c80af17338fb05b161a00f3c7943) | 정적 상자 앞에서 근거리 우회 후 RDDF 복귀 후보 추가 |
| 2026-09-22 | [d3fe73c](https://github.com/Team-Stier/Morai_Sim_team2/commit/d3fe73ce70361161798c81812f5f163bc1a56294) | 프레넷 횡가속도 제한을 현재 주행 설정 4.0으로 저장 |
| 2026-09-22 | [6261245](https://github.com/Team-Stier/Morai_Sim_team2/commit/6261245dcf3d4b0650c2b0121e9b3eb9637b91b3) | run.sh 한 번으로 프레넷 전체 주행 구성 실행 |
| 2026-09-22 | [4e370ce](https://github.com/Team-Stier/Morai_Sim_team2/commit/4e370ce1497ab42d50f7fe3426e85b614e7b64e2) | 고주로의 프레넷 비교 거리를 300미터로 확대 |
| 2026-09-22 | [34451b7](https://github.com/Team-Stier/Morai_Sim_team2/commit/34451b754130620b17ae7f50a1daec6704a5b274) | 좌우 카메라 수신을 기본 실행에서 비활성화 |
| 2026-09-22 | [1ce220b](https://github.com/Team-Stier/Morai_Sim_team2/commit/1ce220b8c513f9c14bf2dc2d4fbbb7270d3b2ed7) | 근거리 장애물 회피 후보를 좌우 모두 생성 |
| 2026-09-22 | [80cf373](https://github.com/Team-Stier/Morai_Sim_team2/commit/80cf373ea243c8349126676584b79638a41a6541) | 회피 후보의 반복 충돌 계산과 확정 경로 재평가 비용 절감 |
| 2026-09-22 | [d91c4c6](https://github.com/Team-Stier/Morai_Sim_team2/commit/d91c4c651767adffc35fec4dbc01109a6c3e2274) | 동적 충돌 예측을 일괄 계산해 회피 평가 지연 추가 감소 |
| 2026-09-22 | [4478b8e](https://github.com/Team-Stier/Morai_Sim_team2/commit/4478b8ec7ef4076206816e4ae2f9003f2f86e58a) | 회피 선택 확인 시간을 0.1초로 단축 |
| 2026-09-22 | [e68a959](https://github.com/Team-Stier/Morai_Sim_team2/commit/e68a959ca6728c089f86370d0f5d865d62e16ee8) | ㄱㅊ음 |
| 2026-09-22 | [607be52](https://github.com/Team-Stier/Morai_Sim_team2/commit/607be52f184eeb69911c7cb5dff3d948339d2363) | 새 경로와 감속·정지 결과를 완료 즉시 활성화 |
| 2026-09-22 | [6214d2f](https://github.com/Team-Stier/Morai_Sim_team2/commit/6214d2fc74e11e03485fda3ee0c9f4930f7080d2) | 회피 후보 탐색 중 불필요한 임시 정지 방지 |
| 2026-09-22 | [205b544](https://github.com/Team-Stier/Morai_Sim_team2/commit/205b54489c62b1ff0892f90fca2a4b6fb9820dc3) | 앞차 추종 간격과 가속 제어 파라미터 조정 |
| 2026-09-22 | [00ca038](https://github.com/Team-Stier/Morai_Sim_team2/commit/00ca038b5e09ab1a6740dc167bc591b325f2b97e) | 주행 bag 분석으로 경로 선택 대기와 가속 응답 조정 |
| 2026-09-22 | [2b05672](https://github.com/Team-Stier/Morai_Sim_team2/commit/2b0567217d452be47116277f337dc41bec6b88f6) | bag 재검증으로 이동 객체 오정지와 막힌 회피 경로 고정 수정 |
| 2026-09-23 | [f325c70](https://github.com/Team-Stier/Morai_Sim_team2/commit/f325c701b3327ef23aaa787b20b8361ffe54aa75) | 일반 경로를 최소 0.5초 유지하고 최신 대기 경로로 교체 |
| 2026-09-23 | [3204201](https://github.com/Team-Stier/Morai_Sim_team2/commit/3204201dd0bfa58bf8444b0d052377411e23c1c3) | 개발 주행의 인지 지연 오정지 완화와 경로 변경 이득 조정 |
| 2026-09-23 | [c1633e2](https://github.com/Team-Stier/Morai_Sim_team2/commit/c1633e28a9b4e735b4433ccc7d95672df77f8823) | 경로 추종 안정성을 위해 가속과 코너 속도 설정 완화 |
| 2026-09-23 | [5f67eb9](https://github.com/Team-Stier/Morai_Sim_team2/commit/5f67eb9324ac647349b96f0aea2cd39754351a2f) | Paik (#17) |
| 2026-10-05 | [4ca0500](https://github.com/Team-Stier/Morai_Sim_team2/commit/4ca0500e11e3cb0d390bfd541c85803d7c01328f) | RViz에 현재 선택된 플래너와 구간 상태 표시 |
| 2026-10-05 | [49e80e6](https://github.com/Team-Stier/Morai_Sim_team2/commit/49e80e68f766edaebf0001195070ba490ea33862) | Frenet 정적 장애물 우회 경로 생성 기능 삭제 |
| 2026-10-05 | [3d4b47b](https://github.com/Team-Stier/Morai_Sim_team2/commit/3d4b47b0e0563d53d63e0252be4ad74db790cbf3) | Frenet 설정 항목에 한국어 설명 주석 추가 |
| 2026-10-06 | [3b047e6](https://github.com/Team-Stier/Morai_Sim_team2/commit/3b047e6ae1943e143bbfe54a2fa9355378566423) | 제어기와 Frenet 조향 변화율 상한을 12 rad/s로 상향 |
| 2026-10-06 | [b4e650d](https://github.com/Team-Stier/Morai_Sim_team2/commit/b4e650d860a8b804dbbaa17c7a5a19703807b398) | Frenet RDDF 기준 경로를 제한된 폭으로 평활화 |
| 2026-10-06 | [cbcd937](https://github.com/Team-Stier/Morai_Sim_team2/commit/cbcd9375bec4c26c85c19bb8397f066c0f817107) | Frenet RDDF 평활화 이동 상한을 15cm로 축소 |
| 2026-10-06 | [5033b2b](https://github.com/Team-Stier/Morai_Sim_team2/commit/5033b2b48ab37d9f1c9b5a67e9bbf0db2f9bd754) | paik 이전 전 현재 로컬 코드 복구 스냅샷 |
| 2026-10-06 | [1411048](https://github.com/Team-Stier/Morai_Sim_team2/commit/141104875209af26fae72a2139ae2d25ece1374b) | Paik (#27) |
| 2026-10-06 | [97ab941](https://github.com/Team-Stier/Morai_Sim_team2/commit/97ab9412832a4cd8a3dcc210454b6020f1cf98d6) | RViz HD Map에 체크포인트 점과 번호 표시 |
| 2026-10-06 | [c494db8](https://github.com/Team-Stier/Morai_Sim_team2/commit/c494db8771b9af663afce11d25bf763ad90168a7) | 고주로 전체 차선 RDDF를 연속 경로로 연결 |
| 2026-10-06 | [f16220f](https://github.com/Team-Stier/Morai_Sim_team2/commit/f16220fec2c2db6763b6e5ef70663f8032da6ec2) | HD맵 신호 정지선과 시각화 코드 반영 |
| 2026-10-06 | [4bcc593](https://github.com/Team-Stier/Morai_Sim_team2/commit/4bcc593a01c8d1a34575d020c790cda9b4d42c24) | Paik (#28) |
| 2026-10-06 | [ff8cdfe](https://github.com/Team-Stier/Morai_Sim_team2/commit/ff8cdfe674e8988e8d893b58c6c823752e041df5) | 신호 정지선 지도와 RViz 표시의 통합 검증 완료 |
| 2026-10-06 | [bef648c](https://github.com/Team-Stier/Morai_Sim_team2/commit/bef648c80afc949ea36df462e3f0247e83950924) | 고주로 외측 RDDF가 CP11을 통과하도록 합류 보정 |

## paik에만 포함된 작성 커밋 (3개)

| 날짜 | 커밋 | 수행 내용 |
| --- | --- | --- |
| 2026-09-23 | [a8918cc](https://github.com/Team-Stier/Morai_Sim_team2/commit/a8918cc360f3e3ed8420a10b0056727e3ea830d5) | 터널 원본 벽선을 HD맵과 RViz에 표시 |
| 2026-09-23 | [a06cbe4](https://github.com/Team-Stier/Morai_Sim_team2/commit/a06cbe4bbd7da2606c31afdf8cd4a2802723ec1e) | 터널 LiDAR 벽 정합을 위치 추정기에 연결 |
| 2026-10-08 | [45ded67](https://github.com/Team-Stier/Morai_Sim_team2/commit/45ded67d34008c57b43f793ce3825c29f32e5d66) | 현재 paik 브랜치의 터널 벽 보정 통합 검증 기록 |
