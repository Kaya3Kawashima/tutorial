<template>
  <main class="main">
    <section class="main_preview">
      <div class="previewHeader">
        <p class="borderBottomText">選択中の商品</p>
      </div>

      <div class="previewImg">
        <figure class="previewImg_productImg">
          <p>
            アイコンを選択して
            <br />
            種類をお選びください
          </p>
        </figure>
      </div>
    </section>
    <table>
      <section class="main_selector">
        <section class="main_selectorBody">
          <div id="step1" class="step_active" style="min-height: 424px">
            <p class="stepDesc">
              ご希望のお飾りの種類の画像をタップすると選択されます。
            </p>

            <button class="itemImgBtn" type="button" @click="checkDerkYellow">
              <figure class="itemImgBtn_imgWrap">
                <img src="/images/hinaningyo.png" alt />
              </figure>
              <h3 class="itemImgBtn_name_derkYellow">雛人形</h3>
            </button>
            <div class="showCheck_derkYellow" v-if="showCheckDerkYellow">
              <img src="/images/check.svg" />
            </div>
            <button class="itemImgBtn" type="button" @click="checkDerkBlue">
              <figure class="itemImgBtn_imgWrap">
                <img src="/images/hinaningyo_white.png" alt />
              </figure>
              <h3 class="itemImgBtn_name_derkBlue">雛人形（白）</h3>
            </button>
            <div class="showCheck_derkBlue" v-if="showCheckDerkBlue">
              <img src="/images/check.svg" />
            </div>
          </div>
        </section>
      </section>
      <section class="main_selectorFooter">
        <div class="totalPrice">
          合計金額
          <span class="totalPrice_red">0円（税込）</span>
        </div>
        <div class="ctrl">
          <button class="ctrl_confirm" type="button">注文内容確認</button>
          <button class="ctrl_btn_next" type="button">STEP.2</button>
        </div>
      </section>
    </table>
  </main>
</template>

<script>
export default {
  data() {
    return {
      showCheckDerkYellow: false,
      showCheckDerkBlue: false,
    };
  },
  methods: {
    checkDerkYellow() {
      this.showCheckDerkYellow = true;
    },
    checkDerkBlue() {
      this.showCheckDerkBlue = true;
    },
  },
};
</script>

<style scoped>
.main {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  position: relative;
  display: flex;
  height: auto;
  margin-top: 46px;
  z-index: 100;
}

.main_preview {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  flex: 1 0 auto;
  max-width: calc(100% - 368px);
  padding: 0 24px;
  background-color: #fff;
}

.previewHeader {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  padding: 8px 0 24px 0px;
}

.borderBottomText {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  margin: 0;
  display: inline-block;
  padding-left: 40px;
  border-bottom: 1px solid #3b3224;
  font-size: 12px;
  margin-bottom: 8px;
  margin-left: -24px;
}

.previewImg {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  position: relative;
  max-width: clamp(
    calc((100vh - 46px - 91px) * 1.3501),
    81.25%,
    calc((100vh - 46px - 91px) * 1.3501)
  );
  max-height: calc(100vh - 46px - 72px);
  margin: 0 auto;
}

.previewImg_productImg {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  margin: 15em 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  transition: opacity 0.4s, z-index 0.4s;
  opacity: 1;
  z-index: 1;
}

.main_selector {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  position: relative;
  flex: 0 0 368px;
  max-width: 368px;
  box-shadow: 0 0 6px rgba(0, 0, 0, 0.08);
  display: flex;
  flex-direction: column;
  overflow-x: hidden;
}

.main_selectorBody {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  flex: 1 0 auto;
  position: relative;
  display: flex;
  margin-bottom: 100px;
  background-color: #f1f1f1;
  height: auto;
}

.step_active {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  top: 0;
  width: 368px;
  max-width: 368px;
  padding: 8px 22px 24px;
  position: static;
  height: auto;
  min-height: calc(100vh - 46px - 100px);
  background-color: #fff;
  transition: left 0.4s 0s ease-out, transform 0.4s 0s ease-out;
  transform: translateX(0);
  filter: brightness(100%);
  z-index: 100;
  overflow-y: auto;
  overflow-x: hidden;
}

.stepDesc {
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  margin: 0;
  margin-bottom: 16px;
  line-height: 1.9;
  font-weight: 500;
  font-size: 12px;
}

.itemImgBtn {
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  color: inherit;
  font: inherit;
  background: transparent;
  padding: 0;
  outline: 0;
  border-radius: 0;
  text-align: inherit;
  overflow: visible;
  text-transform: none;
  cursor: pointer;
  appearance: none;
  position: relative;
  display: block;
  width: 272px;
  max-width: 100%;
  margin: 0 auto 24px;
  transition-property: background-color;
  transition-duration: 0.4s;
  transition-timing-function: ease-out;
}

.itemImgBtn_imgWrap {
  text-align: right;
  text-transform: none;
  cursor: pointer;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 8px 0;
}

.itemImgBtn_name_derkYellow {
  position: relative;
  text-align: inherit;
  text-transform: none;
  cursor: pointer;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  line-height: inherit;
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 40px;
  border-radius: 40px;
  font-weight: 500;
  font-size: 16px;
  color: #fff;
  background-color: #535149;
}

.itemImgBtn_name_derkBlue {
  position: relative;
  font: inherit;
  text-align: inherit;
  text-transform: none;
  cursor: pointer;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  line-height: inherit;
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 40px;
  border-radius: 40px;
  font-weight: 500;
  font-size: 16px;
  color: #fff;
  background-color: #494f5d;
}

.showCheck_derkYellow {
  position: absolute;
  top: 210px;
  left: 280px;
}

.showCheck_derkBlue {
  position: absolute;
  top: 473px;
  left: 280px;
}

.main_selectorFooter {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  flex: 0 0 auto;
  position: fixed;
  bottom: 0;
  background-color: #fff;
  box-shadow: 0 -1px 4px rgba(0, 0, 0, 0.04);
  z-index: 100;
  width: 368px;
}

.totalPrice {
  font-weight: 400;
  color: #3b3224;
  border-style: solid;
  border-width: 0;
  padding: 9px 0;
  background-color: #fff;
  text-align: center;
  line-height: 1.4;
  font-size: 12px;
}

.totalPrice_red {
  text-align: center;
  line-height: 1.4;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  margin-left: 8px;
  font-weight: 700;
  font-size: 16px;
  color: #de3944;
}

.ctrl {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  display: flex;
  height: 60px;
}

.ctrl_confirm {
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  vertical-align: middle;
  font: inherit;
  background: transparent;
  padding: 0;
  margin: 0;
  outline: 0;
  border-radius: 0;
  text-align: inherit;
  overflow: visible;
  text-transform: none;
  cursor: pointer;
  appearance: none;
  flex: 1 1 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #de3944;
  font-weight: 500;
  font-size: 14px;
  color: #fff;
  transition-property: background-color;
  transition: 0.3s;
  transition-timing-function: ease-out;
}

.ctrl_confirm:hover {
  opacity: 0.7;
}

.ctrl_btn_next {
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  vertical-align: middle;
  font: inherit;
  background: transparent;
  margin: 0;
  outline: 0;
  border-radius: 0;
  text-align: inherit;
  overflow: visible;
  text-transform: none;
  appearance: none;
  flex: 1 1 25%;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 68px;
  padding: 0 8px;
  font-weight: 500;
  font-size: 14px;
  transition-property: background-color;
  transition-duration: 0.4s;
  transition-timing-function: ease-out;
  background-color: #f0f0f0;
  color: #b3b3b3;
  pointer-events: none;
  cursor: default;
}
</style>
