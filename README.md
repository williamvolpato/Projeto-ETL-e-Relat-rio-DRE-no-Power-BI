# Projeto: Relatório DRE no Power BI

## Descrição
Este repositório documenta o processo de extração, transformação e carga (ETL) dos dados utilizados para construir um relatório DRE (Demonstração do Resultado do Exercício) no Power BI. O projeto aborda os desafios encontrados, as soluções aplicadas e os resultados obtidos.

---

## Estrutura do Repositório
```
|
|-- dre_tratado_final/               # Banco de dados SQLite tratado
|   |-- dre_tratado_final.db         # Arquivo final após limpeza e ajustes
|
|-- Tratamento_e_Validação/         # Processamento no Colab
|   |-- Notebook_Colab.ipynb         # Código de ETL com validações e correções
|
|-- Vena Dashboard/                 # Arquivo Power BI
|   |-- Vena_Dashboard.pbix         # Relatório final com medidas DAX e visualizações
|
|-- Documentação.md                  # Detalhes do processo e soluções aplicadas
|-- README.md                        # Visão geral do projeto
```

---

## Contexto do Desafio
Foi solicitado o desenvolvimento de um relatório DRE no Power BI, partindo de arquivos brutos com problemas no processo de ETL. O desafio incluía corrigir discrepâncias nos valores finais do Resultado Gerencial do Período e validar a consistência dos dados para garantir uma análise confiável.

---

## Solução Implementada
1. **ETL no Colab:**
   - Removi registros duplicados no banco de dados.
   - Corrigi inconsistências nos valores e formatos de data.
   - Padronizei as tabelas dimensionais (unidades e estrutura).
   - Validei os cálculos comparando com as planilhas originais.

2. **Banco Tratado:**
   - Exportei o banco ajustado para um arquivo SQLite.

3. **Relatório no Power BI:**
   - Desenvolvi medidas DAX para Receita Bruta.
   - Criei análises verticais e horizontais para monitorar variações.
   - Adicionei filtros dinâmicos por mês e tipo de unidade.

---

## Resultados
O processo resultou em um relatório DRE funcional, detalhado e com valores consistentes após a correção dos problemas de ETL. 

O repositório inclui todos os arquivos necessários para reproduzir o processo e continuar evoluindo as análises.

---

## Como Reproduzir
1. **Banco de Dados:**
   - Abra o arquivo SQLite usando o Power BI ou qualquer ferramenta compatível.

2. **Colab:**
   - Execute o notebook para verificar ou ajustar os processos ETL.

3. **Power BI:**
   - Carregue o arquivo .pbix no Power BI Desktop para editar ou visualizar o relatório.

---

## Autor
William Volpato

