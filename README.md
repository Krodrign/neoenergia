<h1>Passos para o setup do ambiente local</h1>

<p>Antes de subir o ambiente local é necessário a intalação do Blade CLI</p>
<p>Siga as intruções para instalar o Blade nesse link aqui: <a href="https://help.liferay.com/hc/en-us/articles/360017885232-Installing-Blade-CLI-">Instalação do Blade CLI</a></p>
<p>Feito a instalação do Blade, clone o repositório e navegue até o diretório <b>root</b> do projeto.</p>
<p>Rode os seguintes comandos em sequência:</p>

```blade gw initBundle``` <br>
```blade gw deploy``` <br>

<p>Após realizar esses comandos, vá até o arquivo /bundles/portal-ext.properties e cole o seginte código:</p>

```
jdbc.default.driverClassName=com.mysql.cj.jdbc.Driver
jdbc.default.url=jdbc:mysql://localhost/lportal?useUnicode=true&characterEncoding=UTF-8&useFastDateParsing=false
jdbc.default.username=root
jdbc.default.password=root
```


<p>Volte para o diretório raiz do projeto e rode o seguinte comando:</p>

```docker compose up```

<p>Após rodar o comando, espere o container iniciar e ainda na raiz do projeto rode o comando:</p>

```blade server run```

