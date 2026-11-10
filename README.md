# Sweeper

개발자 맥에 쌓이는 캐시·개발도구 찌꺼기(패키지 캐시, Xcode, Gradle, Android 에뮬레이터, iOS 시뮬레이터, Docker 등)를 안전하게 정리하는 맥 앱.
(소스는 비공개, 이 저장소에는 배포 파일만 있다)

## 설치

1. [최신 릴리스](https://github.com/dev-fath/Sweeper-releases/releases/latest)에서 `Sweeper-<버전>.dmg` 를 받는다.
2. DMG를 열고 Sweeper를 Applications 폴더로 끌어다 놓는다.
3. 애플 공증을 받지 않은 앱이라 처음 한 번은 직접 허용해야 한다.
   - 실행 → 경고가 뜨면 **완료** → **시스템 설정 → 개인정보 보호 및 보안 → "그래도 열기"**, 또는
   - 터미널에서 `xattr -dr com.apple.quarantine /Applications/Sweeper.app`
4. 휴지통·메일 첨부파일까지 정리하려면 같은 화면의 **전체 디스크 접근 권한**에서 Sweeper 를 허용한다.

## 쓰기 전에

- 처음부터 체크된 **안전** 항목(캐시 등)은 **영구 삭제**된다. 정리 전 확인 창에 영구 삭제 개수가 나오니 꼭 확인한다.
- 대용량·중복 파일과 일부 설정 폴더는 휴지통으로 이동한다. Docker 볼륨·Ollama 모델처럼 영구 삭제되는 **판단 필요** 항목도 있다.
- 정리 기록은 `~/Library/Logs/Sweeper` 에 남는다.

macOS 14 이상, Apple Silicon·Intel 모두 지원. 이후 업데이트는 앱이 알아서 확인한다 (앱 메뉴 → 업데이트 확인…).
