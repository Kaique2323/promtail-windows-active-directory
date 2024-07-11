<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Promtail Windows Active Directory</title>
</head>
<body>
    <h1>Promtail Windows Active Directory</h1>
    <p>Este projeto descreve como criar um serviço Promtail no Windows para ler logs do Active Directory.</p>

    <h2>Passos para Configuração</h2>

    <h3>1. Criar Diretório para o Promtail</h3>
    <p>Crie um diretório para o Promtail. Pode ser em <code>C:\</code> ou, como no exemplo, em <code>C:\Program Files</code>.</p>

    <h3>2. Baixar e Descompactar o Promtail</h3>
    <p>Baixe o Promtail e descompacte-o no diretório criado. Você pode usar o link abaixo:</p>
    <p><a href="https://github.com/grafana/loki/releases/download/v3.1.0/promtail-linux-arm64.zip">Promtail v3.1.0</a></p>

    <h3>3. Configurar o Promtail</h3>
    <p>Crie um arquivo chamado <code>promtail-local-config.yaml</code> e copie o conteúdo do repositório. Lembre-se de alterar o trecho abaixo com a URL do seu servidor Loki:</p>
    <pre>
<code>clients:
  - url: http://seu.loki.com.br:10060/loki/api/v1/push
</code>
    </pre>

    <h3>4. Baixar o WinSW</h3>
    <p>Baixe a versão adequada do WinSW para o seu sistema operacional e coloque-o na mesma pasta do Promtail. Você pode usar o arquivo do repositório ou o link abaixo:</p>
    <p><a href="https://github.com/winsw/winsw/releases">WinSW Releases</a></p>

    <h3>5. Criar Diretório de Logs</h3>
    <p>Crie um diretório chamado <code>logs</code> dentro do diretório do Promtail.</p>

    <h3>6. Criar Arquivo de Serviço do Promtail</h3>
    <p>Crie um arquivo chamado <code>promtail-service.xml</code> e copie o conteúdo do repositório.</p>

    <h3>7. Navegar até o Diretório do Promtail</h3>
    <p>Abra o CMD e navegue até o diretório do Promtail:</p>
    <pre><code>cd C:\Program Files\promtail</code></pre>

    <h3>8. Instalar o Serviço Promtail</h3>
    <p>Instale o serviço Promtail com o comando:</p>
    <pre><code>.\promtail-service.exe install</code></pre>

    <h3>9. Iniciar o Serviço</h3>
    <p>Inicie o serviço Promtail com o comando:</p>
    <pre><code>.\promtail-service.exe start</code></pre>

    <h3>10. Verificar o Status do Serviço</h3>
    <p>Verifique o status do serviço com o comando:</p>
    <pre><code>.\promtail-service.exe status</code></pre>
</body>
</html>
