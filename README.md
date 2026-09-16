# Compliance Suite SST

Sistema de gestão de SST multiempresa para consultoria: **GRO/PGR (NR‑01)**,
**ISO 45001** (cláusulas 4 a 10), documentos obrigatórios, não conformidades,
auditorias, treinamentos e indicadores (KPIs), com visão consolidada de
carteira para consultorias que atendem múltiplas empresas-clientes.

Front-end autocontido (HTML/CSS/JS, sem backend), publicado via GitHub Pages
a partir de `index.html`. Dados de demonstração com 5 empresas fictícias de
setores distintos; persistência local (localStorage) das edições feitas na
sessão do navegador.

## Módulos

- Visão geral da carteira (ranking de compliance, alertas de vencimento)
- Dashboard por empresa (score geral, TF/TG, distribuição de risco)
- NR‑01 · GRO/PGR (inventário de riscos por GHE, plano de ação)
- ISO 45001 (maturidade por cláusula, requisitos legais, objetivos)
- Documentos obrigatórios e vencimentos
- Não conformidades e plano de ação corretivo
- Auditorias internas
- Treinamentos normativos e ASO
- Indicadores (KPIs) com glossário de fórmulas

## Pré-Cadastro do Cliente (FOR-LT-001)

`pre-cadastro-cliente.html` é a versão web da ficha FOR-LT-001, para o
cliente preencher diretamente no navegador (com ou sem internet, uma vez
carregada a página):

- Etapas guiadas equivalentes às abas da planilha original: Instruções,
  Empresa, Setores, Cargos, Anexos e Conferência automática (mesmas regras
  de PENDENTE/OK/PRONTO PARA ENVIO).
- Rascunho salvo automaticamente no navegador (localStorage), com
  exportação/importação de backup em `.json`.
- Exportações na etapa final:
  - **Planilha automatizada (.xlsx)** — reconstrói as abas do FOR-LT-001 já
    preenchidas, com colunas "(auto)" calculadas por fórmula
    (`vendor/xlsx.full.min.js`, biblioteca SheetJS embutida para
    funcionar offline).
  - **Arquivo para o SOC (.csv)** — mesmo layout da aba
    06_Exportação_SOC (CNPJ, setor, cargo, CBO, turno, atividades), pronto
    para importar/colar no sistema SOC.
  - **Orbit Gestão (.json/.csv)** — layout estruturado sugerido para
    integração com o Orbit Gestão da E-Soluções; ajustar nomes de campos
    conforme o template oficial de importação, se houver divergência.
- Ao final, orienta e facilita o envio da ficha e dos anexos ao setor de
  Segurança e Medicina do Trabalho (SESMT) da empresa-cliente (link de
  e-mail pré-preenchido, resumo copiável e impressão/PDF), mantendo o
  fluxo rastreável e alinhado ao controle de documentos da ISO 45001.
