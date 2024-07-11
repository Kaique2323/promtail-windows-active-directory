# promtail-windows-active-directory
Criando um serviço promtail no windows, para ler logs do Active Directory


1. Criar um diretorio parar o Promtail podendo ser do C:\ ou como no exmplo C:\Program Files.

2. Baixar o Promtail e descompactar podendo usar o link abaixo:
https://github.com/grafana/loki/releases/download/v3.1.0/promtail-linux-arm64.zip

3. Criar um arquivo chamado "promtail-local-config.yaml", copiando o do repositorio aqui.
Se lembrando de alterar esse trecho:

clients:
  - url: http://seu.loki.com.br:10060/loki/api/v1/push

4. Baixar o winsw ideal para o SO e colocar na mesma pasta do Promtail, podendo usar o do repositorio ou pelo link abaixo:
https://github.com/winsw/winsw/releases

<h2> 5. Criar um diretotio "logs" dentro do diretorio do Promtail </h2>

<h2> 6. Criar um arquivo chamado "promtail-service.xml", podendo usar o mesmo do repositorio </h2>

<h2> 7. Com CMD ir ate o diretorio do promtail </h2>
<code>cd C:\Program Files\promtail</code>

<h2> 8. Instalar o serviço promtail </h2>
<code>.\promtail-service.exe install</code>

<h2> 9. Startar o serviço </h2>
<code>.\promtail-service.exe start</code>

<h2> 10. Verificar o status </h2>
<code> .\promtail-service.exe status </code>







