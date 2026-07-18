# Contribuindo com Iconia TCG

Este documento define como alterar regras, universo, cartas, design e registros de playtest.

## Princípios

1. Preserve a simplicidade do jogo.
2. Prefira regras comunicáveis por números, cores, símbolos e ícones.
3. Não transforme uma recomendação ou hipótese em regra consolidada sem registrar a decisão.
4. Mantenha terminologia consistente.
5. Registre impactos de balanceamento e acessibilidade infantil.

## Organização dos arquivos

- Use nomes em português, minúsculos e em `kebab-case`.
- Use Markdown em UTF-8.
- Mantenha um assunto principal por arquivo.
- Use caminhos relativos para links internos.
- Imagens e arquivos visuais devem ficar em `assets/`.
- Modelos reutilizáveis devem ficar em `templates/`.

## Alterações de regras

Toda alteração de regra deve:

1. atualizar o arquivo correspondente em `docs/02-sistema/`;
2. atualizar `docs/00-central-do-projeto/decisoes-de-regras.md`;
3. remover ou atualizar a pendência correspondente;
4. registrar a mudança em `CHANGELOG.md`;
5. indicar a necessidade de playtest em `docs/06-playtests/validacao-v1.0.md`.

## Alterações de cânone

Mudanças de universo devem informar:

- o que mudou;
- por que mudou;
- quais páginas foram afetadas;
- se a alteração invalida cartas, personagens ou materiais já produzidos.

## Commits

Mensagens recomendadas:

```text
docs: adiciona cosmologia de Iconia
rules: consolida retorno dos Heróis
cards: adiciona ficha de Brasa
design: define ícones elementais
playtest: registra sessão 2026-07-18
balance: ajusta custo de criatura
fix: corrige terminologia de Faísca
```

## Fluxo pelo VS Code

```bash
git pull
git checkout -b docs/nome-da-alteracao
git add .
git commit -m "docs: descreve a alteração"
git push -u origin docs/nome-da-alteracao
```

Depois, abra um Pull Request no GitHub.

## Sincronização com o Notion

Quando uma página do Notion for atualizada:

1. identifique o arquivo correspondente no mapa de sincronização;
2. compare conteúdo e estado da decisão;
3. atualize o Markdown;
4. registre a data da sincronização no mapa;
5. não copie URLs temporárias de imagens do Notion;
6. mova imagens permanentes para `assets/`.

## Checklist de revisão

- [ ] A regra está clara para jogadores de 8–10 anos?
- [ ] A terminologia está consistente?
- [ ] A mudança preserva a identidade dos quatro elementos?
- [ ] A mudança depende de texto excessivo na carta?
- [ ] Há impacto em cartas existentes?
- [ ] Há impacto em materiais de aprendizagem?
- [ ] É necessário playtest?
- [ ] O changelog foi atualizado?
