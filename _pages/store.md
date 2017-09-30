---
layout: page
title: Store
permalink: /store/
show-in-menu: yes
---

    
    
 
  
 
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
  


<div class="container">
  <h2>Free Dev Kit</h2>
  <form id="formRequest">
  <div class="form-group">
      <label for="Name">Name</label>
      <input type="text" class="form-control" id="Name" placeholder="Enter name" name="Name">
    </div>
    
    <div class="form-group">
      <label for="Email">Email</label>
      <input type="Email" class="form-control" id="Email" placeholder="Enter email" name="Email">
    </div>
    
    <div class="form-group">
      <label for="Contact">Contact Number</label>
      <input type="text" class="form-control" id="Contact" placeholder="Enter contact number" name="Contact">
    </div>
    
    
    
    <button type="button" class="btn btn-default"  name="Submit" id="Submit" onclick="postContactToGoogle()" value="Submit">Submit</button>
    
    
  
    
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











