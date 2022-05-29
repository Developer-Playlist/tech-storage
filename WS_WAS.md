<iframe width="1496" height="664" src="https://www.youtube.com/embed/6xl3wKMjmWg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


<h3>WS와 WAS</h3>

- WS : Web Server / IIS, nginx 등
- WAS : Web Application Server / Django, Flask 등 

<h3>WS의 기능 (전반적인)</h3>

- 인증
- 정적 콘텐츠 관리
- HTTPS 지원
- 콘텐츠 압축
- 가상 호스팅
- 대용량 파일 지원
- 대역폭 스로틀링

<h3>WS의 빠른 이해 (정적 콘텐츠 관리 측면) </h3>

- `<img src='imgsrc'>` 는 Web Application Server 까지 갈 필요가 없음
- 따라서 WS 선에서 처리
