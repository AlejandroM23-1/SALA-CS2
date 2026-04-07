## Seccion A
    Ya que tenemos instalado en Docker el OpenClaw, al momento de la instalacion, el tutorial que seguimos, especifico que para que podamos acceder al OpenClaw desde el navegador, deberiamos haber cambiado de 127.0.0.1 a 0.0.0.0, por esta razon si bien es riesgoso que este abierto a quien sea de la red, aun tiene el proceso de validacion que se debe seguir para poder tener acceso a la interfaz de OpenClaw.

## Seccion B
    Al realizar el analisis, la direcion IP que pudimos observar es la 0.0.0.0 que es una señal de riesgo si solo fuera el programa de OpenClaw, pero debido a que estamos usando Docker, esto es algo que si o si tiene que estar para poder acceder por el navegador a OpenClaw.

## Seccion C
    En este caso, de las 5 rutas que probamos 4 se clasifican como auth real, esto es una buena señal de seguridad, pero uno muestra un mensaje de "not found" que es un Falso Positivo, y esto se debe a que es posible que la ruta que usamos no exista debido a una actualizacion de OpenClaw.

## Seccion D
    Al intentar acceder desde mi dispositivo movil, la pagina si cargo, esto es debido a que estamos ejecutando el OpenClaw en Docker y creamos un puente para poder establecer conexion con OpenClaw.

## Seccion E
    En este caso, para una mayor seguridad, limitimos el acceso a OpenClaw solo para la pc y no para otros dispositivos externos, pero al realizar esta configuracion, se siguio otros pasos, no se modifico nada del archivo .json (se quedo con bin: lan) pero si modificamos el YAML agregando la IP al puerto (127.0.0.1:PUERTO:PUERTO) de esta forma se esta negando el acceso a dispositivos externos.

## Seccion F
    Al mantener todo con los permisos minimos, evitamos estar mas expuesstos y de esta forma nuestros datos estaran mas protegidos asi como nuestros dispositivos.