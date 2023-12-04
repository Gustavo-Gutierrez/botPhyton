Pasos para realizar el proceso
Paso 1:

git clone https://github.com/leifermendez/api-whatsapp-ts

Paso 2:

cd api-whatsapp-ts

Paso 3:

npm install

Paso 4:

npm run build

Paso 5:

npm run dev

Paso 6: Crear un archivo .py con el siguiente codigo y luego ejecutarlo.

import requests
import time 

def sendMessage(para, mensaje):
    url = 'http://localhost:3001/lead'
    
    data = {
        "message": mensaje,
        "phone": para
    }
    headers = {
        'Content-Type':'application/json'
    }
    print(data)
    response = requests.post(url, json=data, headers=headers)
    time.sleep(10)
    return response
    sendMessage('XXXXXXXXX', 'Este es el mensaje')
