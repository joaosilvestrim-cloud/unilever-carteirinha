# Passaporte de Segurança — Unilever

Sistema de carteirinha digital de treinamentos de segurança. Site responsivo único (funciona no celular e no desktop) que substitui as carteirinhas físicas.

## Estrutura do sistema

- **Login** com SSO Unilever (e-mail corporativo como alternativa).
- **App (SHE / Admin)** com rotas reais:
  - Painel de conformidade
  - Colaboradores (lista + ficha completa + carteirinha)
  - Carteirinhas (emissão / envio / PDF)
  - Treinamentos (catálogo e validade)
  - Vencimentos (vencidos e a vencer em 30 dias)
  - Integrações (SharePoint, API UniU, SOC, Power BI)
  - Auditoria (log imutável)
  - Configurações (perfis e regras)
- **Consulta pública** (destino do QR): colaborador informa o RE e vê a carteirinha. Executor e Liberador, fiéis às carteirinhas físicas.

## Logo

O código referencia `unilever.png`. Salve o logo oficial da Unilever com esse nome na raiz do projeto para aparecer em todo o sistema. Sem o arquivo, um "U" vetorial limpo é usado como fallback.

## Dados

`employees.json`: amostra real da base de treinamentos (508 colaboradores, 1.460 habilitações), já embutida no `index.html`. RE de exemplo: `443111`, `808885` (liberador), `373948` (com vencidos).

## Deploy na Vercel

Site estático, sem build. Preset **Other** (Output Directory: `.`). A Vercel publica a produção ao receber um push na `main`.

## Próximos passos

1. Integrar ASO via SOC (time de Saúde).
2. Confirmar a API UniU (NR-6, NR-12, NR-20) com o Tex.
3. Definir origem de NR20, PSM, Combustible dust, Içamento, Escavação.
4. Autenticação/perfis reais e emissão com assinatura digital.
