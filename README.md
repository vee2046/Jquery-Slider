# JQuery Slider Plugin

## Use
    $('.j-high-slider').madSlider({
          formula: function(curLength,length){
            // 百分比进度
            var per = Math.floor(curLength/length*100)
            return per;
          },
          callBack: function(v,me){
            console.log('v='+v);
          }
        })
## Options

    formula: 返回值的计算公式，curLength 当前拖拽长度，length 总长度；
    callBack: 拖拽回调，v是 formula 返回值,me是实例对象

## 交互对象属性值
- bar

所在标签代表进度

```
<div class="slider-bar" data-slider="bar"></div>
```
- drager

所在标签代表拖拽对象

```
<div class="slider-drager" data-slider="drager"></div>
```

## 实例变量
- $element，父级对象
- $drager，拖拽对象
- $bar，进度层