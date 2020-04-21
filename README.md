# 소개

이 creon 패키지는 대신 증권의 비공식 파이썬 클라이언트입니다.  
개발자 경험 Developer Experience 에 초점이 맞추어져 있습니다.  
GPL v3 라이센스 하에 오픈소스 프로젝트로 진행되고 있어 많은 기여와 관심 부탁드립니다.

## 개발자 경험 최우선

{% code title="example.py" %}
```python
from creon.core import Creon


# 환경변수에 등록된 계정값 기반으로 대신증권 클라이언트를 자동으로 로딩합니다.
creon = Creon()

# 종목 코드 가져오기
code = creon.name_to_code('삼성전자')

```
{% endcode %}

## 설치

pip를 이용해 간단하게 설치할 수 있습니다.

```
$ pip install creon
```



