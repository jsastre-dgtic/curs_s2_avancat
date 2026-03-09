```js
var vpais = PLUGIN_DATOSFORMULARIO.getValorCompuesto('CSELPAIS');
var vcodselpais = vpais.getCodigo();

PLUGIN_LOG.debug("vcodselpais: "); 
PLUGIN_LOG.debug(vcodselpais); 

if (PLUGIN_UTILS.esIgual(vcodselpais, '1')){
    DATOS_VALOR.setValorCompuesto('724','ESPANYA');
} else {
    DATOS_VALOR.resetValor();
}
```
