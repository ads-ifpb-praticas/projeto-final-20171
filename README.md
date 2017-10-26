# Avaliação final de Práticas de Programação

Esse repositório contém a descrição do projeto para avaliação final de práticas de programação do semestre **2017.1**.

## Descrição

O objetivo desta avaliação é construir uma aplicação para gerenciar encomendas de uma confeitaria.

- O cadastro da encomenda deve ter:
    + Título
    + Descrição
    + Prazo para entrega

Considerando que os pedidos demoram o mesmo tempo para serem preparados, a aplicação deve ter, além da tela de cadastro **E** edição das encomendas, uma tela para visualizar todas as encomendas, ordenando pela quantidade de dias restantes.

Desse modo, as encomendas que estãos com prazos mais próximos de expirar devem estar no topo da lista e marcados com um uma cor diferente:

- Caso o prazo restante seja de menos de 2 dias mostrar uma indicação em vermelho
- Caso seja entre 3 e 5, uma indicação em cor amarela.
- O restante, uma indicação em cor verde.

## Requisitos

As seguintes ferramentas e tecnologias devem ser utilizadas.

- **Git**. A aplicação deve estar hospedada na *organization* da disciplina. Deve ser criada uma tag chamada `vFINAL` até o prazo final da entrega. Caso não exista tag, será considerado que você **desistiu** do projeto.
- **Maven**. Deve conter dois `profiles`: um para desenvolvimento e outro para `testes`, onde neste estarão contidos os seguintes plugins:
    + Cobertura
    + PMD
    + Checkstyle
- **JSF**. Toda a aplicação deve ser feita com JSF.
- **CDI**. Qualquer dependência criada sem o uso de CDI acarretará em perda total deste quesito.

Além disso, a aplicação deve ter um cobertura de testes mínima de **80%**. Caso seja menor, acarretará em perda total desse quesito.

A aplicação não deve depender de bancos de dados externos e nem de servidores de aplicação ou containers que precisem ser instalados de maneira externa. Utilize bancos de dados embarcados e o container web Tomcat 7 embarcado. Exemplos disso não faltam até mesmo na organização da nossa disciplina.

No momento da avaliação serão executados os seguintes comandos **na raiz do seu repositório**:

- `mvn test`
- `mvn checkstyle:checkstyle`
- `mvn pmd:pmd`
- `mvn checkstyle:check pmd:check`
- `mvn tomcat7:run`

O último comando deve deixar a aplicação executando sem nenhum problema. Caso haja algum problema, a nota será **0**

A entrega do projeto final deve ser realizado até dia 26/10/2017 às 23h59m59s via **Github**. Qualquer alteração feita após esse horário será desconsiderada