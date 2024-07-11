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

5. Criar um diretotio "logs" dentro do diretorio do Promtail

6. Criar um arquivo chamado "promtail-service.xml", podendo usar o mesmo do repositorio

7. Com CMD ir ate o diretorio do promtail
# cd C:\Program Files\promtail

8. Instalar o serviço promtail
# .\promtail-service.exe install

9. Startar o serviço
# .\promtail-service.exe start

10. Verificar o status
<code> .\promtail-service.exe status </code>







