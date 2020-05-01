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





#### Creon

_class Creon_  
크레온 래퍼 클래스입니다. 모든 주식 트레이딩 기능은 이 클래스 객체를 기반으로 수행합니다.

_속성_  
\_\_codes\_\_ - 크레온 API 코드 모듈인 **CpUtil.CpCodeMgr** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
\_\_utils\_\_ - 크레온 API 유틸 모듈인 **CpTrade.CpTdUtil** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
\_\_trades\_\_ - 크레온 API 거래 모듈인 **CpTrade.CpTd0311** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
\_\_trade\_actions\_\_ - sell 와 buy 의 문자열을 각 각 1, 2로 치환 이용하기 위한 딕셔너리 입니다.  
\_\_markets\_\_ - 크레온 API 시장 모듈인 **DsCbo1.StockMst** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
\_\_wallets\_\_ - 크레온 API 계좌 모듈인 **CpTrade.CpTd6033** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
\_\_stock\_code\_\_ - 크레온 API 주식 코드 모듈인 **CpUtil.CpStockCode** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
\_\_chart\_\_ - 크레온 API 주식 차트 모듈인 **CpSysDib.StockChart** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
\_\_Logger\_\_ - 로깅을 위한 파이썬 내장 로거 객체가 할당됩니다.

_메소드_  
def \_\_init\_\_\(self, username: str = '', password: str = '', cert\_password: str = '', path: str = ''\)  
생성자 함수입니다. 관리자 권한이 없으면 PermissionError 예외를 발생시키며 크레온이 구동되어 있지 않으며 [run\_creon\_plus](utils.md#run_creon_plus) 를 통해 구동합니다.  


