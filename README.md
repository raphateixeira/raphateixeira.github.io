# raphateixeira.github.io

Site pessoal do Prof. Dr. Raphael Teixeira (FEE/CAMTUC — UFPA), construído com [Quarto](https://quarto.org/). Reúne ensino, pesquisa, publicações e notas de estudo em controle, eletrônica de potência e aprendizado de máquina aplicado à engenharia.

## Estrutura

- `index.qmd` — página inicial
- `Ensino/` — disciplinas, calendário de aulas do semestre corrente
- `Pesquisa/` — linhas e projetos de pesquisa (repositórios no GitHub)
- `Publicacoes/` — artigos, teses, dissertações e TCCs orientados
- `Notas/` — notas de estudo aprofundadas, com matemática e Python
- `Estudos/` — livros, sites e canais recomendados
- `Documentos/` / `Editais/` — normas institucionais e editais
- `Perfil/` — apresentação do docente
- `_quarto.yml` — navegação (navbar/sidebar), tema e configuração do site
- `custom.scss` — paleta de cores UFPA e color code por categoria

## Desenvolvimento local

```bash
pip install -r requirements.txt
quarto render
quarto preview
```

Algumas notas em `Notas/` executam código Python (NumPy, SciPy, Matplotlib) via engine Jupyter do Quarto.

## Publicação

O deploy é automático: todo push em `main` roda `.github/workflows/publish.yml`, que renderiza o site com Quarto e publica no GitHub Pages.
