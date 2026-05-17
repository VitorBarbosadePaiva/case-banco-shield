# Banco Shield | Engenharia de Analytics

Projeto desenvolvido para o case técnico do Banco Shield com foco em:

- Tratamento e padronização de dados
- Garantia de qualidade e confiabilidade analítica
- Análise de market share, risco e inadimplência
- Construção de dashboard executivo em Power BI
- Geração de insights estratégicos para tomada de decisão

---

# Pipeline ETL

O pipeline foi desenvolvido em Python utilizando Pandas, numpy e possui as seguintes etapas:

## 1. Ingestão dos dados
Leitura dos arquivos CSV brutos disponibilizados no case.

## 2. Padronização
Tratamento de inconsistências textuais:
- nomes de bancos
- produtos
- localidades

Exemplo:
- Hydra
- HIDRA
- hydra

→ Hidra

## 3. Qualidade dos dados
Aplicação de validações para:
- campos obrigatórios
- valores nulos
- duplicidades
- valores negativos
- inconsistências operacionais

## 4. Geração da camada tratada
Criação dos arquivos finais utilizados no dashboard analítico.

---

# Principais decisões tomadas

## Governança e confiabilidade
O projeto priorizou confiabilidade analítica antes da construção visual do dashboard.

Foram identificados riscos relevantes:
- inconsistência de nomenclaturas
- possíveis duplicidades
- produtos com volume relevante e valor zerado
- divergência entre chaves e entidades

A proposta foi estruturar controles automáticos para impedir que inconsistências contaminem indicadores estratégicos.

---

# Dashboard Executivo

O dashboard foi desenvolvido em Power BI com foco executivo.

## Indicadores principais
- Market Share
- Volume de contratos
- Valor financeiro
- Ticket médio
- Taxa de inadimplência 30+
- Produtos mais arriscados
- Regiões mais arriscadas

# Como executar o pipeline

## 1. Criar ambiente virtual

```bash
python -m venv .venv
```

## 2. Ativar ambiente virtual

### Windows
```bash
.venv\Scripts\activate
```

## 3. Instalar dependências

```bash
pip install pandas numpy
```

## 4. Executar notebook

Abrir:
```bash
notebooks/ETL.ipynb
```

Executar todas as células.

---

# Apresentação

A apresentação final do case está disponível em:

```bash
docs/apresentacao_banco_shield.pptx
```

---

# Objetivo do Projeto

Transformar dados operacionais em uma visão executiva confiável para apoiar decisões estratégicas de:
- crescimento
- competitividade
- risco
- governança de dados
