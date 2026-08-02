MÉTODO KÓLLER

CATÁLOGO OFICIAL DE MÓDULOS DO FRAMEWORK

---

FINALIDADE

Este documento define oficialmente os módulos que compõem o Framework Método Kóller.

Seu objetivo é servir como o catálogo funcional oficial do Framework, descrevendo os módulos existentes, suas responsabilidades, suas relações e sua posição dentro da arquitetura.

Este documento não descreve regras de implementação.

Este documento não registra histórico de desenvolvimento.

Este documento não registra Sprints.

Este documento não registra missões.

As regras de implementação encontram-se exclusivamente no documento:

MK_MANUAL_DE_IMPLEMENTAÇÃO_DE_MÓDULO.md

---

DEFINIÇÃO DO FRAMEWORK

O Método Kóller é um Framework modular para gestão operacional de campanhas políticas.

Sua arquitetura é composta por módulos independentes e interoperáveis.

Cada módulo representa uma unidade funcional especializada.

O conjunto desses módulos constitui o Framework completo.

---

PRINCÍPIO DA MODULARIDADE

Todo módulo deverá possuir:

- alta coesão;
- baixo acoplamento;
- responsabilidade única;
- independência funcional sempre que possível.

Integrações entre módulos deverão ocorrer por meio dos pipelines oficiais do Framework.

Nenhum módulo deverá assumir responsabilidades pertencentes a outro módulo.

---

ORGANIZAÇÃO DO FRAMEWORK

O Framework é organizado em módulos.

Cada módulo representa uma capacidade funcional específica.

Todo módulo deverá possuir:

- objetivo;
- responsabilidades;
- entradas;
- saídas;
- dependências;
- artefatos;
- pipeline operacional;
- critérios de aceite.

Cada módulo será implementado por meio de um Sprint próprio, seguindo integralmente o:

MK_MANUAL_DE_IMPLEMENTAÇÃO_DE_MÓDULO.md

---

CONVENÇÕES DO FRAMEWORK

Sempre que aplicável, um módulo deverá possuir os seguintes artefatos:

- FORM (entrada de dados)
- STG (área de staging)
- SCRIPT PROCESSADOR
- BASE DE DADOS
- TABELAS
- LOG
- GATILHOS (Triggers)
- Integrações necessárias

Nem todos os módulos obrigatoriamente possuirão todos esses componentes.

A definição dependerá da natureza funcional do módulo.

---

MÓDULOS OFICIAIS DO FRAMEWORK

---

MÓDULO 01 — PESSOAS

Status

Oficial

Objetivo

Centralizar o cadastro universal de pessoas do Framework.

Responsabilidades

- cadastrar pessoas;
- atualizar cadastros;
- identificar pessoas de forma única;
- servir como base para os demais módulos.

Entradas

- FORM001
- futuras integrações

Saídas

- TB_PESSOAS

Dependências

Nenhuma.

Este é o módulo base do Framework.

Artefatos

- FORM001
- STG001
- BD001
- TB_PESSOAS
- MK_Pessoas.gs
- Código.gs
- Trigger

Pipeline

Entrada

↓

Processamento

↓

Persistência

↓

Atualização da STG

↓

Registro em Log

↓

Fim

Observações

Este módulo é a base estrutural para todos os demais módulos.

---

# MÓDULO 02 — ESCUTATÓRIA

**Status:** Planejado

## Objetivo

Registrar, organizar e acompanhar todas as escutas realizadas pela campanha.

## Responsabilidades

- Registrar escutas;
- Classificar manifestações;
- Acompanhar encaminhamentos;
- Produzir inteligência qualitativa.

## Entradas

- Formulário de Escutatória (MVP).

> **Nota:** A primeira versão do módulo utilizará um único formulário destinado a sintetizar o material obtido durante a escuta. Novos formulários poderão ser incorporados em versões futuras sem alterar a arquitetura do módulo.

## Saídas

- Base de Escutatória.

## Integrações

- Módulo Pessoas (opcional).

> **Nota:** A Escutatória poderá ser vinculada a uma pessoa cadastrada no Módulo Pessoas quando essa identificação existir. O módulo também deverá permitir registros anônimos ou de pessoas ainda não cadastradas, não dependendo dessa integração para seu funcionamento.

## Artefatos

Serão definidos durante o Sprint.

## Pipeline

Será definido durante o Sprint.
---

MÓDULO 03 — AGENDA

Status

Planejado

Objetivo

Gerenciar compromissos, visitas, reuniões e atividades da campanha.

Responsabilidades

- agenda institucional;
- agenda política;
- visitas;
- reuniões;
- compromissos.

Entradas

Formulários e integrações.

Saídas

Agenda consolidada.

Dependências

Módulo Pessoas.

Artefatos

Definidos durante o Sprint.

Pipeline

Será definido durante o Sprint.

Observações

Nenhuma.

---

MÓDULO 04 — EVENTOS

Status

Planejado

Objetivo

Controlar todos os eventos da campanha.

Responsabilidades

- cadastro;
- equipes;
- participantes;
- acompanhamento.

Entradas

Formulários de Eventos.