---
layout: page
title: Store
permalink: /store/
show-in-menu: yes
---

    
<style>
    @import "compass/css3";

/* 
  Author: Sravan Kumar
  Website: http://wittysparks.com
  License: none (public domain)
*/
body{ font:normal 12px/25px Arial, Helvetica, sans-serif}  
.divform{display:table;border-collapse:collapse}
.divform .r{display:table-row}
.divform .c{display:table-cell;padding:5px 0px;vertical-align:middle}
input[type="text"], select, label{height:30px}
input[type="text"], select, textarea, label, input[type="submit"]{margin:0 5px}
input[type="text"], select, textarea{padding:5px;width:96%;border:1px solid #CCC;-webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);-moz-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);border-radius:4px}
input[type="submit"]{margin-top:15px;background-color:#F5F5F5;color:#444444;border:1px solid rgba(0, 0, 0, 0.1);padding:5px;font-weight:bold;box-shadow:0 1px 0 rgba(255, 255, 255, 0.2) inset, 0 1px 2px rgba(0, 0, 0, 0.05);border-radius:4px;background-color:#F5F5F5;background-image:-moz-linear-gradient(top, #ffffff, #e6e6e6);background-image:-webkit-gradient(linear, 0 0, 0 100%, from(#ffffff), to(#e6e6e6));background-image:-webkit-linear-gradient(top, #ffffff, #e6e6e6);background-image:-o-linear-gradient(top, #ffffff, #e6e6e6);background-image:linear-gradient(to bottom, #ffffff, #e6e6e6);background-repeat:repeat-x}
input[type="radio"], input[type="checkbox"]{margin:0 0 0 2%;padding:0;vertical-align:middle}
input[type="text"], select, textarea, .divform, .divform .r, .divform .c, form{box-sizing:border-box;-moz-box-sizing:border-box;-webkit-box-sizing:border-box}

/* iPads (portrait and landscape) */
@media only screen and (min-width:480px) and (max-width:1024px){
body{ font:normal 16px/30px Arial, Helvetica, sans-serif}
.divform, .divform .r, .divform .c{display:block}
.divform .r{clear:both}
.divform .c{width:50%;float:left;padding-left:10px;padding-right:10px}
.divform .c:nth-child(2n+3){clear:left}
label, .fheading, input[type="submit"]{margin-left:0;text-indent:0}
input[type="submit"]{padding-left:20px;padding-right:20px}
textarea, input[type="text"], select{width:100%;margin:0}
input[type="radio"], input[type="checkbox"]{margin:0 5px;padding:0;vertical-align:middle}
.ver2 .c{width:35%}
.ver2 .c:nth-child(2n+2){width:65%}
.c.frwd{width:100%;}
.c.frwd textarea, .c.frwd input[type="text"], .c.frwd select{width:100%}
.ver2 .frwd.c:nth-child(2n+2){width:100%}
}

/* Smartphones (portrait and landscape) */
@media only screen and (max-width:480px){
body{ font:normal 16px/30px Arial, Helvetica, sans-serif}
h1{margin:0 0 20px 0}
label, .fheading, input[type="submit"]{margin:0;text-indent:0}
.divform, .divform .r, .divform .c{display:block}
.divform .r{clear:both}
input[type="text"], select, textarea{width:100%;margin:0}
input[type="radio"], input[type="checkbox"]{margin:0 2%}
input[type="submit"]{width:100%;margin-top:20px}
}

/* Only Safari */
@media screen and (-webkit-min-device-pixel-ratio:0) {
select{text-indent:5px;line-height:24px}
}
 
 </style>
  
 
   
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
  


<div class="container">
  <h2>Free Dev Kit</h2>
  <form name="wittysparks" id="formRequest">
  <div class="form-group">
      <label for="Name">Name</label>
      <input type="text" class="form-control" id="Name" placeholder="Enter name" name="Name">
    </div>
    
    <div class="form-group">
      <label for="Email">Email</label>
      <input type="text" class="form-control" id="Email" placeholder="Enter email" name="Email">
    </div>
    
    <div class="form-group">
      <label for="Contact">Contact Number</label>
      <input type="text" class="form-control" id="Contact" placeholder="Enter contact number" name="Contact">
    </div>
    
    
    
    <button type="submit" class="c"  name="Submit" id="Submit" onclick="postContactToGoogle()" value="Submit">Submit</button>
    <div class="c"><input name="button" type="submit" onclick="postContactToGoogle()" value="Submit"/></div>
    
  
    
  </form>
</div>



<script>
function postContactToGoogle() {
var Name=$('#Name').val();
var Email=$('#Email').val();
var Contact=$('#Contact').val();
$.ajax({
url:"https://docs.google.com/forms/d/e/1FAIpQLSdNV2A_v_6v27q2x5lfZzQ8zGtEeruZHvn6Pfl9wTelSrV_bQ/formResponse",data:{"entry.675230857":Name,"entry.1965877327":Email,"entry.1149358831":Contact},type:"POST",dataType:"xml",statusCode: {0:function() { window.location.replace("thankyou.html");},200:function(){window.location.replace("thankyou.html");}}
});
}
</script>











