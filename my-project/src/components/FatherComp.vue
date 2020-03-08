<template>
    <div>
		<textarea class="lkp-title">父组件的toCity</textarea>
        <textarea v-model="toCity"></textarea>
        <train-city @showCityName="updateCity" :sendData="toCity"></train-city>
		<div id="example">
			{{message.split('').reverse().join('')}}
			
				现在时间是：{{now}}
				更新时间：{{updateNow()}}
			
		</div>
		
    </div>
</template>
	
<script>
  import TrainCity from './train-city.vue'
  export default {
    name:'index',
    components: {TrainCity},
    data () {
      return {
        toCity:"北京",
		message: 'lkp'
      }
    },
    methods:{
      updateCity(data){//触发子组件城市选择-选择城市的事件
        this.toCity = data.cityname;//改变了父组件的值
        console.log('toCity:'+this.toCity)
      },
      updateNow(){
		return Date.now();
     }
    },
	computed: {
		now: function(){
			return Date.now();
		}
	}
  }
</script>
<style >
	.lkp-title {
		color: #FF0000;
	}
</style>