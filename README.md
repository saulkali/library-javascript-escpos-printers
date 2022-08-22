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
'''javascript
const imprimirTicket = () => {
    var impresora = new PrinterEscPos();
};

'''