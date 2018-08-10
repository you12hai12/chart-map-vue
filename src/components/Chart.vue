<template>
	<div id="line" :style="{width:'1900px',height:'400px'}"></div>
</template>

<script>
	import Vue from 'vue'
	import VueResource from 'vue-resource'
	import axios from 'axios'
	import echarts from 'echarts'
	
	Vue.use(VueResource);
	Vue.prototype.$echarts = echarts;
	let lineDatas = require('../../static/line.json')
	export default {
		mounted(){
			this.buildLine();
		},
		methods:{
			buildLine(){
				let lineData = lineDatas.data;
				let names = [];
				let values = [];
				for(let dat of lineData){
					names.push(dat.week);
					values.push(dat.nums);
				}
				let lineChart = this.$echarts.init(document.getElementById("line"));
				lineChart.setOption({
					title:{
						text:'一周人数统计',
				        subtext:'2018年',
				        x:'center',
				        y:'top',
				        textAlign:'left'
					},
					tooltip:{
						trigger: 'axis',
				        axisPointer : {            
				            type : 'shadow'        
				        }
					},
					grid: {
				        left: '3%',
				        right: '4%',
				        bottom: '3%',
				        containLabel: true
				    },
					xAxis:{
						type : 'category',
						axisTick: {
                			alignWithLabel: true
            			},
						data:names
					},
					yAxis:{
						axisLine: {
				            show: false
				        },
				        axisTick: {
				            show: true
				        },
				        axisLabel: {
				            textStyle: {
				                color: '#999'
				            }
				        }
					},
					series:[{
						name:"人数",
						type:"bar",
						data:values
					}]
				});
			}
		}
	}
</script>

<style>
</style>