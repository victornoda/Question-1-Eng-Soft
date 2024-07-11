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

