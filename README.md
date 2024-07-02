# Product Manager Application

## Introdução

Este projeto é uma extensão do [Product Manager Application original](https://github.com/Paloma-Regis-Ferreira/product-manager-exercicio-1.git). Ele continua a utilizar a arquitetura limpa para garantir um código modular, de fácil manutenção e escalável. As principais adições incluem a implementação de testes unitários utilizando o padrão Builder para criação de produtos e a configuração de GitHub Actions para automação de testes e verificação de cobertura de código.

## Alterações Realizadas

### Testes Unitários com Padrão Builder

Foram adicionados testes unitários para garantir a robustez e a confiabilidade da aplicação. O padrão Builder foi utilizado para facilitar a criação de objetos `Product` em diferentes cenários de teste. Isso proporciona uma estrutura clara e flexível para validar o comportamento da aplicação em diversas situações.

### Integração com GitHub Actions

Um fluxo de trabalho do GitHub Actions foi configurado para automatizar o processo de teste e verificação de cobertura de código. Esse fluxo de trabalho é acionado em cada push para o repositório e em pull requests para a branch `master`, garantindo que novas alterações sejam validadas antes de serem mescladas.

#### Passos do GitHub Actions

- **Configuração do Ambiente**: Configuração do ambiente de execução utilizando JDK 22.
- **Compilação e Testes**: Compilação do projeto e execução dos testes unitários.
- **Relatório de Cobertura com JaCoCo**: Geração de relatório de cobertura de código utilizando JaCoCo.
- **Verificação de Cobertura**: Verificação se a cobertura de código é superior a 80%. Caso contrário, o processo de build falha.
- **Arquivamento de Relatórios**: Arquivamento dos relatórios de teste e cobertura para referência.

### Relatório de Testes com JaCoCo

Além dos testes unitários, é possível gerar e visualizar um relatório detalhado de cobertura de código utilizando JaCoCo. Após executar os testes, o relatório fica disponível em HTML e pode ser acessado localmente para verificar a cobertura de código alcançada.

## Como Rodar os Testes

Para rodar os testes localmente, certifique-se de ter o seguinte instalado:

- Java 22
- Gradle 7.5 ou superior

Clone o repositório e execute os seguintes comandos na raiz do projeto:

```bash
./gradlew test
