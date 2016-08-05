Modal com validação click
===================

<img src="https://avatars0.githubusercontent.com/u/70142?v=3&s=400"  />

Web site
----------

### <a href="http://getbootstrap.com.br/javascript/#modals">Modal Jquery</a>

CDNS Necessarias
----------
``` html
<script src="https://code.jquery.com/jquery.min.js"></script>

<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" rel="stylesheet" type="text/css" />

<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>

``` 

Estrutura do form simples
-------------

``` html
<form action="">
  <input type="text"  placeholder="nome">
  <input type="email" placeholder="email">
  <textarea name="" id="" cols="30" rows="10" placeholder="mensagem"></textarea>
  <input type="submit" class="btn" value="enviar">
</form>

<!--por padrão modal no final da página-->
<div class="modal fade" id="modalChamada" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
        <h4 class="modal-title" id="myModalLabel">Proposta recebida!</h4>
      </div>
      <div class="modal-body">
        Obrigado por entrar em contato, em breve retornaremos.
      </div>
      <div class="modal-footer">
      
        <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>-->
      </div>
    </div>
  </div>
</div>

```

``` JavaScript
//Modal para callback de envio

/*
  task: http://dominio.com.br/?enviado
*/


  var modalFuncionar = function () {
    var url = window.location;
    var strURL = new String(url);
    var enviado = (strURL.search("enviado"));
    if (enviado > 0) {
        $('#modalChamada').modal('show');
    }
};




$( ".btn" ).click(function() {
  //ativação o modal
   $('#modalChamada').modal('show');
});



modalFuncionar();
```


Extra estilizando o formulário
----------

``` Css
body {
  font-family: 'Raleway', sans-serif;
  background: #039BE5;
}

h1 {
  font-weight: 600;
  text-align: center; 
  color: #fff;
}

form {
  width: 320px;
  height: auto;
  display: block;
  margin: 100px auto;
  position: relative;
  
}

input, textarea {
  width: 100%;
  max-width: 300px;
  margin-bottom: 8px;
  padding: 10px;
  display: block;
  height: 30px;
  border: 1px solid #2196F3;  
}


.btn {
  width: 80px;
  position: absolute;
  border: 1px solid #2196F3;
  right: 20px;
  height: 30px;
  font-weight: bold;
  background: #fff;
  color: #333;
  text-transform: uppercase;

  trasition: ease-out 256ms;
  
}

textarea {
  height: 150px;
}


.btn:hover {
  transition: ease-out 500ms;
  background: #3f51b5;
  color: #fff;
  cursor: pointer;
}

.user {
  position: relative;
}

.email {
  position: relative;
}


.position-icon-email {
   position: absolute;
   right: 15px;
   top: 20px;
}

.position-icon-user {
   position: absolute;
   right: 15px;
   top: 20px;
}


```


Ver Demo
----------

[Click aqui!](http://daniloagostinho.github.io/modal-click)
