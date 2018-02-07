# bancard-checkout-js
Esta librearía de referencia desarrollada por Bancard permite recolectar la información sensible de una tarjeta de un cliente permitiendo realizar un pago en un sitio del comercio sin salir del mismo. Integra la operacin de `single_buy` de vpos

<b>Precondición</b>

<i>Como condición para utilizar esta librearía y poder integrar el servicio de vPOS el comercio debe estar registrado y habilitado por Bancard contando con un acceso en el portal de comercios así como acceso al servicio de vPOS.</i>

<b>Pasos para realizar la integración</b>

1. Incluir `bancard-checkout.js`
2. Setear clave pública en el evento de onload


## Incluir bancard-checkout.js
Para utilizar la librearía de bancard-checkout se debe incluir la misma y setear la clave asociada a tu comercio. 

```javascript
<script src="bancard-checkout.js"></script>
```

## Setear clave pública en el evento de onload
Es necesario que en el momento de cargar la página se invoque a la funcin `createCheckoutForm` indicando el id del contenedor, clave pública y estilos asociados al elemento embebido.

```javascript
   window.onload = function() {
      BancardCheckout.createCheckoutForm('iframe-container', '[PUBLIC_KEY]', styles);
   };
```
