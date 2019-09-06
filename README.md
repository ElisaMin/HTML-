# 修改index即可
<html><head><title>课程表</title><style>
html{font-size:5vw;}
body{margin:0}
.main{margin:1rem auto;width:90%;}
.day{display:none;margin-bottom: 0.5rem;border-bottom: 1px solid #ddd;}
.numb{width: 24vw;margin-right:1rem;}
.timelist,.card{font-size:.85rem;padding:.5rem;width: 70vw;box-shadow:0 0 3px 0 rgba(0,0,0,.5);background-color:#fff;border-radius:.3rem;margin-bottom:.5rem;min-height:1rem;}
.card {color:#fff;}
.time{width: 100%;}
.place,.name {padding-left: 1rem;font-size: 95%;}
.header {width:90%;display: flex;justify-content:space-between;padding:0.5rem 1rem;font-size:1.25rem;}
.footer {font-size: 0.5rem;padding-left: 1rem;margin-top: 1rem;margin-bottom: 1rem;}
.tabbar{justify-content:center;display:flex;box-shadow: 0 5px 5px rgba(0,0,0,0.1);}
a.tab{margin:0 0.25rem;padding:0.1rem 0.3rem;text-decoration:none;color:#999;} a.tab.active {color: #444;border-bottom: 0.1rem solid darkslateblue;}a.tab:hover{background:#eee} 
a{text-decoration:none;color:#000;}
</style><script>
  function see_today(){
    for (var i=1;i<7;i++) {
	  document.getElementById(i).style.display="none";
	  };
	document.getElementById("see_all").className="tab";
	document.getElementById("see_today").className="tab active";
	var d=new Date();var day=d.getDay();
    document.getElementById(day).style.display="flex";
};function see_all(){
    for (var i=1;i<7;i++) {
	  document.getElementById(i).style.display="flex";
	  };
	document.getElementById("see_all").className="tab active";
	document.getElementById("see_today").className="tab";
}</script></head><body>
<div class="header">
 <a style="justify-content: flex-end;width: 4rem;" href="javascript:void(0);" onclick="window.alert('未完善');" >三</a>
 <div style="justify-content: center;width: 4rem;">课程表</div>
 <div style="width: 4rem;"></div>
</div>
<div class="tabbar">
 <a class="tab active" id="see_today" href="javascript:void(0);" onclick="see_today();">今天课程</a>
 <a class="tab" href="javascript:void(0);" onclick="see_all();" id="see_all">查看全部</a>
</div>
<div class="main">
  <div class="day" id="1"></div>
  <div class="day" id="2"></div>
  <div class="day" id="3"></div>
  <div class="day" id="4"></div>
  <div class="day" id="5"></div>
  <div class="day" id="6"></div>
  <div class="day" id="7"></div>
  <!--上方class="day"的div可删除，用来充数的。-->
  <div class="day" id="8" style="display:flex !important;">
  <!--这里的id="X"是指这是星期X。-->
     <div class="numb">周八</div>
	 <!--建议在两个字之内-->
        <div class="time">
          <div class="timelist">信息1</div>
		  <!--信息1可以是时间-->
		  <div class="card" id="class1" >
		  <!--class1代表第一个课程，如果周一和周四都有同一节课的话请把classX代入进ID。-->
		   <div class="CardHeader">信息1</div>
            <div class="place">信息2</div>
            <div class="name">信息3</div></div>
          <div class="timelist">信息1</div>
  </div></div>
 </div>
 <div class="footer">PowerBy-Heizi·Elisamin</div><footer><script>var d=new Date();var day=d.getDay();document.getElementById(day).style.display="flex";</script><script>
document.getElementById("class1").style.background="cadetblue";
</script><!--这是卡的改色的脚本部分，"lightgray"可以改成任意你喜欢的颜色。--></footer></body></html>
