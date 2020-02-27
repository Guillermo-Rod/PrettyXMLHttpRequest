# PrettyXMLHttpRequest
Make XMLHttpRequest on a easy way
<br />
# Using
-structure 
<br />
  let args ={type: "POST or GET",url: "--your url--", HTML_form_id: "--if you send data, put your form id her -- or null"};
<br />
-you can use the api var default
  api = pretty.create(args);
  <br />
  api.beforeSend(function(){
    //do something before 
  });
  <br />
  api.send(function(state , request){            
    //do something after 
    //state show a boolean value if ocurred a error while sending 
    //request show the request from you url 
  });  
  <br />
  
  --you can use a var 
    <br />
    var http = pretty.create(args);
    <br />
    http.beforeSend(function(){});
    <br />
    http.send(function(){});
