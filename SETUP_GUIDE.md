# 🚀 Como colocar o site online — Guia passo a passo

## O que vais precisar (tudo gratuito)

- [ ] Conta no [GitHub](https://github.com) — cria uma se não tiveres
- [ ] [Quarto](https://quarto.org/docs/get-started/) instalado no teu computador
- [ ] [Git](https://git-scm.com/downloads) instalado no teu computador

---

## Passo 1 — Instalar o Quarto

Vai a **https://quarto.org/docs/get-started/** e faz download para o teu sistema operativo.

Verifica que está instalado:
```bash
quarto --version
```

---

## Passo 2 — Criar um repositório no GitHub

1. Vai a **github.com** e faz login
2. Clica em **"New repository"**
3. Nome do repositório: `yourusername.github.io`  
   ⚠️ Substitui `yourusername` pelo teu username exato do GitHub
4. Deixa **Public**
5. Clica **"Create repository"**

---

## Passo 3 — Colocar os ficheiros no repositório

Abre o terminal na pasta do site (a pasta `mysite` que o Claude criou) e corre:

```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

---

## Passo 4 — Publicar o site

```bash
quarto publish gh-pages
```

O Quarto vai perguntar se queres publicar no GitHub Pages. Diz que sim.

Aguarda 1-2 minutos e o teu site está em:

> **https://yourusername.github.io**

---

## Como publicar novos posts

1. Cria uma pasta nova em `posts/nome-do-post/`
2. Cria um ficheiro `index.qmd` lá dentro (copia a estrutura dos posts de exemplo)
3. Escreve o post
4. Corre no terminal:

```bash
quarto publish gh-pages
```

Só isso. O site atualiza automaticamente.

---

## Personalizar o site

Edita o ficheiro `_quarto.yml`:
- Muda o título do site
- Adiciona os teus links do GitHub e LinkedIn

Edita o ficheiro `about.qmd`:
- Escreve sobre ti
- Adiciona uma foto (coloca um ficheiro `profile.jpg` na pasta raiz)

---

## Estrutura de pastas

```
mysite/
├── _quarto.yml          ← configuração do site
├── index.qmd            ← homepage
├── about.qmd            ← página sobre ti
├── posts.qmd            ← lista de todos os posts
├── styles.css           ← design personalizado
└── posts/
    ├── what-is-counterfactual/
    │   └── index.qmd    ← post teórico (já criado)
    └── causalimpact-practical/
        └── index.qmd    ← post prático (já criado)
```

---

## Dúvidas?

Pede ajuda ao Claude a qualquer momento — para criar novos posts, ajustar o design, ou resolver erros.
