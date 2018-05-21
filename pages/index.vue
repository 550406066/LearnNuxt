<template>
<div>

   <ul>
      <li><nuxt-link :to="{name:'index'}">HOME</nuxt-link></li>
      <li><nuxt-link :to="{name:'about',query:{Id:id}}">ABOUT</nuxt-link></li>
      <li><nuxt-link :to="{name:'news',params:{Id:id}}">NEWS</nuxt-link></li>
    </ul>
    <h2>用户信息</h2>
    {{info.name}}
    {{info.age}}
    {{info.county}}
    <button @click="getData">更新数据</button>
</div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      id: 10,
      info: {
        name: "",
        age: "",
        county: ""
      }
    };
  },

  async asyncData() {
  let { data } = await axios.get("https://easy-mock.com/mock/5b029472ca4d2d1d1c6508dc/scroll_copy/")
    return { info: data.data }
  },
  methods: {
    getData() {
      return axios
        .get("https://easy-mock.com/mock/5b029472ca4d2d1d1c6508dc/scroll_copy/")
        .then(res => {
          this.info = res.data.data;
        });
    }
  }
};
</script>

<style>

</style>
