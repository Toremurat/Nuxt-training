<template>
  <div>
    <b-row>
    <b-col lg="9" md="8" cols="12">
      <blockItems></blockItems>
    </b-col>
      <b-col lg="3" md="4" cols="0" class="d-sm-none d-md-block d-lg-block d-xl-block">
       <div class="col-lg-12">
          <div class="mcard cstm-mcard">
            <div class="mcard-body">
              <p class="mcard-title">Курс обмена валют:</p>
            </div>
          </div>
        </div>
        <div class="col-lg-12">
          <div class="mcard cstm-prodcard">
            <div class="prodcard-body">
              <div alt="" class="cred-mcard"></div>
              <div class="prodcard-title"><p>Кредит Auto</p></div>
            </div>
          </div>
        </div>
        <div class="col-lg-12">
          <div class="mcard cstm-prodcard">
            <div class="prodcard-body">
              <div class="depos-mcard"></div>
              <div class="prodcard-title"><p>Депозиты</p></div>
            </div>
          </div>
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
import blockItems from '~/components/blockItems'
export default {
  components: {
    blockItems
  }
}
</script>

<style>
.mcard.cstm-mcard {
    box-shadow: 0 2px 4px -2px rgba(0, 0, 0, 0.2);
    min-height: 10rem;
    border-radius: 5px;
    margin-bottom: 1rem;
    background-image: url(../assets/img/card-bg.png);
    background-size: cover;
    max-width: 160px!important;
    margin: 0 auto 1rem;
}

.mcard.cstm-mcard p {
    font-size: 0.75rem;
    font-weight: bold;
    padding: 1rem 0.7rem;
    color: #757575;
}
.mcard.cstm-prodcard {
    box-shadow: 0 2px 4px -2px rgba(0, 0, 0, 0.2);
    min-height: 10rem;
    border-radius: 5px;
    margin-bottom: 1rem;
    background-image: url(../assets/img/card-bg.png);
    background-size: cover;
    max-width: 160px!important;
    margin: 0 auto 1rem;
}
.prodcard-title {
    min-height: 2rem;
}

.prodcard-title p {
    border: solid 2px #ebebeb;
    border-top: none;
    margin: 0;
    padding: 5px 10px 10px 15px;
    background: #ba0000;
    color: white;
    font-size: 0.65rem;
    font-weight: bold;
    border-radius: 0 0 5px 5px;
    max-width: 160px!important;
    margin: 0 auto 1rem;
}
.cred-mcard {
    background: url(../assets/img/auto.png);
    background-size: cover;
    min-height: 140px;
    border: 2px solid #ececec;
    border-bottom: 0;
    margin-bottom: 0;
}
.depos-mcard {
    background: url(../assets/img/graph.png);
    background-size: cover;
    min-height: 140px;
    border: 2px solid #ececec;
    border-bottom: 0;
    margin-bottom: 0;

}
</style>
