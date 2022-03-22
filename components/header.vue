<template>
  <div>
    <header class="header">
      <h1 class="headerText">
        <span class="headerText_step"
          ><span>STEP</span>
          <span class="headerText_stepNum">1</span>
        </span>
        <span class="headerText_title">
          <span class="headerText_select">お飾りの種類を選ぶ</span>
          <span class="headerText_required">※必須</span>
        </span>
      </h1>
    </header>
  </div>
</template>

<script></script>
<style scoped>
* {
  margin: 0;
}

.header {
  line-height: 1.15;
  font-weight: 400;
  color: #3b3224;
  box-sizing: border-box;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 46px;
  border: 2px solid #1770ac;
  background-color: #fff;
  z-index: 300;
}

.headerText {
  color: #3b3224;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  font-size: inherit;
  line-height: inherit;
  font-weight: inherit;
  margin: 0;
  display: flex;
  height: 100%;
}

.headerText_step {
  line-height: inherit;
  font-weight: inherit;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 44px;
  padding-right: 6px;
  text-align: center;
  font-size: 10px;
  color: #fff;
  background-image: url("/images/header.svg");
}

.headerText_stepNum {
  line-height: inherit;
  text-align: center;
  color: #fff;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  display: block;
  font-weight: 500;
  font-size: 24px;
}

.headerText_title {
  color: #3b3224;
  line-height: inherit;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  display: flex;
  align-items: center;
  margin-left: 4px;
  font-weight: 500;
  font-size: 16px;
}

.headerText_select {
  color: #3b3224;
  line-height: inherit;
  font-weight: 500;
  font-size: 16px;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  margin-left: 10px;
  font-weight: bold;
}

.headerText_required {
  line-height: inherit;
  font-weight: 500;
  font-size: 16px;
  box-sizing: border-box;
  border-style: solid;
  border-width: 0;
  color: #de3944;
  margin-left: 1px;
  font-weight: bold;
}
</style>
