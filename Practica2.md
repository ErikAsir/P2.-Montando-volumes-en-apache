1. Para comprobar se teño a imaxe no equipo use o comando docker images


2. Agora vou crear un contenedor chamado asir_httpd. Tamen vou a mapear o porto 8080 da maquina co porto 80 do contenedor que é o porto por defecto onde Apache sirve as páxinas Web. Para todo iso use este comando docker run -dit –name asir -p 8080:80 -v “$PWD”/htdocs:/usr/local/apache2/htdocs/httpd

3. Una vez feito o paso anterior para mostrar o noso html no navegador  solo nos quedaria abrir o html no visual studio, editalo e deberia de verse perfectamente no navegador se ponemos http://localhost:8080

4. Este paso é moi semellante ao paso 2 o uunico que temos que cambiar e o nome e porto. O comando seria: docker run -dit -name asir_web1 -p 8000:80 -y “$PWD”/htdocs:/usr/local/apache2/htdocs/httpd -------  docker run -dit -name asir_web2 -p 8090:80 -y “$PWD”/htdocs:/usr/local/apache2/htdocs/httpd

5. Agora so nos queda crear o html e para iso entramos no contenedor htdocs e o creamos con touch logo nos diriximos a archivos do sistema, entramos no htdocs e abrimos o html co visual studio, o editamos, gardamos e listo, se poñemos no buscador http://localhost:8000 deberia de aparecer a nosa paxiana e o mesmo co porto 8090
