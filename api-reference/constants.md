---
description: 'https://github.com/Golden-Goose-Lab/creon/blob/master/creon/constants.py'
---

# constants

### TimeFrameUnit

_**class TimeFrameUnit\(Enum\)**_  
간 단위를 다루기 위한 이넘 클래스 입니다.   
  
_속성_  
**TICK \(값 'T'\)**  
틱을 의미합니다.  
  
__**MINUTE \(값 'm'\)**  
분을 의미합니다.  
  
__**DAY \(값 'D'\)**  
일을 의미합니다.  
  
__**WEEK \(값 'W'\)**  
주를 의미합니다.  
  
__**MONTH \(값 'M'\)**  
월\(달\)을 의미합니다.

### 

###  AccountFilter

**class AccountFilter\(IntFlag\)**  
크레온 API 에서 요구하는 계좌 유형을 다루기 위한 정수형 이넘 클래스입니다.  
  
_속성_  
**ALL \(값 -1\)**  
전체 유을 의미합니다.  
  
__**STOCK \(값 1\)**  
주식 계좌를 의미합니다.

**NATIONAL\_FUTURE \(값 2\)**  
선물 / 옵션 계좌를 의미합니다.  
  
__**EUREX \(값 16\)**  
EUREX 계좌를 의미합니다.  
  
__**INTERNATIONAL\_FUTURE \(값 64\)**  
해외 선물 계좌를 의미합니다.



