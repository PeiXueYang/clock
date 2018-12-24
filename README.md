求时针与分针的夹角问题 ？

现在有这样的 一个需求 给出任意的几时几分，设计一个算法 计算出 时针与分针的夹角。（30min）

首先针对于求时针与分针的夹角问题 首先要明白 钟表走动的原理

时针走一小时 也就是走了30° 此时相当于 60分钟走了30°  说明时针走一分钟 走了 30°/ 60  = 0.5 °

对于分针来说 30° 其实就是走了 5分钟    就说明  一分钟  分针走了6°



知道这个规则 设计算法

function calculate (min,hour) {

  let min = parseInt(min)
  let hour = parseInt(hour)
  
  /**
      0<= min <= 60
      0<= hour <= 12
  **/
  let angle  ;
   if(0<= min <= 60 &&   0<= hour <= 12){
       angle = Math.abs (  (hour*30 + min*0.5) - min*6   )
   }
  
   return angle

}
