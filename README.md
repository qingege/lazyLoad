# lazyLoad
###基本属性介绍
* placeholder：
    - placeholder,值为某一图片路径.此图片用来占据将要加载的图片的位置,待图片加载时,占位图则会隐藏
* effect:
     - 载入使用何种效果
     - effect(特效),值有show(直接显示),fadeIn(淡入),slideDown(下拉)等,常用fadeIn
* threshold:
     - threshold,值为数字,代表页面高度.如设置为200,表示滚动条在离目标位置还有200的高度时就开始加载图片,可以做到不让用户察觉
* event：
    - event,值有click(点击),mouseover(鼠标划过),sporty(运动的),foobar(…).可以实现鼠标莫过或点击图片才开始加载,后两个值未测试…
* container:     
    - container,值为某容器.lazyload默认在拉动浏览器滚动条时生效,这个参数可以让你在拉动某DIV的滚动条时依次加载其中的图片，对某容器中的 图片实现效果
* failurelimit :
    - failurelimit,值为数字.lazyload默认在找到第一张不在可见区域里的图片时则不再继续加载,但当HTML容器混乱的时候可能出现可见区域内图片并没加载出来的情        况,failurelimit意在加载N张可见区域外的图片,以避免出现这个问题.

###实例：

* <script>
    $(function(){
        $("img.lazy").lazyload({
            placeholder: "image/22.jpg", 
            effect: "fadeIn",
            threshold: 50, 
            event: 'click',
            container: $("#container"),   
            failurelimit : 10 
        });
    });
</script> *
