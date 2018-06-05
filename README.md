```
<!DOCTYPE html>
<html lang="en">
<head>
  <script src="https://cdn.bootcss.com/jquery/2.2.3/jquery.js"></script>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>jquery-(Dom || fn)</title>
</head>
<body>
  <div class="box" id="set" title="week">
    <p class="week-1">monday</p>
    <p class="week-2">tuesday</p>
    <p class="week-3">wednesday</p>
    <p class="week-4">thursday</p>
    <p class="week-5">friday</p>
    <p class="week-6">saturday</p>
    <p class="week-7">sunday</p>
    <input type="text" name="" value="username">
  </div>
  <script>
    $('input').val("jirenggu");
    //这是一个读写双用的方法，用来处理input的value，当方法没有参数的时候返回input的value值，当传递了一个参数的时候，方法修改input的value值为参数值
    $('.box').attr("title");
    //获取元素特定属性的值
    $('.box').removeAttr("title");
    //为匹配的元素集合中的每个元素中移除一个属性（attribute）
    //.removeAttr() 方法使用原生的 JavaScript removeAttribute() 函数,但是它的优点是可以直接在一个 jQuery 对象上调用该方法，并且它解决了跨浏览器的属性名不同的问题
    $('.box').prop("id");
    //获取/设置值。
    $('.week-2').css({
      "background-color":"red",
      "font-size":"20px"
    });
    //获取元素style特定property的值
    $('p').addClass("my your")
    //为元素添加class，不是覆盖原class，是追加，也不会检查重复
    $('p').hasClass(".and")
    //检查元素是否包含某个class，返回true/false
    $( "div.box" ).toggleClass( "bounce" )
    //toggle是切换的意思，方法用于切换
  </script>
</body>
</html>

```


```
<!DOCTYPE html>
<html lang="en">
<head>
  <script src="https://cdn.bootcss.com/jquery/2.2.3/jquery.js"></script>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>jquery-(Dom || fn)</title>
</head>
<body>
  <div class="box" id="set" title="week">
    <p class="week-1">monday</p>
    <p class="week-2">tuesday</p>
    <p class="week-3">wednesday</p>
    <p class="week-4">thursday</p>
    <p class="week-5">friday</p>
    <p class="week-6">saturday</p>
    <p class="week-7">sunday</p>
    <input type="text" name="" value="username">
  </div>
  <script>
    $('p').each(function(index){
  	console.log(index + ":" + $(this).text())
    });
    //遍历一个jQuery对象，为每个匹配元素执行一个函数
    var object1 = {
    beijing: { people:20000000 },
    shanghai: { people: 22000000, billing: 1 },
    };
    var object2 = {
      shanghai: { people: 22000000,billing: 2 },
      chongqing: { penple:30000000 }
    };
    $.extend( object1, object2 );
    //合并操作不是递归的
    $('.week-3').clone().appendTo('.week-2');
    //clone()方法深度复制所有匹配的元素集合，包括所有匹配元素、匹配元素的下级元素、文字节点
    var list = $('.week-4');
    alert("index:" + $('p').index(list))  ;
    //从给定集合中查找特定元素index
    $(function(){
    console.log('ready');
    });
    //当DOM准备就绪时，指定一个函数来执行。
  </script>
</body>
</html>

```
