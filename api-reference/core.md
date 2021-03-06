---
description: 'https://github.com/Golden-Goose-Lab/creon/blob/master/creon/core.py'
---

# core

#### COMWrapper

_**class COMWrapper**_  
크레온 윈도우즈 API를 손쉽게 다루기 위한 래핑 클래스입니다. 

_속성_  
**com**  
디스패치된 윈도우즈 API 모듈입니다.

_메소드_  
**def \_\_init\_\_\(self, com\)**  
생성자 함수입니다. 인자로 사용하려는 윈도우즈 API 모듈을 받습니다.

**def \_\_getattr\_\_\(self, item\)**  
디스패치된 윈도우즈 API 모듈내 함수나 변수를 바로 클래스 네이티브처럼 사용하기 위한 함수입니다.  
  
**def block\_request\(self\)**  
윈도우즈 API 모듈내 BlockRequest 를 래핑한 함수입니다.  
  
**def get\_dib\_msg1\(self\)**  
윈도우즈 API 모듈내 GetDibMsg1 를 래핑한 함수입니다.  
  
**def get\_dib\_status\(self\)**  
윈도우즈 API 모듈내 GetDibStatus 를 래핑한 함수입니다.  
  
**def get\_data\_value\(self, key, value\)**  
윈도우즈 API 모듈내 GetDataValue 를 래핑한 함수입니다. key, value 에 대한 GetDataValue 실행 값을 리턴합니다.  
  
**def get\_header\_value\(self, key\)**  
윈도우즈 API 모듈내 GetHeaderValue 를 래핑한 함수입니다. key 에 대한 GetHeaderValue 실행 값을 리턴합니다.  
  
**def set\_input\_value\(self, key, value\)**  
윈도우즈 API 모듈내 SetInputValue 를 래핑한 함수입니다. key, value 에 대한 SetInputValue 실행합니다.





#### Creon

_**class Creon**_  
크레온 래퍼 클래스입니다. 모든 주식 트레이딩 기능은 이 클래스 객체를 기반으로 수행합니다.

_속성_  
**\_\_codes\_\_**  
크레온 API 코드 모듈인 **CpUtil.CpCodeMgr** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
  
**\_\_utils\_\_**  
크레온 API 유틸 모듈인 **CpTrade.CpTdUtil** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
  
**\_\_trades\_\_**  
크레온 API 거래 모듈인 **CpTrade.CpTd0311** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
  
**\_\_trade\_actions\_\_**  
sell 와 buy 의 문자열을 각 각 1, 2로 치환 이용하기 위한 딕셔너리 입니다.  
  
**\_\_markets\_\_**  
크레온 API 시장 모듈인 **DsCbo1.StockMst** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
  
**\_\_wallets\_\_**  
크레온 API 계좌 모듈인 **CpTrade.CpTd6033** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
  
**\_\_stock\_code\_\_**  
크레온 API 주식 코드 모듈인 **CpUtil.CpStockCode** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
  
**\_\_chart\_\_**  
크레온 API 주식 차트 모듈인 **CpSysDib.StockChart** 의 **COMWrapper** 객체가 할당됩니다. 속성 함수로 이용 가능합니다.  
  
**\_\_logger\_\_**  
로깅을 위한 파이썬 내장 로거 객체가 할당됩니다.

_메소드_  
**def \_\_init\_\_\(self, username: str = '', password: str = '', cert\_password: str = '', path: str = ''\)**  
생성자 함수입니다. 관리자 권한이 없으면 PermissionError 예외를 발생시키며 크레온이 구동되어 있지 않으며 [run\_creon\_plus](utils.md#run_creon_plus) 를 통해 구동합니다.

**@property  
def codes\(self\) -&gt; COMWrapper**  
크레온 API 코드 모듈인 **CpUtil.CpCodeMgr** 의 사용을 위한 속성 함수입니다. 최초 실행시 \_\_codes\_\_ 속성에 **COMWrapper** 객체를 할당하며 이후 \_\_codes\_\_ 를 리턴합니다.

**@property  
def trades\(self\) -&gt; COMWrapper**  
크레온 API 거래 모듈인 **CpTrade.CpTd0311** 의 사용을 위한 속성 함수입니다. 최초 실행시 \_\_trades\_\_ 속성에 **COMWrapper** 객체를 할당하며 이후 \_\_trades\_\_ 를 리턴합니다.

**@property  
def markets\(self\) -&gt; COMWrapper**  
크레온 API 시 모듈인 **DsCbo1.StockMst** 의 사용을 위한 속성 함수입니다. 최최초 실행시 \_\_\_markets\_\_ 속성에 **COMWrapper** 객체를 할당하며 이후 \_\_\_markets\_\_ 를 리턴합니다.  
[http://cybosplus.github.io/cpdib\_rtf\_1\_/stockmst.htm](http://cybosplus.github.io/cpdib_rtf_1_/stockmst.htm)

**@property  
def wallets\(self\) -&gt; COMWrapper**  
크레온 API 계좌 모듈인 **CpTrade.CpTd6033** 의 사용을 위한 속성 함수입니다. 최초 실행시 \_\_wallets\_\_ 속성에 **COMWrapper** 객체를 할당하며 이후 \_\_wallets\_\_ 를 리턴합니다.

**@property  
def stock\_code\(self\) -&gt; COMWrapper**  
크레온 API 주식 코드 모듈인 **CpUtil.CpStockCode** 의 사용을 위한 속성 함수입니다. 최초 실행시 \_\_stock\_code\_\_ 속성에 **COMWrapper** 객체를 할당하며 이후 \_\_stock\_code\_\_ 를 리턴합니다.

**@property  
def chart\(self\) -&gt; COMWrapper**  
크레온 API 주식 차트 모듈인 **CpSysDib.StockChart** 의 사용을 위한 속성 함수입니다. 최초 실행시 \_\_chart\_\_ 속성에 **COMWrapper** 객체를 할당하며 이후 \_\_chart\_\_ 를 리턴합니다.

**@property  
def accounts\(self\) -&gt; tuple**  
utils 속성 함수를 통해 로그인된 계정의 계좌번호들을 튜플 형태로 리턴합니다.

**def get\_account\_flags\(self, account: str, account\_filter: AccountFilter\) -&gt; tuple**  
utils 속성 함수를 통해 계좌 플래그을 리턴하는 함수입니다. 인자로 계좌 번호와 [계좌 유형](constants.md#accountfilter)을 받습니다. 계좌 플래그는 거래 함수등에 사용됩니다.

**def get\_all\_codes\(self, category: str, with\_name: bool = False\) -&gt; tuple**  
codes 속성 함수를 통해 시장\(kospi, kosdaq\)을 문자열로 인자로 받아 해당 시장의 모든 종목을 튜플로 리턴하는 함수입니다. with\_name 인자가 True이면 \(코드, 이름\) 형태의 튜플들을 리턴합니다.  
  
**def get\_price\_data\(self, code: str\) -&gt; dict**  
markets 속성 함수를 통해 시세 정보를 딕셔너리로 리턴합니다. 반환하는 데이터는 아래와 같습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xD0A4;</th>
      <th style="text-align:left">&#xAC12;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">code</td>
      <td style="text-align:left">&#xC885;&#xBAA9; &#xCF54;&#xB4DC;</td>
    </tr>
    <tr>
      <td style="text-align:left">name</td>
      <td style="text-align:left">&#xC885;&#xBAA9; &#xC774;&#xB984;</td>
    </tr>
    <tr>
      <td style="text-align:left">time</td>
      <td style="text-align:left">&#xC2DC;&#xAC04;4</td>
    </tr>
    <tr>
      <td style="text-align:left">diff</td>
      <td style="text-align:left">&#xC804; &#xC77C; &#xB300;&#xBE44;</td>
    </tr>
    <tr>
      <td style="text-align:left">price</td>
      <td style="text-align:left">&#xAC00;</td>
    </tr>
    <tr>
      <td style="text-align:left">close_price</td>
      <td style="text-align:left">&#xC885;&#xAC00;</td>
    </tr>
    <tr>
      <td style="text-align:left">high_price</td>
      <td style="text-align:left">&#xACE0;&#xAC00;</td>
    </tr>
    <tr>
      <td style="text-align:left">low_price</td>
      <td style="text-align:left">&#xC800;&#xAC00;</td>
    </tr>
    <tr>
      <td style="text-align:left">offer</td>
      <td style="text-align:left">&#xB9E4;&#xB3C4;&#xD638;&#xAC00;</td>
    </tr>
    <tr>
      <td style="text-align:left">bid</td>
      <td style="text-align:left">&#xB9E4;&#xC218;&#xD638;&#xAC00;</td>
    </tr>
    <tr>
      <td style="text-align:left">volume</td>
      <td style="text-align:left">&#xAC70;&#xB798;&#xB7C9;</td>
    </tr>
    <tr>
      <td style="text-align:left">volume_price</td>
      <td style="text-align:left">&#xAC70;&#xB798;&#xC561;</td>
    </tr>
    <tr>
      <td style="text-align:left">expect_flag</td>
      <td style="text-align:left">
        <p>&#xC608;&#xC0C1; &#xCCB4;&#xACB0; &#xAD6C;&#xBD84; &#xD50C;&#xB798;&#xADF8;</p>
        <p>&apos;0&apos; - &#xB3D9;&#xC2DC;&#xD638;&#xAC00; &#xBC0F; &#xC7A5; &#xC774;&#xC678;
          &#xC2DC;&#xAC04;</p>
        <p>&apos;1&apos; - &#xB3D9;&#xC2DC; &#xD638;&#xAC00; &#xC2DC;&#xAC04;</p>
        <p>&apos;2&apos; - &#xC7A5;&#xB0B4;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">expect_price</td>
      <td style="text-align:left">&#xC608;&#xC0C1; &#xCCB4;&#xACB0;&#xAC00;</td>
    </tr>
    <tr>
      <td style="text-align:left">expect_diff</td>
      <td style="text-align:left">&#xC804; &#xC77C; &#xB300;&#xBE44; &#xC608;&#xC0C1; &#xCCB4;&#xACB0;&#xAC00;</td>
    </tr>
    <tr>
      <td style="text-align:left">expect_volume</td>
      <td style="text-align:left">&#xC608;&#xC0C1; &#xCCB4;&#xACB0; &#xC218;&#xB7C9;</td>
    </tr>
  </tbody>
</table>**def fetch\_ohlcv\(self, code: str, timeframe: tuple, since: datetime, limit: int, fill\_gap=False, use\_adjusted\_price=True\) -&gt; List\[**[**Candle**](types.md#candle)**\]:**  
chart 속성 함수를 통해 과거 시세 정보 OHLCV\(시가, 고가, 저가, 종가, 거래량\) 를 리턴하는 함수 입니다. 종목 코드, 타임프레임\(시간값, [TimeFrameUnit](constants.md#timeframeunit)\), 조회일, 최대조회수 를 인자로 받습니다. fill\_gap 선택 인자를 True 로 하면 갭보정을 적용 할 수 있으며 use\_adjusted\_price 선택인자를 False 로 하면 수정주가 사용을 안 할 수 있습니다.   
이 [링크](https://github.com/Golden-Goose-Lab/creon/blob/master/examples/fetch_price.py)에서 예제를 확인할 수 있으며 반환하는 데이터는 아래와 같습니다.

|  |  |
| :--- | :--- |
| start\_time | 시작일 |
| end\_time | 종료일 |
| open\_price | 시가 |
| high\_price | 고가 |
| low\_price | 저가 |
| close\_price | 종가 |
| volume | 거래량 |

**def get\_holding\_stocks\(self, account\_number: str, flag: str, count: int = 50\) -&gt; dict**  
wallets 속성 함수를 통해 종합 보유 자산 정보를 딕셔너리로 리턴합니다. 계좌번호와 계좌 플래그를 인자로 받으며 개수는 50개로 선택 인자로 받습니다. 계좌 플래그는 get\_account\_flags 를 통해 얻을 수 있습니다. 반환하는 데이터는 아래와 같습니다.

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#xD0A4;</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">total_expect_valuation</td>
      <td style="text-align:left">&#xCD1D; &#xD3C9;&#xAC00; &#xAE08;&#xC561;</td>
    </tr>
    <tr>
      <td style="text-align:left">remain_deposit</td>
      <td style="text-align:left">&#xC608;&#xC218;&#xAE08;</td>
    </tr>
    <tr>
      <td style="text-align:left">stocks</td>
      <td style="text-align:left">
        <p>&#xBCF4;&#xC720; &#xC8FC;&#xC2DD; &#xB515;&#xC154;&#xB108;&#xB9AC; &#xB9AC;&#xC2A4;&#xD2B8;
          <br
          />&#xB515;&#xC154;&#xB108;&#xB9AC; &#xC608;
          <br />{
          <br />&apos;code&apos;: &#xC885;&#xBAA9;&#xCF54;&#xB4DC;,
          <br />&apos;name&apos;: &#xC885;&#xBAA9;&#xBA85;,
          <br />&apos;quantity&apos;: &#xC218;&#xB7C9;,
          <br />&apos;bought_price&apos;: &#xB9E4;&#xC785;&#xAE08;&#xC561;,
          <br />&apos;expect_price&apos;: &#xD3C9;&#xAC00;&#xAE08;&#xC561;,</p>
        <p>&apos;expect_profit&apos;: &#xD3C9;&#xAC00;&#xC218;&#xC775;,
          <br />}</p>
      </td>
    </tr>
  </tbody>
</table>**def \_order\(self, account: str, code: str, quantity: int, price: int, flag: str, action: str\) -&gt; bool**  
trades 속성 함수를 통해 지정가 주문하여 주문의 성공\(체결 X\) 여부를 True / False 로 리턴합니다. 계좌번호, 종목코드, 수량, 가격, 계좌 플래그, 액션\(매수 or 매도\) 를 인자로 받으며 액션은 'buy', 'sell' 문자열로 받아 \_\_trade\_actions\_\_ 속성을 통해 값을 치환하여 사용합니다. 계좌 플래그는 get\_account\_flags 를 통해 얻을 수 있습니다.

**def buy\(self, account: str, code: str, quantity: int, price: int, flag: str\) -&gt; bool**  
\_order 함수를 통해 지정가 매수를 합니다. 계좌번호, 종목코드, 수량, 가격, 계좌 플래그가 필요합니다. 계좌 플래그는 get\_account\_flags 를 통해 얻을 수 있습니다.

**def sell\(self, account: str, code: str, quantity: int, price: int, flag: str\) -&gt; bool**  
\_order 함수를 통해 지정가 매도를 합니다. 계좌번호, 종목코드, 수량, 가격, 계좌 플래그가 필요합니다. 계좌 플래그는 get\_account\_flags 를 통해 얻을 수 있습니다.

**def code\_to\_name\(self, code: str\)**  
stock\_code 속성 함수를 통해 종목 코드를 종목 이름으로 리턴합니다.

**def name\_to\_code\(self, name: str\)**  
stock\_code 속성 함수를 통해 종목 이름을 종목 코드로 리턴합니다.



