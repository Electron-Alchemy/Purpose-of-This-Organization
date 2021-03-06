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

# 진행 상황 

## [2021/06/16]
react app + electron === 'SUCCESS'  
react app + SQLite3 === 'SUCCESS'  
electron + SQLite3 === 'SUCCESS'  
react app + electron + SQLite3 === 'FAILTURE'  
  
아주 그냥 미치고 환장할 노릇이다.  
하지만 언젠가는 반드시 이 연동을 성공해내기를 바란다.  

## [2021/06/17]
Vue.js + electron + SQLite3를 연동시키려는 노력은 무산되었다.  
그러나 Sequelize를 사용하는 것이 하나의 해법이라는 것은 알게 되었다.  
  
나의 현기술로는 이 계획을 성공시키는데에 한계가 있다.  
그리하여 일단은 React와 그 밖의 라이브러리들을 유연하게 사용하는데 집중하겠다.  
당장의 문제를 해결할 수는 없겠으나, 이 같은 내공이 문제 해결에 간접적인 도움이 될 것이다.  

## [2021/06/19] 새벽 3시
일단 React + Electron을 연동하는데에는 성공했다.  
돌고 돌아서 결국 여기까지 오게 된 것이다.   
당장에 사용할 프로그램의 data는 사실 const한 data이므로, sqlite3를 굳이 연동할 필요는 없을 듯하다.  
많은 js파일에 대해서 import, export를 해야해서 귀찮아질 수는 있겠으나, 그 방법이 오히려 깔끔할 것이다.  
성공 repo : https://github.com/Electron-Alchemy/electron-with-react

## [2021/06/21] 
React + Electron을 연동한 것을 베이스로 localStorage연동까지 성공하였다.  
지금 생각하고 있는 대량의 data는 Only Read만 요구함으로, export, import로 처리하고  
사용자가 쓰는 데이터는 localStorage로 처리하자.  
다만, localStorage는 5MB로 그 크기가 제한 된다.  
이 제한을 해제하는 방법을 알아야 하겠지만, 현실적으로 이 용량 이상을 사용할 경우가 얼마나 있을까?  
사실상 electron기반 stand alone APP에 대한 연구는 이로써 완료되었다고 볼 수 있다.  
