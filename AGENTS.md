# AGENTS.md

## 저장소 컨텍스트
이 저장소는 `kngyeol/kngyeol` GitHub 프로필 저장소입니다.
핵심 산출물은 프로필 페이지에 렌더링되는 `README.md`입니다.

## 완료 조건
1. `README.md`에 centered capsule header, 소개, 배지/위젯, metrics 임베드, 최근 활동 마커, 연락처 placeholder, 설정 체크리스트가 포함된다.
2. `modules/`에 배지/위젯/스타일 스니펫 재사용 파일이 존재한다.
3. `assets/` 폴더가 존재하고 `assets/metrics.svg`를 워크플로우가 생성할 수 있다.
4. GitHub Actions 워크플로우가 존재한다.
   - `lowlighter/metrics`로 `assets/metrics.svg` 생성
   - `readme-workflows/recent-activity`로 README 활동 섹션 갱신
5. 워크플로우에 `permissions: contents: write`가 설정되고, 하드코딩된 비밀값이 없다.

## 스타일 선호
- 섹션은 간결하고 깔끔하게 유지
- 헤더는 중앙 정렬
- 배지 목록은 과도하게 길지 않게 유지
- GitHub 렌더링 호환 HTML/Markdown 우선
