# Documentação do Processo de ETL e Desenvolvimento do Relatório DRE no Power BI

## 1. Introdução
Este documento descreve o processo de ETL dos dados usados na construção do relatório DRE no Power BI. Inclui os desafios encontrados, soluções implementadas e a estrutura final para as análises.

---

## 2. Processamento ETL

### 2.1 Problemas Encontrados
1. **Duplicatas no Banco:**
   - Foram encontrados registros duplicados na tabela de fatos (**fato_dre_final**) com os mesmos valores e IDs.
   - **Solução:** Removi as duplicatas no processo de transformação no Colab.

2. **Inconsistências nos Valores:**
   - Diferenças entre os totais calculados na planilha original e no banco.
   - **Solução:** Recalculei os valores no Colab, ajustando filtros e somas.

3. **Formato de Datas (MesRef):**
   - Datas estavam em formato de 'milissegundos'.
   - **Solução:** Padronizei o formato para "dd/MM/yyyy".

4. **Relacionamentos e Chaves Estrangeiras:**
   - Falta de tabelas dimensionais bem definidas para estrutura e unidades.
   - **Solução:** Criei tabelas dimensionais (**dim_estrutura** e **dim_unidade**) e ajustei os relacionamentos no Power BI.

---

## 3. Desenvolvimento do Relatório no Power BI

### 3.1 Medidas DAX Criadas:
1. **ReceitaBruta** - Soma total dos valores financeiros.
2. **ReceitaLiquida** - Receita Bruta menos deduções.
3. **DespesasTotais** - Soma dos valores negativos relacionados a despesas.

### 3.2 Análises Criadas:
- **Análise Vertical (%GT):** Percentual em relação à receita bruta.
- **Análise Horizontal (Variação Mensal):** Comparação de desempenho mês a mês.
- **Gráficos Complementares:** Receita por unidade e tipo de unidade.

---

## 4. Resultados Finais
O relatório final apresenta:
1. **DRE Hierárquico:** Organizado por grupo de contas, destacando receitas, despesas e resultados operacionais.
2. **Análises de Receitas:**
   - Por tipo de unidade (atacado, varejo e escritório).
   - Por unidade específica.
3. **Filtros Dinâmicos:** Mês e tipo de unidade para segmentação rápida.

---

## 5. Conclusão
O processo permitiu criar um relatório para análise de desempenho financeiro. Apesar dos desafios enfrentados com duplicatas, formatos de data e inconsistências nos valores, as soluções garantiram a integridade dos dados.

Esse projeto demonstra a importância de um processo ETL bem estruturado e a criação de modelos de dados para análises financeiras.

---

# ETL Process and DRE Report Development Documentation in Power BI

## 1. Introduction
This document describes the ETL process used to build the DRE (Income Statement) report in Power BI. It includes the challenges faced, solutions implemented, and the final structure for analysis.

---

## 2. ETL Processing

### 2.1 Problems Encountered
1. **Duplicates in the Database:**
   - Duplicate records were found in the fact table (**fato_dre_final**) with identical values and IDs.
   - **Solution:** Removed duplicates during the transformation process in Colab.

2. **Value Inconsistencies:**
   - Differences between totals calculated in the original spreadsheet and the database.
   - **Solution:** Recalculated values in Colab, adjusting filters and sums.

3. **Date Format (MesRef):**
   - Dates were in 'milliseconds' format.
   - **Solution:** Standardized the format to "dd/MM/yyyy".

4. **Relationships and Foreign Keys:**
   - Lack of well-defined dimensional tables for structure and units.
   - **Solution:** Created dimensional tables (**dim_estrutura** and **dim_unidade**) and adjusted relationships in Power BI.

---

## 3. Report Development in Power BI

### 3.1 DAX Measures Created:
1. **ReceitaBruta** - Total sum of financial values.
2. **ReceitaLiquida** - Gross revenue minus deductions.
3. **DespesasTotais** - Sum of negative values related to expenses.

### 3.2 Analyses Created:
- **Vertical Analysis (%GT):** Percentage relative to gross revenue.
- **Horizontal Analysis (Monthly Variation):** Month-to-month performance comparison.
- **Complementary Charts:** Revenue by unit and unit type.

---

## 4. Final Results
The final report presents:
1. **Hierarchical DRE:** Organized by account group, highlighting revenues, expenses, and operating results.
2. **Revenue Analyses:**
   - By unit type (wholesale, retail, and office).
   - By specific unit.
3. **Dynamic Filters:** Month and unit type for quick segmentation.

---

## 5. Conclusion
The process allowed the creation of a report for financial performance analysis. Despite challenges with duplicates, date formats, and value inconsistencies, the solutions ensured data integrity.

This project demonstrates the importance of a well-structured ETL process and data modeling for financial analyses.

