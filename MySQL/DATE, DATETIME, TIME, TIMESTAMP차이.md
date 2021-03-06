# DATE, DATETIME, TIME, TIMESTAMP

## DATE 타입

DATE 타입은 날짜는 포함하지만 시간은 포함하지 않을때 사용하는 타입입니다.

**YYYY-MM-DD 형식** 입력가능하며 **'1000-01-01' 부터 '9999-12-31'** 까지만 입력가능 합니다.

## DATETIME 타입

DATETIME타입은 날짜와 시간을 모두 포함할때 사용하는 타입입니다. 

Mysql 에서 는 **YYYY-MM-DD HH:MM:SS 형식 입력**으로 

**1000-01-01 00:00:00' 부터 9999-12-31 23:59:59** 까지 입력가능합니다.

## TIME 타입

TIME 타입은 HH:MM:SS 으로 시간에 대한 정보를 담는 타입입니다.

TIME 이 가질수 있는 값의 범위는 -838:59:59 ~ 838:59:59 까지 가질 수 있습니다. 

여기서 시간은 날짜중 DAY의 값을 표현할수 있는 범위까지 이기 때문에 838시간이라는 큰 시간까지 포함이 가능합니다.

## TIMESTAMP 타입

TIMESTAMP 타입은 날짜와 시간모두를 포함한 타입입니다.

범위로는 **1970-01-01 00:00:01 ~ 2038-01-19 03:14:07 UTC** 까지 표현할 수 있습니다.

## DATETIME VS TIMESTAMP

DATETIME과 TIMESTAMP는 유사한것 같아 보이지만, 둘의 차이는 다음과 같습니다.

### 1. 타입

DATETIME은 문자형

TIMESTAMP는 숫자형

### 2. 용량

DATETIME은 8byte

TIMESTAMP는 4byte

### 3. 입력

DATETIME은 데이터값을 입력을 해주어야만 날짜가 입력이 됩니다.

TIMESTAMP는 데이터값을 입력해 주지 않고 저장시에 자동으로 현재 날짜가 입력이 됩니다.

출처 : https://blog.naver.com/nieah914/221810697040
