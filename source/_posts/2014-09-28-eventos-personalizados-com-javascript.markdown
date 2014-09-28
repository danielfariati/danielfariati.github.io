---
layout: post
title: "Criando eventos personalizados com javascript"
date: 2014-09-28 14:00:00 -0300
comments: true
categories: desenvolvimento javascript jquery
---

O javascript possui eventos que podemos observar e disparar ações quando forem executados, por exemplo:
```
onclick, onkeypress, onkeyup, onmouseover...
```

Porém, também é possível criar os seus próprios eventos, inclusive enviando dados por eles.

<!-- more -->

Para criar seus eventos, basta fazer o seguinte:

``` javascript
var meuElemento = document.getElementById('elemento');
var meuEvento = new CustomEvent("nomeDoMeuEvento", {
	detail: {
		id: 1
	}
});
meuElemento.dispatchEvent(meuEvento);
```

Para escutar o evento, basta fazer o processo que faria com qualquer outro evento:

``` javascript
var meuElemento = document.getElementById('elemento');
meuElemento.addEventListener("nomeDoMeuEvento", function(e) {
	console.info("Evento disparado: ", e);
	console.info("Dados do evento: ", e.detail);
});
```

--

Fazer esse processo com jQuery também é muito simples.
Para criar o evento, basta fazer:

``` javascript
var meuElemento = $('#elemento');
meuElemento.trigger('nomeDoMeuEvento', [{
	id: 1
}]);
```

E para escutá-lo:
``` javascript
var meuElemento = $('#elemento');
meuElemento.on('nomeDoMeuEvento', function(e, data) {
	console.info("Evento disparado: ", e);
	console.info("Dados do evento: ", data);
});
```

----

Espero que tenham gostado! Por favor, deixe um comentário com seu feedback.

