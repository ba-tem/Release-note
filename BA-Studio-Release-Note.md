# **Release History of BA-Studio**  
## **Version 2.6.3.1 - Mar 26, 2026**  
### *신규*   
 - [EXCEL] GetRangeAsDataFrame : 지정한 범위를 DataFrame으로 반환하는 신규 액티비티 추가
 - [EXCEL] RemoveDuplicates : 중복 데이터를 제거하는 신규 액티비티 추가
 - [WIN32] ShowAutomation : 자동화 창 표시용 신규 액티비티 추가
 - [WIN32] HideAutomation : 자동화 창 숨김용 신규 액티비티 추가
 - [WEB] ClickText : 텍스트 클릭용 신규 액티비티 추가
 - 액티비티 및 프로퍼티 기능 확장 :  
    * EXCEL / GetCellValue, SetCellValue : 셀 위치 지정 방식인 cell 프로퍼티 추가
    * EXCEL / GetWorkSheetAsDataFrame : returnAsText(내부 데이터 텍스트 처리) 옵션 추가
    * WEB / OpenBrowser : 디버깅 포트 사용 여부 프로퍼티 추가
    * WIN32 / 컨트롤 사용하는 액티비티 : 모달 창 우회용 ClosePopups, forceEnableMain 프로퍼티 추가
    * 빌트인 액티비티를 제외한 모든 액티비티에 timesleep 속성 적용
 - 신규 실행 및 편의 기능 추가 : 
    * 스튜디오 Viewer(저장 불가) 모드 생성
    * BA-Recorder 기능 추가
    * 프로젝트, 라이브러리, 태스크 백업 기능 생성 및 Settings 옵션 추가
 -  셀렉터 및 실행 환경 기능 강화 :  
    * Selector 선택 시 LGDisplayExtension 검사 및 종료 로직 추가

### *변경*  
 - 프로퍼티 및 UI 사용성 개선 :  
    * 프로퍼티 창 개선 그룹 생성 및 디자인 변경
    * 사용자 혼선을 방지하기 위해 fileProperties와 Properties에 따라 Input/Output 버튼 캡션 및 배경색 분기 처리
    * UI에서 표시하는 메시지 박스 TopMost 처리 (셀렉터 편집기, 테이블 미리보기 창)
    * 셀렉터 편집기 정보 표시창에 스크롤 적용
 - 코드 편집기 및 편집 동작 개선 :  
    * Python 3.11 구문 지원을 추가 (match ~ case 문 지원)
    * 코드 창, 코드 팝업 창 인텔리센스 개선(DataFrame)
    * 코드 창, 코드 팝업 창 Undo/Redo 시 커서 위치 고정 및 동작 개선
    * Error List 동작 개선 (수정된 에러 삭제 및 신규 에러 추가 최신화 동작 개선)
 - 데이터 처리 및 액티비티 기능 개선 : 
    * DATA / DataFrameFilter : filter 조건에 변수 사용 가능하도록 개선
    * 셀렉터 복원 과정에서 오류 발생 시 "Control not found" 대신 실제 오류 내용 반환하도록 개선
 - 설치 및 실행 환경 개선 : 
    * 설치 파일에 C++ 재배포 패키지 설치 추가
 - Code, Flow 창 및 단축키 관련 문제 수정 :  
    * Flow 창에서 단축키로 Connector, Diagram 생성 가능하던 문제 수정
    * 라이브러리(태스크) 프로퍼티창 및 입/출력 설정 패널에서 Ctrl + K 비정상 동작 문제 수정
    * 변수명이 함수명에 포함된 문자열일 경우 오류가 발생하던 문제 수정
 - Find Item 및 탐색 동작 안정화 : 
    * 접힘 상태에서 Find Item 수행 시, 대상 아이템이 접힌 부모 내부에 있을 경우 부모를 재귀적으로 Expand하여 대상이 보이도록 수정
    * 탐색 범위가 Current Document이면서 태스크에 Predefined Process 액티비티가 있는 경우 오류나는 문제 수정
 - 변수 및 프로퍼티 처리 문제 수정 :  
    * Code 창 또는 Process 액티비티에서 변수 할당 문제 수정
    * 딕셔너리 키(G 전역변수 포함) 이름의 변수 생성 및 수정 문제 수정
    * script 속성이 표시되면 안 되는 액티비티에서 script가 표시되던 문제 수정
    * 프로퍼티 속성 설명이 없거나 보이지 않던 문제 수정
    * InPut/OutPut 변수 로드 시 resource가 없을 경우 오류 발생 문제 수정
    * 라이브러리 태스크 미리보기에서 내부 predefined Process 액티비티의 InPut/OutPut 변수창이 열리고 수정이 가능한 문제 수정
 - 복사/붙여넣기 및 편집 동작 문제 수정 :  
    * 다른 태스크 간 Activity 복사/붙여넣기 중 name 중복 체크 오류 수정
 - 데이터 처리 및 결과 반영 문제 수정 :  
    * DATA / DataFrameFilter 결과가 원복되던 문제 수정
 - 파일 및 리소스 관리 문제 수정 : 
    * 프로젝트 생성 시 프로젝트명의 대소문자를 구분하지 못해 동일 경로에 대한 중복 체크가 되지 않던 문제를 수정했습니다.
    * temp 경로 파일 누수 문제 수정
 - 멀티스레드 및 실행 흐름 문제 수정 :  
    * 멀티스레드가 동작하지 않던 문제 수정
    * 멀티스레드 유효성 검사시 오류가 나는 문제 및 검사 결과 액티비티 이동이 안되는 문제 수정
    * 루프 내부에서 오류 발생 후 예외 처리로 루프를 빠져나간 경우, 루프 탈출 처리가 정상 동작하지 않아 흐름이 깨지던 문제 수정
    * COMMON / UserException 액티비티의 enterOnError 프로퍼티가 정상적으로 동작하지 않던 문제 수정
 - UI 자동화 및 좌표 처리 문제 수정 : 
    * WIN32 / PickScreenText, ClickPickText 미리보기에서 ' 포함 시 미리보기가 동작하지 않던 문제를 수정
    * WIN32 / PickScreenText 미리보기에서 좌표가 음수여도 처리되도록 수정
    * WEB / 클릭 관련 액티비티 anchor 기준이 실제 엘리먼트와 상이하던 문제 수정
 - 디버그 BreakPoint 처리 문제 수정 :  
    * BreakPoint를 가져오지 못하는 문제 수정
    * BreakPoint를 삭제/이동이 안되는 문제 수정

## **Version 2.6.3.0 - Jan 14, 2026**  
### *신규*   
 - [BuiltIn] Group : 개별 액티비티들을 기능적 또는 의미적 기준에 따라 분류하기 위한 컨테이너 액티비티
 - [WIN32] GetRegistryValue : Windows 레지스트리 값 조회
 - [WIN32] SetRegistryValue : Windows 레지스트리 값 추가 및 수정
 - [EXCEL] CopySheetToWorkBook : Excel A 파일의 시트를 B 파일로 복사하는 신규 액티비티 추가
 - 액티비티 프로퍼티 기능 확장 : 
    * WIN32 / TypeText : selector, verify 프로퍼티 추가
    * WIN32 / TypeKeys : selector 프로퍼티 추가
    * WEB / HttpRequest : SSL 인증서 검증 사용 여부 설정용 verify 옵션 추가
    * EXCEL / GetWorksheetAsDataFrame 액티비티 path, password, writeResPassword 옵션 추가
    * 클릭 계열 액티비티에 combinationkey 프로퍼티 추가 (Ctrl, Shift 등 키 조합 지정 가능)
    * WIN32 셀렉터 사용 액티비티에 searchMode 프로퍼티 추가 (탐색 방식 지정 가능)
 - 액티비티 예외 처리 기능 확장 :
    * Activity Exception : 오류 발생 시 다음 Activity로 자동 이동하는 Next 옵션 추가
 - BuiltIn 액티비티 그룹화 기능 확장 :
    * BuiltIn 액티비티 감싸기(Wrapping) 기능 지원
    * BuiltIn 액티비티 Collapse / Expand 기능 지원
 - 코드 편집기 사용성 개선
    * Code 창에서 Ctrl + [-, +, 0] 단축키를 통한 Zoom In / Out / Reset 기능 추가
 - 셀렉터 및 UI 편의 기능 강화
    * SelectorEditor : 노드 목록 간소화 기능 추가

### *변경*  
 - 비정형 텍스트 및 데이터 추출 안정성 개선 :
   * PickScreenText : Top, Left 기준 오름차순 정렬 적용
   * PickScreenText, PickTableData 미리보기 : '/' 문자가 '\/'로 표시되던 문제 개선
   * ClickPickText : 텍스트 매칭 로직 개선 (와일드카드 사용 여부에 따른 처리 분리)
   * 콤보박스 컨트롤, 라벨 컨트롤 텍스트 읽기 기능 개선
   * 그리드 및 화면 캡처 처리 개선
 - 변수(Variables) 및 스코프 처리 개선 :  
   * 스코프가 다른 경우 동일 변수명 사용 가능하도록 개선
   * DataFrame 타입 변수 생성 시 value 영역에 key 값 노출되던 문제 수정
   * 입출력 변수 Date 타입 변수의 날짜 형식 처리 개선
 - 라이브러리 Task 미리보기 사용성 개선
   * Properties / Variables 창: Disabled → ReadOnly 변경 (복사 가능)
   * Exception 및 버튼 기능 비활성화 처리
 - Find Item 기능 안정화
    * 저장되지 않은 항목이 검색 대상에 포함되던 문제 수정
    * 중복 검색 결과 제거
    * 결과 바로가기 - 인덱스 증가에 따른 좌표 누적 오차 문제 해결
 - 코드 편집기 동작 개선
    * Ctrl+K로 변수 등록 시 작성 중 코드 초기화되던 문제 수정(기존 코드 유지 + 변수 코드 정상 반영)
 - 기타 UI 및 동작 개선
    * Default Activity Settings : Tool Box 검색 결과가 설정 화면에 영향을 주던 오류 수정
    * Default Activity Settings : 전체 항목 선택 시 Select All 체크 표시 오류 수정
    * White 스킨에서 비활성화 Activity 구분 어려운 문제 개선
    * 비활성화 상태 시 시각적 구분 강화
    * 액티비티 로드 성능 최적화 진행
    * Undo/Redo: Flow/Code/Variables 화면 실행·실행취소 스택 단일화(일관성 개선)
 - 저장 및 로드 로직 전반 개선
    * 프로젝트 / 태스크 / 라이브러리 / 변수 저장 로직 최적화
    * 포커스된 입력창 변경사항 저장 누락 문제 수정
    * 전체 저장 시 변수 저장 오류 수정
    * 저장 실패 시 재시도 로직 및 로컬 로그 파일 작성 기능 추가
 - 디버깅 및 실행 흐름 안정화
    * 브레이크포인트 추가 시 발생하던 오류 수정
    * 반복 조건 종료 후 루프 내부 및 비활성 Activity에서 중단점 동작 문제 수정
    * "여기서부터 실행" 디버깅 기능 미동작 문제 수정
 - 로그 출력 개선
    * 로그 레벨별 출력 형식 개선
    * 인덱스, 프로퍼티 출력 추가
    * 불필요한 로그 제거
 - 셀렉터 시스템 전면 개선
    * WIN 셀렉터 하이라이트 무한 표시 방식으로 변경 (ESC로 종료, WEB은 기존 3초 표시 방식 유지)
    * WIN, WEB 셀렉터 선택 중 ESC 키로 선택 취소 가능
    * 선택 완료 후 노드에 의미 없는 값이 들어가던 문제 수정
    * 셀렉터 정보에 개행 포함 시 엔진 오류 발생 문제 수정
    * WIN32에서 Control로 모든 타입의 컨트롤 대체 가능하도록 확장
 - 크롬, 엣지 확장 프로그램 버전 업데이트 (0.0.6)
 - 열린 Task가 없는 경우 Properties, Variables 수정 가능하던 문제 수정
 - 프로퍼티 입력 중 저장/실행 시 값이 반영되지 않던 문제 수정
 - Win32 셀렉터 관련 액티비티 timeout 설정값이 무시되던 문제 수정
 - Variables 패널 Date 타입 변수 value가 비어있을 경우 발생하던 오류 수정
 - 디버깅 콘솔 및 셀렉터에서 g 변수 사용 불가 문제 수정
 - Chrome, Edge 확장 프로그램 메시지 수신 로직 개선
 - FPX Import 시 빈 Resource 폴더가 포함이 안되던 문제 수정
 - [BuiltIn] TryExcept : Title 수정 시 Script 내용까지 변경되던 문제 수정
 - [BuiltIn] MultiThread : break_on_error 옵션 미동작 문제 수정
 - 액티비티 복사/붙여넣기 시 그룹 의존성 자동 입력 처리
 - Tag: NoVar을 사용하여 Code창에서 입출력 변수를 선언/사용한 경우 출력 변수를 제대로 전달하지 못하던 문제 수정
 - File Properties에 Description에 변수 생성 기능(Ctrl+K) 사용 가능한 문제 수정
   
## **Version 2.6.2.4 - Aug 29, 2025**  
### *신규*   
 - RPA 프로세스 상세 로그 출력 기능 추가 : CommonSettings에 config 항목을 추가하여 파이썬 내부 로그 출력 기능 제공
 - 파이썬 패키지 추가 : keyboard 패키지 추가, beautifulsoup4 패키지 추가

### *변경*  
 - WEB 셀렉터 업데이트 및 개선 :
   * RPA 프로세스가 실행한 Chrome, Edge 브라우저에서 WEB 셀렉터 사용 가능 (userData -> None 사용 시)
   * WEB 선택 영역 이미지 캡처 기능 개선 (보다 정확한 위치 캡처)
   * 엔진 실행 결과와 미리보기 결과가 동일하도록 동기화
   * css-selector 기반으로 필요한 노드만 선택하도록 개선
   * 브라우저 탭 메시징 유효성 검사 추가로 확장 프로그램이 강제 종료되지 않도록 개선
   * 설정 화면의 Add On 탭에 버전 정보 표시 및 디자인 개선  
 - 프로젝트 매니저 개편
   * 프로젝트 업로드/다운로드 기능 분리
   * 업로드 시 신규 프로젝트는 등록, 기존 프로젝트는 업데이트 되도록 개선
   * 다운로드 시 기존 프로젝트는 정상적으로 종료한 후 덮어쓰기되도록 개선
 - 액티비티 개선
   * FILE / CreateDirectory: createAllDir 속성 추가로 전체 경로 내 모든 폴더 생성 가능
   * SERVER / 필수 입력값 누락 시 명확한 오류 메시지 출력
   * SERVER / GetQueueMessage: QueueName 누락 시 오류 발생하도록 개선
 - 프로젝트 저장 기능 개선
   * 프로젝트 생성 및 다른 이름으로 저장 시 마지막 저장 위치를 자동으로 기억하도록 개선
 - 셀렉터: 파이썬 엔진이 없는 경우 오류 발생 문제 수정
 - 파일 저장: 라이브러리 종료 후 신규 태스크 파일 저장이 되지 않던 문제 수정
 - 프로젝트 업로드: 최신 버전이 9이상 안올라가는 문제 수정
 - 액티비티 복사/붙여넣기: 특정 조건에서 복사된 액티비티 이름 중복 문제 수정
 - 변수 사용: 변수가 없을 경우 변수명이 그대로 출력되던 문제 수정
 - 입출력 변수: 하위 버전과 호환성 문제로 자동 변경 실패 문제 수정
 - 입출력 변수: 입력 변수와 출력 변수 이름이 동일할 경우 유효성 검사 누락 문제 수정
 - 라이브러리: 모든 태스크를 닫고 신규 태스크 생성 시 시작 버튼 비활성화 문제 수정
 - VDI 환경 캡쳐: 물리 모니터가 없는 환경에서 이미지 캡처 기능이 작동하지 않던 문제 수정
 - [WIN32] 클릭 액티비티: 컨트롤 높이 또는 너비가 0일 경우 ValueError 발생하도록 수정
 - [COMMON] KillProcess: 설정한 이름이 포함된 모든 프로세스가 종료되는 문제 수정
 - [EXCEL] Attach: 새로 연 엑셀 파일이 EXCEL.Default()로 참조되지 않는 문제 수정
 - [WIN32] TypeText: clear 속성이 byClipboard가 True일 경우에만 동작하도록 수정, 글자 간 interval 추가로 안정성 개선  

## **Version 2.6.2.2 - Jul 16, 2025**  
### *신규*   
 - [AI] ReadCaptcha 액티비티 생성 - 이미지 캡챠 결과를 반환하는 액티비티, 정부24 및 대법원의 딥러닝 모델이 탑재
 - 서버 실시간 로그 기능 : 프로젝트/태스크 시작과 종료, Log 액티비티 로그, 에러 로그 등을 서버에 실시간으로 전송 기능 추가
 - 공통 함수 파일 추가 : UM_*.pyc 파일이 엔진에 추가되어, 코드 창에서 공통 함수를 직접 호출할 수 있는 기능 추가  

### *변경*  
 - 예외 처리 범위 확대 : 서브 태스크, 라이브러리 태스크 액티비티에도 Exception(Jump, Exec, Call) 처리가 가능하도록 수정.
 - 속성(Properties) 창 UI 변경 : Exception 탭이 항상 열려 있도록 기본 설정 변경.
 - 라이브러리/프로젝트 매니저 동작 개선 : 라이브러리 및 프로젝트 업로드/다운로드 시 프로젝트 저장 이후 작업이 수행되도록 변경.
 - [Excel] FilteredRows 액티비티 속도 개선
 - 공통 설정 파일에 대해 모든 사용자에게 모든 권한을 부여하도록 변경.
 - 셀렉터 캡처 문제 수정 : 셀렉터 객체를 찾을 때, 서브 모니터에서 이미지 캡처가 되지 않던 문제가 수정.
 - [WEB] SaveElementImage 액티비티 오류 수정 : frame, iframe이 포함된 경우 잘못된 이미지를 저장하던 문제 수정.
 - 스크린 캡처 기능 오류 수정 : 캡처 위치가 다르게 찍히는 문제 및 다중 모니터 환경에서 스크린 번호를 찾지 못하는 문제 수정.
 - [AI] ChatWithChatGPT 액티비티 모델명 예외 처리 제거

## **Version 2.6.2.1 - Jul 08, 2025**  
### *신규*   
 - [PDF] ImagesToPdf  액티비티 생성 - 이미지 파일들을 하나의 PDF로 변환하는 액티비티

### *변경*  
 - [WIN32] 셀렉터 timeout 로직 변경 : 셀렉터 탐색 시, 최소 한 번은 시도한 후 timeout 조건을 검사하도록 수정
 - [WIN32] 셀렉터 객체를 찾을 때 timeout 설정이 무시되던 문제를 수정

## **Version 2.6.2.0 - Jul 04, 2025**  
### *신규*   
 - [WIN32] GetAttributeAutomation 액티비티 생성 - 윈도우 객체의 속성 값을 반환하는 액티비티
 - [COMMON] End 액티비티 추가 - 옵션에 따라 현재 태스크 또는 전체 프로세스를 정상 종료하는 액티비티  
 - 액티비티 더블 클릭 액션 추가 : Selector가 있는 액티비티 → 셀렉터 편집기, Script가 있는 액티비티 → 코드 편집기, "태스크 보기"가 있는 액티비티 → 태스크 보기       

### *변경*  
 - [WIN32] 셀렉터 고도화 : WIN32 셀렉터 처리 속도 개선, WIN32 셀렉터 선택 시 정확한 index 반환 기능 개선, 메뉴 스트립 등 포커스가 필요한 객체 선택 시 Thread Wait을 추가하여 선택 안정성 향상
 - [EXCEL] WriteDataFrame 속도 개선
 - 액티비티 검색 로직 개선 : Toolbox에서 'If' 검색 시 'Decision' 액티비티도 함께 검색되도록 키워드 맵핑 강화, Find Item의 Location 기본값을 Current Document에서 Current Project로 변경
 - Export 파일 압축률 향상 : fpx, fpl 등 내보내기 파일의 압축률을 높여 파일 용량 축소
 - 액티비티 활성화/비활성화 개선 : 흐름 제어 액티비티 내부의 액티비티를 활성화할 때, 부모 흐름 제어 액티비티가 비활성화 상태인 경우 부모까지 재귀적으로 활성화
 - 프로퍼티 값에 '문자열' + 전역 변수 + '문자열' 조합 시 오류 발생 문제 수정
 - 프로젝트 업로드 서버의 연결 URL 수정
 - 서브 태스크 또는 라이브러리 태스크 비활성화 한 경우에도 input/output 변수가 초기화되는 문제 수정
 - 흐름 제어 액티비티 비활성화 시 'NoneType' object has no attribute 'keys' 오류 수정
 - 라이브러리 및 프로젝트 업로드/다운로드 버튼 중복 클릭 시 중복 처리되는 문제 수정
 - 디버깅 중 키 오류 발생 문제 수정
 - 디버깅 중 변수에 ", ' 혼용 시 변수 미출력 문제 수정
 - 개행이 허용되지 않아야 하는 프로퍼티에서 개행이 가능했던 문제 수정 (총 23개 액티비티)
 - [WIN32] ControlExists의 timeout이 정상 동작하지 않는 문제 수정
 - [WIN32] 셀렉터에서 데드락 발생으로 프로그램이 멈추는 문제 수정
 - [WIN32] 셀렉터의 파이썬 엔진 오류 발생 시 무한 대기 상태가 되는 문제 수정
   
## **Version 2.6.1.9 - Jun 13, 2025**  
### *변경*  
 - SetAtiveAutomation 액티비티 최상단 표시 기능 추가 : 셀렉터로 선택된 요소가 있는 창을 최상단에 표시하는 기능 추가
 - 중첩된 TryExcept 내부에서 외부로 점프할 때 바깥 TryExcept가 정상 동작하지 않던 문제 수정
 - Ctrl 키를 누른 상태에서 액티비티를 드래그할 때 선 연결이 끊기던 문제 : Ctrl 키를 누른 상태에서 액티비티를 드래그 방지.  

## **Version 2.6.1.7 - May 30, 2025**  
### *신규*   
 - [WIN32] MSAA 방식 컨트롤 추출 기능 추가 (ba_msaa 모듈 추가) : UIA 방식으로 컨트롤을 추출할 수 없는 경우, MSAA 패턴을 사용하여 컨트롤을 추출할 수 있도록 기능 추가
 - 액티비티 단축키 기능 추가 - 액티비티 활성화/비활성화 단축키: Ctrl + D, 액티비티 중단점 설정/해제 단축키: Ctrl + G
 - Project Manager 기능 추가 : 현재 열려 있는 프로젝트를 서버에 업로드, 서버에 업로드된 프로젝트를 현재 프로젝트로 업데이트,서버에 있는 프로젝트 다운로드      

### *변경*  
 - Toolbox 검색 기능 개선 : 한글 입력 방지, 검색어에 해당하는 모든 액티비티 출력
 - 목록형 데이터 추출 로직 개선 : WIN32: GridDataControl의 데이터를 테이블로 추출 가능, WEB: 중첩 테이블 및 중첩 리스트 데이터도 추출 가능, ※ 중첩 테이블 및 리스트는 테이블 미리보기는 지원되지 않으며, 액티비티 리턴은 정상 출력됨
 - Undo/Redo 기능 개선 : 액티비티의 활성화/비활성화 작업도 Undo/Redo에 포함되도록 수정
 - 셀렉터 및 셀렉터 편집기 고도화 : WIN32 셀렉터: distance 속성 추가로 검색 속도 개선, 셀렉터 유효성 검사 시간 3초로 변경, 셀렉터 이름 유효성 검사 로직 강화 (한글, 영문, 숫자, 언더바만 허용), 와일드카드(*) 여러 개 사용 가능하도록 수정, 셀렉터 선택 버튼은 해당 액티비티가 셀렉터 선택을 지원할 경우에만 표시, 동일한 요소가 여러 개인 경우, index 자동 탐색 후 반환, Ctrl + 4 단축키로 셀렉터 모드 변경 가능  
 - 라이브러리 변수 체계 변경 : 전역 변수 기능 삭제, 라이브러리 서브태스크의 output 변수를 수정할 수 있도록 변경  
 - [WEB] OpenBrowser 액티비티 개선 : userData 프로퍼티에서 Default 지정 시, 브라우저의 기본 프로필 사용, Chrome에서 http 프로토콜 사용 가능, Chrome, Edge 모두 디버깅 모드로 실행되도록 변경
 - [WEB] ElementExists 액티비티 리턴값 변경 : 항상 True 또는 False만 반환하도록 수정
 - [BuiltIn] Process 액티비티 개선 :  if, for, while 등 사용자 코드 사용 가능
 - [BuiltIn] Foreach 액티비티 개선 :  iterable한 객체 사용 가능하도록 수정
 - 프로젝트 트리, 라이브러리 트리 UI 개선 : 프로젝트, 라이브러리 폴더 드래그 앤 드랍 방지 추가, 라이브러리 다운로드 관리 트리에서 라이브러리 태스크 위치 이동 방지 추가
 - Worker에서 실행 파일 경로를 읽어오지 못하던 문제 수정 (엔진 수정)
 - WEB 셀렉터가 간헐적으로 종료되지 않는 문제 수정
 - WEB 셀렉터에서 빈 값으로 유효성 검사 시 네이티브 호스트가 종료되는 문제 수정
 - 브라우저가 종료돼도 WEB 셀렉터 네이티브 호스트가 종료되지 않는 문제 수정
 - 테이블 미리보기에서 행의 길이가 다를 경우 오류 발생 문제 수정
 - 액티비티 찾기 기능(Find Item)이 특정 스코프에서 오류 발생하던 문제 수정
 - 라이브러리 input 변수가 빈값일 경우 기본값을 사용하지 못하던 문제 수정
 - 라이브러리 input/output 변수의 타입이 password일 경우 값을 불러오지 못하던 문제 수정
 - Code 창에서 전역 변수명과 같은 딕셔너리 키를 사용할 경우 오류 발생 문제 수정
 - 태스크 파일 열기 시 오류 발생 시 빈 태스크로 저장되던 문제 수정
 - [DATA] DataFrameFilter 액티비티에서 name 변경 시 filter 정보가 사라지는 문제 수정
 - [WEB] ExecuteScript 액티비티에서 전역변수 및 멀티라인 변수 사용이 불가능하던 문제 수정
 - [File] DecompressFile 액티비티에서 압축파일 내 한글 파일명 인코딩 오류 문제 수정
 - 프로젝트트리, 라이브러리트리에서 라이브러리폴더 또는 프로젝트폴더를 Flow창에 Drag and Drop했을 때 오류나는 문제 수정  

## **Version 2.6.1.6 - Apr 24, 2025**  
### *신규*  
 - [WEB] ElementExists 액티비티 생성 - 웹 엘리먼트의 존재 여부를 확인하는 액티비티
 - [WIN3] ImageExists 액티비티 생성 - 화면 내 이미지 존재 여부를 확인하는 액티비티
 - 서버 연결 없이 라이브러리 임포트 기능 추가 : 메뉴바 → Library → Import Library에서 .fpl 파일 불러오기 가능
 - 메뉴바의 View 메뉴에 Library 항목 추가 및 라이브러리 미리보기 기능 제공 : 라이브러리 액티비티에서 우클릭, 라이브러리 탭에서 우클릭  

### *변경*  
 - Ctrl + S(저장 단축키)로 Variable 창의 변경 내용까지 저장되도록 개선
 - Studio 및 Assist 설치 시 IE 사용을 위한 레지스트리 등록 기능 제거 : 대신 Studio 설치 경로(\BATEM\BA-Studio\AddOn)에 레지스트리 삭제/추가용 .bat 파일 제공
 - Input/Output 설정 화면에서 '변수 선택' 목록에 Input 변수도 함께 표시되도록 변경
 - 팝업 코드 편집기에 최대화 및 최소화 버튼 추가
 - 셀렉터 편집기에서 '셀렉터 선택' 클릭 시 자동 저장 후 창 종료되도록 동작 개선
 - Process 액티비티의 script 속성에서 f""(f-string) 내부에 전역 변수를 사용할 수 없던 문제 해결
 - Process 액티비티의 script 속성에서 들여쓰기(Indentation) 오류 발생 문제 수정
 - Process 액티비티 스크립트 작성 시 블록 헤더에 메소드가 있을 경우 정상 작동하지 않던 문제 해결
 - 셀렉터 편집기에서 WEB 셀렉터의 type 속성을 체크했을 때 미리보기에서 따옴표 없이 값이 출력되던 문제 수정  

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
