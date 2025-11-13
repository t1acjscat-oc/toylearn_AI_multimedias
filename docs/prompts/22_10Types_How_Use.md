## 프롬프트 유형과 선택 이유

① ‘상세 설명 및 예시 기반(Instruction + Example)’ 유형

선택 이유:

- AI에게 정확한 HTML/CSS/JS 구조, UI 구성, 인터랙션 요소 등을 명확히 지정해야 함

- 상세하고 누락 없는 기능 요구사항 전달 필요

- 결과물이 “바로 실행 가능한 코드”이므로 모호성을 제거하는 구조화된 지시가 필수

- 또한 개발자가 회의 중 실시간 수정 가능하도록 “명확한 계층 구조로 출력”이 요구됨

② ‘구조화된 출력 요구(Structured Output)’ 유형

선택 이유:

- 단순 코드 한 덩어리가 아니라 UI 섹션별(헤더/플레이어/댓글/테이블/버튼)로 명확히 구분된 출력 필요

- HTML / CSS / JS를 각 섹션별로 분리하여 추후 기능 추가·수정이 용이해야 함

- 코드 재사용성과 유지보수를 위해 구조화된 형태가 적합

## 작성 위해 추가 필요 요건

① 기술 스택 구체화 (이유: 코드 일관성 확보)

- vanilla HTML/CSS/JS 사용

- 외부 프레임워크 사용 여부 명시 (예: 사용하지 않음)

② 웹 구성 요소의 필수 스펙 정의 (이유: 오해 방지·정확한 구현)

- 영상 플레이어

- 타임스탬프 댓글 기능

- 승인/반려 버튼

- 다크 모드 UI

- 데이터 테이블(리뷰 상태 / 업로더 등)

③ 출력 포맷 명확화 (이유: 실사용을 위해 파일 단위로 나누어야 함)

- HTML

- CSS

- JS
각각 분리해서 제공하도록 지시해야 함.

④ 코드 주석 필수 (이유: 회의 중 즉석 수정 용이)

- 섹션별 주석

- 동작 설명

- 수정 포인트 명시

⑤ 반응형 디자인 최소한도 포함 (이유: 회의 시 모바일 프리뷰 필요)

## 가상 문제 상황

제시해주신 상황(멀티미디어 기업, 업무용 웹페이지 요청, 의견 조율을 위한 프로토타입 작성)을 바탕으로 시나리오 챌린지를 생성했습니다.
수강생이 이 시나리오를 보고 "코딩/프로토타이핑" 관련 프롬프트 작성 능력을 훈련할 수 있도록 설계되었습니다.

🎬 시나리오 챌린지: 의견 조율을 위한 신속한 웹 프로토타입 개발

1. 가상 문제 상황
👤 페르소나: 멀티미디어 콘텐츠 기업 '네오스트림'의 프론트엔드 개발자 (3년 차)
🏙 배경:
귀사의 콘텐츠 운영팀으로부터 "사내 영상 리뷰 및 승인용 웹 대시보드" 제작을 긴급하게 요청받았습니다.
현재 기획서가 완성되지 않은 상태이며, 기획팀은 "직관적인 UI", 디자인팀은 "트렌디한 다크 모드", 운영팀은 "데이터 밀집형 테이블"을 각각 주장하며 의견이 좁혀지지 않고 있습니다.
💥 핵심 문제:
말로만 회의를 진행하다 보니 서로 상상하는 결과물이 달라 의사결정이 지연되고 있습니다.
오늘 오후 4시 회의 전까지, 실제로 작동하는 형태의 결과물이 없으면 프로젝트 착수가 무기한 연기될 위기입니다.
디자인 툴(Figma 등)로 그리기에는 시간이 부족하고, 버튼 클릭 등 인터랙션이 가능한 HTML/CSS 기반의 퍼블리싱 결과물을 보여줘야만 이해관계자들을 설득할 수 있습니다.
🎯 해결 과제:
요구사항(영상 플레이어 영역, 타임스탬프 댓글 기능, 승인/반려 버튼, 다크 모드 스타일)을 포함한 **단일 페이지 웹 프로토타입 코드(HTML, CSS, JS)**를 AI를 통해 즉시 생성하십시오.
이 코드는 회의 시간 내에 즉석에서 수정 요청을 반영할 수 있을 만큼 구조가 명확해야 합니다.

2. 훈련 초점 (힌트)
이 문제는 [코딩 및 프로토타입 생성 / 시각화] 능력을 평가
단순한 텍스트 생성이 아니라, 구체적인 UI/UX 요구사항을 구조화된 언어(코드)로 변환하는 프롬프트 엔지니어링 기술이 필요

## 문제 해결 프롬프트 

```


당신은 멀티미디어 콘텐츠 기업 ‘네오스트림’의 3년 차 프론트엔드 개발자를 돕는 **전문 UI 프로토타입 생성 AI**입니다. 오늘 오후 4시, 기획·디자인·운영팀과의 실무 조율 회의를 앞두고 있기 때문에, 실행 가능한 웹 프로토타입 코드를 빠르게 생성해야 합니다.



## 출력 목표 
- 요구된 기능을 포함한 **단일 페이지 웹 프로토타입**
- **HTML / CSS / JS 코드 블록을 각각 별도 섹션으로 분리**
- 모바일에서도 기본 동작이 가능한 최소 반응형 구조
- 모든 섹션에 “주석(comment)”을 풍부하게 작성해 회의 중 즉석 수정 가능하게 할 것
- 외부 프레임워크는 사용하지 않고 **vanilla HTML/CSS/JS** 기반으로 작성

## 반드시 포함해야 할 UI 기능 
1. **상단 헤더**
   - 페이지 제목: “영상 리뷰 & 승인 대시보드”
   - 다크 모드 토글 버튼

2. **영상 플레이어 영역**
   - HTML5 video 태그
   - 재생/일시정지 기본 컨트롤 포함
   - 오른쪽에 영상 메타 정보(파일명, 업로더, 업로드일)

3. **타임스탬프 댓글 기능**
   - 영상 재생 위치를 자동 timestamp로 가져오기
   - 댓글 입력 + 추가 버튼
   - 댓글 목록이 timestamp와 함께 아래 테이블로 표시

4. **승인/반려 버튼**
   - 승인(Approve) / 반려(Reject) 버튼
   - 클릭 시 브라우저 alert 또는 console.log로 상태 출력

5. **데이터 테이블 (운영팀 요구)**
   - 영상 상태(대기/승인/반려), 업로더, 업로드일을 표시하는 밀집형 테이블
   - 다크 모드에서 시인성 높은 컬러 대비 적용

6. **전역 다크 모드 디자인 (디자인팀 요구)**
   - 배경: #1a1a1a
   - 텍스트: #eaeaea
   - 버튼 hover 효과 포함
   - 라운드/섀도우 등 트렌디한 UI

## 출력 형식 (중요!) 
아래 구조 그대로 출력하세요:

### 1) HTML 코드
```html
<!-- HTML -->
(코드)

### 2) css코드
/* CSS */
(코드)

### 3) JavaScript 코드
// JS
(코드)

#품질 기준#

- 각 섹션 명확히 분리 및 주석 필수

- 파일 구조화가 잘 되어 있어 수정·확장이 쉬운 형태

- UI는 간단하지만 “보여줄 때 이해하기 쉬운 구성”

- 코드 오류 없이 실행 가능해야 함

- 다크모드 토글 및 댓글 기능이 실제로 동작할 것

위의 모든 조건을 충족하는 완전한 웹 프로토타입 코드를 생성하세요.
```
## 프롬프트 실행 결과

```
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>영상 리뷰 & 승인 대시보드</title>
    
    <!-- 
      CSS (Styling)
      - 모든 스타일은 이 <style> 태그 안에 정의되어 있습니다.
      - 외부 CSS 파일 없이 단일 파일로 동작합니다.
      - :root 변수를 사용하여 라이트/다크 모드 색상 관리를 용이하게 했습니다.
      - 모바일 대응을 위한 @media 쿼리가 포함되어 있습니다.
    -->
    <style>
        /* --- 0. 글로벌 및 색상 변수 정의 --- */
        :root {
            /* 라이트 모드 기본 색상 */
            --bg-color: #f4f7f6;
            --text-color: #1a1a1a;
            --primary-bg: #ffffff;
            --secondary-bg: #f9f9f9;
            --border-color: #e0e0e0;
            --header-bg: #ffffff;
            --table-header-bg: #f2f2f2;
            --btn-hover-bg: #f0f0f0;
            --shadow-color: rgba(0, 0, 0, 0.05);

            /* 버튼 색상 */
            --btn-primary-bg: #007bff;
            --btn-primary-text: #ffffff;
            --btn-approve-bg: #28a745;
            --btn-approve-text: #ffffff;
            --btn-reject-bg: #dc3545;
            --btn-reject-text: #ffffff;
        }

        /* * [다크 모드 요구사항]
         * - 배경: #1a1a1a
         * - 텍스트: #eaeaea
         * - 기타 UI 요소들도 이에 맞춰 조정
         */
        body.dark-mode {
            --bg-color: #1a1a1a;
            --text-color: #eaeaea;
            --primary-bg: #252525;
            --secondary-bg: #333333;
            --border-color: #444444;
            --header-bg: #202020;
            --table-header-bg: #3a3a3a;
            --btn-hover-bg: #555555;
            --shadow-color: rgba(0, 0, 0, 0.2);

            --btn-primary-bg: #0069d9;
            --btn-approve-bg: #218838;
            --btn-reject-bg: #c82333;
        }

        /* --- 1. 기본 스타일 (Reset & Body) --- */
        * {
            box-sizing: border-box; /* 레이아웃 계산을 쉽게 함 */
            margin: 0;
            padding: 0;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        /* --- 2. 레이아웃 (컨테이너) --- */
        .dashboard-container {
            max-width: 1400px;
            margin: 2rem auto; /* 상하좌우 여백 */
            padding: 1.5rem;
            background-color: var(--primary-bg);
            border-radius: 12px;
            box-shadow: 0 8px 24px var(--shadow-color);
            transition: background-color 0.3s ease;
        }

        main {
            display: grid;
            grid-template-columns: 1fr; /* 모바일 기본 1단 */
            gap: 2rem;
        }

        /* 데스크탑 (992px 이상) 에서는 2단 그리드 적용 */
        @media (min-width: 992px) {
            main {
                /* 왼쪽 70%, 오른쪽 30% 비율 */
                grid-template-columns: minmax(0, 2.5fr) minmax(0, 1fr);
            }
        }
        
        .main-content {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        .sidebar {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }

        /* --- 3. 개별 UI 컴포넌트 --- */
        
        /* 3-1. 상단 헤더 */
        .dashboard-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
            margin-bottom: 1.5rem;
            border-bottom: 1px solid var(--border-color);
            background-color: transparent;
        }

        .dashboard-header h1 {
            font-size: 1.75rem; /* 페이지 제목 */
            font-weight: 600;
            color: var(--text-color);
        }

        /* 다크 모드 토글 버튼 */
        .theme-toggle-btn {
            background-color: var(--secondary-bg);
            border: 1px solid var(--border-color);
            color: var(--text-color);
            padding: 0.5rem 0.75rem;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            transition: background-color 0.2s ease, box-shadow 0.2s ease;
        }

        .theme-toggle-btn:hover {
            background-color: var(--btn-hover-bg);
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        
        /* 섹션 공통 스타일 */
        .dashboard-section {
            background-color: var(--primary-bg);
            border: 1px solid var(--border-color);
            border-radius: 10px;
            overflow: hidden; /* 테이블 등 자식 요소가 모서리를 넘지 않게 */
            transition: background-color 0.3s ease, border-color 0.3s ease;
        }

        .dashboard-section h2 {
            font-size: 1.25rem;
            font-weight: 600;
            padding: 1.25rem 1.5rem;
            border-bottom: 1px solid var(--border-color);
            background-color: var(--secondary-bg);
            transition: background-color 0.3s ease, border-color 0.3s ease;
        }

        .section-content {
            padding: 1.5rem;
        }

        /* 3-2. 영상 플레이어 영역 */
        #main-video {
            width: 100%;
            border-radius: 8px;
            background-color: #000; /* 비디오 로딩 중 배경 */
        }

        /* 3-3. 영상 메타 정보 (사이드바) */
        .video-metadata ul {
            list-style: none;
        }
        .video-metadata li {
            display: flex;
            justify-content: space-between;
            padding: 0.75rem 0;
            border-bottom: 1px dashed var(--border-color);
        }
        .video-metadata li:last-child {
            border-bottom: none;
        }
        .video-metadata li strong {
            color: var(--text-color);
            font-weight: 500;
            margin-right: 1rem;
        }
        .video-metadata li span {
            color: var(--text-color);
            opacity: 0.8;
            text-align: right;
        }

        /* 3-4. 타임스탬프 댓글 기능 */
        .comment-form {
            display: flex;
            gap: 0.75rem;
            margin-bottom: 1.5rem;
        }

        .comment-form input[type="text"] {
            flex-grow: 1; /* 입력창이 가능한 한 넓게 */
            padding: 0.75rem 1rem;
            border: 1px solid var(--border-color);
            border-radius: 8px;
            background-color: var(--bg-color);
            color: var(--text-color);
            font-size: 1rem;
            transition: background-color 0.3s, border-color 0.3s;
        }
        .comment-form input[type="text"]:focus {
            outline: none;
            border-color: var(--btn-primary-bg);
            box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.2);
        }

        /* 3-5. 승인/반려 버튼 */
        .action-buttons {
            display: grid;
            grid-template-columns: 1fr 1fr; /* 1:1 비율 */
            gap: 1rem;
        }

        /* 버튼 공통 스타일 */
        .btn {
            padding: 0.85rem 1rem;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: transform 0.1s ease, box-shadow 0.2s ease, background-color 0.2s ease;
        }
        .btn:hover {
            transform: translateY(-2px); /* 호버 시 살짝 위로 */
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }
        .btn:active {
            transform: translateY(0);
        }

        /* 개별 버튼 스타일 */
        .btn-primary {
            background-color: var(--btn-primary-bg);
            color: var(--btn-primary-text);
        }
        .btn-approve {
            background-color: var(--btn-approve-bg);
            color: var(--btn-approve-text);
        }
        .btn-reject {
            background-color: var(--btn-reject-bg);
            color: var(--btn-reject-text);
        }


        /* 3-6. 데이터 테이블 (댓글 & 운영 현황) */
        .data-table-wrapper {
            width: 100%;
            overflow-x: auto; /* 모바일에서 테이블 스크롤 가능 */
        }

        table.data-table {
            width: 100%;
            border-collapse: collapse; /* 테이블 셀 사이 간격 제거 */
            margin-top: 1rem;
        }

        table.data-table th,
        table.data-table td {
            padding: 0.85rem 1rem;
            text-align: left;
            border-bottom: 1px solid var(--border-color);
            vertical-align: middle;
        }

        /* 테이블 헤더 */
        table.data-table th {
            background-color: var(--table-header-bg);
            font-weight: 600;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* 테이블 바디 (댓글 목록) */
        table.data-table tbody tr:hover {
            background-color: var(--secondary-bg);
        }
        
        /* 밀집형 테이블 (운영팀 요구) */
        .dense-table th,
        .dense-table td {
            padding: 0.6rem 1rem; /* 패딩을 줄여 밀집도 높임 */
        }

        /* 상태 표시용 뱃지 */
        .status-badge {
            padding: 0.25rem 0.6rem;
            border-radius: 12px;
            font-weight: 600;
            font-size: 0.85rem;
            text-transform: capitalize;
        }
        .status-badge.pending {
            background-color: #fff8e1;
            color: #f57f17;
            border: 1px solid #fbc02d;
        }
        .status-badge.approved {
            background-color: #e8f5e9;
            color: #2e7d32;
            border: 1px solid #66bb6a;
        }
        .status-badge.rejected {
            background-color: #ffebee;
            color: #c62828;
            border: 1px solid #ef5350;
        }

        /* 다크 모드용 상태 뱃지 (시인성 확보) */
        body.dark-mode .status-badge.pending {
            background-color: #4a3c1e; color: #fdd835; border-color: #fdd835;
        }
        body.dark-mode .status-badge.approved {
            background-color: #1c3b1e; color: #81c784; border-color: #81c784;
        }
        body.dark-mode .status-badge.rejected {
            background-color: #441c1c; color: #e57373; border-color: #e57373;
        }


        /* --- 4. 모바일 반응형 --- */
        @media (max-width: 768px) {
            .dashboard-container {
                margin: 0;
                padding: 1rem;
                border-radius: 0;
                box-shadow: none;
            }

            .dashboard-header {
                flex-direction: column; /* 헤더 세로 정렬 */
                align-items: flex-start;
                gap: 1rem;
            }

            .dashboard-header h1 {
                font-size: 1.5rem;
            }

            main {
                gap: 1.5rem;
            }

            /* 사이드바 영역을 메인 컨텐츠 아래로 이동 (그리드 순서 변경) */
            @media (min-width: 992px) {
                .main-content { grid-column: 1 / 2; }
                .sidebar { grid-column: 2 / 3; }
            }
            /* 모바일에서는 순서대로 쌓임 */
            
            .section-content {
                padding: 1rem;
            }
            
            .dashboard-section h2 {
                padding: 1rem 1.25rem;
            }
        }

    </style>
</head>
<body>

    <!-- 
      HTML (Structure)
      - 시맨틱 태그 (<header>, <main>, <section>)를 사용하여 구조를 명확히 했습니다.
      - 회의 중 ID나 Class를 기준으로 CSS나 JS를 쉽게 수정할 수 있도록 명명했습니다.
    -->
    <div class="dashboard-container">

        <!-- 1. 상단 헤더 -->
        <header class="dashboard-header">
            <h1>영상 리뷰 & 승인 대시보드</h1>
            <!-- 다크 모드 토글 버튼 -->
            <button id="theme-toggle-btn" class="theme-toggle-btn">
                <span>다크 모드</span> 🌙
            </button>
        </header>

        <!-- 메인 컨텐츠 (그리드 레이아웃) -->
        <main>
            <!-- 메인 컨텐츠 영역 (좌측) -->
            <div class="main-content">
                
                <!-- 2. 영상 플레이어 영역 -->
                <section class="dashboard-section">
                    <!-- 섹션 헤더 -->
                    <h2>영상 플레이어</h2>
                    <!-- 섹션 컨텐츠 -->
                    <div class="section-content">
                        <!-- 
                          - w3schools의 샘플 영상을 placeholder로 사용합니다.
                          - 컨트롤(controls) 속성 포함.
                        -->
                        <video id="main-video" controls poster="https://placehold.co/1920x1080/252525/eaeaea?text=NEOSTREAM+Video">
                            <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
                            <source src="https://www.w3schools.com/html/mov_bbb.ogg" type="video/ogg">
                            브라우저가 video 태그를 지원하지 않습니다.
                        </video>
                    </div>
                </section>

                <!-- 3. 타임스탬프 댓글 기능 -->
                <section class="dashboard-section">
                    <h2>타임스탬프 리뷰</h2>
                    <div class="section-content">
                        <!-- 댓글 입력 폼 -->
                        <div class="comment-form">
                            <input type="text" id="comment-input" placeholder="현재 타임스탬프에 리뷰를 남기세요...">
                            <button id="add-comment-btn" class="btn btn-primary">댓글 추가</button>
                        </div>

                        <!-- 댓글 목록 테이블 -->
                        <div class="data-table-wrapper">
                            <table class="data-table" id="comment-table">
                                <thead>
                                    <tr>
                                        <th>Timestamp</th>
                                        <th>Comment</th>
                                        <th>삭제</th>
                                    </tr>
                                </thead>
                                <!-- JS로 댓글이 추가될 tbody -->
                                <tbody id="comment-list">
                                    <!-- 예시 댓글 (삭제 가능) -->
                                    <tr>
                                        <td>00:03</td>
                                        <td>오프닝 로고 사운드가 너무 큽니다.</td>
                                        <td><button class="btn-delete">X</button></td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                </section>
            </div>

            <!-- 사이드바 영역 (우측) -->
            <div class="sidebar">

                <!-- 4. 승인/반려 버튼 -->
                <section class="dashboard-section">
                    <h2>최종 결정</h2>
                    <div class="section-content action-buttons">
                        <button id="approve-btn" class="btn btn-approve">승인 (Approve)</button>
                        <button id="reject-btn" class="btn btn-reject">반려 (Reject)</button>
                    </div>
                </section>

                <!-- 2-1. 영상 메타 정보 (사이드바) -->
                <section class="dashboard-section">
                    <h2>영상 메타 정보</h2>
                    <div class="section-content video-metadata">
                        <ul>
                            <li><strong>파일명</strong> <span>NS_Final_v1.2.mp4</span></li>
                            <li><strong>업로더</strong> <span>기획팀_김네오</span></li>
                            <li><strong>업로드일</strong> <span>2025-11-13 09:30</span></li>
                            <li><strong>영상 길이</strong> <span>00:10</span></li>
                            <li><strong>해상도</strong> <span>1920x1080</span></li>
                        </ul>
                    </div>
                </section>
                
                <!-- 5. 데이터 테이블 (운영팀 요구) -->
                <section class="dashboard-section">
                    <h2>운영 현황 (밀집형)</h2>
                    <div class="data-table-wrapper">
                        <!-- 밀집형 스타일 적용 -->
                        <table class="data-table dense-table">
                            <thead>
                                <tr>
                                    <th>상태</th>
                                    <th>업로더</th>
                                    <th>업로드일</th>
                                </tr>
                            </thead>
                            <tbody>
                                <!-- 목업 데이터 -->
                                <tr>
                                    <td><span class="status-badge approved">승인</span></td>
                                    <td>디자인팀_이나라</td>
                                    <td>2025-11-12</td>
                                </tr>
                                <tr>
                                    <td><span class="status-badge pending">대기</span></td>
                                    <td>기획팀_김네오</td>
                                    <td>2025-11-13</td>
                                </tr>
                                <tr>
                                    <td><span class="status-badge rejected">반려</span></td>
                                    <td>운영팀_박스트림</td>
                                    <td>2025-11-11</td>
                                </tr>
                                 <tr>
                                    <td><span class="status-badge approved">승인</span></td>
                                    <td>디자인팀_최디자인</td>
                                    <td>2025-11-10</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </section>

            </div>
        </main>
    </div>

    <!-- 
      JavaScript (Functionality)
      - 모든 스크립트는 이 <script> 태그 안에 정의되어 있습니다.
      - DOMContentLoaded 이벤트를 기다려 스크립트가 안전하게 실행되도록 보장합니다.
      - 기능별로 코드가 명확하게 분리되어 있고 주석이 달려있습니다.
    -->
    <script>
        // DOM이 모두 로드된 후 스크립트 실행 (안전한 코드 실행 보장)
        document.addEventListener('DOMContentLoaded', () => {

            /* --- 1. 요소(Element) 선택 --- */
            // (회의 중 빠른 수정을 위해 주요 DOM 요소를 변수로 미리 선언)
            
            // 1-1. 헤더
            const themeToggleBtn = document.getElementById('theme-toggle-btn');
            const themeToggleBtnSpan = themeToggleBtn.querySelector('span'); // 버튼 안 텍스트

            // 1-2. 비디오 및 댓글
            const videoPlayer = document.getElementById('main-video');
            const commentInput = document.getElementById('comment-input');
            const addCommentBtn = document.getElementById('add-comment-btn');
            const commentListBody = document.getElementById('comment-list'); // 댓글 목록 tbody
            const commentTable = document.getElementById('comment-table');

            // 1-3. 승인/반려 버튼
            const approveBtn = document.getElementById('approve-btn');
            const rejectBtn = document.getElementById('reject-btn');


            /* --- 2. 다크 모드 토글 기능 (디자인팀 요구) --- */
            
            // (선택사항) 사용자의 이전 설정을 localStorage에서 확인
            const isDarkMode = localStorage.getItem('darkMode') === 'true';
            if (isDarkMode) {
                document.body.classList.add('dark-mode');
                updateThemeButton(true);
            }

            // 토글 버튼 클릭 이벤트
            themeToggleBtn.addEventListener('click', () => {
                const isDark = document.body.classList.toggle('dark-mode');
                
                // localStorage에 설정 저장
                localStorage.setItem('darkMode', isDark);
                
                // 버튼 텍스트 및 아이콘 업데이트
                updateThemeButton(isDark);
            });

            // 버튼 텍스트/아이콘 업데이트 헬퍼 함수
            function updateThemeButton(isDark) {
                if (isDark) {
                    themeToggleBtnSpan.textContent = '라이트 모드';
                    themeToggleBtn.innerHTML = themeToggleBtnSpan.outerHTML + ' ☀️';
                } else {
                    themeToggleBtnSpan.textContent = '다크 모드';
                    themeToggleBtn.innerHTML = themeToggleBtnSpan.outerHTML + ' 🌙';
                }
            }


            /* --- 3. 타임스탬프 댓글 기능 --- */
            
            // '댓글 추가' 버튼 클릭 이벤트
            addCommentBtn.addEventListener('click', addTimestampComment);
            
            // 엔터 키로도 댓글 추가 (편의 기능)
            commentInput.addEventListener('keypress', (e) => {
                if (e.key === 'Enter') {
                    addTimestampComment();
                }
            });

            // 댓글 추가 함수
            function addTimestampComment() {
                const commentText = commentInput.value.trim(); // 앞뒤 공백 제거

                // 댓글 내용이 없으면 아무것도 안 함
                if (commentText === '') {
                    alert('리뷰 내용을 입력하세요.');
                    commentInput.focus();
                    return;
                }

                // 1. 현재 비디오 시간 가져오기
                const currentTime = videoPlayer.currentTime;
                
                // 2. 시간 포맷팅 (mm:ss)
                const formattedTime = formatTime(currentTime);

                // 3. 새 테이블 행(row) 생성
                const newRow = commentListBody.insertRow(0); // 0: 맨 위에 추가
                newRow.innerHTML = `
                    <td>${formattedTime}</td>
                    <td>${escapeHTML(commentText)}</td> <!-- XSS 방지를 위한 HTML 이스케이프 -->
                    <td><button class="btn-delete">X</button></td>
                `;

                // 4. 입력창 비우기 및 포커스
                commentInput.value = '';
                // commentInput.focus(); // 연속 입력을 위해 주석 처리 (선택)
                
                console.log(`COMMENT ADDED: [${formattedTime}] ${commentText}`);
            }

            // 댓글 삭제 이벤트 (이벤트 위임 사용)
            // (테이블 자체에 이벤트 리스너를 달아, 나중에 추가된 버튼도 동작하게 함)
            commentTable.addEventListener('click', (e) => {
                // 클릭된 요소가 '.btn-delete' 클래스를 가졌는지 확인
                if (e.target.classList.contains('btn-delete')) {
                    // e.target = 버튼
                    // e.target.parentElement = <td>
                    // e.target.parentElement.parentElement = <tr> (삭제할 행)
                    const rowToDelete = e.target.closest('tr');
                    rowToDelete.remove();
                    console.log('COMMENT DELETED');
                }
            });


            /* --- 4. 승인/반려 버튼 기능 --- */
            
            // 승인 버튼 클릭
            approveBtn.addEventListener('click', () => {
                const status = '승인(APPROVED)';
                console.log(`[Action Clicked] 상태: ${status}`);
                // 회의 시연용: 브라우저 alert으로 상태 출력
                alert(`영상 상태가 [승인]으로 변경되었습니다.`);
                
                // (실무 적용 시)
                // fetch('/api/videos/123/approve', { method: 'POST' })
                //   .then(...)
            });

            // 반려 버튼 클릭
            rejectBtn.addEventListener('click', () => {
                const status = '반려(REJECTED)';
                console.log(`[Action Clicked] 상태: ${status}`);
                // 회의 시연용: 브라우저 alert으로 상태 출력
                alert(`영상 상태가 [반려]로 변경되었습니다.`);
                
                // (실무 적용 시)
                // fetch('/api/videos/123/reject', { method: 'POST' })
                //   .then(...)
            });


            /* --- 5. 유틸리티 헬퍼 함수 --- */

            // 초(seconds)를 mm:ss 형식의 문자열로 변환
            function formatTime(seconds) {
                const minutes = Math.floor(seconds / 60);
                const remainingSeconds = Math.floor(seconds % 60);

                // 10초 미만일 때 앞에 0을 붙여줌 (e.g., 03, 09)
                const formattedMinutes = String(minutes).padStart(2, '0');
                const formattedSeconds = String(remainingSeconds).padStart(2, '0');

                return `${formattedMinutes}:${formattedSeconds}`;
            }

            // XSS(Cross-Site Scripting) 방지를 위한 간단한 HTML 이스케이프
            function escapeHTML(str) {
                return str.replace(/[&<>"']/g, function(match) {
                    const escape = {
                        '&': '&amp;',
                        '<': '&lt;',
                        '>': '&gt;',
                        '"': '&quot;',
                        "'": '&#39;'
                    };
                    return escape[match];
                });
            }

            // (페이지 로드 시 초기화 로그)
            console.log('영상 리뷰 대시보드 프로토타입 초기화 완료.');

        }); // DOMContentLoaded End
    </script>

</body>
</html>
```

