<template>
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark" aria-label="Fifth navbar example">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Qualoat</a>
        <img src="../../assets/logo.png" width="38" height="30" class="me-3" alt="Bootstrap">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarsExample05" aria-controls="navbarsExample05" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarsExample05">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item dropdown">
              <b-link to="/"><a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">통계 지원 관리</a></b-link>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">통계 지원 관리</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">랜딩 페이지</a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">새소식 관리</a></li>
                <li><a class="dropdown-item" href="#">SW 개요 관리</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">학습 자료 관리</a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">스터디 관리</a></li>
                <li><a class="dropdown-item" href="#">유튜브 리스트 관리</a></li>
                <li><a class="dropdown-item" href="#">가이드북 업로드 편집기</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">구매 관리</a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">상품 배치 관리</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">다운로드 관리</a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">EULA 편집기</a></li>
                <li><a class="dropdown-item" href="#">Plug-in 파일 업로드 관리자</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">멤버십 관리</a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">회원 정보 조회</a></li>
                <li><a class="dropdown-item" href="#">회원 정보 / 상태 제어</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">라이센스 관리</a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">라이센스 히스토리 조회 툴</a></li>
                <li><a class="dropdown-item" href="#">라이센스 에디터</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">판매 관리</a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Charge-Back List viewer</a></li>
                <li><a class="dropdown-item" href="#">결제 완료 / 취소 내역 조회</a></li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">관리자 계정 관리</a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">관리자 계정 관리</a></li>
                <li><a class="dropdown-item" href="#">관리자 권한 관리</a></li>
              </ul>
            </li>
          </ul>
          <a class="ms-auto link-light" hreflang="ar">관리자 정보</a>
          <a class="ms-auto link-light" hreflang="ar">로그아웃</a>
        </div>
      </div>
    </nav>
</template>

<script setup lang="ts">

</script>