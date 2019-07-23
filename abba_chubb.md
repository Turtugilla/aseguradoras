## Ejemplo Cotización Poliza

#### Entrada
```xml
<COT>
  <DG>
    <NEG Descripción="Identificador que ABA|Seguros asigno al negocio" Tipo="Entero" Opcional="No">6323</NEG>
    <AGE Descripción="Identificador del agente asignado por ABA|Seguros" Tipo="Entero" Opcional="No">155555</AGE>
    <CON Descripción="Identificador del conducto asignado por ABA|Seguros" Tipo="Entero" Opcional="No">116</CON>
    <TAR Descripción="Identificador  que ABA|Seguros asigna a la tarifa" Tipo="Entero" Opcional="No">101</TAR>
    <INIVIG Descripción="Fecha inicio de vigencia formato aaaa-mm-dd" Tipo="Fecha" Opcional="No">2013-06-20</INIVIG>
    <FINVIG Descripción="Fecha Fin de vigencia formato aaaa-mm-dd" Tipo="Fecha" Opcional="No">2014-06-20</FINVIG>
    <TS Descripción="Identificador del tipo de suscripción" Tipo="Entero" Opcional="No">1</TS>
    <AGRUPA Descripción="Identificador de la agrupación" Tipo="Entero" Opcional="Si">2076</AGRUPA>
    <TC Descripción="Identificador tipo de calculo" Tipo="Entero" Opcional="No">1</TC>
    <FP Descripción="Identificador de la forma de pago a utilizar en la cotización" Tipo="Entero" Opcional="No">12</FP>
  </DG>
  <INCISOS>
    <INCISO Descripción="">
      <CVEVEH Descripción="CMST o Clave vehicular si se manda el nodo '<ID>' se debe omitir este" Tipo="Texto" Opcional="Si">01080200109</CVEVEH>
      <DESC Descripción="Descripción el vehículo que se mostrara en la póliza" Tipo="Texto" Opcional="Si">Vehículo de pruebas</DESC>
      <MOD Descripción="Año modelo del vehículo" Tipo="Entero" Opcional="No">2013</MOD>
      <CONDICION Descripción="Si el vehiculo es 0 = Nuevo o 1 = Seminuevo" Tipo="Entero" Opcional="Si">0</CONDICION>
      <PAQ Descripción="Identificador asignado al Paquete que se desea cotizar" Tipo="Entero" Opcional="No">1</PAQ>
      <EDO Descripción="Identificador asignado al Estado de circulación del vehículo" Tipo="Entero" Opcional="No">19</EDO>
      <MUN Descripción="Identificador asignado al Municipio de circulación del vehículo" Tipo="Entero" Opcional="No">1037</MUN>
      <SERV Descripción="Identificador del servicio del vehículo" Tipo="Entero" Opcional="No">1</SERV>
      <USO Descripción="Identificador del uso del vehículo" Tipo="Entero" Opcional="No">1</USO>
      <TDED Descripción="Identificador del tipo de Deducible" Tipo="Entero" Opcional="No">1</TDED>
      <TSA Descripción="Identificador del Tipo de Suma Asegurada" Tipo="Entero" Opcional="No">1</TSA>
      <PD Descripción="Porcentaje de Descuento en punto decimal" Tipo="Flotante" Opcional="No">0</PD>
      <PB Descripción="Porcentaje de Bonificación en punto decimal" Tipo="Flotante" Opcional="No">0</PB>
      <COBS Descripción="Agrupador de las coberturas a modificar ó agregar, Si no se agrega se responderá con las coberturas estándar" Opcional="Si">
        <COB>
          <COBID Descripción="Identificador asignado por ABA|Seguros a la cobertura" Tipo="Entero" Opcional="No">1</COBID>
          <SUMAASEG Descripción="Suma Asegurada,cantidad con la ABA|Seguros respalda la cobertura" Tipo="Entero" Opcional="Si">0</SUMAASEG>
          <DADIC Descripción="Texto de la descripción adicional por ejemplo en adaptaciones" Tipo="String" Opcional="Si"></DADIC>
          <DPCT Descripción="Valor del deducible en punto decimal" Tipo="Real" Opcional="Si">0.05</DPCT>
        </COB>
        <!-- . . . -->
        <COB>
          <COBID>116</COBID>
          <SUMAASEG>0</SUMAASEG>
          <DADIC />
          <DPCT>0</DPCT>
        </COB>
      </COBS>
    </INCISO>
  </INCISOS>
</COT>
```

#### Salida
```xml
<COT>
  <COTID Descripción= "Es el Id de la Cotización necesario para la emisión de la póliza">2837025</COTID>
  <VERID Descripción= "Es el Id de la versión necesario para la emisión de la póliza">2834954</VERID>
  <PNETA Descripción="Prima neta de la cotización, Se recomienda no utilizar este dato para mostrar al cliente">14107.324</PNETA>
  <REC Descripción="Es el recargo correspondiente al pago fraccionado de la cotización,Se recomienda no utilizar este dato para mostrar al cliente">0</REC>
  <IVA Descripción="Total a cobrar de Impuesto al Valor Agregado, Se recomienda no utilizar este dato para mostrar al cliente">2321.1718</IVA>
  <PTOTAL Descripción="Costo total de la cotización, Se recomienda no utilizar este dato para mostrar al cliente">16828.4958</PTOTAL>
  <DTO  Descripción="Descuento otorgado a la cotización, Se recomienda no utilizar este dato para mostrar al cliente">0</DTO>
  <INCISOS>
    <INCISO Descripción="En este agrupador se encuentran se indican los datos y costos específicos del inciso de la cotización">
      <ID Descripción="Identificador conocido como vehiculoid asignado por ABA|Seguros al Vehículo">3435</ID>
      <DESC Descripción="">3008 FELINE 1.6 LTS TURBO L4 TUR AUT 4 ABS CA CE PIEL   </DESC>
      <CVEVEH Descripción="Identificador conocido como CMST o Clave vehicular">01300100303</CVEVEH>
      <MOD Descripción="Año modelo del vehículo">2013</MOD>
      <PAQ Descripción="Identificador asignado por ABA|Seguros al paquete solicitado">1</PAQ>
      <EDO Descripción="Identificador asignado por ABA|Seguros al Estado de circulación del vehículo">19</EDO>
      <MUN Descripción="Identificador asignado por ABA|Seguros al Municipio de circulación del vehículo">1037</MUN>
      <SERV Descripción="Identificador del servicio del vehículo">1</SERV>
      <USO Descripción="Identificador del uso del vehículo">1</USO>
      <TDED Descripción="Identificador del tipo de Deducible">1</TDED>
      <TSA Descripción="Identificador del Tipo de Suma Asegurada">1</TSA>
      <COTINCID Descripción= "Es el inciso de la Cotización necesario para la emisión de la póliza">4377385</COTINCID>
      <VERINCID Descripción="Es el versión de la Cotización necesario para la emisión de la póliza">2834954</VERINCID>
      <NUMINC Descripción="Número de inciso de la Cotización">1</NUMINC>
      <DSEG Descripción="Identificador asignado por ABA|Seguros al dispositivo de seguridad del vehículo">0</DSEG>
      <DSEGEST Descripción="Estatus del dispositivo de seguridad.">0</DSEGEST>
      <DER Descripción="Derechos de emisión del inciso">400</DER>
      <MDESID Descripción="Identificador del motivo del descuento">0</MDESID>
      <PD Descripción="Porcentaje de Descuento">0</PD>
      <DES Descripción="Monto del Descuento">0</DES>
      <PB Descripción="Porcentaje de Bonificación en punto decimal">0</PB>
      <BON Descripción="Monto de la Bonificación">0</BON>
      <REC Descripción="Monto del recargo">0</REC>
      <PREC Descripción="Porcentaje de recargo">0</PREC>
      <PNETA Descripción="Prima neta del inciso de la Cotización">14107.324</PNETA>
      <IVA Descripción="Total a cobrar de Impuesto al Valor Agregado del inciso de la Cotización">2321.1718</IVA>
      <PTOTAL Descripción="Costo total del inciso de la Cotización">16828.4958</PTOTAL>
      <COBINTEROP Descripción="Indica se usan los de wsAbaseguros en lugar de los de wsAutoNet">0</COBINTEROP>
      <RECIBOS Descripción="Simulación de recibos, en ocaciones se ajustaran durante la emision, esta simulación no muestra recibos correctos para las cotizaciones  multianuales">
        <RECIBO> 
          <NUM Descripción="Numero de recibo">1</NUM>
          <INIVIG Descripción="Fecha del inicio de vigencia del recibo">2013-06-20</INIVIG>
          <FINVIG Descripción="Fecha del fin de vigencia del recibo">2014-06-20</FINVIG>
          <LIMPAG Descripción="Fecha limite para el pago del recibo">2013-07-20</LIMPAG>
          <DER Descripción="Derechos a pagar en el recibo">400</DER>
          <REC Descripción="Recargos a pagar en el recibo"0</REC>
          <IVAPCT Descripción="Porcentaje de IVA a pagar en el recibo">0.16</IVAPCT>
          <IVA Descripción="IVA a pagar en el recibo">2321.1712</IVA>
          <PNETA Descripción="Prima neta a pagar en el recibo">14107.32</PNETA>
          <PTOTAL Descripción="Prima total a pagar en el recibo">16828.4912</PTOTAL>
          <END Descripción="Numero de endoso (siempre vendrá con valor cero)">0</END>
        </RECIBO>
      </RECIBOS>
      <COBS Descripción="">
        <COB>
          <COBID Descripción="identificador de la cobertura">84</COBID>
          <DESC Descripción="Nombre de la cobertura">AUTO RELEVO</DESC>
          <SEL Descripción="Indica si la cobertura esta incluida en la cotización">0</SEL>
          <SUMAASEG Descripción="Suma Asegurada, es la cantidad con la ABA|Seguros respalda la cobertura">7</SUMAASEG>
          <SADESC Descripción="Texto descriptivo de la suma asegurada">7</SADESC>
          <DPCT Descripción="Valor del deducible en punto decimal">0</DPCT>
          <DEDESC Descripción="Texto descriptivo del deducible">NO APLICA</DEDESC>
          <PNETA Descripción="Prima neta de la cobertura">0</PNETA>
          <IVA Descripción="Total a cobrar de Impuesto al Valor Agregado para la cobertura">0</IVA>
          <PTOTAL Descripción="Costo total de la cobertura">0</PTOTAL>
          <RECMTO Descripción="Es el recargo correspondiente al pago fraccionado de la cobertura">0</RECMTO>
          <DER Descripción="Derechos de emisión de la cobertura">0</DER>
          <DTOMTO Descripción="Monto del descuento en la cobertura">0</DTOMTO>
          <BONMTO Descripción="Monto de la Bonificación en la cobertura">0</BONMTO>
        </COB>
        <!-- . . . -->
        <COB>
          <COBID>471</COBID>
          <DESC>CEROCIBLE PT</DESC>
          <SEL>0</SEL>
          <SUMAASEG>359900</SUMAASEG>
          <SADESC>AMPARADA</SADESC>
          <DPCT>0.05</DPCT>
          <DEDESC>NO APLICA</DEDESC>
          <PNETA>0</PNETA>
          <IVA>0</IVA>
          <PTOTAL>0</PTOTAL>
          <RECMTO>0</RECMTO>
          <DER>0</DER>
          <DTOMTO>0</DTOMTO>
          <BONMTO>0</BONMTO>
        </COB>
      </COBS>
    </INCISO>
  </INCISOS>
</COT>
```
