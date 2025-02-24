# Capítulo 9: Engenharia de Software Moderna

O capítulo 9 do livro “Engenharia de Software Moderna”, de Marco Túlio Valente, dedica-se à prática do refactoring – ou seja, à reestruturação do código com o objetivo de melhorar sua legibilidade, modularidade e manutenibilidade sem alterar seu comportamento. O autor coloca essa prática como uma resposta às Leis de Lehman, que afirmam que o software tende a se degradar à medida que sofre manutenções, e reforça que bons hábitos de programação, como os defendidos por Kent Beck, são fundamentais para manter a saúde do sistema.

## 1. Conceito e Importância do Refactoring

### Motivação Histórica e Teórica

O capítulo inicia contextualizando a necessidade de manutenção contínua nos sistemas – seja para corrigir bugs, adaptar o sistema a novas regras ou evoluir sua funcionalidade. Diante do envelhecimento natural do código, conforme descrito pelas Leis de Lehman, o refactoring surge como uma prática essencial para “estabilizar” a qualidade interna, evitando que a complexidade aumente de forma incontrolável.

### Definição

Refactoring é apresentado como um conjunto de transformações no código (como extrair, renomear, mover ou dividir métodos e classes) cujo objetivo é melhorar a estrutura e a clareza do sistema sem modificar sua funcionalidade.

## 2. Catálogo de Refactorings

O autor detalha diversos refactorings extraídos do catálogo de Fowler, apresentando nome, motivação, mecânica e exemplos práticos. Entre os principais estão:

- **Extração de Método:**  
  Separar trechos de código de um método grande para métodos menores, facilitando a reutilização e a compreensão. Em sistemas legados ou funções longas, essa técnica pode ser empregada para quebrar a complexidade – por exemplo, em um método que realiza diversas operações (leitura, processamento e escrita de dados), extraindo cada parte em um método específico.

- **Inline de Método:**  
  Inverter a extração quando um método pequeno, de uso limitado, não agrega valor à legibilidade e pode ser incorporado diretamente em seu ponto de chamada. Em situações em que o método é chamado apenas uma vez e possui poucas linhas, eliminá-lo pode simplificar a leitura do código.

- **Movimentação de Método:**  
  Mover um método para outra classe se ele fizer mais sentido logicamente naquele contexto, aumentando a coesão e diminuindo o acoplamento. Se um método em uma classe A utiliza intensivamente os dados e funcionalidades de uma classe B, movê-lo para B pode organizar melhor a responsabilidade das classes.

- **Extração de Classes:**  
  Quando uma classe possui muitas responsabilidades ou atributos, parte desses elementos pode ser extraída para uma nova classe, promovendo a separação de interesses.  
  *Exemplo:* Em uma classe “Pessoa” que gerencia dados pessoais e informações de contato, criar uma classe “Telefone” pode isolar as responsabilidades e facilitar futuras modificações ou expansões.

- **Renomeação:**  
  Ajustar nomes de métodos, classes e variáveis para refletir melhor sua função, o que é essencial para a comunicação entre os desenvolvedores e para a manutenção do código.

## 3. Prática do Refactoring

- **Testes Automatizados:**  
  O capítulo destaca a importância de uma suíte de testes robusta para garantir que, após cada refatoração, o comportamento do sistema se mantenha inalterado.

- **Suporte das IDEs:**  
  São apresentados os recursos que as IDEs modernas oferecem para automatizar e facilitar o processo de refactoring, contribuindo para reduzir erros humanos e acelerar o desenvolvimento.

## 4. Aplicações Práticas do Conteúdo

- **Manutenção de Sistemas Legados:**  
  Em projetos antigos onde o código se tornou difícil de entender e modificar, técnicas de extração de métodos e classes podem ser empregadas para modularizar e clarificar a lógica, facilitando a inclusão de novas funcionalidades ou a correção de bugs.

- **Desenvolvimento Ágil:**  
  Em ambientes que utilizam metodologias ágeis, onde as mudanças são constantes e as entregas frequentes, o refactoring contínuo ajuda a manter a base de código saudável e adaptável, reduzindo o risco de acumular dívidas técnicas.

- **Integração de Novas Funcionalidades:**  
  Ao integrar novas features em um sistema já existente, aplicar refactorings (como mover métodos para a classe correta ou extrair código duplicado) pode simplificar a evolução do sistema e melhorar a testabilidade, garantindo que a adição da nova funcionalidade não quebre comportamentos já consolidados.

- **Melhoria de Reusabilidade:**  
  Ao identificar trechos de código repetido, os desenvolvedores podem extrair esses trechos para métodos ou classes reutilizáveis, promovendo a consistência e facilitando futuras manutenções.

## Conclusão

Este capítulo enfatiza que o refactoring não é apenas uma atividade pontual, mas uma prática contínua e indispensável para a evolução do software. Ao investir em refatorações regulares, as equipes conseguem manter a qualidade do código, reduzir a complexidade e evitar a deterioração natural dos sistemas, permitindo que estes se adaptem às mudanças sem comprometer a confiabilidade. Dessa forma, os conceitos apresentados podem ser aplicados tanto em projetos novos quanto na modernização de sistemas legados, sempre com o objetivo de criar um software mais sustentável e de fácil manutenção ao longo do tempo.
