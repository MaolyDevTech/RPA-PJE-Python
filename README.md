# RPA-PJE-Python

**Caso de Uso: Automação para PJE - Consulta Pública do Brasil**

**Objetivo:**
Automatizar a extração de informações de processos jurídicos eletrônicos (PJE) a partir da Consulta Pública do Brasil, incluindo dados sobre o caso processual, data de distribuição e últimas movimentações, para um associado específico, e salvar essas informações em um arquivo Excel. O projeto visa simplificar e acelerar o processo de coleta de informações legais, economizando tempo e recursos dos associados.

## Procedimento Operacional Padrão (SOP)

### 1. Objetivo do SOP
Automatizar a extração de informações de processos jurídicos eletrônicos.

### 2. Passos do SOP
- **Início**: O associado inicia o sistema automatizado.
- **Acesso ao Site**: O sistema automatizado acessa o site da Consulta Pública do Brasil.
- **Preenchimento dos Campos**: O sistema preenche automaticamente os campos de pesquisa com o número da OAB e seleciona o estado.
- **Clique em "Pesquisar"**: O sistema clica no botão "Pesquisar" automaticamente.
- **Verificação de Pesquisa**: O sistema verifica se a pesquisa foi bem-sucedida. Se não, registra um erro e encerra o processo.
- **Para Cada Processo**:
  - O sistema clica no link do processo.
  - Cria uma nova planilha Excel, se necessário, com as colunas: "Número do Processo", "Data de Distribuição" e "Movimentações".
  - Extrai automaticamente o número do processo e a data de distribuição.
  - Extrai e armazena automaticamente as últimas movimentações.
  - Salva a planilha Excel automaticamente.
  - Conclui o processo de extração e salva as informações no arquivo Excel.
- **Relatório de Conclusão**: O sistema gera um relatório de conclusão.
- **Fim**: Fim do procedimento.

**Ator Principal:**
- Associado (Advogado, Estagiário de Direito, etc.)

**Pré-condições:**
1. O associado possui um dispositivo com acesso à internet.
2. A Consulta Pública do Brasil está disponível e acessível.
3. O sistema automatizado está instalado no dispositivo do associado.
4. O associado forneceu as informações da sua OAB e estado.
5. O associado definiu as configurações de extração, como quais processos específicos deseja consultar.


**Cenário As-Is (Situação Atual):**

- O associado acessa manualmente o site da Consulta Pública do Brasil.
- O associado navega pelo site, preenchendo manualmente os campos de pesquisa com o número da OAB e selecionando o estado.
- Após a pesquisa, o associado clica em cada processo individualmente, coletando as informações de caso, data de distribuição e últimas movimentações.
- O associado cria manualmente uma planilha Excel, insere colunas com títulos apropriados.
- O associado copia e cola os dados de cada processo manualmente na planilha Excel.
- O associado salva a planilha Excel no computador local.

  <img width="5056" alt="As is Diagrama" src="https://github.com/MaolyDevTech/RPA-PJE-Python/assets/144358009/dfa3a4dc-a505-43c2-b847-9909960158da">

  <br><br>


**Cenário To-Be (Situação Desejada):**

- O associado inicia o processo de automação.
- O sistema automatizado acessa o site da Consulta Pública do Brasil.
- O sistema preenche automaticamente os campos de pesquisa com o número da OAB e seleciona o estado.
- O sistema clica no botão "Pesquisar" automaticamente.
- O sistema verifica se a pesquisa foi bem-sucedida.
- Para cada processo listado:
  - O sistema clica no link do processo.
  - O sistema cria uma nova planilha Excel se necessário, com as colunas: "Número do Processo", "Data de Distribuição" e "Movimentações".
  - O sistema extrai automaticamente o número do processo e a data de distribuição.
  - O sistema extrai e armazena automaticamente as últimas movimentações.
  - O sistema salva a planilha Excel automaticamente.
- O sistema conclui o processo de extração e salva as informações no arquivo Excel.
- O sistema gera um relatório de conclusão.

  
**Fluxo Básico:**

1. O associado inicia o sistema automatizado.
2. O sistema automatizado acessa o site da Consulta Pública do Brasil.
3. O sistema preenche automaticamente os campos de pesquisa com o número da OAB e seleciona o estado.
4. O sistema clica no botão "Pesquisar" automaticamente.
5. O sistema verifica se a pesquisa foi bem-sucedida:
   - Se a pesquisa não for bem-sucedida, o sistema registra um erro e encerra o processo.
   - Se a pesquisa for bem-sucedida, o sistema continua para o próximo passo.
6. Para cada processo listado:
   - O sistema clica no link do processo.
   - O sistema cria uma nova planilha Excel se necessário, com as colunas: "Número do Processo", "Data de Distribuição" e "Movimentações".
   - O sistema extrai automaticamente o número do processo e a data de distribuição.
   - O sistema extrai e armazena automaticamente as últimas movimentações.
   - O sistema salva a planilha Excel automaticamente.
7. O sistema conclui o processo de extração e salva as informações no arquivo Excel.
8. O sistema gera um relatório de conclusão.
9. O associado pode revisar o relatório e os dados extraídos.


**Jornada de Usuário:**

1. O associado inicia o programa de automação.
2. O associado fornece suas credenciais de acesso à Consulta Pública do Brasil (se necessário).
3. O associado fornece o número da OAB e seleciona o estado.
4. O associado inicia o processo de extração.
5. O sistema realiza a pesquisa automaticamente.
6. O sistema extrai e armazena os dados dos processos.
7. O associado pode acompanhar o progresso da extração.
8. O sistema conclui a extração e gera um relatório.
9. O associado pode revisar e salvar o arquivo Excel gerado com os dados dos processos.
10. O associado encerra o programa de automação.



**Pós-condições:**
1. O associado possui um arquivo Excel contendo os dados extraídos dos processos jurídicos eletrônicos.
2. O sistema automatizado registra os detalhes da extração e qualquer erro encontrado no processo.

**Exceções:**

1. **Erro na Pesquisa:** Se a pesquisa não for bem-sucedida (por exemplo, devido a problemas de conexão ou indisponibilidade do site da Consulta Pública do Brasil), o sistema deve registrar o erro e notificar o associado.

2. **Erro na Extração de Dados:** Se o sistema encontrar problemas na extração de dados de um processo específico (por exemplo, devido a mudanças na estrutura do site), o sistema deve registrar o erro e continuar com os outros processos, se houver.

3. **Configurações Incompletas:** Se o associado não forneceu as informações necessárias, como número da OAB e estado, o sistema deve notificar o associado e aguardar até que as informações estejam completas antes de iniciar o processo de extração.

4. **Interrupção pelo Associado:** Se o associado interromper manualmente o processo de extração, o sistema deve permitir que o associado decida se deseja salvar os dados coletados até o momento.

![image](https://github.com/MaolyDevTech/RPA-PJE-Python/assets/144358009/7cc3c8cb-898f-4a6f-adb7-92062678e5c3)


   <br> <br>


**Tecnologias Empregadas:**

Linguagem: **Python**


Bibliotecas Utilizadas:

- Selenium: Para automatizar a interação com navegadores da web, com foco no Google Chrome.
- OpenPyXL: Para automatizar a manipulação de planilhas do Excel.

**Passos de Configuração:**

1. Crie um ambiente de desenvolvimento Python:
   ```
   python -m venv processo
   ```

2. Ative o ambiente de desenvolvimento:
   ```
   .\processo\Scripts\activate
   ```

3. Instale as bibliotecas necessárias com o comando:
   ```
   pip install Selenium OpenPyXL
   ```


**Sequência Lógica de Programação:**

1. **Início**
2. Inicie o navegador e acesse o site `https://pje-consulta-publica.tjmg.jus.br/` usando a biblioteca Selenium.
3. Para cada número de OAB e estado:
   - Utilize o Selenium para digitar o número da OAB, selecionar o estado e clicar no botão "Pesquisar".
   - Verifique se a pesquisa foi bem-sucedida:
     - Se a pesquisa não foi bem-sucedida, registre um erro e continue para a próxima iteração.
     - Se a pesquisa foi bem-sucedida, prossiga para o próximo passo.
   - Para cada processo listado:
     - Utilize o Selenium para clicar no link do processo.
     - Verifique se a página de detalhes do processo foi carregada corretamente:
       - Se a página não carregou corretamente, registre um erro e volte à lista de processos.
       - Se a página carregou corretamente, continue para o próximo passo.
     - Verifique se uma planilha Excel já existe:
       - Se a planilha já existir, vá para o próximo passo.
       - Se a planilha não existir, crie uma nova planilha com as colunas: "Número do Processo", "Data de Distribuição" e "Movimentações" usando a biblioteca OpenPyXL.
     - Utilize o Selenium para extrair o número do processo e a data de distribuição.
     - Utilize o Selenium para extrair e armazenar as últimas movimentações.
     - Utilize a biblioteca OpenPyXL para adicionar o número do processo, a data de distribuição e as últimas movimentações à planilha Excel.
     - Salve a planilha Excel.
     - Volte à lista de processos.
   - Volte à página inicial de pesquisa.
4. **Fim**

Com o fim de construir um raciocínio das solicitações da atividade com repeito as atividades a apresentar. A possível ações ou melhorias de projeto que podem ser implementadas rapidamente e com um investimento mínimo de recursos, mas que têm um impacto significativo em relação a negócios, desempenho e viabilidade ao longo do tempo.

## ** "Quick Wins"** 

** "Quick Wins" para o projeto de automação da consulta pública de processos jurídicos eletrônicos (PJE):**

1. **Melhoria na Interface do Usuário (UI)**:
   - Aprimorar a interface do usuário do script de automação para torná-la mais amigável e intuitiva para os associados. Isso reduzirá a necessidade de treinamento e permitirá que os usuários aproveitem ao máximo o sistema. (Melhoria na usabilidade e accessibilidade de produto)

2. **Relatórios de Desempenho e Economia**:
   - Implementar relatórios regulares que mostrem o desempenho do sistema de automação, incluindo o tempo economizado pelos associados e qualquer economia de recursos. Isso permite uma avaliação contínua do ROI(Retorno sobre o Investimento) do projeto. (Aplicação de estratégias BI) 

Essas propostas visariam melhorar a eficiência, a usabilidade e a economia de recursos do projeto, proporcionando benefícios tangíveis de negócios e garantindo que o projeto seja viável ao longo do tempo. Elas podem ser implementadas sem um grande investimento de recursos e fornecerão resultados visíveis rapidamente.

Agora bem, como proposta comercial, estabeleceria a necessidade de implementação, abordando o contexto de solução de problema a atividades repetitivas. Que melhorar a eficiência, a produtividade e reduzirá os custos associados à extração de informações em processos jurídicos eletrônicos.

A automação reduz drasticamente os custos associados ao trabalho manual e ao tempo gasto na extração de informações. A produtividade aumenta, uma vez que a automação realiza tarefas com precisão e eficiência, permitindo que as equipes se concentre em atividades estratégicas e de maior valor.

Quanto ao cálculo de custos pode ser listado e considerados: Desenvolvimento de Software, Hardware, Treinamento, Manutenção e Suporte, Custos Operacionais, Licenças de Software, Tempo de Desenvolvimento e Implementação, Testes e Validação de entre Outros Custos.

Trás uma pesquisa pode chegar ao seguente calculo de totais, que você precisa quantificar cada um desses elementos

**Custo Total = Custo de Desenvolvimento + Custo de Manutenção + Custos de Licenças de Software + Custos de Treinamento + Custos Operacionais - Benefícios Financeiros**

Que podemos envolver em uma caroça de objetiva de rendimentos, expressada na seguente tabela para o maior entendimento. 

**"Tabela de Produtividade, Desempenho, Estabilidade e Tempo vs. Operações Manuais"** 

Que pode ser usada para comparar a eficiência e eficácia da automação RPA em relação às operações manuais. Ela fornece uma visão geral das melhorias que a automação pode trazer em termos de produtividade, desempenho, estabilidade e economia de tempo. Aqui está uma tabela simplificada para ilustrar esse conceito:

| Critério                    | Operações Manuais | Automação RPA |
|-----------------------------|-------------------|--------------|
| **Produtividade**          | Baixa              | Alta         |
| **Desempenho**             | Variável           | Consistente  |
| **Estabilidade**           | Suscetível a erros | Confiável    |
| **Tempo Necessário**       | Alto               | Baixo        |



