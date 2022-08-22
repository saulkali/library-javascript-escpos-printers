# library-javascript-escpos-printers
## como importarlo...
### para poder usar la libreria, es necesario descargar el script o importarlo directo desde mi git con el uso de la etiqueta script de html 
### manera online
> script src="https://github.com/saulkali/library-javascript-escpos-printers/blob/main/escpos.js"
### manera local es necesario descargar la libreria
> script src="escpos.js"

## como usuarlo
### para poder usar el plugin una vez importado podemos crear otro archivo js, donde podremos instanciar y dar uso de los metodos de este plugin.
### traer los nombres de las impresoras detectadas.
```javascript
const obtenerImpresoras = () => {
    var impresora = new PrinterEscPos();
    impresora.getPrinters().then(response =>{
        if(response.status == "OK"){
            response.listPrinter.forEach(namePrinter =>{
                console.log(namePrinter);
            });
        }
    });
};
```

### para imprimir texto, qr, codeBar y imagenes
```javascript
const imprimirTicket = ()=>{
    var impresora = new PrinterEscPos();
    impresora.setText("hola mundo"); // metodo para imprimir texto
    impresora.setQR("123"); // metodo para imprimir codigos QR
    impresora.setBarCode("21","code93"); // metodo para imprimir codigo de barra tiene dos argumentos (codigo, tipo de codigo)
    impresora.setImage("image.png"); // metodo para imprimir imagenes al igual acepta enlaces de imagenes de internet
    impresora.setConfigure(
        font='a',
        bold= true,
        align= "center"
    ); // este metodo solo puede mandar 3 argumentos, para la fuente 'a' o 'b', letras negritas y la aliniacion del texto 'center','right','left'
    impresora.printerIn("lp0"); // una vez configurado el ticket pasamos a mandarlo a la impresora que deseamos imprimir el ticket
};
```

# el uso de este script queda libre, si deseas quitar el marco de agua del plugin puedes contactarme