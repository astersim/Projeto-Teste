Meu Software - Projeto de Saudação
Bem-vindo ao repositório do Meu Software, um projeto simples em Python que implementa uma função de saudação personalizada. Este documento descreve o processo de criação, versionamento e gerenciamento do código utilizando Git e GitHub.
Objetivo do Projeto
O objetivo deste projeto é criar um software básico em Python que solicita o nome do usuário e exibe uma mensagem de saudação. O desenvolvimento foi realizado em etapas, com melhorias incrementais e o uso de branches para novas funcionalidades.
Estrutura do Projeto

meu_software.py: Arquivo principal contendo o código Python do programa.
README.md: Este arquivo, com a documentação do projeto.

Passos de Desenvolvimento
1. Configuração Inicial do Repositório
O repositório foi inicializado com os seguintes comandos:
git init
git remote add origin [<URL_DO_REPOSITORIO>](https://github.com/astersim/Projeto-Teste)

2. Criação do Software Básico
Foi criado o arquivo meu_software.py com uma função simples de saudação. O código inicial é o seguinte:
def saudacao(nome):
    return f"Olá, {nome}! Bem-vindo ao software."

if __name__ == "__main__":
    nome = input("Digite seu nome: ")
    print(saudacao(nome))

Comandos executados:
echo 'def saudacao(nome):' > meu_software.py
echo '    return f"Olá, {nome}! Bem-vindo ao software."' >> meu_software.py
echo 'if __name__ == "__main__":' >> meu_software.py
echo '    nome = input("Digite seu nome: ")' >> meu_software.py
echo '    print(saudacao(nome))' >> meu_software.py
git add meu_software.py
git commit -m "Versão 1: Software básico de saudação"
git push origin main

Descrição: Este commit criou a primeira versão do software, que solicita o nome do usuário e exibe uma saudação personalizada.
3. Melhoria com Verificação de Entrada
O arquivo meu_software.py foi modificado para incluir uma verificação que atribui o nome "Usuário" caso a entrada esteja vazia. O trecho de código adicionado foi:
    if not nome.strip():
        nome = "Usuário"

Comandos executados:
echo '    if not nome.strip():' >> meu_software.py
echo '        nome = "Usuário"' >> meu_software.py
git add meu_software.py
git commit -m "Versão 2: Adicionada verificação de entrada"
git push origin main

Descrição: Esta melhoria garante que o programa trate entradas vazias, atribuindo um nome padrão para evitar saudações inválidas.
4. Criação de uma Branch para Nova Funcionalidade
Uma nova branch chamada nova-funcionalidade foi criada para implementar uma funcionalidade adicional: exibir a saudação em letras maiúsculas. O código da função saudacao foi alterado para:
def saudacao(nome):
    return f"OLÁ, {nome.upper()}! BEM-VINDO AO SOFTWARE."

Comandos executados:
git checkout -b nova-funcionalidade
echo '    return f"OLÁ, {nome.upper()}! BEM-VINDO AO SOFTWARE."' >> meu_software.py
git add meu_software.py
git commit -m "Versão 3: Saudação agora é exibida em maiúsculas"
git push origin nova-funcionalidade

Descrição: A nova branch foi criada para testar a funcionalidade de saudação em maiúsculas, mantendo a branch main estável até que a funcionalidade seja revisada e aprovada.
Como Executar o Projeto

Clone o repositório:git clone [<URL_DO_REPOSITORIO>](https://github.com/astersim/Projeto-Teste)


Navegue até o diretório do projeto:cd Projeto-Teste


Execute o programa:python meu_software.py


Digite seu nome quando solicitado e veja a saudação.

Próximos Passos

Revisar a branch nova-funcionalidade e, se aprovada, realizar o merge com a branch main.
Adicionar mais funcionalidades, como personalização da mensagem ou suporte a múltiplos idiomas.
Implementar testes unitários para garantir a robustez do código.

Contribuições
Contribuições são bem-vindas! Para contribuir:

Faça um fork do repositório.
Crie uma branch para sua funcionalidade (git checkout -b minha-funcionalidade).
Commit suas mudanças (git commit -m "Descrição da mudança").
Envie para o repositório remoto (git push origin minha-funcionalidade).
Abra um Pull Request.
