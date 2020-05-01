---
description: 'https://github.com/Golden-Goose-Lab/creon/blob/master/creon/utils.py'
---

# utils

### **run\_creon\_plus\(\)**

_def run\_creon\_plus\(username: str, password: str, certification\_password: str, starter\_path: str\)_  
크레온 플러스를 실행시키는 유틸리티 함수입니다. 인자로 받은 아이디와 암호, 공인인증서 암호, 그리고 크레온 플러스 바이너리의 경로를 받아 자동으로 로그인까지 완료합니다.



### snake\_to\_camel\(\)

_def snake\_to\_camel\(value: str\) -&gt; str_  
언더 스코어 형태의 문자열을 카멜 케이스의 문자열로 변환하여 리턴하는 유틸리티 함수입니다.



### timeframe\_to\_timedelta\(\)

_def timeframe\_to\_timedelta\(timeframe: tuple\) -&gt; timedelta:_  
수량과 타임프레임\(Integer, [TimeFrameUnit](constants.md#timeframeunit)\)을 튜플 형태로 받아 연산에 필요한 timedelta 값을 리턴하는 유틸리티 함수입니다.





