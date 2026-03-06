# DESAFIO-QA-BEEDOO-2026              

CRIAÇÃO DE CENÁRIOS PLANILHA: https://docs.google.com/spreadsheets/d/1XsC2mWgLPb5r8UuPsU1hsn0XrHIaeTlTa0IYyDzGIzQ/edit?usp=sharing

EXECUÇÃO DOS TESTES: https://drive.google.com/drive/folders/1qh1MNSqzXFrcVQoUMtdn2rKOw0JGpTuT?usp=sharing

Qual você acredita ser o objetivo da aplicação?
RESPOSTA: A aplicação tem como objetivo permitir o cadastro e a listagem de cursos. O usuário pode preencher um formulário com informações do curso, como nome, número de vagas, data e modalidade (online ou presencial), e após o cadastro o curso passa a aparecer na listagem de cursos disponíveis.

Quais são os principais fluxos disponíveis?
RESPOSTA: 1. Cadastro de curso: O usuário preenche o formulário com as informações do curso e realiza o cadastro.
          2. Listagem de cursos: Após cadastrar um curso, ele é exibido na lista de cursos cadastrados.
          3. Exclusão de curso: O usuário pode excluir um curso cadastrado através da opção disponível na listagem.

Quais pontos do sistema você considera mais críticos para teste?
RESPOSTA: - Validação dos campos do formulário
          - Cadastro correto de cursos
          - Exibição correta dos cursos na listagem
          - Funcionamento da exclusão de cursos
          - Tratamento de entradas inválidas (campos vazios, valores negativos, etc)



          RELATORIO DE BUGS
Bug 1 — Sistema permite cadastro com número de vagas negativo
Cadastro permite número de vagas negativo

Passos para reproduzir:

1.Acessar a página Cadastrar curso

2.Preencher os campos do formulário

3.Inserir -100 no campo Número de vagas

4.Clicar em Cadastrar curso

Resultado atual:  O sistema permite cadastrar o curso com número de vagas negativo.

Resultado esperado:  O sistema deve impedir o cadastro e exibir uma mensagem informando que o número de vagas deve ser maior que zero.

Severidade:  Alta


Bug 2 — Sistema permite cadastro de curso sem nome
Sistema permite cadastrar curso sem preencher o nome

Passos para reproduzir:

1.Acessar a página Cadastrar curso

2.Deixar o campo Nome do curso vazio

3.Preencher os demais campos

4.Clicar em Cadastrar curso

Resultado atual:  O curso é cadastrado mesmo sem nome.

Resultado esperado:  O sistema deve exigir o preenchimento do campo Nome do curso antes de permitir o cadastro.

Severidade:  Alta


Bug 3 — Sistema permite cadastro com todos os campos vazios
Sistema permite cadastrar curso sem preencher nenhum campo

Passos para reproduzir:

1.Acessar a página Cadastrar curso

2.Não preencher nenhum campo

3.Clicar em Cadastrar curso

Resultado atual:  O sistema permite cadastrar o curso mesmo com todos os campos vazios.

Resultado esperado:  O sistema deve impedir o cadastro e informar que os campos obrigatórios precisam ser preenchidos.

Severidade:  Alta


Bug 4 — Sistema permite cadastrar curso com 0 vagas
Sistema permite cadastrar curso com zero vagas

Passos para reproduzir:

1.Acessar a página Cadastrar curso

2.Preencher os campos

3.Informar 0 no campo Número de vagas

4.Clicar em Cadastrar curso

Resultado atual:  O sistema permite cadastrar o curso com 0 vagas.

Resultado esperado:  O sistema deveria impedir o cadastro ou validar que o número de vagas deve ser maior que zero.

Severidade:  Média


Bug 5 — Sistema permite cadastrar curso sem selecionar tipo de curso
Sistema permite cadastrar curso sem selecionar modalidade (online ou presencial)

Passos para reproduzir:

1.Acessar a página Cadastrar curso

2.Preencher os campos

3.Não selecionar o tipo de curso

4.Clicar em Cadastrar curso

Resultado atual:  O curso é cadastrado mesmo sem selecionar a modalidade.

Resultado esperado:  O sistema deveria exigir a seleção da modalidade antes do cadastro.

Severidade:  Média


Bug 6 — Sistema permite cadastrar curso sem informar data
Sistema permite cadastrar curso sem data de início ou fim

Passos para reproduzir:

1.Acessar a página Cadastrar curso

2.Preencher os campos

3.Deixar os campos de data vazios

4.Clicar em Cadastrar curso

Resultado atual:  O curso é cadastrado sem data de início ou fim.

Resultado esperado:  O sistema deveria exigir o preenchimento das datas antes de permitir o cadastro.

Severidade:  Média


Bug 7 — Botão excluir curso não remove o curso da lista
Botão "Excluir curso" não remove o curso da lista

Passos para reproduzir:

1.Cadastrar um curso

2.Acessar a lista de cursos

3.Clicar no botão Excluir curso

Resultado atual:  O curso não é removido da lista.

Resultado esperado:  O sistema deveria remover o curso da lista após clicar em Excluir curso.

Severidade:  Alta


Bug 8 — Interface exibe tela azul ocupando metade da tela após cadastro

Título do bug
Interface apresenta área azul ocupando metade da tela na listagem de cursos após cadastro

Passos para reproduzir:

1.Cadastrar um curso

2.Acessar a página Listar cursos

Resultado atual:  Uma área azul aparece ocupando metade da tela na interface.

Resultado esperado:  A interface deveria exibir apenas a listagem de cursos, sem elementos visuais indevidos.

Severidade:  Baixa
