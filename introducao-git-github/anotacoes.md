# Comandos básicos

## git init

Inicia o git naquele diretório, iniciando assim o processo de versionamento.

## git add

Adiciona algo para a área de staged, esperando o commit. 

## git status

Verifica o estado dos arquivos naquele repositório, indicando coisas novas, se algo precisa ser adicionado a área de staged ou se já está pronto para o commit.

## git commit -m

Esse vai fazer o commit, ou seja, como se fosse uma gravação do que foi adicionado ou aterado até aquele momento. Usamos o paramêtro -m para adicionar uma mensagem explicando aquele commit.

## git remote add   

Ele vai adicionar o caminho para o nosso repositório no github, é comum ele ser feito da seguinte maneira: **git remote add origin *link do repositório*.**

## git remote -v

Vai exibir os caminhos adicionandos para o repositório, assim podemos verificar se estão corretos.

## git push

Vai enviar nossos arquivos que foram comitados ao github, utilizamos assim: **git push origin *nome da branch*.**

## git pull

Esse comando ao invés de enviar vai baixar o que está no github para a nossa máquina, ele é utilizado quando o repositório no github possui arquivos que não estão em nossa máquina. Usamos assim: **git pull origin *nome da branch*.**

# Configurar chave SSH

Para configurar uma confiança entre a máquina e o servidor do github, uma chave SSH é utilizada. Para fazer isso devemos seguir os procedimentos:

- Primeiro passo: Criar o par de chaves SSH na máquina, para isso usamos o comando: `ssh-keygen -t ed25519 -C < email usado no github >`. Após isso perguntará em que local será salvo e também solicitará a criação de uma senha.

- Segundo passo: Após a criação das chaves, devemos adicionar o conteudo da chave pública no área de SSH no github.

- Terceiro passo: No terminal vamos iniciar o agente que irá monitorar o uso de nossa chave, para isso usamos o comando: `eval $(ssh-agent -s)`. E por último informamos qual chave ele deve monitorar: `ssh-add < id-chave privada >`.

Pronto, agora é só testar e ver se funciona corretamente.