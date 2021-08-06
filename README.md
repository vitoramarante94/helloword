# Painéis EBSERH

## Acessos necessários para o desenvolvimento dos painéis:

- Conta Office 365
- TFS (Pasta de Painéis)
- Acesso a conta de paineis@ebserh.gov.br

## Fontes de dados:
- Excel: Em caso de arquivos .xls e .xlsx as fontes de dados precisam ser armazenadas no OneDrive da conta paineis@ebserh.gov.br e seguir a nomenclatura padrão dos projetos (área-projeto).
- SQL: Em consultas SQL os scripts devem ser comentados e armazenados na pasta “Source” do TFS (a estrutura de pastas de projetos será explicada no tópico a seguir).
 
## TFS:
- Nome da pasta do projeto deve ser padronizado (sigla do sistema ou área, hífen e o nome do painel, exemplo: aghu-acessos).
- Dentro da pasta do projeto deve conter outras duas pastas: Data (contém as fontes de dados ou scripts) e Source (com o código fonte ou arquivo pbix).
- As notas de release devem explicar devidamente as alterações realizadas, as medidas criadas, os filtros adicionados e visuais removidos ou adicionados.
 
## ETL/Power Query:
- Coerência na modelagem dos dados entre fatos e dimensões, evitando redundância de dados.
- Cardinalidade dos relacionamentos devem estar corretas, de forma que não haja ambiguidade no modelo.
- As tabelas devem seguir padrões na nomenclatura (Ex.: dimHospital e fatCirurgias).
- Quando necessário deve-se criar a tabela Calendário.
- Os dados devem estar devidamente formatados (texto, decimal, inteiro etc.).
 
#Fórmulas e Medidas (DAX):
- Para melhor organização das medidas, recomenda-se a criação de uma tabela para medidas.
- As medidas devem ser feitas de forma explícita, evitando utilizar o recurso de cálculo que o Power BI disponibiliza, exemplo: “Soma de NomeDaColuna” ou “Contagem de NomeDaColuna”.
- As medidas devem ser criadas com o nome em maiúsculo.
 
## Filtros:
- Deve-se evitar filtros de visual e de páginas e optar sempre que possível por filtros explícitos.
- Filtros de visuais devem ser explicitados nas medidas, por exemplo, criar medida com um filtro com a data específica.
- Os visuais devem filtrar corretamente os demais dentro da mesma página.
 
## Layout:
- Para uma padronização de layout foi definido como modelo a ser seguido o painel “vigilância-covid19”.
- O layout do “vigilância-covid19” contém uma página com apontamentos para facilitar a navegação do painel, porém não é uma página obrigatória, pois em painéis com poucas páginas não se faz necessário.
- A segunda página do painel é o padrão a ser utilizado para a disponibilização dos dados, onde possui uma barra superior com o nome do painel seguido dos filtros e a logo ao final, uma barra à esquerda do painel com os cards com as informações macro do painel seguidos da data e hora da última atualização (dinâmica) e a fonte de dados e no centro do painel vem os demais gráficos.
Observação: Outros pontos a serem observados são as cores dos e tamanhos da barra e logo.
 
## Publicação do Painel
- Alterar o caminho da fonte de dados para os dados publicados no OneDrive da conta paineis@ebserh.gov.br
- Alternar credencial de acesso às fontes de dados para a conta paineis@ebserh.gov.br
- Conferir no Power BI online se o relatório subiu para o workspace correto (Homologação e Produção)
 
## Atualização de Dados
- Verificar se o painel está programado para atualizar conforme solicitado pela área requisitante.
- Conferir se o e-mail ssdid@ebserh.gov.br está entre os e-mails cadastrados, para receber os alertas sobre possíveis falhas na atualização do painel.
 
## Segurança
- Painéis com dados sigilosos devem ser compartilhados com as pessoas específicas conforme definido nos requisitos.
- Em caso de dados públicos, os painéis podem ser compartilhados através do link público.


