<template>
<div id="meal_05"></div>
</template>

<script>
  export default {
    name: "AppRadar",
    mounted() {
      //this.init();
     this.getTestData();//this指向getTestData函数
    },
    methods:{
      getTestData(){
        this.$axios.get('/f5_cost_rate',{params:{
          card_no:'181318'
          }}).then(res=>{//异步执行调用数据
          console.log(res.data);//响应数据
          this.init(res.data);//让this指向的init方法响应数据
        })
      },
      init(data){//将数据传入要画的echarts图中名称是init

        let chart = this.$echarts.init(document.getElementById('meal_05'));

          let option = {
            "title": {
              "text": "食堂",
              "textStyle": {
                "color": "#fff",
                "fontSize": 60
              },
              "subtextStyle": {
                "color": "#999",
                "fontSize": 34
              },
              "x": "center",
              "top": "0%"
            },
            "grid": {
              "top": 200,
              "bottom": 100
            },
            "tooltip": {},
            "xAxis": {
              "data": ["关井数", "开井数", "不在线"],
              "axisTick": {
                "show": false
              },
              "axisLine": {
                "show": false
              },
              "axisLabel": {
                "show": false
              }
            },
            "yAxis": {
              "splitLine": {
                "show": false
              },
              "axisTick": {
                "show": false
              },
              "axisLine": {
                "show": false
              },
              "axisLabel": {
                "show": false
              }
            },
            "series": [{
              "name": "",
              "type": "pictorialBar",
              "symbolSize": [100, 45],
              "symbolOffset": [0, -14],
              "z": 12,
              "data": [{
                "name": "关井数",
                "value": "981",
                "trueVal": "98",
                "symbolPosition": "end",
                "itemStyle": {
                  "normal": {
                    "color": "#00fff5"
                  }
                }
              }, {
                "name": "开井数",
                "value": "4991",
                "trueVal": "499",
                "symbolPosition": "end",
                "itemStyle": {
                  "normal": {
                    "color": "#ffcc00"
                  }
                }
              }, {
                "name": "不在线",
                "value": "21",
                "trueVal": "2",
                "symbolPosition": "end",
                "itemStyle": {
                  "normal": {
                    "color": "#b9b7ff"
                  }
                }
              }]
            }, {
              "name": "",
              "type": "pictorialBar",
              "symbolSize": [100, 45],
              "symbolOffset": [0, 24],
              "z": 12,
              "data": [{
                "name": "关井数",
                "value": "981",
                "trueVal": "98",
                "itemStyle": {
                  "normal": {
                    "color": "#43bafe"
                  }
                }
              }, {
                "name": "开井数",
                "value": "4991",
                "trueVal": "499",
                "itemStyle": {
                  "normal": {
                    "color": "#ff7800"
                  }
                }
              }, {
                "name": "不在线",
                "value": "21",
                "trueVal": "2",
                "itemStyle": {
                  "normal": {
                    "color": "#e9a5ff"
                  }
                }
              }]
            }, {
              "name": "",
              "type": "pictorialBar",
              "symbolSize": [150, 75],
              "symbolOffset": [0, 44],
              "z": 11,
              "data": [{
                "name": "关井数",
                "value": "981",
                "trueVal": "98",
                "itemStyle": {
                  "normal": {
                    "color": "transparent",
                    "borderColor": "#43bafe",
                    "borderWidth": 5
                  }
                }
              }, {
                "name": "开井数",
                "value": "4991",
                "trueVal": "499",
                "itemStyle": {
                  "normal": {
                    "color": "transparent",
                    "borderColor": "#ff7800",
                    "borderWidth": 5
                  }
                }
              }, {
                "name": "不在线",
                "value": "21",
                "trueVal": "2",
                "itemStyle": {
                  "normal": {
                    "color": "transparent",
                    "borderColor": "#e9a5ff",
                    "borderWidth": 5
                  }
                }
              }]
            }, {
              "name": "",
              "type": "pictorialBar",
              "symbolSize": [200, 100],
              "symbolOffset": [0, 62],
              "z": 10,
              "data": [{
                "name": "关井数",
                "value": "981",
                "trueVal": "98",
                "itemStyle": {
                  "normal": {
                    "color": "transparent",
                    "borderColor": "#43bafe",
                    "borderType": "dashed",
                    "borderWidth": 5
                  }
                }
              }, {
                "name": "开井数",
                "value": "4991",
                "trueVal": "499",
                "itemStyle": {
                  "normal": {
                    "color": "transparent",
                    "borderColor": "#ff7800",
                    "borderType": "dashed",
                    "borderWidth": 5
                  }
                }
              }, {
                "name": "不在线",
                "value": "21",
                "trueVal": "2",
                "itemStyle": {
                  "normal": {
                    "color": "transparent",
                    "borderColor": "#e9a5ff",
                    "borderType": "dashed",
                    "borderWidth": 5
                  }
                }
              }]
            }, {
              "type": "bar",
              "silent": true,
              "barWidth": 100,
              "barGap": "-100%",
              "label": {
                "normal": {
                  "show": true,
                  "position": "top",
                  "distance": 40,
                  "textStyle": {
                    "color": "#fff",
                    "fontSize": 40
                  }
                }
              },
              "data": [{
                "name": "关井数",
                "value": "981",
                "trueVal": "98",
                "itemStyle": {
                  "normal": {
                    "color": {
                      "x": 0,
                      "y": 0,
                      "x2": 0,
                      "y2": 1,
                      "type": "linear",
                      "global": false,
                      "colorStops": [{
                        "offset": 0,
                        "color": "rgba(0,255,245,0.5)"
                      }, {
                        "offset": 1,
                        "color": "#43bafe"
                      }]
                    }
                  }
                }
              }, {
                "name": "开井数",
                "value": "4991",
                "trueVal": "499",
                "itemStyle": {
                  "normal": {
                    "color": {
                      "x": 0,
                      "y": 0,
                      "x2": 0,
                      "y2": 1,
                      "type": "linear",
                      "global": false,
                      "colorStops": [{
                        "offset": 0,
                        "color": "rgba(255,204,0,0.5)"
                      }, {
                        "offset": 1,
                        "color": "#ff7800"
                      }]
                    }
                  }
                }
              }, {
                "name": "不在线",
                "value": "21",
                "trueVal": "2",
                "itemStyle": {
                  "normal": {
                    "color": {
                      "x": 0,
                      "y": 0,
                      "x2": 0,
                      "y2": 1,
                      "type": "linear",
                      "global": false,
                      "colorStops": [{
                        "offset": 0,
                        "color": "rgba(185,183,255,0.5)"
                      }, {
                        "offset": 1,
                        "color": "#e9a5ff"
                      }]
                    }
                  }
                }
              }]
            }]
          }

          chart.setOption(option);
        }
      }
    }
</script>

<style scoped>
  #meal_05{
    position: absolute;
    bottom:0;
    left: 0;
    width: 25%;
    height: 30%;

  }
</style>
