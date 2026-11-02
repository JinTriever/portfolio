# WhisPet

반려견에게 음악을 들려주는 IoT 제품입니다. 펫뮤즈에서 서비스 기획, 앱·웹 개발, 게이트웨이 연결 기능, 시제품 제작과 App Store 출시를 담당했습니다.

## 주요 기능

- 회원가입·로그인과 반려견 정보 관리
- 반려견 음악 선택과 보호자 목소리를 활용한 TTS
- 앱에서 게이트웨이의 Wi-Fi 초기 설정
- 게이트웨이의 스피커 탐색과 자동 연결
- 상품 구매와 웰컴페이먼츠 결제 화면 연동

## 구현 방식

Vue.js로 반응형 웹을 만들고 Flutter WebView 앱과 메시지 통신을 연결했습니다. 화면과 사용자 입력은 웹에서 처리하고 Bluetooth 연결·녹음 등 네이티브 기능은 Flutter에서 처리했습니다. 결제 화면 호출과 반환 응답 처리를 구현했으며 WebView 앱을 App Store에 출시했습니다.

기성품 VIM1S 게이트웨이에 연결 소프트웨어를 구현했습니다. 앱에서 Bluetooth로 Wi-Fi SSID·비밀번호를 보내면 게이트웨이가 네트워크에 연결되도록 구성했습니다. Android·Kotlin으로 BLE GATT 서버와 클라이언트 역할을 나눠 설정 정보를 받고, PET_MUSE 스피커를 탐색·연결하고 WAV 데이터를 분할 전송했습니다.

웹에서는 Pinia와 Vue Router로 상태·화면 이동을 관리하고 Axios로 API를 호출했습니다. Firebase Realtime Database로 기기 상태를 구독하고 명령 데이터를 등록했습니다. 이후 Flutter 네이티브 화면으로 옮기는 작업에서는 Riverpod·GoRouter·Dio를 사용했습니다.

앱 디자인은 디자이너와 함께 진행했습니다. 서버 개발과 Bluetooth 스피커 PCB 제작은 외주로 진행했으며, 직접 담당한 부분은 앱·웹과 게이트웨이 연결 소프트웨어입니다.

## 사용 기술

Flutter, Dart, Vue.js, TypeScript, WebView, Android, Kotlin, Bluetooth LE, Firebase, VIM1S
