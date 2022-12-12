<template>
  <TheHeader></TheHeader>
  <TheNavigator></TheNavigator>
    <div class="container" style="text-align: left; height: 800px;">

      <div style="padding-top: 50px;" v-if="tab == 1">
        <h2>브랜드 관리</h2>
        <p class="lead">브랜드와 브랜드의 아이템을 관리할 수 있는 페이지입니다.</p>
        <p style="margin: 0;">브랜드는 갯수 제한 없이 등록 가능합니다.</p>
        <p style="margin: 0;">등록된 브랜드를 [전시관리 > 브랜드X싸이월드] 메뉴를 통해 선물가게 메인 화면에 노출할 브랜드를 설정합니다.</p>
      </div>
      <div style="padding-top: 50px;" v-if="tab == 2">
        <h2>브랜드 이력 관리</h2>
        <p class="lead">브랜드X싸이월드 영역에 노출되는 브랜드 관리 이력을 조회할 수 있습니다.</p>
      </div>

      <div style="padding-top: 70px; padding-bottom: 70px;">
        <input type="radio" class="btn-check" name="options" id="option1" autocomplete="off" @click="tabClick(1)" checked>
        <label class="btn btn-secondary" for="option1" style="width: 50%;">브랜드 관리</label>
        <input type="radio" class="btn-check" name="options" id="option2" autocomplete="off" @click="tabClick(2)">
        <label class="btn btn-secondary" for="option2" style="width: 50%;">브랜드 이력 관리</label>
      </div>

      <div>
        <table class="table" v-if="tab == 1">
          <tbody>
            <tr>
              <th style="background-color: lightgray; width: 20%;" scope="row" >브랜드명</th>
              <td><input class="form-control" style="width: 100%;" v-model="searchObj.brandName"></td>
              <td style="background-color: lightgray; width: 20%;" >선물가게 노출 여부</td>
              <td>
                <input class="form-check-input" v-model="searchObj.displayAll" type="checkbox" value="" id="displayAll">
                <label class="form-check-label" for="displayAll" style="padding-right: 10px;">
                  전체
                </label>
                <input class="form-check-input" v-model="searchObj.displayOn" type="checkbox" value="" id="displayOn">
                <label class="form-check-label" for="displayOn" style="padding-right: 10px;">
                  노출
                </label>
                <input class="form-check-input" v-model="searchObj.displayOff" type="checkbox" value="" id="displayOff">
                <label class="form-check-label" for="displayOff" style="padding-right: 10px;">
                  노출 안 함
                </label>
              </td>
            </tr>
            <tr>
              <th style="background-color: lightgray;"  scope="row">검색</th>
              <td colspan="3" style="width: 500px;">
                <v-select @click="chnageCategory(value)" class="form-select" aria-label="Default select example" style="width: 20%; margin-right: 10px; display: inline;">
                  :items=""
                  <option value="1" selected>등록자</option>
                  <option value="2">수정자</option>
                </v-select>
                <input class="form-control" style="width: 40%; display: inline;" v-model="searchObj.updateName">
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

      <div>
        <p>전체 : <code>0</code> 건 | 노출 : <code>0</code>건 | 비노출 : <code>0</code>건</p>
      </div>

      <div style="margin-top: 40px;"  v-if="tab == 1">
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

  <h1>searchObj = {{ searchObj }}</h1>

    <TheFooter></TheFooter>
</template>

<style>

</style>

<script setup lang="ts">
import { ref, reactive, toRef } from 'vue'
import TheHeader from '@/components/single/TheHeader.vue'
import TheNavigator from '@/components/single/TheNavigator.vue'
import TheFooter from '@/components/single/TheFooter.vue'
import { brandSearchObj } from '@/modules/interface/interfaceSearch'

let tab: Number | any = ref(1);

let searchForms: Object = reactive({
  
});

let searchObj: brandSearchObj = reactive({
  brandName: null,
  createName: null,
  firstCount: 0,
  displayAll: true,
  displayOn: true,
  displayOff: true,
  size: 50,
  updateName: null,
})

const tabClick: Function = (tabNumber: Number) => {
  console.log("searchObj : ", searchObj)
  tab.value = tabNumber;
}
const chnageCategory: Function = (value : any) => {
  console.log("chnageCategory : ", value);
  // tab.value = cateNumber;
}

</script>