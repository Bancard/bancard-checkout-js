# bancard-checkout-js
Esta librearía de referencia desarrollada por Bancard permite recolectar la información sensible de una tarjeta de un cliente permitiendo realizar un pago en un sitio del comercio sin salir del mismo. Integra la operacin de `single_buy` de vpos

<b>Precondición</b>

<i>Como condición para utilizar esta librearía y poder integrar el servicio de vPOS el comercio debe estar registrado y habilitado por Bancard contando con un acceso en el portal de comercios así como acceso al servicio de vPOS.</i>

<b>Pasos para realizar la integración</b>

1. Incluir `bancard-checkout.js`
2. Iniciar contenedor en evento de onload


## Incluir bancard-checkout.js
Para utilizar la librearía de bancard-checkout se debe incluir la misma y setear la clave asociada a tu comercio. 

```javascript
<script src="bancard-checkout.js"></script>
```

## Iniciar contenedor en evento de onload y estilos
Es necesario que en el momento de cargar la página (onload) se invoque a la función `createCheckoutForm` indicando el id del contenedor, clave pública y estilos asociados al elemento embebido.

<b>Ejemplo de invocación </b>
   
```javascript
   window.onload = function() {
      BancardCheckout.createForm('iframe-container', '[PROCESS_ID]', styles);
   };
```

### Modificar estilos 
Puede modificarse la información de estilos del contenedor con atributros ya definidos. La lista completa es:

```
  - name: input-background-color
    text: Color fondo de campos
    type: color
    default: '#FFFFFF'
  - name: input-text-color
    text: Color texto de campos
    type: color
    default: '#555555'
  - name: input-border-color
    text: Color borde de campos
    type: color
    default: '#CCCCCC'
  - name: button-background-color
    text: Color fondo del botón
    type: color
    default: '#5CB85C'
  - name: button-text-color
    text: Color texto del botón
    type: color
    default: '#FFFFFF'
  - name: button-border-color
    text: Color borde del botón
    type: color
    default: '#4CAE4C'
  - name: form-background-color
    text: Color fondo de formulario
    type: color
    default: '#FFFFFF'
  - name: form-border-color
    text: Color del borde del formulario
    type: color
    default: '#DDDDDD'
  - name: header-background-color
    text: Color fondo de encabezado
    type: color
    default: '#F5F5F5'
  - name: header-text-color
    text: Color texto de encabezado
    type: color
    default: '#333333'
  - name: hr-border-color
    text: Color de linea separadora
    type: color
    default: '#EEEEEE'
  - name: header-show
    text: Mostrar encabezado
    type: boolean
    default: true
  - name: watermark-show
    text: Mostrar marca de agua
    type: boolean
    default: true
```

Ejemplo:

```javascript
      styles = {
        'input-background-color' : '#453454',
        'input-text-color': '#B22222',
        'input-border-color' : '#CCCCCC',
        'input-placeholder-color' : '#999999',
        'button-background-color' : '#5CB85C',
        'button-text-color' : '#FFFFFF',
        'button-border-color' : '#4CAE4C',
        'form-background-color' : '#999999',
        'form-border-color' : '#DDDDDD',
        'header-background-color' : '#F5F5F5',
        'header-text-color' : '#333333',
        'hr-border-color' : '#B22222',
        'label-kyc-text-color' : '#555555',
        'header-show' : false,
        'watermark-show' : false
      }
```
