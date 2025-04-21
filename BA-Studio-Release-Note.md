# **Release History of BA-Studio**
## **Version 2.6.1.5 - Apr 21, 2025** 
### *변경* 
 - [WEB] SendKeys 액티비티 clear옵션에 Ctrl + a -> del 기능 추가
 - 라이브러리, 서브태스크 액티비티를 끌어다 놓는 경우 output변수 value 컬럼 초기화 및 value 컬럼에서 편집 불가능하도록 수정
 - Input, Output 변수 사용 오류 수정 - output 변수가 덮어 쓰여지는 문제 수정 / input, output 변수가 제대로 값을 주고 받을 수 없는 문제 수정
 - TryExcept 액티비티 Exception에서 오류나는 경우에도 Finally 이후로 실행되는 문제 수정
 - DataFrameFilter 액티비티 복사 붙여넣기 할때 Filter 정보 복사 안되는 오류 수정
 - Code창의 함수 실행시 변수 값 할당 오류나는 문제 수정
 - Code창에서 매개변수가 없는 함수를 작성할 경우 오류 나는 문제 수정

## **Version 2.6.1.4 - Apr 11, 2025**  
### *신규*  
 - [WEB] EdgeAttach 액티비티 생성 - 디버깅 모드로 실행된 Edge 브라우저를 객체로 가져오는 액티비티
 - [WEB] ExecuteScript 액티비티 script프로퍼티에 코드 에디터 추가 - ExecuteScript 액티비티에서 자바스크립 작성을 위한 코드 에디터 추가

### *변경*  
 - 전역 변수 사용 방식 변경 - 전역 변수는 「g.변수명」 형태로 사용 (Code 창, 프로퍼티 창)
 - 셀렉터 관리 범위 변경 - 기존 프로젝트 전역 관리에서 태스크 단위 관리로 범위 축소
 - 셀렉터 편집기 결과 문자열 수정 기능 추가  - 미리보기 창에서 결과 문자열 직접 수정 가능
 - 예외처리 우선 순위 변경 - TryExcept 액티비티의 Try 블록 내에서 예외처리 우선순위 변경 ,   변경 후 우선순위: 액티비티 Exception[jump, exec, call] > TryExcept Exception > OnError 액티비티
 - OpenBrowser 액티비티에서 Chrome 브라우저 사용 시, 디버깅 모드로 실행하도록 변경 (ChromeAttach 액티비티 사용 가능)
 - 액티비티의 이름(Name) 필드에 Ctrl + K 단축키 기능 추가
 - WEB / 엘리먼트를 못찾는 경우 NoSuchElement 오류 처리
 - OnError 액티비티가 에러 없이 실행되는 경우 태스크가 종료되지 않던 문제 수정
 - WEB 셀렉터의 type 속성이 따옴표(") 처리 없이 값을 반환하던 문제 수정
 - 테이블 데이터 미리보기 시 로딩 창이 표시되지 않던 문제 수정
 - 테이블 데이터 미리보기에서 빈 값을 조회 시 무한 대기 상태가 되던 문제 수정
 - 라이브러리 태스크에서 I/O 변수를 지정하지 못하던 문제 수정
 - 중첩 TryExcept에서 Try분기 외 부분에서 에러나는 경우 그대로 종료하는 문제 수정
 - Loop 안에서 모든 변수가 초기화 되는 문제 수정 및 Input, Output 컨버팅 오류 문제 수정
 - Input,Output 창에서 password, date 타입 변수를 지정하는 경우 오류 나는 문제 수정
 - SelectorEditor에서 WEB 셀렉터 유효성 검사 누를 경우 NativeHost가 없을 경우 창이 비활성화되는 문제 수정
 - 2개 이상 중첩된 서브태스크 동작 시 Output 변수의 값이 변경이 안되는 문제 수정
 - 프로젝트 내부에서 라이브러리 중첩 라이브러리 태스크 사용시 input, output 변수를 최신화하지 못하는 문제 수정  

## **Version 2.5.0 - Mar 29, 2024**
### *신규*   
 - Custom Activity 생성 기능 추가 - 사용자 정의 액티비티를 만들고 관리할 수 있는 기능   
 - Debugging 기능 추가 - 디버깅 실행, 중단점 설정, 단계별 실행, 변수 확인 등 프로세스 디버깅 기능   
 - Engine 분리   
 - 값 반환 액티비티 및 Message Box 액티비티 고정 이름 설정(prefix)   
 - 저장 버튼을 누를 경우 하단에 저장이 완료되었다는 Alert 창 생성   
 - ItemColor - 프로퍼티창에서도 설정할 수 있도록 기능 추가   
 - Logs 창, Code창, Debug Console창 - 검색 기능 추가   
 - Select Info - Win32, WEB selector가 수집한 윈도우 객체 또는 엘리먼트 객체의 정보를 표시하는 기능 추가   
 - Settings - Engine Version 선택 기능 추가   
 - WinPicker - Name, ClassName, AutomationID, Depth, Index 등 정보 표시 추가   
 - WebPicker - MousePosition, ElementSize, frame정보, TagName, Attributes 등 정보 표시 추가   
 - 대기화면 - 프로그램을 열고 태스크를 여는 대기시간에 splashFrom 추가

### *변경*
 - Project창 > Run Task - 무조건 프로젝트가 실행되는 오류 수정
 - [Toolbox]Project에서 Predefined Process 액티비티 비활성화 처리
 - [Diagram] 시작 액티비티, 끝 액티비티가 없는 꺽여있는 연결선 또는 꺽여있는 연결선만 단독으로 복사할 경우 붙여넣을 때 발생되는 오류 수정
 - [Project] 2.3.0 이하 버전 Task를 Import 하지 못하도록 수정
 - Logs, Debug - Logging 메모리 관리 - 메모리 중첩 방지(메모리 관리 효율화)
 - [Property] Property 설명 추가 (Predefined Process, MultiThread 액티비티)
 - [Diagram] Start Shape에 여러개의 액티비티가 추가되는 오류 수정
 - StartPage가 실행 중일 경우 다시 프로그램을 실행 시킬때 발생 하는 오류 수정
 - [Code] Code창에 코드 작성 후 다이어그램을 추가하는 경우 작성한 Code가 사라지는 오류 수정
 - [Variables] 프로젝트를 열고 새로운 태스크 선택후 프로젝트로 전환하면 변수가 복사되는 오류 수정
 - [Variables] Global 변수의 key값을 변경한 경우 변경 전 변수와 변경 후 변수 2개가 생기는 오류 수정
 - [Task Converter To V2.3] 폴더명과 fpp 파일명일 다를 경우 프로젝트 정보가 입력이 안되는 오류 수정

## **Version 2.4.2 - Jan 16, 2024**   
### *변경*  
 - [TaskConverter] 구 버전에서 컨버팅하는 경우 정상적으로 파일이 안열리는 오류 수정
 - [Resource Variables] Resource 변수 초기화 문제 수  
 - [ScreenCapture] 원격 환경에서 selector 사용 및 capture 안되는 오류 수정  

## **Version 2.4.1 - Nov 28, 2023**   
### *신규*  
 - [Web] OpenBrowser 비밀 번호 저장 팝업 비활성화
 - [Variables] 기존 R변수를 삭제하고 Variables창에 선언한 이름 그대로 변수를 사용할 수 있게 변경
 - [Settings] MultiThread Validation 활성화/ 비활성화 옵션 추가


### *변경*  
 - [Export] Project, fp Export 기능 중 덮어쓰기 기능 보완
 - [MultiThread] 선으로 연결하는 경우 연결 기능 보완
 - [Show Predefine ] 탭이 활성화가 버그 수정
 - [MultiThread ] 스레드 동작 중 Loop, Decision 및 관련 액티비티가 기능 오류 패치
 - [MultiThread Validation] Predefine의 경로가 상대경로일 경우 발생되는 오류 수정
 - [Loop, MultiThread] 루프나 멀티스레드 액티비티만 있을 경우 발생하는 저장 오류 수정
 - [Loop, MultiThread] 루프나 멀티스레드 액티브, 디액티브 액샌 오류 수정
 - [메뉴] SimpleConnector, Pointer 선택시 발생하는 오류 수정

## **Version 2.4.0 - Sep 26, 2023** 
### *신규*
- [MultiThread] 멀티스레드 기능 추가 , 전용 액티비티  
- [MultiThread] 한 스레드내에서 공유가 가능한 스레드 변수 T 추가 ex) T["변수명"] = 값
- [Validation] 메뉴 추가 - Connector, MultiThread 유효성 검사
- [Properties] 프로퍼티 설명 창 추가
- [기타] StartPage - 메뉴얼 링크, Release Note 링크 추가

    
### *변경*
- [UI] Flow Chart창 삭제, BuiltIn 그룹 생성, Project Tree 창 왼쪽 상단 위치, Property 창 크기 확장, status bar 숨김
- [Properties window] additional 지원
- [Properties] imageview 스크롤 기능 추가
- [Diagram] Loop 액티비티 최하단으로 위치하여 안에 액티비티 클릭이 되도록 수정
- [Diagrma] 로드 이후 Loop 사이즈 조절이 불가한 문제 해결
- [Diagrma] Find 기능에서 Loop 액티비티는 못 찾는 문제 수정  
- [log]  engine Exception 발생시 log창에 출력하도록 수정
- [Taskconverter] 여러개의 Task를 동시에 컨버터 할 경우 Code, Packages, image가 중복되는 문제 해결
- [기타] 캡쳐 이미지 tmp 파일이 남는 문제 해결




## **Version 2.3.1 - Aug 07, 2023**  
### *변경*
- [Property Window] Decision 액티비티의 경우 프로퍼티 폼 더블클릭으로 안뜨도록 변경
- [Property Window] taskname, filename 설명 추가
- [Find String In Value, Find Number In Value] join 프로퍼티 반대로 적힌 부분 수
- [Variables] 테마변경으로 너무 좁아져서 높이 변경
- [Diagram] Highlighter 부분 선 연결 안되도록 변경
- [Connector] Connecter 메뉴 클릭 후 발생하는 일부 버그 수정

## **Version 2.3.0 - Jun 09, 2023**  
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

## **Version 2.2.0 - Sep 30, 2022**     
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

## **Version 2.1.6 - Jan 04, 2022**  
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

## **Version 2.1.5 - Jun 16, 2021**  
*v2.1.5 BA-Studio는 변경사항 없이, 엔진과 BA-Assit가 변경되었습니다.*

<br>
<br>

## **Version 2.1.4 - May 14, 2021**  
### *Program*
<li> Find : like 연산자 추가</li>

<br>
<br>   

## **Version 2.1.3 - Jun 16, 2021**  
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

## **Version 2.1.2 - Jan 14, 2021**   
### *Program*   
<li>Toolbox에 Activity 즐겨찾기 기능 추가</li>
          <li>이미지 캡쳐모듈 추가</li>
          
<br>
<br>   

## **Version 2.1.1 - Nov 5, 2020**   
*v2.1.1 BA-Studio는 변경사항 없이, 엔진만 변경되었습니다.*   

<br>
<br>    

## **Version 2.1.0 - Sep 25, 2020**   
### *Diagram*    
<li>Diagram Item 생성위치 자동조정 로직 개선 </li>    

### *Program*    
<li>Project Tree Width 버그픽스</li>
          <li>Toolbox Activity 아이콘 Height 조정 버그 픽스</li>
          <li>Empty Document 실행방지 기능 추가</li>
          <li>Project Task 를 FP 파일로 Export</li>    
          <li>Picker 버그 수정 및 기능개선</li> 
