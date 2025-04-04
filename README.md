# BancoDadosI
Aula Banco de Dados e Exercicios.

-- Criando uma tabela chamada "alunos"
CREATE TABLE alunos (
    id INTEGER PRIMARY KEY AUTOINCREMENT, -- ID único e auto-incrementado
    nome TEXT NOT NULL, -- Nome obrigatório
    idade INTEGER, -- Idade do aluno
    curso TEXT -- Curso matriculado
);

-----------------------------------------------------------

-- Inserindo alunos na tabela
INSERT INTO alunos (nome, idade, curso) VALUES ('Ana Souza', 22, 'Engenharia');
INSERT INTO alunos (nome, idade, curso) VALUES ('Carlos Lima', 25, 'Computação');
INSERT INTO alunos (nome, idade, curso) VALUES ('Mariana Oliveira', 20, 'Matemática');
-----------------------------------------------------------


-- Selecionando todos os registros da tabela alunos
SELECT * FROM alunos;


-------------------------------------------------------------


-- Selecionando apenas alunos do curso de Computação
SELECT * FROM alunos WHERE curso = 'Computação';

-------------------------------------------------------------


-- Atualizando a idade da aluna Ana Souza
UPDATE alunos SET idade = 23 WHERE nome = 'Ana Souza';

------------------------------------------------------------

-- Removendo um aluno específico
DELETE FROM alunos WHERE nome = 'Carlos Lima';

-------------------------------------------------------------

-- Ordenando os alunos por idade (do mais novo para o mais velho)
SELECT * FROM alunos ORDER BY idade ASC;

---------------------------------------------------------------

-- Ordenando por idade (do mais velho para o mais novo)
SELECT * FROM alunos ORDER BY idade DESC;

-----------------------------------------------------------------

-- Contando o número total de alunos na tabela
SELECT COUNT(*) FROM alunos;


-----------------------------------------------------------------

-- Obtendo a média de idade dos alunos
SELECT AVG(idade) FROM alunos;

-- Obtendo a maior idade registrada
SELECT MAX(idade) FROM alunos;

-- Obtendo a menor idade registrada
SELECT MIN(idade) FROM alunos;

-------------------------------------------------------------------
-- Apagando a tabela alunos
DROP TABLE alunos;

