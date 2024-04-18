<script setup></script>

<template>
  <footer>
    <div class="footer-container">
      <div class="footer-intro row">
        <div class="company-details col-12 col-md-4">
          <img
            src="../assets/logo-colored.png"
            style="width: 180px; height: 35px"
          />
          <div class="text-weight-bold">
            우리는 국가의 장벽을 넘어 최고의 인재를 매칭해드립니다.
          </div>
          <div class="text-gray text-weight-bolder">010-0000-0000</div>
          <div class="text-gray text-weight-bolder">aaaaa@naver.com</div>
        </div>

        <div class="row col-12 col-md-8 work-card-container">
          <div class="col-6 col-md-3 work-card" v-for="index in 4" :key="index">
            <img src="../assets/code.png" style="width: 40px; height: 40px" />

            <div class="text-weight-bold">해외 개발자 원격 채용</div>

            <div class="text-weight-bold">
              바로가기
              <img
                src="../assets/arrow.png"
                style="width: 20px; height: 20px"
              />
            </div>
          </div>
        </div>
      </div>

      <div class="footer-address-info row">
        <div class="col-12 col-sm-6 col-md-3">
          <div class="text-weight-bold">상호명</div>
          <div>하이퍼하이어</div>
          <div class="text-gray text-weight-bold">
            Hyperhire India Private Limited
          </div>
        </div>

        <div class="col-12 col-sm-6 col-md-3">
          <div class="text-weight-bold">대표 CEO</div>
          <div>김주현</div>
          <div class="text-gray text-weight-bold">Juhyun Kim</div>
        </div>

        <div class="col-12 col-sm-6 col-md-3">
          <div class="text-weight-bold">사업자등록번호 CIN</div>
          <div>427-86-01187</div>
          <div class="text-gray text-weight-bold">U74110DL2016PTC290812</div>
        </div>

        <div class="col-12 col-sm-6 col-md-3">
          <div class="text-weight-bold">주소 ADDRESS</div>
          <div>서울특별시 강남대로 479, 지하 1층 238호</div>
          <div class="text-gray text-weight-bold">
            D-138, Street number 11, Jagjeet Nagar, North East Delhi, New Delhi,
            110053 India
          </div>
        </div>
      </div>

      <div class="text-gray text-weight-bold">ⓒ 2023 Hyperhire</div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  background-color: #fbfbfb;
  color: black;
  padding: 50px 0;
}

.footer-container {
  max-width: 1162px;
  width: 100%;
  margin: 0 auto;
  padding: 20px;
}

.company-details {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.text-gray {
  color: #5e626f;
}
.work-card-container {
  display: flex;
  gap: 15px;

  @media (max-width: 1000px) {
    padding-top: 20px;
  }
}

.work-card {
  max-width: 170px;
  width: 100%;
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 10px;
  border-radius: 10px;
  background-color: white;

  @media (min-width: 1000px) {
    padding-top: 20px;
    max-width: 160px;
  }
}

.footer-address-info {
  padding: 40px 0;

  @media (max-width: 1000px) {
    gap: 20px;
    padding: 30px 0;
  }
}
</style>
