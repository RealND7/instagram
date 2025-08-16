<!DOCTYPE html> <!-- HTML5 문서임을 선언 -->
<html lang="en"> <!-- 언어 설정: 영어 -->

<head>
  <meta charset="UTF-8" /> <!-- 문자 인코딩 UTF-8 -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0" /> <!-- 반응형 뷰포트 설정 -->
  <title>Document</title> <!-- 브라우저 탭 제목 -->
  
  <!-- 공통 스타일 + 페이지 구성별 스타일 분리 -->
  <link rel="stylesheet" href="styles/general.css" />
  <link rel="stylesheet" href="styles/header.css" />
  <link rel="stylesheet" href="styles/main.css" />
  <link rel="stylesheet" href="styles/side.css" />
</head>

<body>
  <!-- ✅ 상단 고정형 헤더 영역 (로고 + 검색창 + 버튼 아이콘 등) -->
  <header class="header">
    <nav class="header__content"> <!-- 헤더 내부 콘텐츠 정렬용 래퍼 -->
      <div class="header__buttons"> <!-- 좌측 로고 -->
        <a href="index.html" class="header__home">
          <img src="assets/icons/logo.svg" alt="logo" class="header__logo" />
        </a>
      </div>

      <div class="header__search"> <!-- 검색창 -->
        <img src="assets/icons/search.svg" alt="search" />
        <input type="text" placeholder="search..." />
      </div>

      <div class="header__buttons"> <!-- 우측 아이콘들 (홈, 쇼핑, 메신저, 프로필) -->
        <a href="#"><img src="assets/icons/home.svg" alt="" /></a>
        <a href="#"><img src="assets/icons/shop.svg" alt="" /></a>
        <a href="#"><img src="assets/icons/messenger.svg" alt="" /></a>
        <div class="profile__picture">
          <img src="assets/images/avatar.png" alt="" />
        </div>
      </div>
    </nav>
  </header>

  <!-- ✅ 메인 콘텐츠 영역 (스토리 + 포스트 + 사이드메뉴) -->
  <main class="main-container">
    <section class="content-container"> <!-- 전체 콘텐츠 영역 -->
      <div class="content">
        
        <!-- ✅ 스토리 목록 (유저 아바타 원형 목록) -->
        <div class="stories">
          <div class="stories__content">
            <!-- 반복되는 스토리 카드 -->
            <button class="story">
              <div class="story__avatar">
                <div class="story__border"> <!-- SVG 원형 테두리 -->
                  <svg width="64" height="64">
                    <circle r="31" cy="32" cx="32" />
                  </svg>
                </div>
                <div class="story__picture"> <!-- 아바타 이미지 -->
                  <img src="assets/images/avatar.png" alt="user picture" />
                </div>
              </div>
              <span class="story__user">user1</span> <!-- 사용자 이름 -->
            </button>
            <!-- 총 9개 반복됨 (user1) -->
          </div>
        </div>

        <!-- ✅ 게시물 목록 -->
        <div class="posts">
          <!-- 게시물 1개 (반복 구조) -->
          <article class="post">
            <div class="post__header">
              <div class="post__profile">
                <a class="post__avatar" href="#"><img src="assets/images/avatar.png" /></a>
                <a class="post__user" href="#">user1</a>
              </div>
              <button class="post__more-options"><img src="assets/icons/more.svg" /></button>
            </div>

            <div class="post__content">
              <div class="post__medias">
                <img class="post__media" src="assets/images/picture.jpeg" alt="post content" />
              </div>
            </div>

            <div class="post__footer">
              <div class="post__buttons">
                <!-- 좋아요 / 댓글 / 북마크 아이콘 -->
                <button><img src="assets/icons/heart.svg" /></button>
                <button><img src="assets/icons/comment.svg" /></button>
                <button class="post__button--align-right"><img src="assets/icons/bookmark.svg" /></button>
              </div>
              <div class="post__infos">
                <div class="post__likes">
                  <a class="post__likes-avatar" href="#"><img src="assets/images/avatar.png" /></a>
                  <span>Liked by <a href="#">user2</a> and <a href="#">33 others</a></span>
                </div>
                <div class="post__description">
                  <span><a href="#">user</a> description</span>
                </div>
                <span class="post__date-time">30 minutes ago</span>
              </div>
            </div>
          </article>
          <!-- 총 3개 게시물 반복 -->
        </div>
      </div>

      <!-- ✅ 사이드 메뉴 (프로필 + 추천 사용자 + 하단 링크) -->
      <div class="side-menu">
        <!-- 사용자 정보 -->
        <div class="side-menu__user-profile">
          <a class="side-menu__user-avatar" href="#"><img src="assets/images/avatar.png" /></a>
          <div class="side-menu__user-info">
            <a href="#">user1</a>
            <span>nickname</span>
          </div>
          <button class="side-menu__user-button">Switch</button>
        </div>

        <!-- 추천 사용자 목록 -->
        <div class="side-menu__suggestions-section">
          <div class="side-menu__suggestions-header">
            <h2>Suggestions for you</h2>
            <button>See All</button>
          </div>
          <div class="side-menu__suggestions-content">
            <div class="side-menu__suggestion">
              <a class="side-menu__suggestion-avatar" href="#"><img src="assets/images/avatar.png" /></a>
              <div class="side-menu__suggestion-info">
                <a href="#">user11</a>
                <span>Followed by user2, user3 and others</span>
              </div>
              <button class="side-menu__suggestion-button">Follow</button>
            </div>
            <!-- 2개 추천 카드 반복 -->
          </div>
        </div>

        <!-- 푸터 링크 -->
        <div class="side-menu__footer">
          <div class="side-menu__footer-links">
            <ul class="side-menu__footer-list">
              <li><a>About</a></li>
              <li><a>Help</a></li>
              <li><a>Press</a></li>
              <li><a>API</a></li>
            </ul>
          </div>
          <span>&copy; 2023 instagram from facebook</span>
        </div>
      </div>
    </section>
  </main>
</body>
</html>
