# Vault

최재호(James Choi)의 개인 금고 저장소. 개인정보, 가족, 재정, 차량, 건강, 여행, 개발 메모, 회사 HR 인사카드 등을 마크다운으로 관리한다.

tienipia-hr 에이전트(김근식 대리)가 vault 도구를 통해 읽기/쓰기를 수행한다.

**경고: 이 저장소에는 은행 계좌번호, 연락처, 주소, 가족 정보 등 민감한 개인정보가 포함되어 있다.**

## 소유자 정보

- 이름: 최재호 (JAEHO CHOI, James Choi)
- 생년월일: 1995.01.12
- 이메일: tienipia@gmail.com

## 디렉토리 구조

```
profile/              인적사항 (이름, 생년월일, 가족, 학력)
finance/              재정 (은행 계좌, 세금)
vehicles/             차량 (BMW i4, 그랜드 스타렉스)
health/               건강 (체성분, 식단)
interests/            관심사 (음악 등)
travel/               여행 기록
dev/                  개발 메모 (AWS, Cloudflare)
hr/                   회사 인사카드 (대표 전용)
personal_schedule/    개인 일정 (미팅, 약속)
```

## 작성 규칙

- 기본 언어: 한국어 (개발 메모는 영어 혼용)
- 파일명: 소문자, 언더스코어 구분 (예: `bmw_i4.md`)
- 날짜 형식: `YYYY.MM.DD` 또는 `YYYY-MM-DD`
- 교차 링크: 상대 경로 마크다운 링크 `[텍스트](../경로/파일.md)`
- 커밋 메시지: 짧은 영어, 소문자, 동사 원형 (예: `update inbody`, `add schedule`)

## 접근 권한

- **대표 (tienipia)**: vault 도구를 통해 전체 읽기/쓰기
- **직원**: 접근 불가 (코드 레벨 차단)
- **LLM 에이전트**: 대표와 대화 시에만 vault 도구 사용 가능
