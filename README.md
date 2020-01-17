"# evolutionscsas" 



<h3>1 Buscar la ruta de instalación: </h3>
<br>
en windows instalar xmapp y abrir terminal htdocs
en linux colocar carpeta en /var/www/html 
realizar configuraciones necesarias de apache

<h3>2. Clonar Repositorio: </h3>
<br>
**Comando:**
`git clone https://github.com/Desarrollo-zeros/evolutionscsas`




<h3>3. Abrir carpeta contenedora del proyecto, buscar archivo back-end: </h3>
<br>
Abrir CMD o Terminal
<br>
**Comando:**
<br>
`cd Api`  //ir a la carpeta
<br>
`dotnet restore` //para recuperar las dependencias
<br>
**'Para crear la migracion de datos, primero debe ir a la carpeta:
 Infrastructura/Context y dentro de ella buscar `optionsBuilder.UseSqlServer(@"Data Source=142.93.117.217;Initial Catalog=prueba;persist security info=True;user id=sa;password=4015594Wae");`'**
 <br>
Carbiar por los datos del servidor (SQL SERVER)
<br>

`dotnet ef database update` //migrar a la base de datos



<h3>4. Modificar la URL en Api/Program: </h3>
<br>
`webBuilder.UseStartup<Startup>()
                        .UseUrls("http://142.93.117.217:44344");`
<br>

<h3>5. Modificar la URL en Api/Properties/launchSettings.json: </h3>
<br>
```json
{
   "$schema": "http://json.schemastore.org/launchsettings.json",
   "iisSettings": {
     "windowsAuthentication": false,
     "anonymousAuthentication": true,
     "iisExpress": {
       "applicationUrl": "http://142.93.117.217:50988",
       "sslPort": 44344
     }
   },
   "profiles": {
     "IIS Express": {
       "commandName": "IISExpress",
       "launchBrowser": true,
       "launchUrl": "",
       "environmentVariables": {
         "ASPNETCORE_ENVIRONMENT": "Development"
       }
     },
     "Api": {
       "commandName": "Project",
       "launchBrowser": true,
       "launchUrl": "",
       "applicationUrl": "https://142.93.117.217:5001;http://142.93.117.217:5000",
       "environmentVariables": {
         "ASPNETCORE_ENVIRONMENT": "Development"
       }
     }
   }
 }
```
<h3>6. Prender el servidor en la ruta back-end/Api: </h3>
<br>
**Comando:**
`dotnet run`


<h1>Servidor Online</h1>

http://142.93.117.217

Usuarios de prueba:

```json
[

{
  "username" : "zeros",
  "password" : "toor"
},
{
  "username" : "test",
  "password" : "test"
}
]
```
