# PrettyXMLHttpRequest
  
Make XMLHttpRequest on a easy way !

## About PrettyXMLHttpRequest

Pretty XMLHttpRequest is a minified library of javascript that allows to send Post and Get request to any server with a easy way, using pure javascript with a elegant syntax.   
## Using

You only need call three functions.
You can use the api var default if you need just request:

__- api .__

if you will send more than one request create your custom var:

__- var my_cuztom_api .__



## First -- Arguments

You must define three params on a object: 

__- var args = {method: (string), url: (string), HTML_form_id: (string or null)};__

- Method:

must be "POST" or "GET".

- Url:

must be "https://your-url".

- HTML_form_id:

Must be "your_form_id" (__NOT document.getElementById('your_form_id')!__) or null if you don't need send data.

- Pretty create()

You must pass this args to the create function:

__- api = pretty.create(args);__



## Second -- Before send

This function is optional, if you need do or validate something before send the request.

- Before send:

__- api.beforeSend(function(){
<br>
});__



## Third -- Send

This function sends the request and receives two arguments from the response

- Send:

__- api.send(function(status , request){        
<br>
});__

- Status: 

This status contains a boolean value it means if the request was done successfully or occurred some error during the sending.

- Response

This "response" contains the json that your server responded.



## Additional functions

- Push input

<b>IMPORTAN! you must define as null the HTML_form_id argument </b>

This function helps you to push the input by input for construct the data will send on your server.
You can define the javascript element: document.getElementById('your_input_id').

< input type="text" id="token_id" name="token_" value="23Sdsd344"> 


const element = document.getElementById('token_');


## Completely usage


__- api = pretty.create(args);
<br>
api.beforeSend(function(){
<br>
});
<br>
api.send(function(status , request){        
<br>
});__ 
  

## Contributions

if you want report any bug or contribute to this javascript library contact us: 
- **[Guillermo-Rod@dev.mx](https://gmail.com/)**

## MMO&Friends

See other packages we offer and could be useful:

- Upload Massive Files: 

Storage and save on the db at the same time (Laravel package).
- Calculate age: 

Calculate age with date of birth (javascript library).

- Estados de mexico y sus municipios:

Pone en un < select> todos los estados y al cambiar de estado devuelve sus municipios, en otro select, es configurable y facil de usar (javascript library)



## License

The PrettyXMLHttpRequest is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).