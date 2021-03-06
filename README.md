 ## 기술조사
- Vue
- Vuex
- Vue-router
- axios
- dragula

## 기능구현
- SPA
- 인증
- 트렐로 

## 작업
퍼블리셔 -> FE : html, css             
BE -> FE : API             
FE는 html, css, API를 가지고 js(Vue)로 작업             

## 화면
#### 홈화면 
로그아웃 상태                  
email, pwd 입력하면 로그인         
![1](https://user-images.githubusercontent.com/42309919/108061802-2b623e80-709c-11eb-8935-fd49ac7ef88e.PNG)

#### 홈화면 
로그인 상태             
board 리스트 노출         
board 생성                  
![2](https://user-images.githubusercontent.com/42309919/108061804-2bfad500-709c-11eb-8b89-913c4295c868.PNG)

#### board 생성 
![3](https://user-images.githubusercontent.com/42309919/108061743-1a193200-709c-11eb-9285-f0028f9e8432.PNG)

#### card 생성 
![4](https://user-images.githubusercontent.com/42309919/108061746-1ab1c880-709c-11eb-9fd5-72da28c0309c.PNG)

#### card 설명 추가   
![6](https://user-images.githubusercontent.com/42309919/108061750-1b4a5f00-709c-11eb-829c-fc4f5859c784.PNG)

#### board, card 드래그 위치 변경 
![5](https://user-images.githubusercontent.com/42309919/108061749-1b4a5f00-709c-11eb-97c5-c7d5f171c305.PNG)

#### side 메뉴 
board 삭제              
배경색 변경                 
![7](https://user-images.githubusercontent.com/42309919/108061751-1be2f580-709c-11eb-8e8c-9d8403309b5d.PNG)
![8](https://user-images.githubusercontent.com/42309919/108062810-a5df8e00-709d-11eb-989a-ba0d3aec829a.PNG)

## API List
#### Helath
curl localhost:3000/health
#### Login
curl -X POST localhost:3000/login -d 'email=test@test.com&password=123123'
*** 
#### Get board list
curl localhost:3000/boards -H 'Authorization: Bearer token'
#### Get board
curl localhost:3000/boards/1 -H 'Authorization: Bearer token'
#### Add board
curl -X POST localhost:3000/boards -H 'Authorization: Bearer token' -d "title=string"
#### Edit board
curl -X PUT localhost:3000/boards/1 -H 'Authorization: Bearer token' -d "title=string&bgColor=string"
#### Delete board
curl -X DELETE localhost:3000/boards/1 -H 'Authorization: Bearer token'"
***
#### Add list
curl -X POST localhost:3000/lists -H 'Authorization: Bearer token' -d "title=string&boardId=number&pos=number"
#### Edit list
curl -X PUT localhost:3000/lists/1 -H 'Authorization: Bearer token' -d "title=string&pos=number"
#### Delete list
curl -X DELETE localhost:3000/lists/1 -H 'Authorization: Bearer token'
*** 
#### Add card
curl -X POST localhost:3000/cards -H 'Authorization: Bearer token' -d "title=string&listId=number&pos=number"
#### Get card
curl localhost:3000/cards/1 -H 'Authorization: Bearer token'
#### Edit card
curl -X PUT localhost:3000/cards/1 -H 'Authorization: Bearer token' -d "title=string&description=string&listId=number&pos=number"
#### Delete card
curl -X DELETE localhost:3000/cards/1 -H 'Authorization: Bearer token'

## 완강은 즐거웡 :D 
![trello](https://user-images.githubusercontent.com/42309919/108055546-79267900-7093-11eb-84b3-1b63867b5a51.PNG)

