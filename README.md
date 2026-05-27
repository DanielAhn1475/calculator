# 중국 위안·미국 달러 한화 계산기

GitHub Pages에 올려서 사용할 수 있는 `index.html` 1개짜리 환율 계산기입니다.

## 이번 수정 내용

기존 Python GUI에서 `HTTP Error 403: Forbidden`이 나오는 문제를 줄이기 위해 다음을 수정했습니다.

- Python `urllib` 요청에 브라우저형 `User-Agent` 헤더 추가
- 환율 API를 1개만 쓰지 않고 여러 API를 순서대로 시도하도록 변경
- 1차: Frankfurter v2
- 2차: Frankfurter legacy
- 3차: ExchangeRate-API open endpoint
- API가 모두 실패하면 수동 환율 입력으로 계산 가능

## GitHub Pages 사용 방법

1. GitHub 저장소를 만듭니다.
2. `index.html` 파일을 저장소 최상위 폴더에 업로드합니다.
3. GitHub 저장소의 `Settings` → `Pages`로 이동합니다.
4. `Deploy from a branch`를 선택하고 `main` / `/root`로 설정합니다.
5. 발급된 GitHub Pages 주소로 접속합니다.

## 기능

- 중국 위안(CNY) → 한화(KRW) 자동 계산
- 미국 달러(USD) → 한화(KRW) 자동 계산
- 한화(KRW) → 중국 위안(CNY) 역계산
- 한화(KRW) → 미국 달러(USD) 역계산
- CNY / USD 탭 전환
- 무료 환율 API 자동 불러오기
- API 실패 시 수동 환율 입력 가능
- 모바일 화면 대응
- 10 / 50 / 100 / 1,000 빠른 입력 버튼

## 파일 설명

| 파일 | 설명 |
|---|---|
| `index.html` | GitHub Pages용 웹 계산기 |
| `yuan_gui.py` | Windows PC에서 실행 가능한 Python Tkinter GUI 버전 |

## Python GUI 실행 방법

```bash
python yuan_gui.py
```

## 참고

환율은 참고용입니다. 실제 은행, 카드사, 환전소의 수수료와 적용 환율은 다를 수 있습니다.
