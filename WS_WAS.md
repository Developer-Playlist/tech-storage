<h3>Youtube 참고자료</h3>
{즉문즉설} WAS와 WS의 차이점은? (feat. Nginx, Node Express, Flask) 

[![WS_WAS](https://i.ytimg.com/vi/6xl3wKMjmWg/hqdefault.jpg?s…AFwAcABBg==&rs=AOn4CLAPDX4cbHWuKmJzy-aBQ45nMft-ag)](https://www.youtube.com/watch?v=6xl3wKMjmWg "{즉문즉설} WAS와 WS의 차이점은? (feat. Nginx, Node Express, Flask)")

```
cf. 
- github markdown 은 iframe (tag), target="_blank" (attr) 등을 지원안함 
- 새창에서 보고싶다면 cmd 누르고 클릭
```

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
