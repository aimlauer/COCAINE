## Fibertel

Significado de cada LED.     
| LED           | Color         |   Descripción                                                                                                                                            |
| ------------- | ------------- | -----------------                                                                                                                                        |
| Power         | Green         | Successfully connected or router at 10/100 Mbps.                                                                                                         |
| Ethnet        | Green/Blue    | Modem is scanning for a downstream channel. A solid LED means the downstream connection is established from the cable network/Internet.                  |
| DS            | Blinks Green  | Modem is ranging, trying to establish an upstream connection. A solid LED means the downstream connection is established to the cable network/Internet.  |
| US            | Blinks Green  | Modem is ranging, trying to establish an upstream connection. |
| US & DS       | Blinking G/B  |  Indicates a modem firmware upgrade in progress. This should last 3-5 minutes. |
| Ready         | Green         | Modem successfully registered with the ISP network                                                                                                        |



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
A este valor lo podés mirar cuando desconectás el coaxil y lo reseteás.
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
5. Ahora vamos a http://provisioning.fibertel.com.ar/asp/nuevoII_passICC/confirma.asp para
conseguir el número de cliente.
6. Desconectate de esa cuenta.
7. Vamos nuevamente a [dameunaip](http://dameunaip.com.ar) y nos logueamos con los respectivos datos
obtenidos anteriormente.
8. Editamos la URL para acceder directamente a LiberarCM.xhtml (http://dameunaip.com.ar/CVWebTecnico/auth/LiberarCM.xhtml).
Nos saldrá un login en donde usamos los siguientes datos:
```
Usuario: service2  
Clave: service2 
```
9. Se te va a reiniciar el módem y vas a tener que volver a configurar toda tu WiFi de nuevo si es que estás conectado por WiFi, si usás cable seguí las instrucciones de abajo para terminar de configurarlo,
podés restablecer los datos de tu WiFi simplemente desconectado el cable coaxil del módem, dándole al Reset y accediendo a 192.168.0.1 volvés a poner como
estaba todo.  
10. Estando en este paso me pasó que no podía acceder a ninguna página con el led de ONLINE prendido pero si tenía acceso a [dameunaip](http://dameunaip.com.ar) y en Administrar.xhtml el **EstadoCM** estaba como _Pendiente_, si es tu caso, hace lo siguiente:    
Estando logueado con tus datos en [dameunaip](http://dameunaip.com.ar) entrá a ActivarCM desde acá (http://dameunaip.com.ar/CVWebTecnico/auth/ActivarCM.xhtml) dale a "Continuar".
11. Y volvé a configurar tu WiFi desde ahí, se va a resetear tu módem una vez más.
Deberías tener acceso a internet a partir de este momento, quedando el *EstadoCM* como Habilitado.

Ahora deberías tenerlo liberado.

#### OBSERVACIONES
A veces pasa que el login te dice que es incorrecto pero sólo tenés que volverlo a intentar no es que
te banearon o algo por el estilo, el sistema de logeo funciona mal.

> https://www.taringa.net/+ciencia_educacion/como-liberar-un-cablemodem-de-fibertel_1diuzo
