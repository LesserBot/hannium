# Flask 접근순서
(설치할것 확장python, python for vscode ,python extension pack,flask-snippets)
1. 파이썬과 vscode 설치이후 ctrl+shift=p 누르기
2. python: select inter~ 해서 파이썬 설치경로 설정
3. 파이썬의 scripts  위치를 복사해 '시스템 환경 변수 편집 -> 환경 변수 -> 아래블록 path에 추가
4. powershell에 CategoryInfo : 보안 오류: (:) [], PSSecurityException 가 뜨면 windowpowershell을 관리자 권한으로 들어가서 ExecutionPolicy 입력
5. Restricted 라고 나올시 Set-ExecutionPolicy RemoteSigned 을 하고 Y 후 다시 ExecutionPolicy입력하여 확인
6. 이후 코드 (vscode)
```
> pip3 install virtualenv
> virtualenv venv
> cd venv
> activate or .\activate
(이제 앞에 venv 라는게 생김)
> deactivate (가상환경 비활성화)
> pip install flask or > pip3 install flask

- 기본 코드
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Hello, world!"

if __name__ == '__main__':
    app.run()