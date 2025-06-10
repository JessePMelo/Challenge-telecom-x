# TelecomX Churn Analysis - Oracle Next Education Challenge

Este projeto faz parte do desafio de Data Science do programa Oracle Next Education (ONE) - Turma G8. O objetivo é analisar a evasão de clientes (churn) em uma empresa de serviços de internet (fictícia - TelecomX), identificar padrões de cancelamento e propor soluções estratégicas baseadas em dados.

## 📂 Sobre o Dataset
- Fonte: [GitHub Dataset JSON](https://raw.githubusercontent.com/ingridcristh/challenge2-data-science/refs/heads/main/TelecomX_Data.json)
- Total de registros: **7.267 clientes**
- Estrutura original com colunas aninhadas (dicionários)
- Variável-alvo: **Churn (Cancelou)**

## ⚙️ Etapas do Projeto

### 1. Extração e Limpeza
- Leitura do arquivo JSON direto da web
- Normalização das colunas aninhadas (customer, phone, internet, account)
- Tradução das variáveis e padronização de nomenclatura
- Conversão de dados não numéricos para formato adequado

### 2. Enriquecimento dos Dados
- Criação da coluna `Contas_Diarias` (mensalidade / dias do mês)
- Conversão de `Cancelou` para binário: `Cancelou_Num`
- Criação da coluna `Qtd_Servicos` com base na soma de serviços contratados

### 3. Análise Exploratória
- Gráficos:
  - Pizza: proporção de cancelamento
  - Barras: Gênero, Tipo de Contrato, Método de Pagamento, Dependentes
  - Boxplot: Mensalidade x Cancelamento
- Análise estatística com `.describe()`
- Segmentação de clientes que cancelaram

### 4. Correlações Numéricas
- `Contas_Diarias` x `Cancelou_Num` → correlação fraca positiva (~0.19)
- `Qtd_Servicos` x `Cancelou_Num` → correlação fraca negativa (~-0.07)

## 📈 Principais Insights
- 26% dos clientes cancelaram o serviço.
- Clientes com **contrato mensal** têm maior propensão à evasão.
- **Débito automático** é o método de pagamento com maior cancelamento.
- Clientes **sem dependentes** cancelam mais.
- Clientes com **mensalidades mais altas** cancelam com mais frequência.
- Menor quantidade de serviços está levemente relacionada à maior evasão.

## 📆 Recomendações Estratégicas

1. **Reavaliar contratos mensais** com incentivos para migração.
2. **Monitorar cobranças altas** com ações proativas e bonificações.
3. **Criar planos individuais** para clientes sem dependentes.
4. **Rever canais de pagamento**, especialmente débito automático.
5. **Implementar modelo preditivo de churn** com campanhas direcionadas.
6. **Incentivar contratação de múltiplos serviços** com pacotes e fidelização.

## 📊 Ferramentas Utilizadas
- **Python**
- **Pandas**
- **Seaborn / Matplotlib**
- **Google Colab**

## 📅 Autor
Jessé Pereira de Melo  
Projeto desenvolvido como parte do desafio Oracle Next Education - Data Science

---

> "Decisões baseadas em dados são melhores que opiniões baseadas em sorte."
