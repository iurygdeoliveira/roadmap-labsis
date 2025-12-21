# Aula 001 - Criando seu Repositório no GitHub

**Bloco:** Planejamento e Concepção  
**Duração:** 1h00

## 📚 Conteúdo Programático

-   Introdução ao Git e GitHub
-   Criação de repositório no GitHub
-   Fluxo básico: `git add`, `git commit`, `git push`
-   Submissão de tarefas na plataforma LabSIS

## 🎯 Objetivos de Aprendizagem

Ao final desta aula, você será capaz de:

-   Criar um repositório no GitHub para seu projeto
-   Executar o fluxo básico de versionamento com Git
-   Submeter suas tarefas corretamente na plataforma LabSIS

## ✅ Atividades

### 1. Criando uma Conta no GitHub (se necessário) (10min)

Se você ainda não possui uma conta no GitHub:

1.  Acesse [github.com](https://github.com/)
2.  Clique em **Sign up**
3.  Preencha seus dados (use seu email institucional se possível)
4.  Confirme seu email

### 2. Criando seu Repositório (15min)

![Criação de Repositório](https://docs.github.com/assets/cb-31554/images/help/repository/create-repository-name.png)

1.  Faça login no GitHub
2.  Clique no botão **+** no canto superior direito e selecione **New repository**
3.  Configure seu repositório:
    -   **Repository name:** Nome do seu projeto (ex: `meu-projeto-labsis`)
    -   **Description:** Uma breve descrição do projeto
    -   **Visibility:** Escolha `Public` (recomendado para portfólio) ou `Private`
    -   **Initialize this repository with:** Marque **Add a README file**
4.  Clique em **Create repository**
5.  Copie a URL do repositório (ex: `https://github.com/seu-usuario/meu-projeto-labsis`)

### 3. Clonando e Fazendo seu Primeiro Commit (20min)

Abra o terminal e execute os comandos abaixo:

```bash
# 1. Clone o repositório para sua máquina
git clone https://github.com/seu-usuario/meu-projeto-labsis.git

# 2. Entre na pasta do projeto
cd meu-projeto-labsis

# 3. Crie um arquivo de teste
echo "# Meu Projeto LabSIS" > PROJETO.md

# 4. Adicione todas as mudanças ao stage
git add .

# 5. Faça o commit com uma mensagem descritiva
git commit -m "feat: adiciona arquivo inicial do projeto"

# 6. Envie as mudanças para o GitHub
git push origin main
```

> **💡 Dica:** Após o `git push`, verifique no GitHub se o arquivo apareceu no repositório.

### 4. Obtendo o Link e Hash do Commit (10min)

Para submeter sua tarefa no LabSIS, você precisará de duas informações:

#### Link do Repositório

É a URL do seu repositório no GitHub:

```
https://github.com/seu-usuario/meu-projeto-labsis
```

#### Hash do Commit

Para obter o hash do último commit, execute no terminal:

```bash
git log -1 --format="%H"
```

O resultado será algo como:

```
a1b2c3d4e5f6g7h8i9j0k1l2m3n4o5p6q7r8s9t0
```

> **💡 Alternativa:** Você também pode ver o hash do commit diretamente no GitHub, clicando em "Commits" na página do repositório.

### 5. Submetendo no LabSIS (5min)

1.  Acesse a plataforma **LabSIS** com suas credenciais
2.  Navegue até a seção de **Aulas/Tarefas**
3.  Localize esta aula na lista
4.  Clique em **Entregar Tarefa**
5.  Preencha os campos:
    -   **Link do Repositório:** Cole a URL do seu repositório GitHub
    -   **Hash do Commit:** Cole o hash obtido no passo anterior
6.  Confirme a submissão

## 📝 Projeto Autoral

### Tarefa desta aula:

Criar um repositório no GitHub para seu projeto e submeter o link e hash do commit na plataforma LabSIS.

### Critérios que serão utilizados para avaliar a tarefa:

-   [ ] Repositório criado no GitHub
-   [ ] Pelo menos um commit realizado
-   [ ] Link do repositório correto submetido no LabSIS
-   [ ] Hash do commit válido submetido no LabSIS

## 🔗 Recursos

### Documentação Oficial

-   [Git - Documentação Oficial](https://git-scm.com/doc)
-   [GitHub Docs](https://docs.github.com/)
-   [Git Tutorial Interativo](https://learngitbranching.js.org/?locale=pt_BR)

### Tutoriais Recomendados

-   [GitHub para Iniciantes - YouTube](https://www.youtube.com/results?search_query=github+para+iniciantes+pt)
-   [Guia Rápido de Git](https://rogerdudler.github.io/git-guide/index.pt_BR.html)

## 📌 Anotações

Espaço para suas anotações durante o estudo:

```
[Adicione suas anotações aqui]
```

## ✨ Dificuldades e Soluções

Registre as dificuldades encontradas e como você as resolveu:

| Dificuldade                            | Solução                                         | Aprendizado                              |
| -------------------------------------- | ----------------------------------------------- | ---------------------------------------- |
| Ex: Erro de autenticação no `git push` | Configurar SSH ou usar Personal Access Token    | GitHub exige autenticação segura         |
| Ex: Não consegui encontrar o hash      | Usei `git log -1 --format="%H"` ou vi no GitHub | O hash identifica unicamente cada commit |

## 🚀 Próxima Aula

Na próxima aula, você aprenderá sobre: **Definindo sua Ideia de Projeto** para escolher e estruturar a ideia do seu projeto para a disciplina.
