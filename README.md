<h1> promtail-windows-active-directory </h1>
<p> Criando um serviço promtail no windows, para ler logs do Active Directory </p>


<h3> 1. Criar um diretorio parar o Promtail podendo ser do C:\ ou como no exmplo C:\Program Files. </h3>

<h3> 2. Baixar o Promtail e descompactar podendo usar o link abaixo: </h3>
https://github.com/grafana/loki/releases/download/v3.1.0/promtail-linux-arm64.zip

<h3> 3. Criar um arquivo chamado "promtail-local-config.yaml", copiando o do repositorio aqui. </h3>
Se lembrando de alterar esse trecho:

<p>clients:</p>
 <p> - url: http://seu.loki.com.br:10060/loki/api/v1/push</p>

<h3> 4. Baixar o winsw ideal para o SO e colocar na mesma pasta do Promtail, podendo usar o do repositorio ou pelo link abaixo: </h3>
https://github.com/winsw/winsw/releases

<h3> 5. Criar um diretotio "logs" dentro do diretorio do Promtail </h3>

<h3> 6. Criar um arquivo chamado "promtail-service.xml", podendo usar o mesmo do repositorio </h3>

<h3> 7. Com CMD ir ate o diretorio do promtail </h3>
<code>cd C:\Program Files\promtail</code>

<h3> 8. Instalar o serviço promtail </h3>
<code>.\promtail-service.exe install</code>

<h3> 9. Startar o serviço </h3>
<code>.\promtail-service.exe start</code>

<h3> 10. Verificar o status </h3>
<code> .\promtail-service.exe status </code>







