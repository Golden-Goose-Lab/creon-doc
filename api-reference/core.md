---
description: 'https://github.com/Golden-Goose-Lab/creon/blob/master/creon/core.py'
---

# core

#### COMWrapper

_class COMWrapper_  
크레온 윈도우즈 API를 손쉽게 다루기 위한 래핑 클래스입니다. 

_속성_  
com - 디스패치된 윈도우즈 API 모듈입니다.

_메소드_  
def \_\_init\_\_\(self, com\)  
생성자 함수입니다. 인자로 사용하려는 윈도우즈 API 모듈을 받습니다.

def \_\_getattr\_\_\(self, item\)  
디스패치된 윈도우즈 API 모듈내 함수나 변수를 바로 클래스 네이티브처럼 사용하기 위한 함수입니다.  
  
def block\_request\(self\)  
윈도우즈 API 모듈내 BlockRequest 를 래핑한 함수입니다.  
  
def get\_dib\_msg1\(self\)  
윈도우즈 API 모듈내 GetDibMsg1 를 래핑한 함수입니다.  
  
def get\_dib\_status\(self\)  
윈도우즈 API 모듈내 GetDibStatus 를 래핑한 함수입니다.  
  
def get\_data\_value\(self, key, value\)  
윈도우즈 API 모듈내 GetDataValue 를 래핑한 함수입니다. key, value 에 대한 GetDataValue 실행 값을 리턴합니다.  
  
def get\_header\_value\(self, key\)  
윈도우즈 API 모듈내 GetHeaderValue 를 래핑한 함수입니다. key 에 대한 GetHeaderValue 실행 값을 리턴합니다.  
  
def set\_input\_value\(self, key, value\)  
윈도우즈 API 모듈내 SetInputValue 를 래핑한 함수입니다. key, value 에 대한 SetInputValue 실행합니다.  
  


\_\_

\_\_

**class Creon**

