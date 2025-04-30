<h1>Cadastro de Alunos - Java Desktop com NetBeans e MySQL</h1> 

Este projeto é um **sistema de cadastro de alunos** desenvolvido em Java, utilizando o NetBeans como IDE e um banco de dados MySQL. O sistema implementa um CRUD completo (Criar, Ler, Atualizar e Deletar) e é composto por uma interface gráfica usando **Java Swing**.

<h2>Funcionalidades</h2> 

<ul>
    <li>Cadastro de novos alunos no banco de dados</li>
    <li>Exibição dos alunos cadastrados em uma tabela</li>
    <li>Pesquisa de alunos por nome com filtro </li>
    <li>Edição de dados dos alunos já cadastrados</li>
    <li>Exclusão de alunos do banco de dados</li>
    <li>Conexão com o banco de dados MySQL usando JDBC</li>
    <li>Interface gráfica desenvolvida com o Swing (JFrame)</li>
</ul>

<h2>Funcionamento do Sistema</h2> 

1. **Cadastro de Alunos**:  
   Ao iniciar o sistema, o usuário pode adicionar um novo aluno indo em arquivo(no canto superior esquerdo) -> novo, preenchendo os campos necessários, como nome, série e turma. O aluno será salvo no banco de dados.

2. **Filtro de Alunos**:  
   O programa permite que o usuario filtre alunos pelo nome

3. **Edição de Alunos**:  
    Para editar um aluno da lista, baste selecionar o aluno, ir em arquivo->alterar.

4. **Exclusão de Alunos**:  
   O usuário pode excluir um aluno diretamente da lista de pesquisa. Uma vez excluído, o aluno é removido permanentemente do banco de dados.

5. **Banco de Dados**:  
   O sistema utiliza um banco de dados MySQL para armazenar as informações dos alunos. A classe `BdAluno` gerencia as operações de inserção, atualização, pesquisa e exclusão de registros no banco.

<h2>Estrutura do Projeto</h2> 

O projeto está dividido em três pacotes principais:

<h3>1. vo - Pacote de Objetos de Valor (VO)</h3> 

Este pacote contém a classe `Aluno`, que representa o objeto do aluno no sistema.


<h3>2. bd - Pacote de Acesso ao Banco de Dados</h3> 

Contém as classes responsáveis pela comunicação com o banco de dados MySQL.
<ul>
<li><b>Bd</b>:  Gerencia a conexão com o banco de dados.</li>
<li><b>BdAluno</b>:  Realiza as operações CRUD para os alunos.</li>
</ul>

<h3> 2. tela - Pacote de Interface gráfica </h3>

Contém as classes responsáveis pela comunicação com o banco de dados MySQL.
<ul>
<li><b>TelaLocaliza</b>: Tela de pesquisa e listagem de alunos.</li>
<li><b>TelaAluno</b>: Tela para cadastro e edição de alunos.</li>
</ul>

<h2>Como Rodar o Sistema</h2>

<ol>
  <li>
    <strong>Configurar o MySQL</strong>:<br>
    Certifique-se de que o MySQL esteja instalado e em execução em seu computador. Crie o banco de dados <code>aluno</code> e a tabela <code>aluno</code> conforme o script abaixo:
    
```
CREATE DATABASE aluno;
USE aluno;
CREATE TABLE aluno (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(50),
    serie INT,
    turma VARCHAR(10)
);
```
  <li><strong>Copiar o projeto via git</strong>:<br>
  <li><strong>Rodar o arquivo via IDE</strong>:
<h2>Créditos</h2>
Projeto do curso técnico do colégio Santana ministrado pelo professor Lucio Mauro Braga Machado

