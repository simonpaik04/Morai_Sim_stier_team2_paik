# 자료 출처와 확인 범위

## 소스 기준

- 팀 main: [42fdefa812747820b635231a0ab36845d58cdb7e](https://github.com/Team-Stier/Morai_Sim_team2/tree/42fdefa812747820b635231a0ab36845d58cdb7e)
- 팀 paik: [45ded67d34008c57b43f793ce3825c29f32e5d66](https://github.com/Team-Stier/Morai_Sim_team2/tree/45ded67d34008c57b43f793ce3825c29f32e5d66)
- 확인일: 2026-10-08
- 팀 원본은 조회만 했으며, 이 포트폴리오에는 팀 소스 전체를 복사하지 않았습니다.

## 이미지

| 자료 | 원본과 시점 | 보여주는 내용 |
| --- | --- | --- |
| [메인 주행 화면](../assets/morai-rviz-driving.png) | `global-path-demo-running.png`, 2026-09-21 | MORAI·RViz 전역경로 추종 개발 실행 |
| [HD Map](../assets/hd-map-preview.png) | 팀 main `src/hd_map_pkg/docs/katri_hd_map_preview.png` | 지도 레이어·RDDF 미리보기 |
| [LiDAR 실행](../assets/lidar-leveling-rviz.png) | `lidar-horizontalization-20260914/rviz.png`, 2026-09-14 | 센서 좌표계의 기존 LiDAR 표시 |
| [곡률 분석](../assets/rddf-curvature-comparison.png) | `frenet-relaxation-20261006/curvature_comparison.png`, 2026-10-06 | 이전 0.30m 상한 설정의 오프라인 비교 |

원본 경로와 SHA-256은 [media-provenance.json](media-provenance.json)에 기록했습니다. 이미지는 기존 자료를 그대로 복사했으며 AI로 만든 실행 화면이나 새 주행 캡처는 포함하지 않았습니다.

## 수치와 한계

- [LiDAR 실행 집계](lidar-runtime-audit.json): 10초 관측 73개. 해당 기록의 `ready=false`, `stop_required=true` 등 개발 상태를 포함합니다. 관측 수신과 주행 승인·인식 정확도는 서로 다른 확인입니다.
- [RDDF 평활화 수치](rddf-smoothing-experiment.json): 이전 상한 0.30m의 오프라인 실험. 고속 구간 최대 절대 곡률 0.1783577643→0.0643108514 /m, 전체 최대 기준 경로 이동 0.1760859548m. 현재 0.15m 설정의 측정값으로 사용하지 않습니다.
- 터널 벽 보정의 2026-10-08 통합 기록은 빌드와 일부 producer-consumer 테스트를 확인했습니다. 원본 기록에는 외부 센서 프로필 SHA 불일치와 LiDAR 표시 통합 테스트 실패도 남아 있습니다. 전체 검사 성공·터널 완주로 요약하지 않습니다.
- 현재 Frenet 정적 장애물 전용 우회 후보는 삭제 상태입니다. 이전 커밋은 개발 이력으로 남기되 현재 기능과 구분합니다.

## 이번 문서 작업의 검증

커밋 작성자·브랜치 포함 여부·대표 diff·현재 소스·기존 실행 기록을 확인하고, Markdown 로컬 링크·첨부 자료·문서 형식을 검사했습니다. ROS 빌드나 MORAI 주행을 이번 포트폴리오 정리에서 새로 실행한 것은 아닙니다.
