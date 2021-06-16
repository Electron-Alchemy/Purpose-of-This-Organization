# 개요
목적은 단순히 어플리케이션 하나를 만드는 것에서부터 시작하였다.  
하지만 사람의 욕심은 끝이 없는 법이다.  
어플리케이션도 그냥 어플리케이션이 아니라,  
윈도우, 맥, 안드로이드 아이폰 모두에서 돌아가는 프로그램을 개발하고자 한다.  
그러던 도중에 웹 기반으로 어플을 만들면 ~~우려먹기 좋다는~~ 채산성이 좋다는 이야기를 들어서  
바로 웹을 배우기 시작하였다.  
  
하지만 프로젝트를 진행하면서 문제가 생겼다.  
바로 웹 호스팅과 서버비는 결코 무료가 아니라는 점이다.  
하지만 때려죽여도 돈을 내기가 싫었던 나라는 인간은  
결국 웹 호스팅이 아닌 electron으로 앱을 띄우고  
데이터는 서버가 아닌 sqlite3 + local server + IPC로 처리하기로 결심하였다.  

# 목적
electron + sqlite3를 베이스로 두고 그 위에 react를 얹어서 어플 개발을 용이하게 하려고 한다.  
즉, react app + electron + SQLite3의 연동을 하려는 것이다.

# 현재 상황
react app + electron === 'SUCCESS'  
react app + SQLite3 === 'SUCCESS'  
electron + SQLite3 === 'SUCCESS'  
react app + electron + SQLite3 === 'FAILTURE'  
  
아주 그냥 미치고 환장할 노릇이다.  
반드시 이 연동을 성공해내기를 바란다.  
