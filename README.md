# todo-generator
랜덤 할일 생성기v1.0

[![made-with-Markdown](https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg)](http://commonmark.org)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/choipureum/todo-generator) 
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
> 할일 없을 때 랜덤 할일 생성기 v1.0.0

## 핵심 기능  Key Feature
- 특정 사용자의 모든 repository들을 돌며 오늘 commit을 확인합니다.(여러 사용자여도 되는데 github api특성상 호출 limit/hour 있기 때문에 1명 하세요) 
  - 오늘 commit이 존재할 때는 메세지를 보내지 않습니다.
- 설정값에 미치지 못하는 commit 수(default:1)일 경우, 자동으로 알람 메시지를 전송합니다. (단 컴퓨터가 실행 중이어야합니다.)

## 사용 How To Use
  
- 설정파일 변경(key.txt)
  - 설정파일 예제(key.txt)에서 필요한 access_token값들, 설정등을 채워주세요
    - `{TWILIO_ACCOUNT_SID}` : twilio accout sid
    - `{TWILIO_AUTH_TOKEN}` : twilio auth token
    - `{TWILIO_PHONE_NUMBER}` : twilio에서 발급받은 휴대폰 번호
    - `{GITHUB_ACCESS_TOKEN}` : 깃헙 public acess_token 발급받은 뒤 설정
    - `{YOUR NAME}` : 이름
    - `{YOUR PHONE NUMBER}` : SMS를 받을 휴대폰 번호
    
- 윈도우 프로세스 등록

## Contributing
- [@choipureum](https://github.com/choipureum)

## Reference
```
using Twilio;
using Twilio.Rest.Api.V2010.Account;
```
- [twilio API](https://www.twilio.com/docs/sms)
- [github API](https://docs.github.com/en/rest/reference)

## Links
- Repository: https://github.com/choipureum/CommitChecker
- Issue tracker: https://github.com/choipureum/CommitChecker/issues
  - 보안 취약점 등의 민감한 이슈인 경우 poo1994.imbc.com 로 연락주십시오. 

## Testing
### 윈도우 서비스 설정
![image](https://user-images.githubusercontent.com/55127127/112115713-d6ff3100-8bfc-11eb-9c89-0163abe29aab.png)
### SMS Test
![image](https://user-images.githubusercontent.com/55127127/112115841-feee9480-8bfc-11eb-9326-6b5346a138d9.png)
