code
====
function tools(){
    var top=$(document).scrollTop();
    if(($.browser.msie==true)&&($.browser.version==6.0)){
        if(top>150)$("#box").css({position:"absolute",top:top-0});
    }else{
        if(top>150)$("#box").css({position:"fixed",top:0});
    }
         if(top<=150)$("#box").css({position:"static",top:0});
}

$(function(){
    window.onscroll=tools;
    window.onresize=tools;
});
