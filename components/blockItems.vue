<template>
  <div id="Cards">
      <b-row>
        <b-col xl="6" md="12" cols="12">
          <div class="card cstm-card">
            <div class="card-body">
              <b-row>
                <b-col xl="2" md="2" cols="2"><div class="icon-bg-badge"><fa class="icon-badge" :icon="['fas', 'briefcase']" /></div></b-col>
                <b-col xl="10" md="10" cols="10"><h3 class="card-title"> Special title treatment</h3></b-col>
              </b-row>
            </div>
          </div>
        </b-col>
        <b-col xl="6" md="12" cols="12">
          <div class="card cstm-card">
            <div class="card-body">
              <b-row>
                <b-col xl="2" md="2" cols="2"><div class="icon-bg-badge"><fa class="icon-badge" :icon="['fas', 'book']" /></div></b-col>
                <b-col xl="10" md="10" cols="10"><h3 class="card-title"> Special title treatment</h3></b-col>
              </b-row>
            </div>
          </div>
        </b-col>
      </b-row>
      <b-row>
        <b-col xl="6" md="12" cols="12">
          <div class="card cstm-card">
            <div class="card-body">
              <b-row>
                <b-col xl="2" md="2" cols="2"><div class="icon-bg-badge"><fa class="icon-badge" :icon="['fas', 'briefcase']" /></div></b-col>
                <b-col xl="10" md="10" cols="10"><h3 class="card-title"> Special title treatment</h3></b-col>
              </b-row>
            </div>
          </div>
        </b-col>
        <b-col xl="6" md="12" cols="12">
          <div class="card cstm-card">
            <div class="card-body">
              <b-row>
                <b-col xl="2" md="2" cols="2"><div class="icon-bg-badge"><fa class="icon-badge" :icon="['fas', 'book']" /></div></b-col>
                <b-col xl="10" md="10" cols="10"><h3 class="card-title"> Special title treatment</h3></b-col>
              </b-row>
            </div>
          </div>
        </b-col>
      </b-row>
      <b-row>
        <b-col xl="6" md="12" cols="12">
          <div class="card cstm-card">
            <div class="card-body">
              <b-row>
                <b-col xl="2" md="2" cols="2"><div class="icon-bg-badge"><fa class="icon-badge" :icon="['fas', 'briefcase']" /></div></b-col>
                <b-col xl="10" md="10" cols="10"><h3 class="card-title"> Special title treatment</h3></b-col>
              </b-row>
            </div>
          </div>
        </b-col>
        <b-col xl="6" md="12" cols="12">
          <div class="card cstm-card">
            <div class="card-body">
              <b-row>
                <b-col xl="2" md="2" cols="2"><div class="icon-bg-badge"><fa class="icon-badge" :icon="['fas', 'book']" /></div></b-col>
                <b-col xl="10" md="10" cols="10"><h3 class="card-title"> Special title treatment</h3></b-col>
              </b-row>
            </div>
          </div>
        </b-col>
      </b-row>
    </div>
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
.icon-bg-badge {
    background-image: url(../assets/img/badge.png);
    background-size: cover;
    width: 40px;
    height: 80px;
    margin: -24px auto 0;
}
.icon-badge {
    margin: 30px auto;
    font-size: 1.2rem;
    width: 40px!important;
    text-align: center;
    color: #9b1b1f;
}
.card.cstm-card {
    box-shadow: 0 2px 4px -2px rgba(0,0,0,0.2);
    min-height: 25rem;
    border-radius: 5px;
    background-image: url(../assets/img/card-bg.png);
    background-size: cover;
    margin-bottom: 2rem;
}

.card.cstm-card h3.card-title {
    color: red;
    border-bottom: 3px solid red;
    width: 100%;
    padding-bottom: 0.5rem;
}

.card.cstm-card.cstm-line {
    float: right;
    width: 80%;
}

img.cstm-badge {
    position: absolute;
    top: -40%;
    left: 10%;
    width: 90%;
}
</style>
