# Medidor de temperatura con RaspberryPi

Sensor de temperatura usando raspberry pi

![] ( implementación1.jpg)

![] ( implementación2.jpg)

//codigo Python

//from time import sleep, strftime, time
//import serial, time
//arduino = serial.Serial('/dev/ttyACM0', 9600)
//while True:
//    cadena = arduino.readline()
//      if(cadena.decode() != ''):
//        cadena = str(cadena.decode())
//        cadena = cadena.split(',')
        luz = int(cadena[0])
        #  humedad = int(cadena[1])
            if luz > 600: # Si hay mucha luz
        #      imprimir = 'Luz: '+str(luz)+' - Humedad: '+str(humedad)
            imprimir = 'Luz: '+str(luz)
            print(imprimir)
            with open("/home/pi/Desktop/registro_LDR.csv","a") as log: #, "a") as log:#"a" es registro continuo
                log.write("{0},{1}\n".format(strftime("%Y-%m-%d %H:%M:%S"),str(imprimir)))
        time.sleep(1)
arduino.close()

