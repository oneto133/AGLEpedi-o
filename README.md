# Introdução

Durante o desenvolvimento de soluções para otimizar a gestão de estoque na [AGL Brasil](https://www.aglbrasil.com/), foi indentificado uma série de requisitos que são essenciais para garantir a eficiência e a precisão do processo, questões como gerenciamento de perdas, enderaçamento correto, gestão de espaço estão no topo do assunto a ser debatido. Vamos nessa!

### Requisitos:

A iniciar pelos requisitos, temos alguns requisitos base para começarmos tendo uma noção de algumas necessidades da Expedição da [AGL Brasil](https://www.aglbrasil.com/) hoje.

* **Rastreabilidade em tempo real:** A capacidade de acompanhar a localização e o status de cada item em estoque, desde a entrada até a saída, é fundamental para evitar perdas e otimizar a reposição.
  
* **Integração com o sistema *[Piloto](https://performancei.com.br/):*** A sincronização entre o sistema de gestão de estoque e o sistema Piloto é crucial para garantir que o estoque esteja sempre atualizado e evitar rupturas.
  
* **Geração de relatórios personalizados:** A capacidade de gerar relatórios detalhados sobre o desempenho do estoque, como giro de estoque, nível de serviço e obsolescência, é essencial para a tomada de decisões estratégicas.
  
* **Alertas automáticos:** A implementação de um sistema de alertas para notificar sobre níveis de estoque baixos, endereços disponíveis e outras situações críticas é fundamental para evitar problemas operacionais.
  
* **Equipamentos**: A necessidade de equipamentos como coletores de dados para realizar o inventário tem se mostrado fundamental desde o recebimento até a separação, que é quando o produto passa a deixar de ser estoque e passa a estar em meio que uma situação flutuante.
  
* **Inteligência Artificial:** Explorar a possibilidade de utilizar soluções de inteligência artificial para otimizar a previsão de demanda e a gestão de reposição realizando um balanço do que brevemente sairá o do que possivelmente ocupará aquele espaço, como consequência, otimizando custos de espaço de armazenamento, pois, cada produto em cada espaço no qual está alocado, querendo ou não é um custo para a empresa.

### Impacto dos requisitos:

**A implementação desses requisitos trará diversos benefícios para a AGL Brasil, como:**

* **Redução de custos:** Otimização da gestão de estoque, diminuição de perdas por obsolescência e redução de custos com armazenagem.
  
* **Melhora na qualidade do atendimento ao cliente:** Maior disponibilidade de produtos, redução do tempo de entrega e aumento da satisfação do cliente.
  
* **Aumento da eficiência operacional:** Automação de processos, redução de erros manuais e otimização da utilização de recursos.
  
* **Tomada de decisões mais assertivas:** Disponibilidade de dados precisos e atualizados para a tomada de decisões estratégicas.

**Faseamento:**
Claro, o sistema que se é descrito nesse artigo não deve ser levado como uma exigência ou algo urgente que em um estalar de dedos deverá aparecer instantâneamente, a necessidade de se documentar algo como esse, surgiu ao percerber que ideias e funcionários engajados a AGL tem, porém eles estão acanhados, assim fica apenas como uma crítica que logo se desaparece e após não terá importância para ninguém mais, nem mesmo para o elaborador. Os requisitos aqui apresentados foram totalmente desenvolvidos por funcionários que buscam um melhor ambiente de trabalho e um certeza de que amanhã teremos algo melhor para todos. Sendo assim, o que se pretende com isso é implementar o sistema de forma gradual, iniciando pelos módulos mais críticos e expandindo para os demais à medida que os resultados forem sendo obtidos.

## O que iniciamos?

De primeiro momento, para se minimizar a dificuldade de localização precisa de produtos, foi elaborada uma planilha no excel para que se fizesse esse controle de forma automatizada, porém alguns limites foram encontrados, como:

* Dificuldade de dados atualizados em tempo real, já que a rotatividade de produtos do estoque é altíssima, exigindo um sistema que acompanhe as mudanças em tempo real, garantindo  precisão das informações.

* Conforme requistos são concluídos, requistos vão surgindo, uma última funcionalidade implementada foi a implementação de um módulo de picking, auxiliando os profissionais responsáveis pela separação de pedidos e diminuindo considerávelmente a quantidade de tempo para a localização de produtos, a dificuldade para localização de pedidos se dá ao tentar de primeiro momento gerir um espaço sem muito planejamento, pois como ainda não se tem um levantamento do espaço disponível real, o mesmo não se pode ser aproveitado de forma eficaz, assim tendo que fazer a alocação de produtos de forma manual. Um exemplo de alocação de forma manual é quando se sabe que determinado produto não tem previsão de chagda nos próximos dias, então seu espaço é usado para alocar determinado produto que não tem espaço reservado de início, em consequência disso a volatilidade de endereçamento acaba sendo inevitável, causando assim atraso e imprecisão na separação de pedidos.

* Acessibilidade da planilha, os principais dispositivos usados nos processos de separação e inventário de estoque são feitas através de tablets, ao acessar a planilha disponibilizada de forma online algumas funcionalidades se tornam incompatíveis e não muito funcionais para o usuário, como atraso nas repostas ao requisitar dados a base, mesmo que interna, além de não ser muito usual e intuitivo, o que prejudica a adaptação e ergonomia cognitiva do usuário.

* Criação de um layout para entender como estão localizadas ruas e espaços para alocação de produtos já está sendo criado, como citado acima, são ideias e essas ideias precisam ser documentadas, pois só assim se consegue manter o bom entendimento do que se é preciso para realizar melhorias.

* Ao endereçar os produtos na base de dados, foi feito uma salva de dados com o que já se é requisitado no mercado, `Ruas`, `Módulos`, `Nível`, `Vão/Apartamento` garantindo assim uma flexibilidade a uma possível integração a outros sistemas.

