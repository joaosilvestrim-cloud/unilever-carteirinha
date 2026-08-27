# Carteirinha Digital de Treinamentos — Unilever

Protótipo de alta fidelidade. Site responsivo (sem app) que substitui as carteirinhas físicas de treinamentos de segurança.

## Duas visões

- **Colaborador** (celular): informa o RE ou lê o QR Code e vê a carteirinha digital. Alterna entre **Executor** (verso "Validade dos Treinamentos") e **Liberador** ("Autorização para Trabalhos Especializados").
- **Administração** (Ana / SHE): painel de conformidade, colaboradores, treinamentos e fontes de dados (SharePoint, API UniU, SOC).

## Dados

`employees.json` traz uma amostra real da base de treinamentos (508 colaboradores, 1.460 habilitações). Os dados já vêm embutidos no `index.html`; o JSON fica no repo só como referência para a fase de sistema.

RE de exemplo: `443111`, `808885` (liberador), `373948` (com vencidos).

## Deploy na Vercel

É um site estático (um único `index.html`). Sem build.

Opção 1 — CLI:
```bash
cd unilever-carteirinha
npx vercel --prod
```

Opção 2 — GitHub + Vercel: suba o repo e importe na Vercel com preset **Other** (Framework Preset: Other, Build Command: vazio, Output Directory: `.`).

## Próximos passos para virar sistema

1. Integrar ASO via SOC (time de Saúde).
2. Confirmar a API UniU (NR-6, NR-12, NR-20) com o Tex.
3. Definir origem de NR20, PSM, Combustible dust, Içamento, Escavação (hoje em branco na base).
4. Login/perfis: Admin, SHE, Colaborador (consulta sem login).
