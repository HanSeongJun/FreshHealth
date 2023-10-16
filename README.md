# FreshHealth
### 1. 당 제로 맛집 추천 지도
* **`FreshHealth_NaverMap.html`**
<img width="844" alt="스크린샷 2023-10-16 오후 7 29 24" src="https://github.com/HanSeongJun/FreshHealth/assets/67749318/61fc3c3a-03ae-43f2-a10e-ee35aa73e3ee">

**Marker Code**
```hthml
        <!-- #이름 마커 & 정보 START -->
        var #식당이름_변수명 = new naver.maps.Marker({
            position: new naver.maps.LatLng(#위도, #경도),
            map: map
        });

        var #식당이름_변수명_contentString = [
            '<style>',
            '   @font-face {',
            '       font-family: "Pretendard-Regular";',
            '       src: url("https://cdn.jsdelivr.net/gh/Project-Noonnu/noonfonts_2107@1.1/Pretendard-Regular.woff") format("woff");',
            '       font-weight: 400;',
            '       font-style: normal;',
            '   }',
            '</style>',
            '<style>',
            '   .square-image {',
            '       border-radius: 5px; /* 테두리 라운드 크기 조절 */',
            '       border: 1px solid #999;',
            '       transition: border-color 0.3s; /* 테두리 색상 변경에 대한 전환 설정 */',
            '   }',
            '   .square-image:hover {',
            '       border-color: #0080FF; /* 호버 시 테두리 색상 변경 */',
            '   }',
            '</style>',
            '<div class="iw_inner">',
            '   <p style="font-size: 20px; color: rgb(80, 160, 96); font-family: Pretendard-Regular; margin: 10px; margin-bottom: 5px; margin-left: 13px;"><strong>#이름</strong> <span style="font-size: 14px; color: #999;">#식당종류</span></p>',
            '   <p style="font-family: Pretendard-Regular; font-size: 12px; margin: 0px; margin-bottom: 3px; margin-left: 13px; margin-right: 13px;">#도로명주소</p>',
            '   <p style="font-family: Pretendard-Regular; color: #999; font-size: 12px; margin: 3px; margin-left: 13px; margin-right: 13px;">(지번)#번지주소 <span style="font-size: 12px; color: #0080FF; margin-left: 10px;">#번호</span></p>', // 번호를 추가하고 스타일을 적용
            '   <div style="display: flex;">', // 이미지들을 나란히 배치하기 위한 flex 컨테이너
            '       <a href="#네이버지도링크" style="text-decoration: none;" target="_blank">', // 링크 주소를 설정하고 target="_blank" 추가
            '           <img src="https://ifh.cc/g/d4VsOA.png" alt="베지잇 이미지" style="width: 100%; max-width: 130px; height: 35px; margin: 10px;" class="square-image">', // 베이짓 이미지
            '       </a>',
            '       <a href="#네이버지도링크" style="text-decoration: none;" target="_blank">', // 링크 주소를 설정하고 target="_blank" 추가
            '           <img src="https://ifh.cc/g/fRtJSg.jpg" alt="이미지" style="width: 100%; max-width: 130px; height: 35px; margin-top: 10px; margin-right: 10px;" class="square-image">', // 마지막 이미지
            '       </a>',
            '   </div>',
            '</div>'
        ].join('');

        var #식당이름_변수명_infowindow = new naver.maps.InfoWindow({
            content: #식당이름_변수명_contentString,
            maxWidth: 400,
            borderColor: '#CCC', // 테두리 색상 변경
            borderWidth: 1
        });

        naver.maps.Event.addListener(#식당이름_변수명, "click", function(e) {
            if (#식당이름_변수명_infowindow.getMap()) {
                #식당이름_변수명_infowindow.close();
            } else {
                #식당이름_변수명_infowindow.open(map, #식당이름_변수명);
            }
        });
        <!-- #이름 마커 & 정보 END -->
```


