#### meta, description, 간략한설명

#####(0).앞서 알아야 할 내용  
.
    1.검색 엔진들이 검색 결과에서 페이지의 정보를 미리 보여주기 위해서 meta description을 자주 사용한다.
        즉, meta description 태그는 웹페이지의 축약된 설명을 제공하는 태그로, 검색결과 페이지에서 검색자(이용자)에게
        페이지의 요약내용을 미리 보여주는 부분이다.
        [링크 : https://mathbang.net/402]   
        [링크 : https://blog.naver.com/neoworld2009/221841712971]
.
    2.키워드로 채우는 것은 피하고, 각 페이지의 교유의 description을 갖도록 해야한다. 즉, 웹사이트의 모든
        페이지에 동일한 description 메타 태그를 사용하지 않는것이 좋다. 그 예로 더쿠,인스티즈는 메인,글 목록까지는 description이 같은데, 세부 글 내용들어가면 
        그 글의 본문 내용들이 description으로 들어간다. 디시인은 메인, 글 목록, 세부 글 모두 description모두 다르다. 또 디시인 세부 글 들어갔을때 description이 글 본문 인데,
        어느정도 본문이 description에 적히다가 끊긴다. 또한 meta property description과 적혀지는게 똑같다.(끊어지는것도 똑같)         
        [링크 : https://mathbang.net/402]   
        [링크 : https://vanplenetworks.com/ko/%EA%B2%80%EC%83%89%EC%97%94%EC%A7%84-%EC%B5%9C%EC%A0%81%ED%99%94-%EA%B8%B0%EC%B4%88-description-%EB%A9%94%ED%83%80-%ED%83%9C%EA%B7%B8/]
.
    3.노출(설명) 되는 곳 - 구글,네이버에 키워드 검색시, 해당 결과 웹페이지 urlor웹페이지 이름 밑이나, 링크밑의 GNB 밑에 뜬다. 
        네이버
            [PC]
                (1).
            [모바일]
                (2).
.                
        구글
            [PC]
                (1).
            [모바일]
                (2).
.                
        추가내용 :
            1.네이버 모바일에서 웹사이트 검색시에 결과의 url이 m.도메인.com으로 안뜨고 www.도메인.com 혹은 도메인.com으로 뜨는 것
                처음에 link canonical태그가 안되있는곳은 검색결과 웹사이트의 url노출이 m.도메인.com이 아닌 도메인.com으로 뜨는줄알았는데
                '훈스' 홈페이지도 모바일에 그냥 도메인.com으로 뜬다.(즉, 네이버가 임의로 이렇게 하거나, 내가 놓친 태그가 있거나)
                +
                문제는, 디시인사이드 같은경우, 네이버 모바일에서 디시인사이드를 검색하면, 웹사이트 노출에 url이 www.dcinside.com이 나오고
                description란도 pc의 html이 적용된다(gall.dcinside.com, dcinside.com 둘다 모바일과 pc의 html의 meta name description이 다름).
                (모바일 검색인데도), 그런데 어떤 웹사이트 검색하여 m.도메인.com이 url로 노출됬을때, 이 웹사이트의 
                m.도메인.com html문서의 meta name description이 도메인.com(pc버전) html의 meta name description과 다른경우 과연 pc버전의 html을
                해석하여 meta name description을 내놓을지 아니면 모바일버전의 html을 분석하여 meta name description을 내놓을지 확인을 못해봤다.
                즉,
                (1).모바일로 검색하였을시에 도메인.com 혹은 www.도메인.com으로 뜨는경우는 PC버전의 html을 분석하여 description을 노출시키며(www.dcinside.com,
                    gall.dcinside.com 둘다 pc와 모바일 html의 name description이 다름)
                (2).설령 모바일로 검색하였을때, m.도메인.com이 뜬다하여도 모바일의 html을 분석하여 name description을 적용할지 PC의 html을 분석하여 name description
                    을 적용할지 모르니
                =    
                결론 : PC,모바일 둘의 description을 통일시키자.
.                 
            2.구글에서는 모바일로 검색시에 디시인사이드를 검색하면, 웹사이트 노출 url이 m.dcinside.com으로 뜨는데 description 부분에는 www.dcinside.com인 PC버전의 html
                의 name description을 해석하여 노출시킨다. 또한 디시인사이드 갤러리라 치니, 디시인사이드 웹사이트가 노출되며 url이 m.dcinside.com이라 뜨는데 이번에는 모바일
                m.dcinside.com의 name description을 해석하여 설명노출란에 적혀져있었다.
                즉,
                (1).모바일 url(m.도메인.com)이 떠도, PC버전의 html의 name description을 해석하여 노출시키면서, 
                (2).위의 디시인사이드 갤러리를 친경우에는 모바일버전(m.dcinside.com)의 name description이 해석되어 설명노출란에 적혀져있으니
                =
                결론 : PC,모바일 둘의 description을 통일시키자.
.                
            3.네이버는 (1)'meta name description태그' ,(2)'meta property og description태그'중에 (1),(2)둘다 적혀져있으면, (1)을 적용하고,(1)이 없고
                (2)만 있는경우 (2)를 설명노출(네이버 검색시뜨는)란에 적용한다.(ex.아누앤핸-meta name description과 meta og description이 다르다., 플레이송스
                meta name description은 없고 meta og description 태그만 있다.) 하지만, 구글은 (2)는 설명노출란에 전혀 적용시키지 않고, (1)태그의 여부만 상관하여 설명노출란에 적용한다.
                즉, (1)태그는 없고 (2)태그만 있으면, 구글 검색시 웹사이트 설명노출란에 본문내용이 뜬다.(ex.플레이송스 meta name description은 없고 meta og description 태그만 있다.)
                (네이버와 구글의 PC,모바일 검색에서 둘다 이렇게 반영했다.)
.                
            4.네이버에서는 플레이송스 같은 웹사이트의 meta property description를 반영해서 검색시 웹사이트 설명노출란에 표시되지만, 본문내용도 같이 써진다. 
                이 경우, 추측할수있는내용이,
                1.meta name description이 아니여서 저렇게 본문 내용이 보이는거다.
                    -> 하지만 일베사이트(meta name description이 없고,meta og description만 있다.)는 네이버에 검색시에 본문내용이 뜨지 않는다.
                2.아니면 description에 너무 적게 적어서 본문내용이 들어간거다 
                    -> 신세계백화점(meta name description반영),일베(meta og description반영),인스티즈(meta name description 반영)의 경우 contents가 충분히 적은데, 본문내용이 안뜬다.
                    [링크 : https://kin.naver.com/qna/detail.nhn?d1id=1&dirId=10504&docId=335222437&qb=64Sk7J2067KEIO2KueyglSDri6jslrQg6rKA7IOJ7IucIOybueyCrOydtO2KuA==&enc=utf8&section=kin&rank=1&search_sort=0&spq=0]
                3.본문컨텐츠나, 웹페이지완성도(태그들)이 부족하여 그렇게 뜰 수도 있다.
                이렇게 추측해볼 수 있다.
                +
                종결.
                네이버에 키워드를 적어 검색하였을때 설명노출란에 그 해당 홈페이지의 description 태그의 내용보다 본문에 표시되고
                있는 내용이 더 잘 해당 웹사이트를 나타낸다고 하면 네이버 검색시스템이 해당 사이트의 description대신 본문 텍스트가 설명 노출란에 표시될 수 있다 한다.
                [링크 : https://imweb.me/faq?mode=view&category=29&category2=35&idx=28230]
.                
            5.네이버는 모바일에서는 '기업정보 펼쳐보기', PC에서는 '기업정보'란이 있는데, NICE평가정보의 기업정보를 등록하면 설정되는것으로, 
                웹사이트 검색시뜨는 설명노출란에 description에 적어놓는 내용은 안보이고, 이 기업정보의 설명글이 대신 노출된다. 예를들어, 쿠팡은
                (meta name description없고, PC는 meta og description만 있으며, 모바일은 두 태그다 없다.) 네이버에서 PC검색이나 모바일검색시 모두 설명노출란에
                meta og description이 뜨는게 아닌, 기업정보 설명글이 뜬다. 네이버는 PC는 meta name description이 있고, 네이버 모바일은 meta name description은
                없고 meta og description만 있는데, 네이버 PC검색 에서는 설명노출란에 PC의 meta name description이 뜨고, 모바일에서 네이버 검색시에는 기업정보 글이 떳다.
                즉,
                (1).기업정보 설명글이 있으면, meta og description이 있어도 대신할 수 있으며,(쿠팡)
                (2).meta name description가 적혀져있으면 이게 설명노출을 대신하고 meta og description이면 기업설명이 설명노출을 대신한다.(네이버)
                고 볼 수 있다.
                (구글 검색은 상관없다.)
.
[링크 : ]
.
    거기다가 디시인사이드가 오히려 canonical url을 안써서 네이버에 디시인사이드 쳤을때, 디시인사이드 갤러리가 뜨는 거일 수도 있다.
    [링크 : https://kin.naver.com/qna/detail.nhn?d1id=1&dirId=1060107&docId=348816075&qb=64Sk7J2067KEIOuplOyduOyCrOydtO2KuA==&enc=utf8&section=kin&rank=3&search_sort=0&spq=0]
    아니면 구글에 디시인사이드, 디시인사이드 갤러리 쳤을때 각각 m.dcinside.com이 뜨는건 맞지만 서로 다른 html파일을 분석한게 
    canonical 태그가 없어서 그런거 아닌가?
    .
    구글 m.dcinside.com가보면 카카오 맞춤형 광고랑 구글 광고 있는데??
.        
#####(1).전체태그
.
    < meta name="description" content
.    
#####(2).기능
.
    ㅁ
.
#####(3).사용법
.
    ㅁ
.    
#####(4).위치
.
    ㅁ
.
####(5).타 웹사이트 태그예시    
.
    1.더쿠(PC,모바일)
        < meta name="description" content="국내외 이슈 정보 커뮤니티. 일상, 유머, 생활정보, 연예, 국내아이돌, 일본아이돌, 드라마, 배우, 축구, 야구, 배구, 스포츠, 이슈, 뉴스, 시사, 뷰티, 애니, 각종 취미 등">
    2.인스티즈(PC,모바일)
        < meta name="description" content="인스티즈(instiz)">
    3.디시인사이드
        {1}.PC
            < meta name="description" content="국내 최대 커뮤니티 포털, 인터넷 트렌드의 중심 디시인사이드, dcinside">
        {2}.모바일
            < meta name="description" content="내 최대 커뮤니티 포털 디시인사이드. 힛갤러리, 유저이슈 등 인터넷 트렌드 총 집합, gallery, hit gallery, dcgame, dcnews, dc, dcinside. gall, 디시인사이드, 디시, 디씨, 디씨인사이드, 디시뉴스, 갤러리, 갤, 힛갤, 유저이슈, 김유식, 유식대장, 코갤, 코미디프로그램갤러리, 야갤, 국내야구 갤러리">
    3-1.디시인사이드 갤러리
        {1}.PC
            < meta name="description" content="국내 최대 커뮤니티 포털 디시인사이드. 힛갤러리, 유저이슈 등 인터넷 트렌드 총 집합">
        {2}.모바일
            <meta name="description" content="">
    4.아누앤헨(PC,모바일) + (유일하게, meta property description과 meta name description이 다르다.)
        < meta name="description" content="인도 핸드메이드 패브릭 브랜드, 자체제작 침구, 의류, 소품, 원단 직수입, 인도 그릇, 구매대행 서비스 등">
.       

아, 더쿠 서브페이지 내용들이(글 제목아님) meta description으로 들어가고,
제목은 title로 들어가네.

공유하기할때 표현된다는데 이거 알아보기

그리고 네이버나 구글 검색에 밑에도 나오던데 그것도

서브페이지 밑에 나오는것도, 즉 그 안에 글같은거 브라우저검색시 뜨는거

그 외에도, 그냥 링크 공유해도 그 안에 description내용이 뜨네
https://kin.naver.com/qna/detail.nhn?d1id=2&dirId=2010605&docId=334502827&qb=6rWt64K07Jm4IOydtOyKiCDsoJXrs7Qg7Luk666k64uI7Yuw&enc=utf8&section=kin&rank=1&search_sort=0&spq=0
https://blog.naver.com/moojuk01v/221775115105

https://kin.naver.com/qna/detail.nhn?d1id=1&dirId=10501&docId=351849344&qb=64Sk7J2067KEIOybueyCrOydtO2KuCDrk7HroZ0g7J2066aE&enc=utf8&section=kin&rank=1&search_sort=0&spq=0
엥 뭐야 og:description도 충분히 알아야 겠는데??

타이틀이나, description이 오히려 네이버,구글 글 검색이나 웹사이트 노출에 더 도움이되고
description은 홈페이지 공유할때 거기에 description내용이 들어가고, 상세 글은 내용이 들어가기 때문이다.
title은 웹사이트 이름이나 상세 글의 제목이기 때문에 그렇다.
keywords meta태그는 거의 아예 영향을 안주는거같다.
+ 더 찾아봐야 하긴한다.




사이트 설명, description에 해당하는 내용이 가끔반영되지않고, 본문 텍스트가
대신해서 표시될 수도 있다함.
https://imweb.me/faq?mode=view&category=29&category2=35&idx=28230
