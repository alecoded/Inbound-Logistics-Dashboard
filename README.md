**Inbound Logistics Dashboard - Business Case Study**

**Sobre o Projeto**

Este projeto consiste em um dashboard de Business Intelligence desenvolvido para analisar a performance da cadeia de suprimentos (Inbound). O objetivo é fornecer visibilidade sobre os prazos de entrega, custos logísticos e eficiência dos fornecedores, permitindo decisões baseadas em dados para otimizar a operação de entrada de mercadorias.

**Tecnologias Utilizadas**

**Power BI Desktop:** Construção do dashboard e visualizações.

**Power Query (Linguagem M):** Processamento, limpeza e transformação de dados (ETL).

**DAX: Criação de medidas calculadas e indicadores de performance (KPIs).**

**Tratamento de Dados & Governança (Data Quality)**
Um diferencial deste projeto foi a identificação e tratamento de inconsistências no banco de dados original.

**Identificação de Erros:** Detectamos registros onde a data de entrega (Delivered) era anterior à data estimada (ETA) ou até mesmo à data de conclusão da produção.

**Solução Implementada (Linguagem M):** No Power Query, foi criada uma coluna de "Flag de Qualidade" para classificar cada pedido como:

✅ Válido: Fluxo cronológico correto.

⚠️ Inconsistente: Registros com datas retroativas ou erros sistêmicos.

**Proteção de KPIs:** As fórmulas de Lead Time foram ajustadas via DAX para considerar apenas dados "Válidos", evitando que datas erradas distorcessem a média real de entrega.

**Análise de Fluxo de Doca:** Foi analisada a relação entre Delivered (chegada física) e ENTRY (entrada sistêmica), permitindo identificar o tempo médio de processamento no armazém.

**Indicadores Principais (KPIs)**
O dashboard apresenta visões críticas para a gestão de Supply Chain:

**Lead Time Médio:** Tempo total desde a produção até a entrega final.

**Distribuição por Modal:** Comparação de volume e custos entre frete Marítimo (SEA) e Aéreo (AIR).

**Performance de Fornecedores:** Volume e custos por origem (ex: China e Portugal).

**Acompanhamento de Prazos:** Comparação entre datas reais e DEADLINE (OTIF).


**Visualização do Painel** - Primeira Página

<img width="1476" height="815" alt="image" src="https://github.com/user-attachments/assets/28cf3147-557e-4991-9b1c-a207196bcd03" />


**Visualização do Painel** - Segunda Página 


<img width="1483" height="835" alt="image" src="https://github.com/user-attachments/assets/c94ca234-b3f7-4aba-95f0-55f3ee961338" />


**Conclusão**
Este case demonstra a importância da etapa de Data Cleaning. Ao isolar as inconsistências de datas, o dashboard tornou-se uma ferramenta de auditoria, capaz de apontar falhas no registro de dados do ERP, além de fornecer métricas logísticas precisas para a diretoria.
