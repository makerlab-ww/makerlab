# 웹교재 (MkDocs)

## 개요
- 고등학교 수업용 웹교재. 일반적인 교재 형태(장·절 구조)로 만든다.
- 공간·방 형태의 꾸밈은 하지 않는다.
- 현재 영역: 3D 모델링(Autodesk Fusion + Bambu Lab P1S 출력).
  아두이노 등 다른 과목은 나중에 상단 탭으로 추가한다.

## 작업 방식 (중요)
- 작업할 영역의 `자료/(영역)/가이드.md`를 먼저 읽을 것.
- 단계별로 진행한다. 파일을 만들거나 고치기 전에 반드시 먼저 확인받는다.
- 설명은 간결한 한국어로.
- 본문 내용을 임의로 지어내지 않는다. 내용이 없는 곳은
  `<!-- TODO: ... -->`로 남기고 보고한다.

## 기술 설정
- MkDocs + Material 테마, `theme.language: ko`
- 기능: navigation.tabs, navigation.sections, navigation.top,
  navigation.footer(이전/다음), content.code.copy, search
- 한글 글꼴: Noto Sans KR
- 각 페이지에 "이 페이지 편집" 버튼 (repo_url, edit_uri)
- 배포: GitHub Actions로 main 브랜치 push 시 GitHub Pages 자동 배포

## 폴더 구조
```
자료/(영역)/  ← 가이드.md, 대본 등 원재료 (웹에 안 올라감)
docs/(영역)/  ← 교재 페이지
docs/(영역)/images/(절번호)/  ← 그림
```

## 진행 순서
1. 환경 확인: Python 설치 여부 확인 → mkdocs-material 설치
2. mkdocs.yml 작성, 목차대로 빈 페이지 22개를 양식에 맞춰 생성
3. 로컬 미리보기(mkdocs serve)로 모양 확인 → 선생님 확인
4. 01번 페이지 본문 작성 (선생님이 제공하는 대본 기반)
5. GitHub 저장소 연결 및 Actions 배포 설정
