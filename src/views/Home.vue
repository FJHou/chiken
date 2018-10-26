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
    <Row class="flex">
      <Col span="2">大飞：</Col>
      <Col span="2">
      <InputNumber v-model="fly"
                   placeholder="输入人头" />
      </Col>
      <Col span="2">￥：<span>{{countingFly}}</span> </Col>
      <Divider type="vertical" />
      <Col span="2"
           class="pay">应付</Col>
      <Col>豆子￥：<span>{{countingBean-countingFly}}</span> </Col>
      <Divider type="vertical" />
      <Col>鹏哥￥：<span>{{countingBird-countingFly}}</span> </Col>
      <Divider type="vertical" />
      <Col>侯哥￥：<span>{{countingMonkey-countingFly}}</span> </Col>
    </Row>
    <Divider></Divider>
    <Row class="flex">
      <Col span="2">豆子：</Col>
      <Col span="2">
      <InputNumber v-model="bean"
                   placeholder="输入人头" />
      </Col>
      <Col span="2">￥：<span>{{countingBean}}</span> </Col>
      <Divider type="vertical" />
      <Col span="2"
           class="pay">应付</Col>
      <Col>大飞￥：<span>{{countingFly-countingBean}}</span> </Col>
      <Divider type="vertical" />
      <Col>鹏哥￥：<span>{{countingBird-countingBean}}</span> </Col>
      <Divider type="vertical" />
      <Col>侯哥￥：<span>{{countingMonkey-countingBean}}</span> </Col>
    </Row>
    <Divider></Divider>
    <Row class="flex">
      <Col span="2">鹏哥：</Col>
      <Col span="2">
      <InputNumber v-model="bird"
                   placeholder="输入人头" />
      </Col>
      <Col span="2">￥：<span>{{countingBird}}</span> </Col>
      <Divider type="vertical" />
      <Col span="2"
           class="pay">应付</Col>
      <Col>大飞￥：<span>{{countingFly-countingBird}}</span> </Col>
      <Divider type="vertical" />
      <Col>鹏哥￥：<span>{{countingBird-countingBird}}</span> </Col>
      <Divider type="vertical" />
      <Col>侯哥￥：<span>{{countingMonkey-countingBird}}</span> </Col>
    </Row>
    <Divider></Divider>
    <Row class="flex">
      <Col span="2">侯哥：</Col>
      <Col span="2">
      <InputNumber v-model="monkey"
                   placeholder="输入人头" />
      </Col>
      <Col span="2">￥：<span>{{countingMonkey}}</span> </Col>
      <Divider type="vertical" />
      <Col span="2"
           class="pay">应付</Col>
      <Col>大飞￥：<span>{{countingFly - countingMonkey}}</span> </Col>
      <Divider type="vertical" />
      <Col>豆子￥：<span>{{countingBean - countingMonkey}}</span> </Col>
      <Divider type="vertical" />
      <Col>鹏哥￥：<span>{{countingBird-countingMonkey}}</span> </Col>
    </Row>
    <Divider></Divider>
    <Button type="success"
            @click="chikenEnding">结束战斗</Button>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  data() {
    return {
      fly: 0,
      bean: 0,
      bird: 0,
      monkey: 0,
      baseNumber: 0.5
    };
  },

  computed: {
    countingFly() {
      return this.baseNumber * this.fly;
    },
    countingBean() {
      return this.baseNumber * this.bean;
    },
    countingBird() {
      return this.baseNumber * this.bird;
    },
    countingMonkey() {
      return this.baseNumber * this.monkey;
    }
    // winner() {
    //   let players = [{
    //     name: "大飞",
    //     value: this.countingFly
    //   },{
    //     name: "豆子",
    //     value: this.countingBean
    //   },{
    //     name: "鹏哥",
    //     value: this.countingBird
    //   },{
    //     name: "侯哥",
    //     value: this.countingMonkey
    //   }]
    //   return Math.max()
    // }
  },

  methods: {
    chikenEnding() {
      alert("傻篮子鹏哥哥，哈哈哈哈");
    }
  },

  components: {
    HelloWorld
  }
};
</script>

<style scoped lang="less">
.home {
  font-size: 20px;
  .flex {
    display: flex;
    align-items: center;
  }
  .pay {
    color: red;
    font-weight: bolder;
  }
}
</style>

