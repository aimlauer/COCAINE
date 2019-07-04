## Fibertel

### Verificar niveles de Downstream y Upstream normales.
Podemos mirarlos visitando [dameunaip](http://dameunaip.com.ar) o [provisioning](http://provisioning.fibertel.com.ar/) ambos redirigen a la misma dirección ip (181.30.128.34).
#### Downstream Power Level
```
-10dBmV a + 10dBmV es aceptable para los módem.   
-7dBmV A + 7dBmV es el rango ideal y es también el rango especificado para módem de telefonía.   
Un técnico de instalación tendría como objetivo, por un valor cercano a al valor 0 dBmV
```
#### Downstream Signal to Noise Ratio (SNR)
```
Este número debe ser al menos mayor de +33 dB. Más alto es mejor.     
Cualquier valor por debajo de 33dB es probable que tenga transferencias lentas, problemas de conexiones, etc.
```
A este valor lo podés mirar cuando desconectás el coaxial y lo reseteás.
#### Upstream Power Level
```
El valor debe estar entre +35 a +49 dBmV
```

## Liberar un CableModem de Fibertel

1. Visitamos el servicio ofrecido por Fibertel [dameunaip](http://dameunaip.com.ar).
2. Para obtener nuestros datos (no te los van a dar) necesitamos ingresar primero con esta cuenta:
```
ID Componente: 258277559     
ID Cliente: 6432880
```
3. En el menú a la izquierda, le damos a Administrar o editando la URL en la barra de direcciónes agregando /auth/Administrar.xhtml, (http://dameunaip.com.ar/CVWebTecnico/auth/Administrar.xhtml).
4. Accedemos a ActivarCM.html (http://dameunaip.com.ar/CVWebTecnico/auth/ActivarCM.xhtml).
En donde aparecerá un mensaje que contiene tu ID de Componente, algo como:
```
El dispositivo que se intenta instalar ya está instalado en el producto 1412544028.
```
5. Accedemos a http://provisioning.fibertel.com.ar/asp/nuevoII_passICC/confirma.asp para
conseguir el número de cliente.
6. Vamos nuevamente a ![dameunaip](http://dameunaip.com.ar) y nos logueamos con los respectivos datos
obtenidos anteriormente.
7. Editamos la URL para acceder directamente a LiberarCM.xhtml (http://dameunaip.com.ar/CVWebTecnico/auth/LiberarCM.xhtml).
Nos saldrá un login en donde usamos los siguientes datos:
```
Usuario: service2  
Clave: service2 
```
Se te va a reiniciar el módem y vas a tener que volver a configurar toda tu WiFi de nuevo, simplemente
desconectado el cable del módem y dandole al botón Reset y accediendo a 192.168.0.1 volvés a poner como
estaba todo.  
### Advertencia
Me pasó que no podía acceder a ninguna página con el led de ONLINE prendido, si es tu caso.
Hace lo siguiente:
1. Acedé a ActivarCM desde acá (http://dameunaip.com.ar/CVWebTecnico/auth/ActivarCM.xhtml).
2. Y volvé a configurar tu WiFi desde ahí, se va a resetear tu módem una vez más.
Quedando así liberado el CM. 
