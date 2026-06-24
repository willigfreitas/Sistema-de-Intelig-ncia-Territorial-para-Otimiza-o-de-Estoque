# 🚗 Sistema de Inteligência Territorial para Otimização de Estoque

![Mapa de Influência Territorial](./maps/mapa_estoque.png)

## 📌 Sobre o Projeto

Este projeto apresenta uma solução de Inteligência Territorial aplicada à gestão de estoque de veículos em uma rede de concessionárias.

O objetivo é utilizar dados operacionais, informações socioeconômicas e análise espacial para identificar oportunidades de realocação de veículos entre unidades, reduzindo tempo de estoque parado e aumentando a eficiência comercial.

A solução integra **Banco de Dados Geográfico, SQL avançado e análise espacial**, transformando dados em recomendações estratégicas para tomada de decisão.

---

# 🎯 Problema de Negócio

Veículos parados em estoque representam capital imobilizado e perda de oportunidade comercial.

O sistema busca responder:

- Qual concessionária possui maior potencial para determinado veículo?
- Existe demanda regional compatível com o perfil do veículo?
- A distância entre lojas e clientes influencia a decisão de realocação?

---

# 🏗️ Arquitetura da Solução

Fluxo geral:

Dados Operacionais  
⬇️  
PostgreSQL + PostGIS  
⬇️  
Regras de Inteligência Territorial (PL/pgSQL)  
⬇️  
QGIS para análise e visualização  
⬇️  
Recomendação estratégica de alocação


---

# 🚀 Tecnologias Utilizadas

| Categoria | Tecnologias |
|---|---|
| Banco de Dados | PostgreSQL 16 |
| Banco Espacial | PostGIS |
| Análise Geográfica | QGIS |
| Modelagem | brModelo |
| Linguagem | SQL / PL-PGSQL |

---

# 🧠 Principais Implementações Técnicas

## 🌎 Análise Espacial

Utilização da função:

`ST_DWithin`

para criação de áreas de influência comercial através de buffers de aproximadamente 80 km.

Essa abordagem permite identificar concessionárias dentro de uma região estratégica para atendimento da demanda.

---

## ⚙️ Automação de Recomendação

Foi desenvolvida a função:

```sql
fn_recomendar_loja_veiculo()
