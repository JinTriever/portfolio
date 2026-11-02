# 펫하루

반려견의 외출과 생활 기록을 모아 보고 분리불안 체크와 훈련을 함께 관리하는 Flutter 앱입니다.

## 주요 기능

- 외출·산책 시간과 위치 기록
- 날짜별 기록 조회와 주간·월간 통계
- 분리불안 체크와 훈련 진행 관리
- 여러 반려견의 프로필 등록·전환
- 급여·배변·체중·병원·접종 기록과 사진 앨범
- 일상·훈련·생일·접종 알림
- 기록 백업·복원과 공유

## 구현 방식

Flutter·Dart로 기능별 화면과 기록 모델을 구성했습니다. SharedPreferences에 JSON 형태로 프로필·생활 기록·설정을 저장하고, 백업 파일을 내보내거나 불러올 수 있도록 만들었습니다.

geolocator로 산책 위치를 수집하고 flutter_map으로 경로를 표시했습니다. fl_chart와 table_calendar로 기록을 차트와 달력에서 확인하도록 구성했습니다.

flutter_local_notifications와 timezone으로 알림을 예약했습니다. Android의 배터리 최적화 설정은 Kotlin·MethodChannel로 연결했고, 권한 허용 후 알림을 다시 등록하도록 처리했습니다.

Gemini REST API로 기록 요약을 보내 짧은 조언을 만들고 호출 횟수 제한과 응답 캐시를 적용했습니다. 카메라 밝기 변화로 맥박 간격을 추정하는 심박·스트레스 화면도 실험 기능으로 구현했습니다.

## 사용 기술

Flutter, Dart, Kotlin, SharedPreferences, JSON, geolocator, flutter_map, fl_chart, flutter_local_notifications, Gemini API
