# 사용 방법

## 의존성 설치

대신증권의 HTS인 크레온과 API 인터페이스인 크레온 플러스 설치가 필요합니다.

아래 공식 링크에 접속하여 설치가 가능합니다. 설치 뒤 통신이 제대로 이루어지는지 확인을 권장합니다.

{% embed url="https://money2.creontrade.com/E5/WTS/Customer/GuideTrading/CW\_DownloadCenter.aspx" %}

## creon 패키지 설치

```bash
$ pip install creon
```

## 환경 변수

{% hint style="info" %}
환경변수를 사용하지않고 [Creon 객체 생성](api-reference/core.md#creon)시 인자로 로그인 정보를 넘겨주어 사용할 수도 있습니다. 
{% endhint %}

```
set CREON_USERNAME=크레온 로그인 아이디
set CREON_PASSWORD=크레온 로그인 비밀번호
set CREON_CERTIFICATION_PASSWORD=크레온 로그인 공인인증서 비밀번호
set CREON_PATH=크레온 설치 경로
```

## 기본적인 사용

{% hint style="danger" %}
크레온 플러스\(API\)는 64비트를 지원하지 않습니다, 따라서 32비트 파이썬으로 구동하여야 합니다.
{% endhint %}

### 매수 매도

[https://github.com/Golden-Goose-Lab/creon/blob/master/examples/buy\_and\_sell.py](https://github.com/Golden-Goose-Lab/creon/blob/master/examples/buy_and_sell.py)  
특정 가격을 기준으로 2% 이상 등락시 매수와 매도를 반복하는 예제 입니다.

### 시세 확인

[https://github.com/Golden-Goose-Lab/creon/blob/master/examples/fetch\_price.py](https://github.com/Golden-Goose-Lab/creon/blob/master/examples/fetch_price.py)  
특정 종목의 1년, 한달,  일주일, 어제의 시세 정보를 가져오는 예제입니다.

### 계좌 확인

[https://github.com/Golden-Goose-Lab/creon/blob/master/examples/fetch\_balance.py](https://github.com/Golden-Goose-Lab/creon/blob/master/examples/fetch_balance.py)  
로그인 된 계정의 계좌를 잔고, 보유 종목을 확인하는 예제입니다.



