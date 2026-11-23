# 바이브 코딩 딥러닝 · SDG AI 프로젝트 교육자료

고2 정보 수행평가 "바이브 코딩으로 딥러닝 만들기" 공유 사이트입니다.

- 학생용 페이지: 누구나 볼 수 있어요.
- 교사용 페이지: 비밀번호로 잠겨 있어요. 내용은 암호화되어 있어서, 비밀번호 없이는 소스를 열어도 읽을 수 없어요.

## 파일

| 파일 | 내용 |
|---|---|
| `index.html` | 사이트 전체 (학생용 + 암호화된 교사용) |
| `assets/` | 첫 화면 사진 (포스터 예시, 웹앱 화면, 학습 곡선) |
| `.nojekyll` | GitHub Pages가 파일을 그대로 보여 주게 하는 빈 파일 |

## GitHub Pages로 배포하기

1. GitHub에서 **New repository**를 만들어요. 이름 예: `vibe-dl`. **Public**으로 만들어요.
2. 저장소 화면에서 **Add file → Upload files**를 누르고, 이 폴더의 파일을 모두 끌어다 놓은 뒤 **Commit changes**를 눌러요.
   - `assets` 폴더는 폴더째 끌어다 놓아요.
   - `.nojekyll`이 안 보이면 숨김 파일 보기를 켜거나, **Add file → Create new file**로 이름만 `.nojekyll`인 빈 파일을 만들어요.
3. **Settings → Pages**에서 Source를 **Deploy from a branch**, Branch를 **main / (root)**로 고르고 **Save**를 눌러요.
4. 1~2분 뒤 `https://아이디.github.io/vibe-dl/` 주소로 열려요.

## 내용 바꾸기

이 저장소에는 완성된 `index.html`만 있어요. 교사용 원문을 보호하려고 원본 파일(`student.html`, `teacher.html`, `style.css`, `build.py`)은 넣지 않았어요. 원본을 고친 뒤 아래처럼 `index.html`을 다시 만들어 이 파일만 바꿔 올리면 돼요.

```bash
pip install cryptography
python build.py "새 비밀번호"
```

공개 저장소에는 암호화된 교사용 내용이 그대로 올라가요. 비밀번호는 길고 추측하기 어렵게 정하세요. 원본 `teacher.html`은 공개 저장소에 올리지 마세요.
