# 简介
 本套日历现依赖于jQuery实现，根据香港天文台提供的数据，关于中国农历的测算从1901-2100年的测算数据，不一定准确，仅供参考。

# 文件描述
  JS文件中（almanac.js）均有详细的注释。里面主要包含三个对象
  * Almanac 这部分代码包含日历的绘画、更新、二十四节气、天干地支等信息的计算和显示
  * DateSelection 日历顶部右侧切换年、月所封装的操作函数
  * global 全局变量

# 截图
  ![日历截图](shortcut.png)

# 使用方法
`
  $("#id_almanac").almanac({
    /**
     * 画日历之后调用函数
     */
    afterDrawCld: function(year, month){
      console.log('加载完成');
    },
    /**
     * 双击某一天的事件
     */
    dbClickDay: function(elem){
      var _this = $(elem);
      console.log('阳历：' + _this.attr('data-year') + '年' + _this.attr('data-month') + '月' + _this.attr('data-solor'));
    },
    /**
     * 单击某一天的事件
     */
    clickDay: function(elem){
      var _this = $(elem);
      console.log('阳历：' + _this.attr('data-year') + '年' + _this.attr('data-month') + '月' + _this.attr('data-solor'));
    }
  });

`
详细请参见index.html示例文件。

# Q/A
  联系方式：yima1006@foxmail.com