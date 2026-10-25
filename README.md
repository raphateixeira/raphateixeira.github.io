# raphateixeira.github.io

Site pessoal do Prof. Dr. Raphael Teixeira (FEE/CAMTUC — UFPA), construído com [Quarto](https://quarto.org/):
ensino, pesquisa, projetos de iniciação científica, publicações, laboratório e documentos.

## Estrutura

- `index.qmd` — página inicial (apresentação, semestre atual, novidades, linhas de pesquisa, publicações recentes)
- Ensino: o menu leva ao site do repositório [Ensino](https://raphateixeira.github.io/Ensino/) (disciplinas e horários)
- `Pesquisa/` — linhas e repositórios de pesquisa
- `Projetos/` — temas de iniciação científica (um `.qmd` por tema, listados automaticamente)
- `Publicacoes/` — artigos, tese, dissertação e trabalhos orientados
- `LINCE/` — laboratório: equipamentos e bancadas
- `Documentos/`, `Editais/` — normas institucionais e editais
- `Perfil/` — apresentação do docente
- `_quarto.yml` — navbar e configuração do site
- `custom.scss` — componentes próprios deste site (classes `.site-*`)
- `_rodape.html` — rodapé com links institucionais, bases de pesquisa e perfis

O visual base (navbar, tipografia, cartões, botões) vem do tema compartilhado `TemaRTx.scss`, mantido em
[raphateixeira/.github](https://github.com/raphateixeira/.github) e baixado no build (não versionado aqui).

## Manutenção a cada semestre

Na página inicial, atualizar "Neste semestre" e "Novidades"; a grade de horários fica no repositório `Ensino`
(`horarios.csv`).

## Desenvolvimento local

```bash
sh ../.github/scripts/atualizar-tema.sh   # baixa o TemaRTx.scss canônico
pip install -r requirements.txt
quarto preview
```

## Publicação

Todo push em `main` roda `.github/workflows/publish.yml`, que chama o workflow compartilhado de
`raphateixeira/.github`: renderiza com Quarto e publica no GitHub Pages.
