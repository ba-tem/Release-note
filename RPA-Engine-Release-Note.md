# **Release History of RPA-Engine**   

## **$\textcolor{dodgerblue}{\textsf{Version 2.3.0 - Jun 09, 2023}}$**   
### *신규*    
- [web] Table To List : table 태그의 값을 리스트로 가져오는 액티비티 , table 태그의 구조 그대로 2중 리스트로 반환한다. 옵션을 이용하여 추출 시작행, 끝 행을 지정하여 추출할 수 있다.   
- [PDF] getTextFromRect : PDF 파일의 특정 영역의 텍스트를 가져오는 액티비티, 특정 영역의 선택은 시작 x, y 좌표 높이, 길이로 지정합니다.   
- [Common] WaitForProcess : 특정 프로세스가 실행되기를 대기하는 액티비티 , 프로세스의 이름은 작업 관리자에서 참조   
- [OCR] TesseractOCR Image To Text : 테서렉트 OCR을 사용하여 이미지에서 텍스트를 추출하는 액티비티, 테서렉트 엔진을 따로 설치해야하며, 전처리 옵션을 선택할 수 있다.

### *변경*    
- [web] Open browser : 로딩타임아웃 시간지정 , Headless 실행 , userdata 사용 , 자동화메시지 표시 , 웹드라이버 경로 설정 (폐쇄망)   
- [web] Click, DoubleClick : 엘리먼트 타입지정(css , Xpath , ClassName , ID, TagName) , WaitClickable , aitParams   
- [web] GetAttribute , GetItem , GetText , SaveElementeImage , Scroll into element, Sendkeys , SetValue , Wait Disappear, Select : 엘리먼트 타입지정(css , Xpath , ClassName , ID, TagName), waitParams   
- [web] Select dropbox item : 엘리먼트 타입지정 (css , Xpath , ClassName , ID, TagName ) , waitParams , select index/value/text(추가됨)   
- [web] Switch Frame : 기본 프레임으로 돌아가는 SwitchDefault 프로퍼티 추가
- [web] Timesleep(property) : 각 액티비티에 기능 후 잠시 대기 기능 추가 (Default 0) , Wait 액티비티 사용을 줄이기 위해 프로퍼티 추가
- [PDF] Password(property) : 비밀번호가 있는 문서를 처리 위한 Password 확인 프로퍼티 추가
- [win32] Timesleep(property) : 각 액티비티에 기능 후 잠시 대기 기능 추가 (Default 0) , Wait 액티비티 사용을 줄이기 위해 프로퍼티 추가
- [Common] WaitForProcessWindow : 최대 대기시간 지정하는 timeout 프로퍼티 추가
- [HWP] Save As HWP : pdf 저장 옵션 추가
- [Excel] SetNumberFormatRange : 기존 format 옵션 수동입력 방식에서 Select 방식으로 변경, "G/표준", "0.00", "0.00%", "mm/dd/yyyy", "hh:mm:ss", "0.00E+00", "@" 중  선택이 가능하다.   
  
<br/>   

## **$\textcolor{dodgerblue}{\textsf{Version 2.2.0 - Sep 30, 2022}}$**     

### *신규 기능*   
<li>[web]Click Alert - 브라우저의 alert창을 클릭하는 액티비티 생성</li>
<li>[web]Switch Browser Window - 브라우저 창을 전환하는 액티비티 생성</li>
<li>[web]Switch Frame - 웹에서 frame 태그를 전환하는 액티비티 생성</li>
<li>[web]Select Drop Down - select태그의 옵션을 선택할 수 있는 액티비티 생성</li>
<li>[web]Double Click - 엘리먼트를 더블 클릭하는 액티비티 생성</li>
<li>[web]Scroll into Element - 지정된 엘리먼트까지 페이지를 스크롤하는 액티비티 생성</li>
<li>[web]FTP File Transfer - FTP를 이용하여 파일을 업로드하고 다운로드하는 액티비티 생성</li>
<li>[excel]FindCellValueByCondition2 - 지정된 조건에 맞는 데이터를 탐색하여 결과를 반환하는 액티비티 생성</li>
<li>[excel]Get Sheets As List - 워크북의 시트의 이름을 리스트로 반환하는 액티비티 생성</li>
<li>[WIN32]Screen Capture - 현재의 화면을 캡쳐하는 액티비티 생성</li>
<li>[COMMON]User Exception - 사용자가 임의의 오류를 발생시키는 액티비티 생성</li>
<li>[WORD]Get All Texts - 현재 컨트롤하는 워드의 전체 문서를 가져오도록 수정</li>
<li>[WORD]Create Word Instance - 워드의 인스턴스를 생성하는 액티비티 생성</li>
<li>[WORD]Open Word - 워드 파일을 여는 액티비티 생성</li>
<li>[WORD]Save Current Word - 현재 활성화된 워드 파일을 저장하는 액티비티 생성</li>
<li>[WORD]Save As Current Word - 현재 활성화된 워드 파일을 다른 이름으로 저장하는 액티비티 생성</li>
<li>[WORD]Close Instance - 열려 있는 워드 인스턴스를 종료하는 액티비티 생성</li>
<li>[WORD]Close Current Word - 현재 활성화된 워드 다큐먼트를 종료하는 액티비티 생성</li>
<li>[WORD]Create New Word - 새로운 워드 문서를 생성하는 액티비티 생성</li>
<li>[WORD]Set Text - 현재 커서 위치에 텍스트를 입력하는 액티비티 생성</li>
<li>[WORD]Move Cursor Position - 현재 커서의 위치를 이동시키는 액티비티 생성</li>
<li>[WORD]Set Selection - 선택영역을 지정하는 액티비티 생성</li>
<li>[WORD]Set Selection Style - 선택영역의 스타일을 지정하는 액티비티 생성</li>
<li>[WORD]Get Selection As Text - 선택영역의 텍스트를 가져오는 액티비티 생성</li>
<li>[WORD]Delete Selection Text - 선택영역의 텍스트를 지우는 액티비티 생성</li>
<li>[WORD]Collapse Selection - 선택영역을 해제하는 액티비티 생성</li>
<li>[HWP]Open HWP - 한글 파일을 여는 액티비티 생성</li>
<li>[HWP]Create HWP - 새로운 한글 파일을 만드는 액티비티 생성</li>
<li>[HWP]Save HWP - 현재 활성화된 한글 파일을 저장하는 액티비티 생성</li>
<li>[HWP]Save As HWP - 현재 활성화된 한글 파일을 다른 이름으로 저장하는 액티비티 생성</li>
<li>[HWP]Close HWP - 현재 열려있는 한글 도큐먼트를 닫는 액티비티 생성</li>
<li>[HWP]Close HWP Instance - 한글 인스턴스를 종료하는 액티비티 생성</li>
<li>[HWP]Get Specific Page As Text - 한글 파일의 특정 페이지의 텍스트를 읽어오는 액티비티 생성</li>
<li>[HWP]Set Text - 현재 커서 위치에 텍스트를 입력하는 액티비티 생성</li>
<li>[HWP]Insert Image - 현재 커서 위치에 이미지를 삽입하는 액티비티 생성</li>		  		 
<li>[HWP]Clear HWP- 현재 문서를 모두 지우고 새문서를 여는 액티비티 생성</li>
<li>[HWP]Get Cursor Position - 현재 커서의 위치를 반환하는 액티비티 생성</li>
<li>[HWP]Set Cursor Position - 커서의 위치를 특정 위치로 지정하는 액티비티 생성</li>
<li>[HWP]Copy - 지정한 선택영역을 복사하는 액티비티 생성</li>		  		
<li>[HWP]Paste - 복사한 값을 붙여넣기하는 액티비티 생성</li>
<li>[HWP]Select All - 전체 영역을 선택하는 액티비티 생성</li>
<li>[HWP]Set Seletion - 특정 영역을 selection으로 지정하는 액티비티 생성</li>
<li>[HWP]Move Cursor - 현재 커서의 위치를 기준으로 커서를 이동시키는 액티비티 생성</li>
<li>[HWP]Get Selection As Text - 선택된 영역의 텍스트를 반환하는 액티비티 생성</li>
<li>[HWP]Create Table - 현재 커서위치에 표를 만드는 액티비티 생성</li>
<li>[HWP]Set Selection Style - 선택된 영역의 스타일을 지정하는 액티비티 생성</li>
<li>[HWP]Delete Text - 현재 커서의 위치에서 옵션에 따라 텍스트를 지우는 액티비티 생성</li>
<li>[HWP]PostgreSQL Select - postgre DB를 사용하여 데이터를 select하는 액티비티 생성</li>
<li>[HWP]PostgreSQL Update- postgre DB를 사용하여 데이터를 update하는 액티비티 생성</li>    

### *변경 사항*    
<li>오류가 난 액티비티 명시적으로 debug에 표시</li>
<li>log level에 oneline 옵션 추가</li>
<li>라이브러리 버전과 디테일 버전을 추가</li>
<li>[WEB]Click	-	retry 프로퍼티를 추가하여 실패할 경우 재시도 횟수를 정할 수 있도록 수정</li>
<li>[WEB]Wait	-	retry 프로퍼티를 추가하여 실패할 경우 재시도 횟수를 정할 수 있도록 수정</li>
<li>[WEB]GetAttribute	-	retry 프로퍼티를 추가하여 실패할 경우 재시도 횟수를 정할 수 있도록 수정</li>
<li>[WEB]GetText	-	retry 프로퍼티를 추가하여 실패할 경우 재시도 횟수를 정할 수 있도록 수정</li>
<li>[WEB]SendKeys	-	retry 프로퍼티를 추가하여 실패할 경우 재시도 횟수를 정할 수 있도록 수정</li>
<li>[WEB]GetItems	-	retry 프로퍼티를 추가하여 실패할 경우 재시도 횟수를 정할 수 있도록 수정</li>
<li>[WEB]Wait Disappear	-	retry 프로퍼티를 추가하여 실패할 경우 재시도 횟수를 정할 수 있도록 수정</li>
<li>[WEB]Open Browser	-	브라우저 옵션에 EdgeIeMode 추가</li>
<li>[WEB]Open Browser	-	timeout기능 추가</li>
<li>[WEB]WEB.Default	-	기본값 Edge로 변경</li>
<li>[WEB]WEB.Default	-	가장 최근에 열린 브라우저로 WEB.Default 설정</li>
<li>[WEB]__FINALIZE__()	-	psutil모듈을 사용해서 ie를 종료하도록 수정</li>
<li>[EXCEL]Get Range As Collection	-	셀이 하나일 경우에도 하나의 셀을 온전히 가져오도록 수정</li>
<li>[EXCEL]Get Worksheet As Collection	-	셀이 하나일 경우에도 하나의 셀을 온전히 가져오도록 수정</li>
<li>[EXCEL]FilteredRows	-	float 형태의 값이 들어가 있을 경우에도 정상적으로 값을 가져오도록 수정</li>
<li>[EXCEL]RangeBorderAround	-	RGB값으로 다양한 색상으로 수정이 가능하도록 수정</li>
<li>[EXCEL]SetRangeFormat	-	RGB값으로 다양한 색상으로 수정이 가능하도록 수정</li>
<li>[WIN32]MessageBox	-	타임아웃 기능 추가, 본문 텍스트를 drag하고 paste 할 수 있도록 수정	</li>
<li>[WIN32]Convert to Grayscale	-	이미지를 못 찾으면 confidence를 10프로씩 낮춰 30프로가 될 때까지 이미지를 찾도록 수정	</li>
<li>[WIN32]Convert to Grayscale	-	threshold 값을 변경하면 정확히 임계값 처리가 되도록 수정	</li>
<li>[DATETIME]Today	-	오류가 발생하지 않고 정확히 날짜 연산이 되도록 수정	</li>     

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.6 - Jan 04, 2022}}$**     

### *신규 기능*    
<li>[win32]- MoveMouse(신규) : x, y 좌표로 마우스 커서를 이동시키는 액티비티	</li>
<li>[win32]- ScrollMouse(신규) : 마우스 커서가 위치한 위치에 스크롤을 적용하는 액티비티	</li>
<li>[win32]- Get Mouse Position(신규) : 현재 마우스의 커서의 x, y 좌표를 리스트로 감싸서 반환하는 액티비티	</li>
<li>[win32] - Get Top Window Path(신규) : 윈도우 최상단 창의 Path를 가져오는 액티비티	</li>
<li>[web]- Wait Disappear(신규) :  특정 element가 없어질 때까지 대기하는 액티비티	</li>
<li>[web]- Maximize(신규) : 웹 창을 최대화하는 액티비티	</li>
<li>[web]- Mininize(신규) : 웹 창을 최소화하는 액티비티	</li>
<li>[web] - Scroll Into Element(신규)  : 지정한 엘리먼트로 스크롤하는 신규 액티비티	</li>   

### *변경 사항*    
<li>[image]- Invert Color : 한글경로 인식 가능하도록 수정, dest_path 입력가능	</li>
<li>[image]- Convert to Greyscle :  threshold 옵션 드롭다운으로 변경, dest_path 입력가능 	</li>				
<li>[excel]- FindCellValueByCondition :  속도 개선	</li>
<li>[excel]- FindRowAsCollection :  속도 개선	</li>
<li>[excel]- Exit : Default Instance Exit 후 워크북 Open이 되도록 수정	</li>
<li>[excel]- BulkCopyRows : 파일명이 동일한 경우 에러 및 로그 발생하도록 처리	</li>
<li>[excel]- PasteSepcialRange : 붙여넣기 타입 옵션으로 추가(드롭박스 형식)	</li>
<li>[excel]- create instance : 엑셀 인스턴스  생성 시 창 최대화	</li>
<li>[excel]- FilteredRows : 필터링 이전의 인덱스 확인 불가 => row의 index값을 리스트 0번 째 요소에 추가하는 옵션 추가	</li>
<li>[excel]- RangeBorderAround : rgb값으로 색상 지정 가능하도록 옵션수정 	</li>
<li>[excel]- GetRangeAsCollection :  속도 개선	</li>
<li>[excel]- GetWorksheetAsDictionary :  beginRow 프로퍼티 추가	</li>
<li>[excel]- GetWorksheetAsCollection :  속도 개선	</li>
<li>[excel]- GetWorksheetAsCollection : password프로퍼티 추가로 password가 있는 파일 오픈할 수 있도록 수정	</li>
<li>[excel]- GetWorksheetAsDictionary : password프로퍼티 추가로 password가 있는 파일 오픈할 수 있도록 수정	</li>    
<li>[win32]Click Automation : 마우스의 움직임을 지정하는 Move 옵션 추가	</li>
<li>[win32]DoubleClick Automation : 마우스의 움직임을 지정하는 Move 옵션 추가	</li>
<li>[win32]MessageBox : Window 최상단으로 활성화되도록 수정	</li>
<li>[win32]Execute : cmd 명령어 앱실행 가능, cmd의 시작위치 지정이 가능하도록 property 추가, waiting 시 Timeout옵션 추가	</li>
<li>[win32]Maximize : 최대화할 경우 무조건 최상단으로 뜨도록 설정	</li>  
<li>[web]- WEB.Default() : default 값을 chrome으로 수정하고 가장 최근에 오픈한 브라우저를 Default()로 설정, Close Browser 액티비티를 사용하여 WEB.Default를 초기화 할 수 있음.	</li>
<li>[web]- msdgedriver.exe 최신 드라이버 변경 :  에지드라이버와 에지브라우저의 버전을 동기화 시켜야 함, 에지 사용시 브라우저 자동업데이트등의 설정은 OFF 해야 함	</li>
<li>디렉토리 구분자 잘못 바뀌는 부분 수정</li>
<li>read text : encoding 옵션을 추가하여 사용자 지정이 가능하도록 수정</li>
<li>On error : Error Count 횟수 지정 옵션 추가</li>
<li>today : 날짜 연산시 day out of range 오류 해결 및 정확한 날짜 연산을 위해 윤년인진 확인하는 함수 구현</li>    

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.5 - Jun 16, 2021}}$**     

### *신규 기능*     
<li>[file] - Compress Folder : (신규추가) 폴더를 zip 파일로 압축</li>
<li>[file] - Compress Files : (신규추가) 특정 폴더의 파일들을 zip으로 압축</li>
<li>[file] - Decompress File : (신규추가) zip파일을 압축 해제</li>
<li>[file] - Move Latest File : (신규추가)  특정 경로의 가장 최신 파일을 지정 경로로 이동</li>
<li>[PDF ] - Merge PDF : (신규추가) 두 개의 pdf 파일을 하나의 파일로 병합</li>
<li>[PDF ] - Merge PDF Files : (신규추가) 여러 개의 pdf 파일을 하나의 파일로 병합</li>
<li>- Find Strings In Value : (신규추가) 특정 값에서 문자만 찾기</li>
<li>- Find numbers In Value : (신규추가)  특정 값에서 숫자만 찾기</li>
<li>[Word] - Get Texts : (신규추가) 워드 파일의 전체 텍스트 추출</li>     

### *변경 사항*     
<li>[Email] SendMail(Outlook) : bcc 빈값일때 오류 수정</li>       
<li>[excel] FilteredRow : 2차원 리스트로 리턴되도록 수정</li>   
<li>[excel] PasteSpecialRange : 1. 시작 셀(beginCell)의 값을 지정하여 원하는 위치부터 데이터 범위를 가져올 수 있도록 수정  2. 리턴되는 데이터 타입 변경(튜플 -> 리스트)</li>   
<li>[excel] DeleteCellRange : 기존 함수명 변경(DeleteCell -> DeleteCellRange) 및 액티비티 추가</li>   
<li>[excel] OpenWorkbook : 암호 문서 열기 기능 추가(옵션 반영)</li>    
<li>OnError : Jump 예외로 빠지는 경우는 OnError Loop Count에서 제외</li>    
<li>[PDF ]- Convert to Grey : 한글 경로 정상적으로 실행되도록 수정함</li>    

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.4 - May 14, 2021}}$**      

### *신규 기능*     
<li>[PDF] Total page Count 추가</li>
<li>[PDF] To PNG 추가</li>
<li>[PDF] Read PDF Text  추가</li>
<li>[PDF] Read PDF Text as list 추가 </li>
<li>[image] Invert Color  추가</li>
<li>[image]Convert to Greyscale 추가</li>
<li>[excel] CellAddress 추가</li>    

### *변경 사항*      
<li>[excel] SetFilter  field 기본값 0 -> 1  로 변경 </li>
<li> [excel] FontSize 디폴트 값 11로 변경</li>
<li>[excel] GetWorkSheetAsCollection // Close 옵션 추가</li>
<li>[Email] SendMail -전송 그룹 동기화 시간을 조절하기 위한 beforeTime, afterTime 추가, 숨은 참조(bcc) 추가</li>
<li>[file] AppendToTextFile 액티비티 - 숫자형(int, float) 데이터 인자로 전달 시 string으로 변경하는 작업 추가</li>
<li>LogWrite : 텍스트 파일 입력 시 받는 변수의 타입을 모두 string으로 변경</li>    

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.3 - Jun 16, 2021}}$**      

### *신규 기능*     
<li>[Excel] CopyFilteredRows</li>
<li>[Excel] CellByName</li>
<li>[Excel] ClearFilter</li>
<li>[Excel] SetFilter</li>
<li>[Excel]GetActiveCell</li>
<li>BreakFor Activity 추가</li>     

### *변경 사항*       
<li>[Excel]OpenWorkbook - 엑셀 파일간 데이터 참조시, Update 팝업창 비활성화 옵션 추가</li>
<li>[Win32]Automation ClassName 활용한 Path Select방식과 이전 버전에서 사용된 방식을 동일하게 사용할 수 있도록 패치</li>     

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.2 - Jan 14, 2021}}$**      

### *신규 기능*      
<li>Dashoboard 설정 및 연동 기능 추가 </li>     

### *변경 사항*       
<li>BA Player 동시실행 개선</li>        

## **$\textcolor{dodgerblue}{\textsf{Version 2.1.0 - Sep 25, 2020}}$**      

### *신규 기능*       
<li>[Web] HTTP Request 액티비티 추가</li>      
<li>[Excel] RemoveRow 액티비티 추가</li>     

### *변경 사항*        
<li>[Excel] GetNumberOfColumns, WriteDictionary,CopyAndAppendRange, CopyAndAppendRangeIf,CopyAndPasteBottomRange 버그 수정</li>  
