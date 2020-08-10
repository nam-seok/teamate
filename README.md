# teamate

# hyperledger fabric sample 

## pre-condition

* curl, docker, docker-compose, go, nodejs, python 
* hyperledger fabric-docker images are installed
* GOPATH are configured
* hyperledger bineries are installed (cryptogen, configtxgen ... etcs)

# -network

## 1. generating crypto-config directory, genesis.block, channel and anchor peer transactions

cd network

./generate.sh

## 2. starting the network, create channel and join 

./start.sh

# -chaincode

## 3. chaincode install, instsantiate and test(invoke, query, invoke)

./cc_tea.sh instantiate v1.0

# -prototype

cd ../prototype

## 4. nodejs module install

npm install

## 5. certification works

node enrollAdmin.js

node registerUser.js

## 6. server start

node server.js

## 7. open web browser and connect to localhost:8080



#### prototype 사이트 맵 구조

![](C:\Users\27\Downloads\Untitled Diagram.jpg)

#### -web_templete

1. #### teamate network로 이동

   ```powershell
   cd teamate
   ```

2. #### ./teardown.sh 실행을 통해 container 제거

   ```powershell
   ./teardown.sh
   ```

3. #### ./start.sh 실행을 통한 network 실행

   ```powershell
   ./start.sh
   ```

4. #### ./cc_tea.sh 실행을 통한 chaincode install

   ```powershell
   ./cc_tea.sh instantiate v1.0
   ```

5. #### web_template로 이동 후 npm을 이용한 라이브러리 설치

   ```powershell
   cd ../web_template && npm install
   ```

6. #### enrollAdmin.js 실행을 통한 adminID 등록

   web_template 폴더 안에 Wallet 폴더가 존재하면 삭제 후 다음과 같은 명령어 실행

   ```powershell
   node enrollAdmin.js
   ```

7. ####  registerUser.js 실행을 통한 User 등록

   ```powershell
   node registerUser.js
   ```

8. #### server start

   ```powershell
   node server.js
   ```

   

9. #### 구성 및 소개영상

   ![Untitled Diagram (1)](C:\Users\27\Downloads\Untitled Diagram (1).png)

   <video src="C:\Users\27\Downloads\ezgif.com-video-to-gif.mp4"></video>

![Untitled Diagram (2)](C:\Users\27\Downloads\Untitled Diagram (2).jpg)

#### Template 시나리오 모드

![Untitled Diagram (1)](C:\Users\27\Downloads\Untitled Diagram (1).jpg)



