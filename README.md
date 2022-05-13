///Aplicacion mediante microservicios K8S Wordpress////
1.Paso Crear el archivo de configmap.yaml como se indica en el archivo llamado app-configmap.yaml.
1.2 Procedemos a crear el confingmap mediante el comando kubectl create -f app-configmap.yaml
1.3 Procedemos a utilziar el comando kubectl get configmap, asi podemos corroborar que el archivo se creo correctamente.
2.Creamos ahora un archivo secret como lo indica el archivo app-secret.yaml.
2.1 Utilizaremos el comando kubectl create -f app-secret.yaml
3.Ahora creamores el deploy de backend como lo indica el archivo be-deployment.yaml
3.1 Con el commando kubectl create -f be-deployment.yaml
3.2 Con el comando kubectl get deployment, podemos corrobar que el archivo de back end se creo correctamente.
3.3 Crearemos el volumen para el back end.
3.4 con el comando kubectl create -f be-persistentvolumeclaim.yaml. procedemos a crear el volumen del deployment del back end.
3.5 Luego procedemos a crear el servicio como lo indica el archivo be-service.yaml.
3.6 Con el comando kubectl create -f be-service.yaml
3.7 COn el comando kubectl get service corroboramos que el archivo se haya creado correctamente.
4.Ahora creamores el deploy del front end como lo indica el archivo fe-deployment.yaml
4.1 Con el commando kubectl create -f fe-deployment.yaml
4.2 Con el comando kubectl get deployment, podemos corrobar que el archivo de back end se creo correctamente.
4.3 Crearemos el volumen para el front end.
4.4 con el comando kubectl create -f fe-persistentvolumeclaim.yaml. procedemos a crear el volumen del deployment del back end.
4.5 Luego procedemos a crear el servicio como lo indica el archivo fe-service.yaml.
4.6 Con el comando kubectl create -f fe-service.yaml
4.7 Con el comando kubectl get service corroboramos que el archivo se haya creado correctamente.
5.Una vez creado los comandos correcamente procederemos a corroborar si nuestra aplicacion esta corriendo en nuestro propio host. 
5.1 kubectl get all.
5.2 Observamos como todo se creo correctamente.
5.3 Con  el comando kubectl get service. Podemos obtrener la direccion de nuestro puerto en el archivo llamado 
5.4 utilizando la direccion
5.5 localhost:Direcion que indique.
5.6 localhost:32045.
5.7 Una vez ingresado deberia de poder ingresar a la app de Wordpress
6 Con los comandos kubectl apply -f nombre del archivo podemos crear un update de cualquier archivo.
6.1 con el comando kubectl roll out -f nombre del archivo podemos crear un rollback del archivo modificado.
