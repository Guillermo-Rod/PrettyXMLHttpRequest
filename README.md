# PrettyXMLHttpRequest
Make XMLHttpRequest on a easy way

#Using
-structure
  let args ={type: "POST or GET",url: "--your url--", HTML_form_id: "--if you send data, put your form id her -- or null"};
  
-you can use the api var default
  api = pretty.create(args);
  api.beforeSend(function(){
    //do something before 
  });
  api.send(function(state , request){            
    //do something after 
    //state show a boolean value if ocurred a error while sending 
    //request show the request from you url 
  });  
  
  --you can use a var 
    var http = pretty.create(args);
    http.beforeSend(function(){});
    http.send(function(){});
