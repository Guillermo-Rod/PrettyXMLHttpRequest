# PrettyXMLHttpRequest

_Make XMLHttpRequest on a easy way !_


## About 🚀

_Pretty XMLHttpRequest is a minified library of javascript that allows to send Post and Get request to any server with a easy way, using pure javascript with a elegant syntax._

You only need call **two functions**

_**Stable version v1.0.0**_ 


### Download 🔧

_Just download the file.min.js and add it on your html_

```
<script src="./prettyXMLHttpRequest.min.js"></script>
```


### Using ⚙️

_You can use the `api` var default if you need just one request._

```
api 
```

_if you will send more than one request create your `var custom`:_

```
var my_custom_var_api1
var my_custom_var_api2
```

_You must define three params on a `object`:_ 

* method - must be "POST" or "GET".
* url - must be "https://your-url".
* HTML_form_id - Must be "your_form_id" (*NOT document.getElementById('your_form_id')!*) or if you don't need send data put null.

```
var args = {method: (string), url: (string), HTML_form_id: (string or null) };
```

_You must pass these args to the create function with the `object pretty`:_

```
api = pretty.create(args)
```


_Before send, this function is optional, if you need do or validate something before send the request:_

```
api.beforeSend(function(){
	
});
```

_This function sends the request and receives two arguments in response from the server:_

* `status` - this status contains a boolean value it means if the request was done successfully or occurred some error during the sending.
* `response` - this contains the `json` that your server responded.

```
api.send(function(status , request){        

});
```


## Completely usage 🔩

```
<h1>Creation form</h1>

<form id="creation_form_id">
	<label>User name</label>
	<input type="text" name="user_name" value="Guillermo Rodriguez">		
	<input type="text" name="mail" value="Guillermo-Rod@dev.mx">		
	<input type="button" value="Subir documentos" onclick="send('POST','./create-user','creation_form_id')">
</form>

<button onclick="send('GET','./fetch-users', null)">Fetch users</button>


<script src="./prettyXMLHttpRequest.min.js"></script>
<script>

	function send(arg_method, arg_url, arg_form_id){

		var args = {method: arg_method, url: arg_url, HTML_form_id: arg_form_id };
		api = pretty.create(args);
		api.beforeSend(function(){
			alert('Sending data...');
		});	
		api.send(function(status , request){        		
			console.log(request);
		});
	}
</script>
```  


## Additional functions 🔧

_if you need send a `POST` method request without a `form` you can use `null` and `.pushInput()` function, for make a one per one the `inputs` that you need._ 

_Or if you just need add additional inputs in yout `form` , you can use the `.pushInput()` function too! :_

```

var array_names    = ['user_name', 'user_id'];			
var array_values   = ['Guillermo', 1];
var array_elements = [document.getElementById('_'),document.getElementById('_')];

var args = {method: "POST", url: "./my-url", HTML_form_id: null};
or
var args = {method: "POST", url: "./my-url", HTML_form_id: 'my_form_id'};

api = pretty.create(args);
api.pushInput("user_id",1);		
api.pushInput(1,0);		
api.pushInput(array_names,array_values);			
api.pushInput(array_elements);	
api.pushInput(document.getElementsByName('_token')[0]); //laravel token ?		
```

_if you need send a `GET` method request for search, you can use `null` and `.pushUrlParam()` function:_

```
<h1>Searching form</h1>

<form>
	<label>User name</label>
	<input type="text" name="search" value="Guillermo Rodriguez" id="input_search_user">			
	<input type="button" value="Subir documentos" onclick="send('GET','./search-user',null)">
</form>

<script src="./prettyXMLHttpRequest.min.js"></script>
<script>
	var array_names    = ['user_name', 'user_id'];			
	var array_values   = ['Guillermo', 1];
	var array_elements = [document.getElementById('_'),document.getElementById('_')];	

	function send(arg_method, arg_url, arg_form_id){

		var args = {method: arg_method, url: arg_url, HTML_form_id: arg_form_id };
		
		api = pretty.create(args);
		api.pushUrlParam("mail","mail@mail.com");		
		api.pushUrlParam(1,2020);		
		api.pushUrlParam(array_names,array_values);		
		api.pushUrlParam(document.getElementById('input_search_user'));				
		api.pushUrlParam(array_elements);			
		api.beforeSend(function(){
			//example: ./search-user?search=Guillermo%Rodriguez etc..

			alert('Sending data...');
		});	
		api.send(function(status , request){        		
			console.log(request); 
		});
	}
</script>
```  


## Contributions 🖇️

_if you want report any bug or contribute to this javascript library contact us:_
* [guillermo.rodriguez.dev@gmail.com](https://gmail.com/)- Developer*


## MMO&Friends 🎁

_See other packages we offer and could be useful:_


## License 📄

The PrettyXMLHttpRequest is open-source software licensed under the [GPL-3.0 Licence](https://opensource.org/licenses/GPL-3.0).



---
✒️ [Guillermo-Rod](https://github.com/Guillermo-Rod) ❤️💀













