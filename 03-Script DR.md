```js
var parametre = PLUGIN_DOMINIOS.crearParametros();
var v_uo = PLUGIN_DATOSFORMULARIO.getValorCompuesto('C_SEL_DIR3_1');
var codiuo = v_uo.getCodigo();

parametre.addParametro('codiDir3',codiuo);
var d_uof = PLUGIN_DOMINIOS.invocarDominio('CAIB.UO_PBE',parametre);
var res = d_uof.getNumeroFilas();

PLUGIN_LOG.debug('Resultats' + res); 
var cod = '';
var desc = '';
if (res>0){
	for (i=1;i<=res;i++){
		cod = d_uof.getValor(i, 'CODIDIR3');
		desc = d_uof.getValor(i, 'NOM');
        DATOS_VALORESPOSIBLES.addValorPosible(cod, desc);
	}
}
```
