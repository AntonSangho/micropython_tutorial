# Rasberry pi Hardware Tutorial

## 준비물  
- 라즈베리파이 400
- SD카드(4G이상)
- 브레드보드
- GPIO연장 커넥터
- 마우스 (블루투스보다는 유선이나 동글이 있는 마우스) 
  
## 운영체제(Operate System) 준비
   1. Raspberry Pi Imager v1.75를 관리자 권한으로 실행
   2. SD card 연결 
   3. "운영체제 선택" -> Rasberry Pi OS Full(32-BIT) , "저장소 선택" -> 연결된 USB장치
   4. 설정
      - Hostname 설정:
        네트워크에 접속된 장치에 주어지는 이름을 설정해줘야하는데, 학생들이 동일한 네트워크에서 장치를 식별하기위해서 각자 고유의 Hostname을 설정해준다. 예) 영문이름+핸드폰번호뒷자리
      - **이름은 기본으로 pi로 진행하는게 나중에 usergroup 명령어를 실행할 때 편할 듯**
        
   6. 쓰기
      - 설정을 마쳤으면 쓰기 버튼을 눌러서 SD card에 이미지를 쓴다. 쓰기 이후에 검사과정이 수행된다. 확인 과정이 끝나면 SD카드를 제거할 수 있다.
   7. 전원연결하고 모니터에 화면이 나오는 것을 확인한다. 
   8. 운영체제 기본세팅
      - 국가 설정 : South Korea
      - 시간 : Seoul
      - 키보드 : Korean
      - Wifi setting
      - 모니터 화면비율설정
         * 라즈베리파이 아이콘 -> 기본설정 -> Raspberry pi Configuration -> Display tab -> Headless Resoluton 을 720x480으로 변경
  9. 업데이트를 진행
      - **(생각보다 시간이 걸리기 때문에 이 시간에 맞춰서 뭔가 이론 수업을 진행하는게 어떨지)**
  10. 재시작 

  ## Thonny사용해보기   
  1. 좌측 상단 라즈베리파이 로고 클릭 -> 개발 -> Thonny 실행
  2. python을 먼저 실행해본다.
     - 에디터 화면에 아래와 같이 입력한 후에 실행을 한다 
     ```python
     print("hello world")
     ```
  3. 하드웨어를 제어해보기
     - [GPIO 권한 설정](https://www.raspberrypi.com/documentation/computers/raspberry-pi.html#permissions): 사용자가 라즈베리파이의 GPIO 그룹 안에 있어야 한다.
     - 터미널을 실행한다.( 좌측 상단에 검정색 네모 아이콘) 그리고 아래의 명령어를 입력한다.
        ```bash
       sudo usermod -a -G gpio <username>```
     - 4번 핀과 GND에 LED를 연결한다. 
     - [python blink 코드작성](https://www.raspberrypi.com/documentation/computers/raspberry-pi.html#led)


### 고려사항   
- 웹 브라우징으 하면서 컴퓨터가 멈추는 현상을 어떻게 해결할 것인가
- 하드웨어를 제어할 때 어떠한 라이브리를 참고 할 것인가
* 네이티브 파이썬을 사용할 것인가 아니면 Circuitpython을 사용할 것인가. 

Adadruit library를 쓸려면 Blinka를 설치해야한다. 



### 참고링크   
- [라즈베리파이 공식사이트 getting started](https://www.raspberrypi.com/documentation/computers/getting-started.html)
- 영어로 된 Tutorial을 번역하기 위해서 chrome extension을 설치 : 구글에 "Chrome translate extention"
