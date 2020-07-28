###[meta property og] title

####(0).앞서 알아야 할 내용  
.
    1.og(오픈그래프 태그)는 페이스북에서 만든 태그로, 페이스북의 대부분의 콘텐츠는 url로 공유되는데, url입력시 facebook에 콘텐츠가 표시되는 방식을 관리하기
        위해 정보를 제공하는 meta태그를 만들었다. 이는 현제, 네이버(블로그,지식in),티스토리(블로그)와 카카오, 트위터(일부분)에서도 사용되고 있다.
        [링크 : https://blog.naver.com/hightch/221995979923]
.
    2.각각의 매체에 여러 URL을 적용해보았다.(PC버전, 모바일&어플에서 URL 확인)
        (1).네이버 지식in 
            {1}.제목 노출란에 표시
            {2}.< title>태그가 함께 있어도 og:title 적용
            {3}.og:title태그가 없으면 < title>가 대신 표시한다.(celebmine.com으로 해봄)
        (2).네이버 블로그 글쓰기(PC브라우저,모바일브라우저)
            {1}.제목 노출란에 ~ 표시
            {2}.< title>태그가 함께 있어도 og:title 적용
            {3}.og:title태그가 없으면 < title>가 대신 표시한다.(celebmine.com으로 해봄)
        (3).티스토리 블로그 글쓰기(PC브라우저,모바일브라우저)
            {1}.제목 노출란에 ~ 표시
            {2}.< title>태그가 함께 있어도 og:title 적용
            {3}.og:title태그가 없으면 < title>가 대신 표시한다.(celebmine.com으로 해봄)
        (4).페이스북(PC브라우저,어플)
            {1}.제목 노출란에 ~ 표시
            {2}.< title>태그가 함께 있어도 og:title 적용
            {3}.og:title태그가 없으면 < title>가 대신 표시한다.(celebmine.com으로 해봄)        
        (5).트위터(PC브라우저,어플)
            {1}.제목 노출란에 ~ 표시
            {2}.< title>태그가 함께 있어도 og:title 적용
            {3}.og:title태그가 없으면 실행되지 않는다.(celebmine.com으로 해봄) 
        (6).카카오톡(PC소프트웨어,어플)
            {1}.제목 노출란에 ~ 표시
            {2}.< title>태그가 함께 있어도 og:title 적용
            {3}.og:title태그가 없으면 < title>가 대신 표시한다.(celebmine.com으로 해봄)  
        [추가내용]
            1.https://blog.naver.com/ton0070/221999067935 네이버 블로그를 네이버 지식in, 네이버 블로그 글쓰기, 티스토리 블로그 글쓰기, 페이스북에 url올려놓아도 요약문에
                제목 부분에 < title>이 뜨는데(여긴 og:title이 없다.) title의 ': 네이버 블로그'만 빼고 뜬다. 디시인사이드도, https://gall.dcinside.com/board/view/?id=hit&no=15891
                이 링크 url 올려보면 '- HIT 갤러리'가 있는데 네이버 블로그 url 올린것과는 다르게 이것도 요약문의 제목 부분에 그대로 노출된다.
                (추가내용 : 인스티즈 글, https://www.instiz.net/pt/6756991?happystart=1 도 네이버 지식in 글쓰기나 네이버 블로그 글 쓰기 하면, 마지막에 title의 '- 인스티즈'가 빠져서
                제목란에 보이는데, 이는 og:title이 적용되서 그렇다. 위에 네이버 블로그 글을 살펴보니 < head>태그안에 og:title 태그가 안보여도, < body>태그 라든지 그 안에 og:title의 역활을 하는
                태그가 있거나, og:title을 < body>태그안에서 적용하는 방식이 있는것 같다.), 
                아니면,
                https://blog.naver.com/PostView.nhn?blogId=ton0070&logNo=221999067935&proxyReferer=https:%2F%2Fblog.naver.com%2Fton0070%2F221999067935 이 url과
                https://blog.naver.com/ton0070/221999067935 이 네이버 블로그 url이 같은 내용을 포함하고있는데, 첫번째 url에는 og:title, og:description이 모두 적혀져있었다. 여기에는 < title>에는 ': 네이버 블로그'가 붙는데
                og:title에는 ': 네이버 블로그'가 안붙는다. 이것과도 연관이 있는것 같다.
                이것과 관련해서더 알아야 할 사항이 있으면 더 공부하자
            2.https://theqoo.net/cook/1515298974의 경우, < title>에 피자모양 이모티콘이 들어가고, og:title에도 피자모양 이모티콘이 들어가는데,
                크롬 브라우저 탭란에도 표시가 되고, og:title의 경우도, 지식in,네이버블로그,티스토리,카카오톡,페이스북,트위터모두 피자모양 이모티콘이 잘 표현됬다.. 근데, 잘 보면 더쿠의 og:title에는
                &#x1f355 라는 코드가 적혀져있는데, 이게 모두 피자모양으로 보여져서 적용되는거다.
                (브라우저 탭란에 이모티콘이 들어가는것에 대해 더 공부해야할 필요가 있으면 하기, 또한 og:title에 자동으로 코드삽입 되는것에 대해 필요한 사항이 있으면 하기)
            3.위의 내용들은 모두 PC브라우저와 어플(트위터,페이스북,카카오톡),모바일(네이버,티스토리)에서 모두 확인한 결과다.
.
####(1).전체태그
.
    < meta property="og:title" content="~">
.
####(2).기능
.
    각 매체별 url입력시 미리보기의 제목을 보여줌
.
####(3).위치
.
    meta name태그 아래에 보통 위치시킨다.
.
####(4).타 웹사이트 태그예시   
. 
        1.인스티즈
            [링크 : https://www.instiz.net/pt/6756991]
                < meta property="og:title" content="2004년경 유행했다는 중학생 패션.jpg">
                < title>2004년경 유행했다는 중학생 패션.jpg - 인스티즈(instiz) 인티포털< /title>
            [링크 : https://www.instiz.net/name/37227136]
                < meta property="og:title" content="여행일정 어떤지봐죠ㅋㅋㅋ😊😍">
                < title>여행일정 어떤지봐죠ㅋㅋㅋ😊😍 - 인스티즈(instiz) 익명잡담< /title>
        2.더쿠
            [링크 : https://theqoo.net/cook/1515298974]
                < meta property="og:title" content="포테이토 피자&amp;#x1f355; - 요리 카테고리">
                < title>포테이토 피자🍕 - 요리 카테고리< /title>
        3.디시인사이드
            [링크 : https://gall.dcinside.com/board/view/?id=hit&no=15891]
                < meta property="og:title" content="[스압] 평범한 가정식 저녁밥상 (6월) - HIT 갤러리">
                < title>[스압] 평범한 가정식 저녁밥상 (6월) - HIT 갤러리< /title>
        4.네이버
            [링크 : https://www.naver.com/]   
                < meta property="og:title" content="네이버">
                < title>NAVER< /title>
            [링크 : https://blog.naver.com/ton0070/221999067935]
                x(못찾음)
                < title>[국민] 정국이 지민에게 미안했던 것 : 네이버 블로그< /title>
        5.셀럽마인
            [링크 : http://www.celebmine.com/]   
            [링크 : http://celebmine.com/hi1/detail.html]
.