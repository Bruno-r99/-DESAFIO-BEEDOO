# DESAFIO-BEEDOO

Link dos Cenarios e grafico de report:https://docs.google.com/spreadsheets/d/1drAf9be8PromJV16-ZhtUn3yozEPaRqXoCZ1MiHLX3s/edit?usp=sharing 

Link das evidências em MP4: https://drive.google.com/drive/folders/1_EuWNCdByC_wqjpptsNF2EViYJ0Ev4X_?usp=sharing 

  História 
Eu como usuário da frente de cadastro de curso 
Quero realizar cadastro e exclusão de curso 
Para atender alunos da universidade metropolitana de Cubatão 

Premissas: 
1- Desenvolvedores e QA com acessos necessários para iniciar o desenvolvimento e testes. 
2- Infraestrutura e pipelines criados no ambiente. 
3- Desenho de solução detalhado e alinhado com arquitetura. 
4- Cenários de testes. 

Plano de Teste - Sistema de Cadastro de Usuários

1. Introdução: 
➢ Descrição do sistema: O sistema de cadastro de usuários permitirá o registro e gerenciamento de novos usuários em uma plataforma online. 
➢ Objetivos dos testes: Verificar a funcionalidade e desempenho de cadastro de usuários.

2. Escopo dos Testes: 
➢ Funcionalidades Incluídas: 
■ Registro de novo usuário com campos obrigatório (nome do curso, descrição do curso, instrutor, url da imagem, data inicio, data fim, numero de vagas e tipo de curso). 
■ Validação de listagem de curso. 
■ Validação de exclusão de curso. 
■ Validação de curso de exclusão de curso sem confirmação. 
■ Cadastrar curso com sucesso. 
■ Validação de cadastro sem preenchimento de todos os campos.
■ Validação da url da imagem de capa.
■ Validação de datas. 

3. Metodologia e Ferramentas: 
➢ Metodologia: Teste Ágil com ciclos de interação de duas semanas. 
➢ Ferramentas: Postman para validação de API, Cypress para automatizar o fluxo front end, e excell. 

4. Cenario de Teste: 
➢ Cenario de Teste: Listar todos os cursos disponíveis.
➢ Cenario de Teste: Listagem de cursos não há cursos cadastrados. 
➢ Cenario de Teste: Exclusão de um curso. 
➢ Cenario de Teste: Tentativa de exclusão de um curso sem confirmação. 
➢ Cenario de Teste: Cadastrar um curso com sucesso. 
➢ Cenario de Teste: Tentativa de cadastrar um curso sem preencher todos os campos obrigatórios. 
➢ Cenario de Teste: Validação da URL da imagem de capa. 
➢ Cenario de Teste: Validação de datas (Data de início após a data de fim).

5. Cronograma de Testes: 
➢ Semana 1: Preparação do ambiente de testes, criação dos Cenarios de teste e revisão da documentação. 
➢ Semana 2: Execução dos testes manuais e automatizados, análise dos resultados e correção de defeitos encontrados. 

6. Equipe de Testes: 
➢ Testadores: [Bruno Almeida – Analista QA Junior] 

7. Critérios de Aceitação:
➢ Todos os casos de teste devem ser executados sem erros. 
➢ As funcionalidades de cadastro de curso devem atender aos requisitos especificados. 

8. Considerações Finais: 
➢ Ao final dos testes, será gerado um relatório detalhado com os resultados, conclusões e recomendações para a equipe de desenvolvimento. 

BUG: 
Foram encontrados 6 BUGS.

BUG 1 Resumo - Mesmo com nenhum cadastro a mensagem "Nenhum curso disponível" não é exibida na tela. 
Descrição: Ao validar mensagem " Nenhum curso disponivél" ao clicar na lista de curso, foi detectado que não é retornado nenhuma mensagem.

BUG 2 Resumo - Quando clico no botão "excluir curso" uma mensagem de confirmação "Curso excluído com sucesso!" aparece, porém o curso continua na tela. 
Descrição: Ao clicar no botão excluir curso mesmo aparecendo a mensagem "Curso excluido com sucesso" o curso não é excluido da tela.

BUG 3 Resumo - Deveria aparecer na tela ao clicar no botão excluir curso a opção de excluir SIM/NÃO. 
Descrição: Ao clicar na opção excluir curso e tentar reverter a exclusão deviria aparecer a opção SIM/NÃO na tela. 

BUG 4 Resumo - Mesmo não preenchendo alguns campos obrigatórios ele gera um cadastro. 
Descrição: Mesmmo que ao deixar um campo em branco ou passar um dado inválido o sistema cria um novo curso na lista. 

BUG 5 Resumo - Mesmo não passando a URL ele ainda cria um cadastro. 
Descrição: Ao tentar criar um curso sem a URL ele ainda cria um cadastro. 

BUG 6 Resumo - Mesmo inserindo uma data de conclusão anterior a de ínicio o cadastro ainda é realizado. 
Descrição: Ao tentar criar um cadastro com a anterior a data atual o sistema não deveria criar um cadastro mesmo assim ele cria com sucesso. 

Vulnerabilidade do sistema: 
1- Sistema não aparece mensagem de nemhum curso disponivél. 
2- Curso não é excluido da listagem de curso.
3- Não foi identificado a opção SIM/NÃO para excluir curso.

