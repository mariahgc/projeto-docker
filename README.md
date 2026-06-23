# Projeto Docker - Relatório

## 1. Qual a diferença entre imagem e container?

A imagem é como um modelo pronto da aplicação, onde já vem tudo configurado (sistema, dependências e código).
Já o container é quando essa imagem está realmente rodando, ou seja, é a aplicação em execução de forma isolada no sistema.

## 2. Qual processo está executando dentro do container?

Dentro do container está rodando o processo principal da aplicação Node.js. Esse processo é o responsável por manter o servidor ativo e responder às requisições HTTP. Ele normalmente aparece como o processo principal (PID 1 dentro do container).

## 3. O container possui kernel próprio? Justifique.

Não. O container não tem kernel próprio. Ele usa o kernel do próprio sistema operacional do host (Linux).
Por isso ele é mais leve que uma máquina virtual, já que não precisa iniciar um sistema inteiro.

## 4. Qual recurso foi limitado na sua infraestrutura?

Foi definido um limite de memória RAM de 128 MB para o container.. Isso faz parte do controle de recursos do Docker, evitando que a aplicação consuma mais memória do que o permitido.

## 5. Qual a finalidade do volume Docker utilizado?

O volume foi utilizado para salvar os dados do banco MySQL. Assim, mesmo que o container seja removido ou reiniciado, os dados continuam salvos no volume e não são perdidos.

## 6. Qual a finalidade da rede Docker criada?

Foi criada para permitir a comunicação entre os containers (Node.js e MySQL). Ela garante que os serviços consigam se enxergar de forma isolada e segura sem depender diretamente da rede externa.

## 7. Por que executar aplicações como usuário não-root?

Aumenta a segurança da aplicação, limita permissões dentro do container evitando que caso ocorra falha ou ataque a aplicação tenha acesso total ao sistema.

## 8. Por que Docker não é uma máquina virtual?

Porque o Docker não virtualiza um sistema operacional completo. Ele compartilha o kernel do host e só isola processos, e uma máquina virtual cria um sistema operacional inteiro, com kernel próprio o que torna mais pesado.

## 9. O que representa o PID exibido na rota /info?

É o identificador do processo principal ele indica qual processo está ativo e sendo executado naquele momento.

## 10. Cite três conceitos de Sistemas Operacionais presentes neste projeto.

Segurança, gerenciamento de memória e redes.