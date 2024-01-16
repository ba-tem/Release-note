# **Release History of BA-Assist**   
## **Version 2.4.2 - Jan 16, 2024**   
### *신규*   
 - [MultiProcess] 동시에 여려 개의 Task를 실행할 수 있는 기능  
 - [Setting] Rollback - Backup한 Setting 파일을 복원하는 기능 추가
 - [Setting] 변경 세팅 내용 확인하도록 변경점 체크 기능 추가

### *변경* 
 - [Schedule] Export, Import - Temp 폴더 삭제
 - [Setting] Backup - Temp 폴더 삭제

## **Version 2.4.1 - Nov 28, 2023**   
### *변경*   
 - [Trigger] 트리거를 추가할 경우 새로 추가할 트리거에 기존의 트리거 값이 남아있는 오류 수정  
 - [Schedule] 스케쥴이 disable인 경우에도 캘린더에 예정일이 표기되는 오류 수정

## **Version 2.4.0 - Sep 26, 2023** 
### *신규*  
- [Setting] ScreenSaver off 기능 활성화

### *변경*
- Log 검색 필터 날짜 설정 변경 (최초는 오늘 날짜로 설정되도록 수정)
  
## **Version 2.3.1 - Aug 07, 2023**
### *변경*
- 화면 Hide 상태인 경우 작업목록(Alt+Tab)에서 보이지 않도록 처리

## **Version 2.3.0 - Jun 09, 2023** 
### *신규*    
- Dashboard : 태스크의 작동 현황을 표시하는 Dashboard 패널 추가   
- Schedule :  태스크의 스케쥴을 표시하는 Schedule 패널 추가   
- Schedule export 기능 추가   
- Setting export 기능 추가    
- [ScreenRecording] 태스크 실행시 실행화면을 녹화하는 기능 추가   
  
### *변경*   
- .Net Framework 업데이트 : 4.5 => 4.8    
- Devexpress 업데이트 : 18.1.3 => 22.2  
- 테마 및 컨트롤 디자인 변경   
- [Task list] Grid 타입의 리스트에서 Card 타입의 리스트로 변경   
- 스케줄 기능 설명 추가    
- Queue 기능 설명 추가    
  
<br/>


## **Version 2.2.0 - Sep 30, 2022**   

### *신규 기능*   
<li>에러 발생 시 ScreenShot 기능을 켜고 끌 수 있도록 옵션 추가</li>
          <li>log 창에 로그를 우클릭하면 log를 삭제할 수 있도록 기능 추가</li>
          <li>스케줄 : Last라는 달의 마지막 날을 선택할 수 있는 기능 추가</li>   
          
### *변경 사항*   
<li>어시스트의 디테일 버전과 엔진의 디테일 버전도 표시되도록 수정</li>
<li>리본 그룹 재정립, 그룹별로 UI를 수정 (기능은 동일)</li>
<li>진행 중인 작업을 중지하는 버튼 추가</li>
<li>oneline이라는 새로운 로그 모드 생성</li>   

## **Version 2.1.6 - Jan 04, 2022**   

### *신규 기능*    
<li>Log Print Option 추가 : full, normal, simple, none</li>
<li>스케줄 지정 시 queue 적용 옵션 기능 추가 : 동일 태스크가 스케줄로 연달아 중복 실행되는 경우 스케줄이 큐에 쌓이지 않는 경우 발생하므로, 옵션을 Parallel을 지정해야 함. </li>
<li>TempFolder, LogFile 정리기능이 있는 실행파일 추가 - BACleanUp.exe 를 스케줄에 등록해서 관리하면 됨</li>    

### *변경 사항*     
<li>Dashboard : 사용되는 DB를 MariaDB에서 SQLite로 변경</li>    

## **Version 2.1.5 - Jun 16, 2021**   

### *변경 사항*     
<li>Task 실행 버그 수정</li>    

## **Version 2.1.4 - May 14, 2021**   

### *신규 기능*    
<li>Update Task 기능 추가  => Task 파일 변경시 Task 삭제/추가가 아닌 Update Task 파일 변경 (동일한 파일을 업데이트 하는 경우에 적용됩니다.)</li>
<li>Open folder in file exploer  => Task 파일 위치 열기</li>    

## **Version 2.1.3 - Jun 16, 2021**   

### *신규 기능*   
<li>Log - 에러내용을 팝업창에서 상세 확인 - Message 셀 우클릭 </li>
<li>Task Watcher 및 Queue Task 기능 추가</li>
<li>오류시 스크린 캡쳐 : Assist 직접실행 or 스케줄 실행도중 오류 발생시  C:\logs\BA-ScreenShot 에 "yyyyMMddHHmmss.png" 로 자동 저장됨</li>    

### *변경 사항*   
<li>Block Keyboard & Mouse : 스케줄 실행시에도 Block 처리.</li>     

## **Version 2.1.2 - Jan 14, 2021**   

### *신규 기능*    
<li>Dashoboard 설정 및 연동 기능 추가 </li>   

### *변경 사항*   
<li>BA Player 동시실행 개선</li>    

## **Version 2.1.1 - Nov 5, 2020**   

*v2.1.1 BA-Assist는 변경사항 없이, 엔진만 변경되었습니다.*    


## **Version 2.1.0 - Sep 25, 2020**   
### *변경 사항*    
<li>Task 폴더 삭제 관련 버그 픽스</li>        
<li>UI 개선</li>
