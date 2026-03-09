var usuari = PLUGIN_SESIONTRAMITACION.getUsuario();
var nif = usuari.getNif();

DATOS_VALORESINICIALES.setValor('CNIF', usuari.getNif());
DATOS_VALORESINICIALES.setValor('CNOM', usuari.getNombre());
DATOS_VALORESINICIALES.setValor('CLLIN1', usuari.getApellido1());
DATOS_VALORESINICIALES.setValor('CLLIN2', usuari.getApellido2());
DATOS_VALORESINICIALES.setValor('CEMAIL', usuari.getEmail());
