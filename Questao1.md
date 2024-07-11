# 1. **Introdução ao GitHub**

### **O que é GitHub?**

GitHub é uma plataforma de hospedagem de código-fonte e desenvolvimento colaborativo que utiliza o sistema de controle de versão Git. Através do GitHub, desenvolvedores podem colaborar em projetos de forma eficiente, utilizando funcionalidades como controle de versão, issues, pull requests, entre outros.

### **História e evolução do GitHub**

O GitHub foi fundado em 2008 por Tom Preston-Werner, Chris Wanstrath, PJ Hyett e Scott Chacon. Desde sua criação, o GitHub tem evoluído significativamente, tornando-se a principal plataforma de hospedagem de código-fonte do mundo. Em 2018, a Microsoft adquiriu o GitHub por US$ 7,5 bilhões, o que permitiu a integração de diversos serviços e a expansão das funcionalidades da plataforma.

### **Principais funcionalidades e benefícios**

	•	Repositórios: Permitem armazenar código-fonte, arquivos e histórico de versões de um projeto.
	•	Controle de versão com Git: Facilita o rastreamento de alterações no código, possibilitando a colaboração entre múltiplos desenvolvedores.
	•	Issues: Ferramenta de rastreamento de problemas e tarefas, ajudando na gestão de projetos.
	•	Pull Requests: Permite a revisão e integração de alterações propostas por diferentes colaboradores.
	•	GitHub Actions: Ferramenta de automação de workflows, possibilitando a integração contínua e entrega contínua (CI/CD).
	•	GitHub Pages: Permite a hospedagem de sites estáticos diretamente a partir de repositórios.
	•	Comunidade: Acesso a milhões de projetos open-source, onde é possível colaborar e aprender com outros desenvolvedores.

# 2. **Configuração Inicial**

### **Criando uma conta no GitHub**

1. **Acesse o site**: Vá para [GitHub.com](https://github.com) e clique em "Sign up".
2. **Preencha o formulário de cadastro**: Insira seu e-mail, crie um username e uma senha.
3. **Verifique seu e-mail**: GitHub enviará um e-mail de confirmação para validar seu endereço de e-mail.
4. **Complete o perfil**: Adicione informações adicionais como foto, bio, etc.

### **Instalando o Git e configurando no GitHub**

**No Windows:**

1. Acesse [Git para Windows](https://gitforwindows.org/) e baixe o instalador.
2. Execute o instalador e siga as instruções na tela.

**No macOS:**

1. Use Homebrew (se estiver instalado) para instalar o Git:
    ```bash
    brew install git
    ```
2. Ou baixe o instalador do [site oficial do Git](https://git-scm.com).

**No Linux:**

1. Use o gerenciador de pacotes da sua distribuição:
    ```bash
    sudo apt-get install git # Debian/Ubuntu
    sudo yum install git # Fedora
    ```

#### Configurando o Git

Depois de instalar o Git, configure seu nome de usuário e e-mail:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```

### Primeiros passos: criando e clonando repositórios

#### Criando um repositório

1. **Acesse seu GitHub**: Faça login na sua conta.
2. **Crie um novo repositório**: Clique no ícone de "+" no canto superior direito e selecione "New repository".
3. **Configure o repositório**: Insira um nome, descrição (opcional), escolha entre público ou privado e adicione um README (opcional).

#### Clonando um repositório

```bash
# Clonar um repositório
git clone https://github.com/usuario/repo.git
```

#### Adicionando arquivos e fazendo commit

1. **Adicione arquivos ao repositório**:
    ```bash
    cd repo # Entre no diretório do repositório clonado
    echo "# Meu novo projeto" >> README.md
    git add README.md
    ```

2. **Faça commit das alterações**:
    ```bash
    git commit -m "Adiciona README inicial"
    ```

3. **Envie as alterações para o repositório remoto**:
    ```bash
    git push origin main
    ```

## 3. Comandos Básicos do Git

### Estrutura de um repositório Git

Um repositório Git contém a seguinte estrutura de diretórios e arquivos:

- **.git/**: Diretório oculto que contém todos os dados de controle de versão para o repositório.
- **README.md**: Arquivo de texto que descreve o projeto.
- **Arquivos do projeto**: Código-fonte e outros arquivos necessários para o projeto.

### Iniciando um repositório

Para iniciar um novo repositório Git, use o comando `git init`.

```bash
# Cria um novo repositório Git no diretório atual
git init

# Cria um novo repositório Git em um diretório específico
git init nome-do-diretorio
```

### Principais comandos

#### git init

Inicializa um novo repositório Git.

```bash
git init
```

#### git add

Adiciona arquivos ao índice (staging area) para serem comitados.

```bash
# Adiciona um arquivo específico
git add nome-do-arquivo

# Adiciona todos os arquivos no diretório atual
git add .
```

#### git commit

Salva as alterações no repositório local.

```bash
# Comita as alterações com uma mensagem descritiva
git commit -m "Mensagem do commit"
```

#### git push

Envia os commits do repositório local para o repositório remoto.

```bash
# Envia os commits para a branch principal (main) do repositório remoto
git push origin main
```

#### git pull

Atualiza o repositório local com as alterações do repositório remoto.

```bash
# Baixa as alterações e mescla com a branch principal (main)
git pull origin main
```

### Gerenciamento de branches

Branches são linhas paralelas de desenvolvimento, permitindo que você trabalhe em novas funcionalidades ou correções sem afetar o código principal.

#### Criar uma nova branch

```bash
# Cria uma nova branch
git checkout -b nome-da-branch
```

#### Mudar para uma branch existente

```bash
# Alterna para uma branch existente
git checkout nome-da-branch
```

#### Listar todas as branches

```bash
# Lista todas as branches no repositório
git branch
```

#### Mesclar uma branch

```bash
# Mescla a branch especificada com a branch atual
git merge nome-da-branch
```

### Exemplo de uso

1. **Inicializar um repositório**:
    ```bash
    git init
    ```

2. **Adicionar arquivos**:
    ```bash
    echo "Hello, GitHub" > hello.txt
    git add hello.txt
    ```

3. **Fazer commit das alterações**:
    ```bash
    git commit -m "Adiciona arquivo hello.txt"
    ```

4. **Criar uma nova branch**:
    ```bash
    git checkout -b nova-funcionalidade
    ```

5. **Mesclar a branch de volta para a principal**:
    ```bash
    git checkout main
    git merge nova-funcionalidade
    ```

6. **Enviar as alterações para o repositório remoto**:
    ```bash
    git push origin main
    ```

## 4. Trabalho Colaborativo

### Clonando e forkeando repositórios

#### Clonando um repositório

Clonar um repositório cria uma cópia completa do repositório remoto no seu computador. Use o comando `git clone` com a URL do repositório.

```bash
# Clonar um repositório do GitHub
git clone https://github.com/usuario/repo.git
```

#### Forkeando um repositório

Forkear um repositório cria uma cópia do repositório no seu próprio perfil do GitHub. Isso é útil quando você deseja contribuir para um projeto, pois você pode fazer alterações na sua cópia (fork) e então enviar essas alterações de volta ao repositório original através de um pull request.

1. **Acesse o repositório que deseja forkar**: Vá para o repositório no GitHub.
2. **Clique em "Fork"**: No canto superior direito, clique no botão "Fork".
3. **Faça alterações no seu fork**: Clone o repositório forkado e faça as alterações necessárias.
4. **Envie as alterações de volta ao repositório original**: Crie um pull request (explicado abaixo).

### Pull requests: como criar e gerenciar

#### Criando um pull request

1. **Crie uma branch para suas alterações**:
    ```bash
    git checkout -b minha-nova-funcionalidade
    ```
2. **Faça commit das suas alterações**:
    ```bash
    git add .
    git commit -m "Descrição das minhas alterações"
    ```
3. **Envie sua branch para o GitHub**:
    ```bash
    git push origin minha-nova-funcionalidade
    ```
4. **Crie o pull request**: 
    - Acesse o repositório no GitHub.
    - Clique em "Pull requests".
    - Clique em "New pull request".
    - Selecione a branch com suas alterações e compare com a branch principal.
    - Clique em "Create pull request" e forneça uma descrição detalhada das suas alterações.

### Revisão de código e merge de pull requests

1. **Revisão de código**:
    - Outros desenvolvedores podem revisar seu pull request.
    - Eles podem deixar comentários, solicitar mudanças ou aprovar as alterações.

2. **Merge do pull request**:
    - Após a aprovação, o pull request pode ser mesclado na branch principal.
    - Isso pode ser feito pelo autor do pull request ou por outro colaborador com permissões adequadas.

### Resolvendo conflitos

Conflitos de merge ocorrem quando há alterações conflitantes no mesmo arquivo. Para resolver conflitos:

1. **Identifique o conflito**: O Git indicará os arquivos em conflito durante um merge.
2. **Edite os arquivos em conflito**: Abra os arquivos e decida quais alterações manter. As partes conflitantes serão marcadas assim:
    ```plaintext
    <<<<<<< HEAD
    Esta é a mudança na branch principal
    =======
    Esta é a mudança na sua branch
    >>>>>>> nome-da-branch
    ```
3. **Faça commit das alterações resolvidas**:
    ```bash
    git add nome-do-arquivo
    git commit -m "Resolve conflitos de merge"
    ```
4. **Complete o merge**:
    ```bash
    git merge nome-da-branch
    ```
## 5. Funcionalidades Avançadas

### GitHub Actions: automatizando fluxos de trabalho

GitHub Actions é uma plataforma de automação que permite configurar e automatizar fluxos de trabalho de desenvolvimento diretamente no GitHub. Com GitHub Actions, você pode criar pipelines de CI/CD para construir, testar e implantar seu código automaticamente.

#### Exemplo de um arquivo de workflow

Crie um arquivo chamado `.github/workflows/main.yml` no seu repositório para definir um workflow:

```yaml
name: CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: Configure Node.js
      uses: actions/setup-node@v2
      with:
        node-version: '14'
    - run: npm install
    - run: npm run build
    - run: npm test
```

### Issues e Projects: gerenciamento de tarefas e projetos

#### Issues

Issues são usadas para rastrear tarefas, melhorias e bugs para seus projetos. Elas podem ser comentadas, etiquetadas e atribuídas a usuários específicos.

1. **Criando uma issue**:
    - Vá para a aba "Issues" no seu repositório.
    - Clique em "New issue".
    - Preencha o título e a descrição da issue.
    - Clique em "Submit new issue".

#### Projects

Projects são quadros Kanban que ajudam a organizar e priorizar o trabalho. Eles podem ser usados para planejar sprints, gerenciar tarefas e monitorar o progresso.

1. **Criando um projeto**:
    - Vá para a aba "Projects" no seu repositório.
    - Clique em "New project".
    - Dê um nome ao projeto e escolha um template.
    - Adicione colunas e cartões para organizar suas tarefas.

### GitHub Pages: criando sites estáticos com GitHub

GitHub Pages é um serviço que permite hospedar sites estáticos diretamente de um repositório no GitHub. É ideal para documentações, blogs e páginas de projetos.

1. **Criando um site com GitHub Pages**:
    - Crie um repositório chamado `username.github.io`.
    - Adicione arquivos HTML, CSS e JavaScript ao repositório.
    - Vá para a aba "Settings" do repositório.
    - Role para baixo até "GitHub Pages" e selecione a branch a partir da qual o site será publicado.
    - Seu site estará disponível em `https://username.github.io`.

#### Exemplo de configuração básica de GitHub Pages

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Site</title>
</head>
<body>
    <h1>Bem-vindo ao meu site no GitHub Pages!</h1>
    <p>Este é um exemplo de site estático.</p>
</body>
</html>
```

### Integrações e APIs

GitHub oferece várias integrações e APIs que permitem expandir e personalizar a funcionalidade da plataforma.

#### Integrações populares

- **Slack**: Receba notificações sobre atividades no seu repositório diretamente no Slack.
- **Jenkins**: Integre seu repositório com Jenkins para pipelines de CI/CD.
- **Travis CI**: Use Travis CI para automação de testes e builds.

#### Usando a API do GitHub

A API do GitHub permite que você acesse dados do GitHub programaticamente. Você pode usar a API para automatizar tarefas, criar ferramentas personalizadas e integrar GitHub com outros serviços.

##### Exemplo de uso da API com curl

```bash
# Obter informações sobre um repositório
curl -H "Authorization: token SEU_TOKEN" https://api.github.com/repos/usuario/repo
```


## 6. Boas Práticas e Dicas

### Escrevendo bons commits e mensagens

#### Dicas para escrever bons commits

1. **Commits frequentes e pequenos**: Faça commits frequentemente e mantenha-os pequenos para facilitar a revisão e rastreamento de mudanças.
2. **Mensagens descritivas**: Use mensagens de commit descritivas que expliquem claramente o que foi alterado e por quê.
3. **Use o imperativo**: Escreva mensagens de commit no imperativo, como se estivesse dando um comando (ex.: "Corrige bug no login").

#### Exemplo de boas mensagens de commit

```plaintext
# Boa mensagem de commit
Corrige erro de validação no formulário de login

# Má mensagem de commit
Conserta coisa
```

### Estrutura organizacional de repositórios

#### Organização de arquivos e pastas

1. **Mantenha uma estrutura clara**: Organize seus arquivos em pastas de acordo com sua função (ex.: `src` para código-fonte, `tests` para testes).
2. **Use arquivos README**: Inclua arquivos README em diretórios principais para descrever o conteúdo e propósito da pasta.
3. **Separe configurações e dependências**: Coloque arquivos de configuração e dependências em pastas específicas (ex.: `config` para configurações, `lib` para bibliotecas).

#### Exemplo de estrutura de repositório

```plaintext
my-project/
├── src/
│   ├── main.py
│   └── utils.py
├── tests/
│   ├── test_main.py
│   └── test_utils.py
├── config/
│   └── settings.py
├── README.md
└── .gitignore
```

### Segurança e permissões

#### Dicas de segurança

1. **Gerencie permissões**: Controle quem pode acessar e modificar seu repositório através de configurações de permissões no GitHub.
2. **Use chaves SSH**: Configure chaves SSH para autenticação segura ao interagir com repositórios remotos.
3. **Não compartilhe informações sensíveis**: Evite adicionar informações sensíveis como senhas ou tokens de API diretamente no código.

#### Configuração de permissões no GitHub

1. **Acesse as configurações do repositório**: Vá para a aba "Settings" do repositório.
2. **Gerencie a equipe**: Adicione ou remova colaboradores e defina suas permissões (read, write, admin).
3. **Configurar branches protegidas**: Defina branches que requerem revisões de código antes de serem mescladas.

### Uso de templates e arquivos de configuração

#### Arquivo .gitignore

O arquivo `.gitignore` é usado para especificar quais arquivos e diretórios devem ser ignorados pelo Git.

```plaintext
# Ignorar arquivos compilados
*.class
*.o

# Ignorar diretórios de build
/build/
/dist/

/# Ignorar arquivos de configuração locais
config/local_settings.py
```

#### Arquivo README.md

O arquivo `README.md` é usado para documentar o projeto, fornecendo informações importantes sobre o que o projeto faz, como configurá-lo e como usá-lo.

```markdown
# Nome do Projeto

Descrição breve do projeto.

## Instalação

Passos para instalar as dependências e configurar o ambiente.

```bash
# Exemplo de comando para instalação
pip install -r requirements.txt
```

## Uso

Instruções sobre como usar o projeto.

```bash
# Exemplo de comando para execução
python main.py
```

## Contribuição

Guia sobre como contribuir para o projeto.
```

### Exemplo de template de Pull Request

Um template de Pull Request ajuda a garantir que todas as informações necessárias sejam fornecidas ao criar um pull request.

```markdown
## Descrição

Por favor, inclua um resumo das mudanças e qual issue foi resolvida. Liste quaisquer dependências que estão sendo incluídas com este pull request.

## Tipo de Mudança

- [ ] Bug fix
- [ ] Nova funcionalidade
- [ ] Mudança de quebra
- [ ] Outra

## Checklist

- [ ] Meu código segue o estilo de código do projeto
- [ ] Realizei um auto-review do meu próprio código
- [ ] Fiz as mudanças correspondentes na documentação
- [ ] Adicionei testes que provam que minha correção é eficaz ou que minha funcionalidade funciona
- [ ] Testes novos e existentes passam localmente com minhas mudanças
```


# Exercícios

	•	Qual é a diferença entre clonar e forkar um repositório?
	•	Como você pode gerenciar tarefas e projetos usando Issues e Projects no GitHub?
	•	Quais são algumas práticas recomendadas para manter a segurança e gerenciar permissões no GitHub?
