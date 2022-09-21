# Introduction
OpenWeather API 이용해 날씨 App
* Component Language : JavaScript
* design : Photoshop

# Description
단일 페이지로 구성,사용자가 검색창에 도시명을 입력하면 해당 도시의 온도,습도,풍속,등의 날씨 정보와 현재날짜를 아이콘,사진과 함께 알려주는 앱입니다.

# Creation Period
2022-07-03 ~ 07-05

# finished version
![weather](https://user-images.githubusercontent.com/102776957/190940083-c3f2959d-d37b-48a4-b41c-e0294953b78f.jpg)

# Features
* Ajax처리

# Development(important part)
* openweathermap.org사이트 API key발급 데이터 ?q = 부분을 이용하면 도시명 값, ?id= 도시의 정보를 얻어올수 있다.
* 도시검색을 일일이 넣기 번거러워 아래 주요 도시명을 추가하였다 a태그에 data속성을 추가

* 클릭이벤트를 넣어 각 데이터를 넣어준다.

 ```C
  $(".country-city a").each(function (idx, item) {
        $(item).on("click", function (e) {
          e.preventDefault();
          const newcity = $(item).data("city");
          weathers(newcity);
        });
      });
```

* 날씨에 따라 아이콘,배경 변경하기 json 서버에서 주는 데이터를 가져와 번호에 맞게 데이터를 뿌려줬다. (데이타 중간 중간에 번호가없다)
![1](https://user-images.githubusercontent.com/102776957/190941613-ca28bded-d4a4-4420-8e9c-f9514aaaefc5.JPG)

* 키보드로 입력받기

```C
search.addEventListener('keydown', function(e){
    if(e.keyCode === 13) {
      // 함수실행
    }
}
```
