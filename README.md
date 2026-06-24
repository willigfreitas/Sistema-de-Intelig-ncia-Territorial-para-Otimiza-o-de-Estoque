# Sistema de Inteligência Territorial para Otimização de Estoque

Este repositório contém o projeto desenvolvido como parte da disciplina de Modelagem de Banco de Dados. O sistema visa otimizar a distribuição de veículos em uma rede de concessionárias, utilizando inteligência de dados e análise geoespacial para reduzir o tempo de estoque parado e aumentar a rotatividade de vendas.

## 🚀 Tecnologias Utilizadas
- **Banco de Dados:** PostgreSQL 16
- **Geoprocessamento:** PostGIS
- **Visualização e Análise:** QGIS (Layouts de Impressão)
- **Modelagem:** brModelo
- **Linguagem:** SQL (PL/pgSQL para automação)

## 🧠 Destaques Técnicos
- **Análise Espacial:** Utilização de buffers de 80km (via `ST_DWithin`) para delimitar áreas de influência comercial.
- **Automação:** Implementação de funções (`fn_recomendar_loja_veiculo`) e triggers (`trg_recomendar_loja_veiculo`) que recomendam automaticamente a realocação de veículos com base em categoria, público-alvo e preço.
- **Governança:** Estrutura de dados normalizada e otimizada para suporte à decisão estratégica.

## 📁 Estrutura do Repositório
- `/database`: Contém os scripts `.sql` para criação das tabelas, funções e triggers.
- `/maps`: Mapas finais de severidade de estoque e influência territorial (PNG/PDF).
- `/docs`: Relatório completo detalhando a modelagem lógica, requisitos e resultados alcançados.

## 📊 Visualização de Resultados
Os mapas foram gerados no QGIS, integrando dados econômicos do IBGE com as métricas operacionais da rede de concessionárias.



---
*Desenvolvido por: Eliezer, Luiz e William Freitas.*
*Orientação: Profa. Yara | 2026*
