# Servidor base de datos postgres

Nuestra imagen se construye en base a la image sumistrada por <b>postgres</b>.<br/>
Comando para la creacion de nuestra propia imagen:
<ul type="disk">
<li><b>docker build -t postgres_db .</b></li>
</ul>

Ademas tenemos disponible una(1) variable de entorno (<b>POSTGRES_PASSWORD</b>) con el fin de crear un password a nuestro servidor de base de datos<br/>

<ul type="disk">
<li>Variable de entorno (<b>POSTGRES_PASSWORD</b>): de no enviar esta bandera -e con su respectiva asignación de variable este tomará por defecto(123456789) para la contraseña de nuestro servidor de base de datos</li>
</ul>

Ejemplo del comando: 

<ul type="disk">
<li><b>docker run -d --name postgres_db -e POSTGRES_PASSWORD=123456 postgres_db</b></li>
</ul>

Si desea conocer la ip que tiene asignado nuestro contenedor puede ejecutar el siguiente comando:

<ul type="disk">
<li>docker inspect --format='{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' $i <b>name_container/id_container</b></li>
</ul>
