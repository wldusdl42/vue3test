<template>
  <div style="font-family: 'hanna'">
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
              <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown" aria-expanded="false">통계 지원 관리</a>
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
    
    <div class="container" style="text-align: left; height: 950px;">

      <div style="padding-top: 50px;">
        <h2>브랜드 관리</h2>
        <p class="lead">브랜드와 브랜드의 아이템을 관리할 수 있는 페이지입니다.</p>
        <p style="margin: 0;">브랜드는 갯수 제한 없이 등록 가능합니다.</p>
        <p style="margin: 0;">등록된 브랜드를 [전시관리 > 브랜드X싸이월드] 메뉴를 통해 선물가게 메인 화면에 노출할 브랜드를 설정합니다.</p>
      </div>

      <div style="padding-top: 70px; padding-bottom: 70px;">
        <input type="radio" class="btn-check" name="options" id="option1" autocomplete="off" checked>
        <label class="btn btn-secondary" for="option1" style="width: 50%;">브랜드 관리</label>
        <input type="radio" class="btn-check" name="options" id="option2" autocomplete="off">
        <label class="btn btn-secondary" for="option2" style="width: 50%;">브랜드 이력 관리</label>
      </div>

      <div>
        <table class="table">
          <tbody>
            <tr>
              <th style="background-color: lightgray; width: 20%;" scope="row" >브랜드명</th>
              <td><input class="form-control" style="width: 100%;"></td>
              <td style="background-color: lightgray; width: 20%;" >선물가게 노출 여부</td>
              <td>
                <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault" checked>
                <label class="form-check-label" for="flexCheckDefault" style="padding-right: 10px;">
                  전체
                </label>
                <input class="form-check-input" type="checkbox" value="" id="flexCheckChecked" checked>
                <label class="form-check-label" for="flexCheckChecked" style="padding-right: 10px;">
                  노출
                </label>
                <input class="form-check-input" type="checkbox" value="" id="flexCheckChecked" checked>
                <label class="form-check-label" for="flexCheckChecked" style="padding-right: 10px;">
                  노출 안 함
                </label>
              </td>
            </tr>
            <tr>
              <th style="background-color: lightgray;"  scope="row">검색</th>
              <td colspan="3" style="width: 500px;">
                <select class="form-select" aria-label="Default select example" style="width: 20%; margin-right: 10px; display: inline;">
                  <option selected>등록자</option>
                  <option value="1">수정자</option>
                </select>
                <input class="form-control" style="width: 40%; display: inline;">
              </td>
            </tr>
          </tbody>
        </table>

        <div class="btn-group-center" role="group" aria-label="Basic radio toggle button group" style="text-align: center;">
          <input type="radio" class="btn-check" name="btnradio" id="btnradio1" autocomplete="off" checked>
          <label class="btn btn-outline-primary" for="btnradio1" style="margin-right: 10px;">검색</label>
          <input type="radio" class="btn-check" name="btnradio" id="btnradio2" autocomplete="off">
          <label class="btn btn-outline-primary" for="btnradio2">초기화</label>
        </div>
      </div>

      <div style="margin-top: 40px;">
        <table class="table table-striped-columns">
          <thead>
            <tr>
              <th scope="col">No.</th>
              <th scope="col">브랜드명</th>
              <th scope="col">로고</th>
              <th scope="col">아이템 수</th>
              <th scope="col">등록일시</th>
              <th scope="col">등록자</th>
              <th scope="col">수정일시</th>
              <th scope="col">수정자</th>
              <th scope="col">선물가게 노출 여부</th>
              <th scope="col">수정</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <th scope="row">1</th>
              <td>2</td>
              <td>3</td>
              <td>4</td>
              <td>5</td>
              <td>6</td>
              <td>7</td>
              <td>8</td>
              <td>9</td>
              <td>수정</td>
            </tr>
          </tbody>
        </table>
      </div>

      <nav aria-label="Page navigation example" style="margin-left: 37%;">
        <ul class="pagination">
          <li class="page-item">
            <a class="page-link" href="#" aria-label="Previous">
              <i class="bi bi-chevron-double-left"></i>
            </a>
          </li>
          <li class="page-item active"><a class="page-link" href="#">1</a></li>
          <li class="page-item"><a class="page-link" href="#">2</a></li>
          <li class="page-item"><a class="page-link" href="#">3</a></li>
          <li class="page-item">
            <a class="page-link" href="#" aria-label="Next">
              <i class="bi bi-chevron-double-right"></i>
            </a>
          </li>
        </ul>
      </nav>

    </div>

    <footer class="text-muted py-5">
      <div class="container">
        <p class="mb-1">Album example is &copy; Bootstrap, but please download and customize it for yourself!</p>
      </div>
    </footer>
  </div>
</template>

<style>
@font-face {
  font-family: 'hanna';
  src: url('../../assets/font/BMHANNAPro.ttf');
}
</style>

<script lang="ts">

</script>