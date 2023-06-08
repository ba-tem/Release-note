# **Release History of BA-Studio**

## **$\textcolor{dodgerblue}{\textsf{Version 2.3.0 - Jun 09, 2023}}$**  
### *신규*
- 시작페이지 생성 : 신규 파일, 파일 오픈, 신규 프로젝트, 프로젝트 오픈을 선택할 수 있는 시작 페이지 생성
- [debug] 폰트 및 폰트 사이즈 변경, 창 크기 변경, 속도 향상을 위해 컨트롤 변경   
- [print diagram] 다이아그램을 이미지로 출력하는 기능 추가   
- [diagram color] 다이아그램의 색상을 변경 기능 추가 
- fp파일에 정보파일 추가    
- [TaskConverter] 하위 버전 호환을 위한 Task Converter 추가
- [BARecorder] 키보드와 마우스 이벤트를 모니터링(레코딩)하여 새로운 Task 자동생성    
- [Setting] 새로운 창으로 setting을 설정할 수 있도록 수정    
- [Setting] 오류가 발생할 경우 오류 내용을 표시하는 Error Message Mode 옵션 생성    
- [Setting] 자동 저장 여부를 지정하는 Auto Save 옵션 생성    
- [Setting] PropertyForm 사용 여부를 지정하는 옵션 생성    
- [Setting] ScreenRecording 사용 여부를 지정하는 옵션 생성    
- 가독성이 향상된 다이어그램 프로퍼티 창 새로 생성    
- [Web Picker] shift + tab을 이용하여 브라우저 탭과 창을 이동할 수 있다.    
- [Web Picker] 크롬브라우저의 경우 기존에 떠있는 브라우저에 픽커를 생성할 수 있다. (크롬이 디버그 모드여야 한다.)    
- [Web Picker] 픽커가 생성될 수 없는 환경에서는 안내 메시지 박스를 띄우고 픽커가 생성이 가능할 페이지 이동까지 대기한다.

### *변경*   
- .Net Framework 업데이트 : 4.5 => 4.8    
- Devexpress 업데이트 : 18.1.3 => 22.2    
- 모든 창과 프로그램 기본 테마 변경    
- [Web Picker] xpath도 뽑아 올 수 있도록 기능 변경
- [Picker] 마우스의 x, y 좌표를 가져오도록 기능 변경
- StartItem 생성 방법 변경    
- [Predefine task] 태스크의 이름으로 텍스트 추가

<br/>   

## **$\textcolor{dodgerblue}{\textsf{Version 2.2.0 - Sep 30, 2022}}$**     
### *Diagram 변경사항*
- Loop : Loop의 왼쪽이나, 오른쪽에 다른 Item을 놓고(왼쪽 상단을 잡고 Drag) 움지기면 분리되거나 늘어나는 현상 패치
- Loop : LoopItem 깨지는 버그 수정
- Loop : Loop 아이템에 description 프로퍼티 추가
- Decision : prenext 오류처리
- Decision : yes만 있는 경우 connector validation 오류 수정
- Decision : decision index 1만 else로 가게 되어 있음 = > decision index 1,3 모두 else로 가도록 수정
- Activities : 액티비티에서 내부 함수가 안보이도록 수정
- Activities : 모든 액티비티에 description을 마우스 툴팁으로 나오도록 기능 추가
- Activities : 액티비티 중간에 새로운 액티비티 생성 시 커넥터를 삭제하고 다시 연결하여도 연결이 안되는 문제 수정
- connector : connection이 안되는 경우 yellow 선으로 연결 오류 명시적 표시 추가  

### *Program 변경 사항*
- 프로세스 실행 전에 파이썬을 종료하도록 수정  
- project에서 main 화면이 아닌 곳에서 종료할 경우 종료가 안되는 문제 해결  
- 로그창 우측으로 띄운 후 프로젝트 종료 안되는 버그 수정
- 동일 경로의 문서가 중복으로 열리지 않도록 수정
- 탭 변경 시 code창 내용이 사라지지 않도록 수정
- project를 켰을 경우 간헐적으로 종료가 안되는 경우 수정
- web picker가 iframe이 있을 경우 꺼지는 문제 수정
- 변수창에서 변수 생성 시 키값 자동으로 할당하도록 수정
- 프로젝트로 열려있을 경우 프로젝트도 다른 이름으로 저장되도록 수정
- BA-studio가 열려있을 경우 fpp, fp 또는 스튜디오 아이콘을 더블 클릭하면 최상위 그리고 활성화 되도록 수정
- 최근 사용 항목 추가 (최근 연 파일 10개를 보여주는 기능 추가)
- pathfinder // 윈도우 경로를 입력하면 그 곳을 표시해주는 기능 추가

### *Toolbox 변경 사항*
- 툴박스 안에 액티비티 이름에 마우스를 호버링 할 경우 해당 액티비티의 설명이 툴팁으로 나오도록 기능 추가
- 가장 최근 사용한 10개의 액티비티를 담는 History 그룹 생성 
- 기본 그룹을 관리할 수 있는 기본 그룹 관리 기능 추가
- 커스텀 그룹을 생성할 수 있는 기능 추가
- 전체 열기 또는 전체 닫기 기능 추가
- 그룹 캡션을 더블 클릭하여 그룹을 열거나 닫거나 할 수 있도록 수정

### *UI 변경 사항*
- 스튜디오와 엔진의 디테일 버전까지 표시되도록 수정
- UI 정렬이 맞도록 수정
- 가운데 정렬을 표시하는 아이콘을 제대로 보이도록 수정
- 화면 배율에 상관없이 UI가 깨지지 않도록 수정

<br>
<br>

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.6 - Jan 04, 2022}}$**  
### *Diagram*
- Decision  : no 선 연결이 안되어있으면 error 발생이 아닌 무한루프에 빠지는 버그 수정
- Decision : if문 생성 후 "yes"문만 생성 후 connector validation 사용 시 에러 발생 수정
- Loop : EndFor부분 Connector 연결이 안되는 오류 수정  
- Loop : 빈 리스트 루프 시 1회 실행되던 현상 수정
- Loop : 사이즈 늘린후 줄어들게 가능하기
- 드래그시 자동정렬 그랩 변경 범위 적게 ( Guide Shape 생성)
- 액티비티의 간격을 6칸에서 4칸으로 수정   
  
### *Program*
<li> print Debug : WriteDebug 시 OutofMemoryException 처리 - StringBuilder 리스트</li>
          <li>print Debug : debug 출력시 텍스트 박스 용량 초과시 텍스트 파일에 저장</li>
          <li>print Debug : 실행 파일 이름 및 Task 이름 정상출력 되도록 수정 ( 파일을 한번 오픈해서 저장해야 파일 이름이 저장되고 출력됨)</li>
          <li>print Debug : Log Print Option 추가 : full, normal, simple, none</li>
          <li>Web / Selector  : 다이얼로그 탭 입력 시, 위치 이동 추가 - 상하이동 가능</li>
          <li>액티비티 항목 사전순 정렬 기능 추가 ( 그룹에서 우클릭)</li>
          <li>동일 타스크를 오픈할 경우 동일 파일이 여러 창으로 열리는 현상 : 동일 경로 문서는 열리지 않게 수정</li>  
          
<br>
<br>

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.5 - Jun 16, 2021}}$**  
*v2.1.5 BA-Studio는 변경사항 없이, 엔진과 BA-Assit가 변경되었습니다.*

<br>
<br>

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.4 - May 14, 2021}}$**  
### *Program*
<li> Find : like 연산자 추가</li>

<br>
<br>   

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.3 - Jun 16, 2021}}$**  
### *Diagram*   
<li>Connector Validator 추가 - Document 빈화면에서 우클릭 후 Connector Validator 클릭 => 연결되지 않을 경우 붉은 점선으로 표시됨</li>
          <li>Start와 연결된 Item을 변경할 경우 비정상 실행되는 오류 패치 </li>   
          
### *Program*   
<li>신규파일 생성시 파일명 Validation - 공백 및 특수문자 체크</li>
          <li>Studio 비정상 종료시 열린문서 자동 Save 추가 - no title Document 는 저장되지 않음</li>
          <li>Document를 float 했을 경우 오류 패치</li>
          <li>다수의 브라우저가 있을때 Picker가 타겟으로 설정된 주소로 실행되지 않았던 오류 패치</li> 
<br>
<br>   

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.2 - Jan 14, 2021}}$**   
### *Program*   
<li>Toolbox에 Activity 즐겨찾기 기능 추가</li>
          <li>이미지 캡쳐모듈 추가</li>
          
<br>
<br>   

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.1 - Nov 5, 2020}}$**   
*v2.1.1 BA-Studio는 변경사항 없이, 엔진만 변경되었습니다.*   

<br>
<br>    

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.0 - Sep 25, 2020}}$**   
### *Diagram*    
<li>Diagram Item 생성위치 자동조정 로직 개선 </li>    

### *Program*    
<li>Project Tree Width 버그픽스</li>
          <li>Toolbox Activity 아이콘 Height 조정 버그 픽스</li>
          <li>Empty Document 실행방지 기능 추가</li>
          <li>Project Task 를 FP 파일로 Export</li>    
          <li>Picker 버그 수정 및 기능개선</li> 
