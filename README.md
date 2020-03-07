# PrettyXMLHttpRequest

_Make XMLHttpRequest on a easy way !_


## About 🚀

_Pretty XMLHttpRequest is a minified library of javascript that allows to send Post and Get request to any server with a easy way, using pure javascript with a elegant syntax._

You only need call **two functions**


### Download 🔧

_Just download the file.min.js and add it on your html_

```
<script src="./prettyXMLHttpRequest.min.js"></script>
```

### Using ⚙️

_You only need call three functions._
_You can use the api var default if you need just one request._

```
api 
```

_if you will send more than one request create your custom var:_

```
var my_custom_var_api
```

_You must define three params on a object:_ 

* method - must be "POST" or "GET".
* url - must be "https://your-url".
* HTML_form_id - Must be "your_form_id" (NOT document.getElementById('your_form_id')!) or null if you don't need send data.

```
var args = {method: (string), url: (string), HTML_form_id: (string or null) };
```

_You must pass these args to the create function with the pretty var:_

```
api = pretty.create(args)
```


_Before send, this function is optional, if you need do or validate something before send the request:_

```
api.beforeSend(function(){
	
});
```

_This function sends the request and receives two arguments in response from the server:_

* status - this status contains a boolean value it means if the request was done successfully or occurred some error during the sending.
* response - this contains the json that your server responded.

```
api.send(function(status , request){        

});
```



## Completely usage 🔩

```
var args = {method: (string), url: (string), HTML_form_id: (string or null) };
api = pretty.create(args);
api.beforeSend(function(){

});	
api.send(function(status , request){        

});
```  


## Contributions 🖇️

_if you want report any bug or contribute to this javascript library contact us:_
* [Guillermo-Rod@dev.mx](https://gmail.com/)- Developer*



## MMO&Friends 🎁

_See other packages we offer and could be useful:_

* Upload Massive Files - Storage and save on the db at the same time (Laravel package).


## License 📄

The PrettyXMLHttpRequest is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).



---
[Guillermo-Rod](https://github.com/Guillermo-Rod) ❤️💀













