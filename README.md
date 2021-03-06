# Geocoder Python Version

## 개요
> 2018년 진행한 졸업 프로젝트의 데이터베이스를 구축하기 위해 제작한 파이썬 코드 입니다.
>
> 졸업 프로젝트로 제작한 안드로이드 앱에서 사용된 구글 지도에 마커를 찍기 위해서는 도로명 주소가 아닌 위도와 경도 값을 필요로 합니다.
>
> 따라서, 사전에 도로명 주소로 크롤링한 주소를 안드로이드 앱에서 사용하기 위해 위도와 경도로 변경하는 코드 입니다.


## 구현 내용
> Google API를 이용하여 주소를 윈도, 경도로 바꿔는 코드
>
> 엑셀(.xlsx 형식)파일에서 주소를 읽어 해당 주소를 위도와 경도를 변환한다.
>
> 예) address.xlsx 파일의 1열의 주소를 위도(2열), 경도(3열)로 변환한다.
>
> 주소 | 경도 | 위도
> --------- | --------- | --------
> 서울 강남구 선릉로 836 삼원빌딩 1~2층 | 37.5265058 | 127.0405179

## 사용방법
> convertPlace.py 소스코드 파일과 address.xlsx 엑셀파일을 같은 경로에 위치시킨다.
>
> convertPlace.py를 실행하면 같은 폴더 위치에 있는 address.xlsx 파일의 첫번째 열에 위치한 주소를 읽어온다.
>
> 읽어온 첫번째 열을 위도와 경도로 변환하고, 이를 2열(경도)과 3열(위도)에 저장하게 된다.
>
> 변환 과정은 Google의 Geocoder를 이용하고, 변환에 실패한 경우에 일정시간이 지난 후에 재시도를 하게 된다.
>
> 변환 결과는 위의 구현내용의 예를 참고하면 된다.
>

