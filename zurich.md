# Zurich
Estan pruebas se realizaron en el software SoapUI

Al realizar la petición con el siguiente mensaje SOAP:
```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:web="http://webservices.zurich.com/">
   <soapenv:Header>
   	<wsse:Security xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">
         <UsernameToken xmlns="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd">
            <Username>pruebasws</Username>
            <Password>pruebasws</Password> 
         </UsernameToken>
     </wsse:Security>
 </soapenv:Header>
   <soapenv:Body>
      <web:reqCatEstadosAutos>
         <web:numRequest>8</web:numRequest>
         <web:catalogo>1</web:catalogo>
         <web:usuario>pruebasws</web:usuario>
         <web:agente>99181</web:agente>
      </web:reqCatEstadosAutos>
   </soapenv:Body>
</soapenv:Envelope>
```
La petición queda en espera y arroja el error de **TimeoutException: Read timed out.**



