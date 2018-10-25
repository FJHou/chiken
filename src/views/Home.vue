<template>
  <div class="home">
    <Row>
      <Col>人头价格：<InputNumber :max="10"
                   :min="0.1"
                   v-model="baseNumber"
                   :step="0.1"></InputNumber>
      </Col>

    </Row>

    <Divider></Divider>
    <Row>
      <Col span="2">大飞：</Col>
      <Col span="2">
      <InputNumber v-model="fly"
                   placeholder="输入人头" />
      </Col>
      <Col span="2">￥：<span>{{this.baseNumber * fly}}</span> </Col>
    </Row>
    <Divider></Divider>
    <Row>
      <Col span="2">豆子：</Col>
      <Col span="2">
      <InputNumber v-model="bean"
                   placeholder="输入人头" />
      </Col>
      <Col span="2">￥：<span>{{this.baseNumber * bean}}</span> </Col>
    </Row>
    <Divider></Divider>
    <Row>
      <Col span="2">鹏哥：</Col>
      <Col span="2">
      <InputNumber v-model="bird"
                   placeholder="输入人头" />
      </Col>
      <Col span="2">￥：<span>{{this.baseNumber * bird}}</span> </Col>
    </Row>
    <Divider></Divider>
    <Row>
      <Col span="2">侯哥：</Col>
      <Col span="2">
      <InputNumber v-model="monkey"
                   placeholder="输入人头" />
      </Col>
      <Col span="2">￥：<span>{{this.baseNumber * monkey}}</span> </Col>
    </Row>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  data() {
    return {
      fly: "",
      bean: "",
      bird: "",
      monkey: "",
      baseNumber: 0.5
    };
  },

  computed: {
    countingDafei() {
      return this.baseNumber * fly;
    }
  },

  components: {
    HelloWorld
  }
};
</script>

<style>
.title {
  font-size: 40px;
  color: red;
}
</style>

