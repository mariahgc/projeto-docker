# Projeto Docker - Sistemas Operacionais

## 1. Qual a diferença entre imagem e container?

Imagem é um modelo pronto contendo sistema, bibliotecas e aplicação.
Container é uma instância em execução dessa imagem.

## 2. Qual processo está executando dentro do container?

O processo Node.js executando o arquivo server.js.

## 3. O container possui kernel próprio? Justifique.

Não. Containers compartilham o kernel do sistema operacional hospedeiro.

## 4. Qual recurso foi limitado na sua infraestrutura?

A memória RAM foi limitada para 128 MB.

## 5. Qual a finalidade do volume Docker utilizado?

Persistir os dados do banco MySQL mesmo após reiniciar ou remover containers.

## 6. Qual a finalidade da rede Docker criada?

Permitir comunicação isolada entre a aplicação Node.js e o banco MySQL.

## 7. Por que executar aplicações como usuário não-root?

Para aumentar a segurança e reduzir impactos em caso de invasão.

## 8. Por que Docker não é uma máquina virtual?

Porque Docker compartilha o kernel do host e virtualiza apenas processos, enquanto máquinas virtuais possuem sistema operacional completo.

## 9. O que representa o PID exibido na rota /info?

É o identificador do processo principal em execução dentro do container.

## 10. Cite três conceitos de Sistemas Operacionais presentes neste projeto.

- Processos
- Gerenciamento de memória
- Redes