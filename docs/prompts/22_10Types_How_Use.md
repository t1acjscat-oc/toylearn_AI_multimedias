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
<!-- HTML -->
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <title>영상 리뷰 & 승인 대시보드</title>
  <!-- Viewport 설정: 모바일에서도 기본 반응형 동작을 위해 필수 -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- 외부 CSS 파일로 분리해도 되고, 회의용으로는 한 파일에 두어도 무방 -->
  <link rel="stylesheet" href="styles.css" />
</head>
<!-- 초기 진입 시 다크 모드 적용을 위해 dark-mode 클래스 부여 -->
<body class="dark-mode">
  <div class="app-container">
    <!-- ================= 상단 헤더 ================= -->
    <header class="app-header">
      <div class="header-left">
        <h1>영상 리뷰 &amp; 승인 대시보드</h1>
        <p class="header-subtitle">
          기획 · 디자인 · 운영팀 실무 조율용 프로토타입
        </p>
      </div>

      <div class="header-right">
        <!-- 다크 모드 토글 버튼 -->
        <!-- 실제 모드 상태는 JS에서 body class로 제어 -->
        <button id="themeToggleBtn" class="btn btn-outline">
          🌙 다크 모드
        </button>
      </div>
    </header>

    <!-- ================= 메인 레이아웃 ================= -->
    <main>
      <!-- ====== 영상 & 댓글 & 메타 정보 레이아웃 ====== -->
      <section class="video-layout">
        <!-- 왼쪽: 영상 플레이어 + 타임스탬프 댓글 영역 -->
        <section class="video-section">
          <!-- 영상 플레이어 영역 -->
          <div class="card video-card">
            <h2 class="section-title">리뷰 대상 영상</h2>
            <video
              id="reviewVideo"
              class="video-player"
              controls
              preload="metadata"
            >
              <!-- 회의용 placeholder. 실제 서비스에서는 동적으로 src 교체 가능 -->
              <source src="sample-video.mp4" type="video/mp4" />
              브라우저가 video 태그를 지원하지 않습니다.
            </video>
          </div>

          <!-- 타임스탬프 댓글 입력 영역 -->
          <div class="card comment-input-card">
            <h3 class="section-title">타임스탬프 댓글</h3>
            <div class="comment-input-row">
              <!-- 현재 재생 위치를 표시하는 라벨 -->
              <span id="currentTimeLabel" class="timestamp-label">
                00:00
              </span>
              <!-- 댓글 입력 필드 -->
              <input
                type="text"
                id="commentInput"
                class="text-input"
                placeholder="현재 시점에 대한 피드백을 입력하세요 (예: 00:12 자막 색상 조정 필요)"
              />
              <!-- 댓글 추가 버튼 -->
              <button id="addCommentBtn" class="btn btn-primary">
                + 댓글 추가
              </button>
            </div>

            <!-- 타임스탬프 댓글 목록 테이블 -->
            <!-- 운영/디자인/기획 모두 한눈에 보기 쉽도록 밀집형 구조로 구성 -->
            <div class="table-wrapper">
              <table class="data-table" id="commentTable">
                <thead>
                  <tr>
                    <th style="width: 80px;">타임스탬프</th>
                    <th>댓글 내용</th>
                  </tr>
                </thead>
                <tbody>
                  <!-- JS에서 동적으로 tr 추가 -->
                  <!-- 예시 row를 미리 하나 넣어두면 논의 시 직관적 -->
                  <!--
                  <tr>
                    <td>00:05</td>
                    <td>인트로 로고 표시 시간 1초 정도 늘리기</td>
                  </tr>
                  -->
                </tbody>
              </table>
            </div>
            <p class="helper-text">
              ※ 타임스탬프를 클릭하면 해당 시점으로 재생 위치가 이동합니다.
            </p>
          </div>
        </section>

        <!-- 오른쪽: 영상 메타 정보 + 승인/반려 버튼 -->
        <aside class="side-panel">
          <!-- 영상 메타 정보 카드 -->
          <div class="card meta-card">
            <h3 class="section-title">영상 메타 정보</h3>
            <dl class="meta-list">
              <div class="meta-row">
                <dt>파일명</dt>
                <dd id="metaFilename">campaign_video_v3_final.mp4</dd>
              </div>
              <div class="meta-row">
                <dt>업로더</dt>
                <dd id="metaUploader">홍길동 (콘텐츠팀)</dd>
              </div>
              <div class="meta-row">
                <dt>업로드일</dt>
                <dd id="metaUploadDate">2025-11-13</dd>
              </div>
              <div class="meta-row">
                <dt>영상 길이</dt>
                <!-- JS에서 metadata 로드 후 자동 설정해도 되지만, 프로토타입에서는 임의 값 사용 -->
                <dd id="metaDuration">00:45</dd>
              </div>
            </dl>
          </div>

          <!-- 승인/반려 버튼 영역 -->
          <div class="card approval-card">
            <h3 class="section-title">승인 상태</h3>
            <p class="helper-text">
              최종 승인/반려 결과는 운영팀 데이터 테이블에 반영됩니다.
            </p>
            <div class="approval-btn-group">
              <!-- 승인 버튼 -->
              <button id="approveBtn" class="btn btn-success">
                ✅ 승인 (Approve)
              </button>
              <!-- 반려 버튼 -->
              <button id="rejectBtn" class="btn btn-danger">
                ❌ 반려 (Reject)
              </button>
            </div>
            <!-- 현재 상태 표시용 레이블 (JS에서 업데이트) -->
            <p class="status-label">
              현재 상태: <span id="currentStatusText">대기</span>
            </p>
          </div>
        </aside>
      </section>

      <!-- ====== 운영팀용 데이터 테이블 영역 ====== -->
      <section class="card ope
```

