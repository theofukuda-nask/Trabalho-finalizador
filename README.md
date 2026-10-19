RF001 — Fazer Login
Descrição: O sistema deve permitir que o usuário acesse sua conta utilizando suas credenciais.
Atores: Usuário.
Pré-condições: O usuário deve possuir uma conta cadastrada.
Entradas:
E-mail;
Senha.
Processamento:
O usuário acessa a tela inicial do aplicativo.
O usuário informa seu e-mail e sua senha.
O sistema verifica os dados informados.
O sistema permite o acesso caso as credenciais estejam corretas.
Saída: O usuário acessa a página inicial do aplicativo.
Regras de negócio:
- O e-mail e a senha devem corresponder a uma conta cadastrada.
Exceções:
Caso os dados estejam incorretos, o sistema deve informar o usuário.
Caso algum campo esteja vazio, o sistema deve solicitar o preenchimento.
RF002 — Visualizar Página Inicial
Descrição: O sistema deve apresentar a página inicial do aplicativo, permitindo que o usuário acesse suas principais funcionalidades.
Atores: Usuário.
Pré-condições: O usuário deve acessar o aplicativo.
Entradas:
- Solicitação de acesso à página inicial.
Processamento:
O usuário acessa a página inicial.
O sistema apresenta a tela principal.
O sistema disponibiliza as opções de navegação para as demais funcionalidades.
Saída: A página inicial é exibida com as opções de navegação do aplicativo.
Regras de negócio:
- As opções de navegação devem direcionar o usuário às telas correspondentes.
Exceções:
- Caso a página não seja carregada, o sistema deve informar o usuário.
RF003 — Visualizar Carrinho de Compras
Descrição: O sistema deve permitir que o usuário visualize os produtos adicionados ao carrinho.
Atores: Usuário.
Pré-condições: O usuário deve acessar a opção de carrinho.
Entradas:
- Solicitação de visualização do carrinho.
Processamento:
O usuário seleciona o ícone do carrinho.
O sistema apresenta os produtos adicionados.
O sistema exibe os nomes e as quantidades dos produtos.
O sistema apresenta o valor total da compra, quando disponível.
Saída: O usuário visualiza os produtos presentes no carrinho.
Regras de negócio:
O carrinho deve apresentar somente os produtos adicionados pelo usuário.
O valor total deve corresponder aos itens presentes no carrinho.
Exceções:
- Caso o carrinho esteja vazio, o sistema deve informar que não existem produtos adicionados.
RF004 — Remover Produtos do Carrinho
Descrição: O sistema deve permitir que o usuário remova produtos do carrinho antes de finalizar a compra.
Atores: Usuário.
Pré-condições: O carrinho deve possuir pelo menos um produto.
Entradas:
- Produto selecionado para remoção.
Processamento:
O usuário acessa o carrinho.
O usuário seleciona a opção de cancelar ou remover um produto.
O sistema remove o produto selecionado.
O sistema atualiza os itens e o valor total do carrinho.
Saída: O produto selecionado é removido do carrinho.
Regras de negócio:
- Somente os produtos selecionados para remoção devem ser retirados.
Exceções:
- Caso o produto não esteja no carrinho, o sistema deve informar que não foi possível removê-lo.
RF005 — Finalizar Compra
Descrição: O sistema deve permitir que o usuário confirme a compra dos produtos presentes no carrinho.
Atores: Usuário.
Pré-condições: O carrinho deve possuir pelo menos um produto disponível para compra.
Entradas:
Produtos selecionados;
Quantidades;
Dados necessários para concluir a compra.
Processamento:
O usuário acessa o carrinho.
O sistema apresenta os produtos selecionados.
O usuário seleciona a opção "Comprar".
O sistema verifica os produtos e os valores.
O sistema registra o pedido após a confirmação das informações necessárias.
O sistema apresenta a confirmação da compra.
Saída: O pedido é registrado e o usuário recebe uma confirmação.
Regras de negócio:
O carrinho não pode estar vazio.
Os produtos devem estar disponíveis para compra.
O usuário deve visualizar os valores antes de confirmar o pedido.
Exceções:
Caso o carrinho esteja vazio, o sistema deve impedir a compra.
Caso algum produto esteja indisponível, o sistema deve informar o usuário.
Caso ocorra uma falha na compra, o sistema deve informar que o pedido não foi concluído.
RF006 — Pesquisar Produtos
Descrição: O sistema deve permitir que o usuário pesquise produtos de energia renovável pelo nome ou por palavras-chave.
Atores: Usuário.
Pré-condições: O usuário deve acessar a tela de pesquisa.
Entradas:
Nome do produto;
Palavra-chave.
Processamento:
O usuário acessa a tela de pesquisa.
O usuário digita o nome do produto desejado.
O sistema pesquisa os produtos correspondentes.
O sistema apresenta os resultados encontrados.
Saída: Uma lista de produtos relacionados à pesquisa é exibida.
Regras de negócio:
- A pesquisa deve considerar os produtos disponíveis no catálogo.
Exceções:
Caso nenhum produto seja encontrado, o sistema deve informar o usuário.
Caso o campo esteja vazio, o sistema pode apresentar todos os produtos disponíveis.
RF007 — Visualizar Detalhes dos Produtos
Descrição: O sistema deve permitir que o usuário visualize informações sobre um produto selecionado.
Atores: Usuário.
Pré-condições: O produto deve estar disponível no catálogo.
Entradas:
- Produto selecionado.
Processamento:
O usuário seleciona um produto na lista.
O sistema apresenta a tela de detalhes.
O sistema exibe o nome, a imagem e as informações disponíveis sobre o produto.
O sistema disponibiliza a opção de adicionar o produto ao carrinho, quando aplicável.
Saída: O usuário visualiza os detalhes do produto selecionado.
Regras de negócio:
- As informações apresentadas devem corresponder ao produto escolhido.
Exceções:
- Caso o produto não seja encontrado, o sistema deve informar o usuário.
RF008 — Adicionar Produtos ao Carrinho
Descrição: O sistema deve permitir que o usuário adicione produtos ao carrinho para comprá-los posteriormente.
Atores: Usuário.
Pré-condições: O produto deve existir no catálogo e estar disponível para compra.
Entradas:
Produto selecionado;
Quantidade desejada, quando aplicável.
Processamento:
O usuário seleciona um produto.
O usuário seleciona a opção de adicionar ao carrinho.
O sistema verifica a disponibilidade do produto.
O sistema adiciona o produto ao carrinho.
O sistema informa que o produto foi adicionado.
Saída: O produto é incluído no carrinho de compras.
Regras de negócio:
A quantidade adicionada deve ser válida.
O produto deve estar disponível para compra.
Exceções:
Caso o produto esteja indisponível, o sistema deve impedir sua inclusão.
Caso ocorra uma falha, o sistema deve informar que não foi possível adicionar o produto.
RF009 — Visualizar Lista de Entregas
Descrição: O sistema deve permitir que o usuário visualize a lista de entregas relacionadas aos seus pedidos.
Atores: Usuário.
Pré-condições: O usuário deve acessar a opção de lista de entregas.
Entradas:
- Solicitação de visualização da lista de entregas.
Processamento:
O usuário acessa a opção "Lista de entregas".
O sistema consulta os pedidos do usuário que possuem informações de entrega.
O sistema apresenta os pedidos e suas respectivas situações.
O usuário pode selecionar um pedido para visualizar mais informações, caso essa funcionalidade esteja disponível.
Saída: O usuário visualiza a lista de entregas e as informações disponíveis sobre seus pedidos.
Regras de negócio:
A lista deve apresentar somente pedidos relacionados ao usuário.
As informações devem corresponder à situação atual dos pedidos.
Exceções:
Caso não existam entregas registradas, o sistema deve informar o usuário.
Caso ocorra uma falha na consulta, o sistema deve informar que não foi possível carregar a lista.
RF010 — Visualizar Informações sobre a Ecodar
Descrição: O sistema deve permitir que o usuário consulte informações sobre a empresa Ecodar e sua atuação no setor de energia renovável.
Atores: Usuário.
Pré-condições: O usuário deve acessar a opção "Sobre nós".
Entradas:
- Solicitação de acesso à página "Sobre nós".
Processamento:
O usuário seleciona a opção "Sobre nós".
O sistema apresenta a página correspondente.
O sistema exibe as informações institucionais disponíveis sobre a Ecodar.
Saída: O usuário visualiza informações sobre a empresa.
Regras de negócio:
- As informações devem estar relacionadas à empresa e à sua atuação.
Exceções:
- Caso a página não possa ser carregada, o sistema deve informar o usuário.
RF011 — Visualizar Perfil
Descrição: O sistema deve permitir que o usuário acesse seu perfil para consultar suas informações pessoais.
Atores: Usuário.
Pré-condições: O usuário deve estar autenticado.
Entradas:
- Solicitação de acesso ao perfil.
Processamento:
O usuário seleciona a opção "Perfil".
O sistema identifica a conta autenticada.
O sistema consulta os dados do usuário.
O sistema apresenta as informações disponíveis.
Saída: O usuário visualiza as informações de seu perfil.
Regras de negócio:
- O usuário somente pode visualizar os dados de sua própria conta.
Exceções:
Caso o usuário não esteja autenticado, o sistema deve solicitar o login.
Caso ocorra uma falha ao carregar o perfil, o sistema deve informar o usuário.






Requisitos Não Funcionais — Ecodar
Os requisitos não funcionais definem como o aplicativo Ecodar deve funcionar, considerando aspectos como desempenho, segurança, usabilidade, compatibilidade e confiabilidade.
Como o projeto é um trabalho escolar, os requisitos abaixo são simples e adequados ao protótipo apresentado no Figma.
RNF001 — Usabilidade
Descrição: O sistema deve possuir uma interface simples e intuitiva, permitindo que os usuários utilizem suas funcionalidades sem dificuldades.
Categoria: Usabilidade.
Requisitos:
Os botões e ícones devem ser fáceis de identificar.
As opções de navegação devem ser organizadas de forma clara.
As informações dos produtos devem ser apresentadas de maneira legível.
Critério de aceitação: O usuário deve conseguir navegar entre as telas principais e encontrar os produtos sem precisar de instruções externas.
RNF002 — Desempenho
Descrição: O sistema deve apresentar respostas rápidas às ações realizadas pelo usuário.
Categoria: Desempenho.
Requisitos:
As páginas principais devem carregar em até 3 segundos em condições normais de uso.
As pesquisas de produtos devem apresentar resultados rapidamente.
As operações do carrinho devem atualizar as informações sem demora excessiva.
Critério de aceitação: As principais funcionalidades devem responder dentro do tempo estabelecido quando utilizadas em condições adequadas de conexão e processamento.
RNF003 — Segurança
Descrição: O sistema deve proteger os dados pessoais dos usuários e as informações relacionadas às suas contas.
Categoria: Segurança.
Requisitos:
As senhas devem ser armazenadas de forma segura.
O acesso ao perfil e aos pedidos deve ser restrito ao usuário autenticado correspondente.
As informações transmitidas entre o aplicativo e o servidor devem utilizar uma conexão segura.
Os dados de pagamento devem ser tratados de forma segura.
Critério de aceitação: Um usuário não deve conseguir acessar os dados pessoais ou os pedidos de outra conta sem autorização.
RNF004 — Compatibilidade
Descrição: O sistema deve funcionar adequadamente nos dispositivos e navegadores definidos para o projeto.
Categoria: Compatibilidade.
Requisitos:
A interface deve ser compatível com dispositivos móveis.
Os elementos da tela devem se adaptar a diferentes tamanhos de tela.
Caso o sistema seja disponibilizado como site, deve funcionar nos principais navegadores modernos.
Critério de aceitação: As telas devem permanecer legíveis e utilizáveis nos dispositivos e ambientes previstos para a aplicação.
RNF005 — Disponibilidade
Descrição: O sistema deve estar disponível para utilização sempre que o usuário precisar acessar suas funcionalidades, respeitando eventuais períodos de manutenção.
Categoria: Disponibilidade.
Requisitos:
O sistema deve estar disponível durante a maior parte do tempo.
Eventuais manutenções devem ser realizadas de forma a reduzir interrupções.
Caso o sistema fique indisponível, o usuário deve receber uma mensagem informativa quando possível.
Critério de aceitação: O usuário deve conseguir acessar as funcionalidades normalmente quando o sistema estiver operacional.
RNF006 — Confiabilidade
Descrição: O sistema deve executar suas operações corretamente, preservando a consistência das informações.
Categoria: Confiabilidade.
Requisitos:
Os valores do carrinho devem ser calculados corretamente.
Os produtos adicionados ou removidos devem ser atualizados adequadamente.
Os pedidos confirmados devem manter suas informações registradas.
O sistema não deve confirmar pagamentos que não tenham sido aprovados.
Critério de aceitação: As operações realizadas devem produzir resultados consistentes com as ações do usuário.
RNF007 — Facilidade de Manutenção
Descrição: O sistema deve ser desenvolvido de forma organizada para facilitar futuras correções e melhorias.
Categoria: Manutenibilidade.
Requisitos:
O código deve ser organizado e legível.
As funcionalidades devem ser separadas em partes que facilitem sua manutenção.
Os erros identificados devem poder ser corrigidos sem exigir a reconstrução de todo o sistema.
Critério de aceitação: Deve ser possível realizar alterações e correções no sistema sem comprometer desnecessariamente as demais funcionalidades.
RNF008 — Acessibilidade
Descrição: O sistema deve apresentar elementos que facilitem a utilização por pessoas com diferentes necessidades.
Categoria: Acessibilidade.
Requisitos:
Os textos devem possuir tamanho adequado para leitura.
Os botões devem apresentar identificação clara.
As informações importantes não devem ser transmitidas apenas por cores.
As imagens informativas devem possuir descrições textuais quando aplicável.
Critério de aceitação: As principais funcionalidades devem ser compreensíveis e utilizáveis por pessoas com diferentes necessidades de acesso.
RNF009 — Integridade dos Dados
Descrição: O sistema deve preservar a correção e a consistência das informações dos usuários, produtos e pedidos.
Categoria: Integridade.
Requisitos:
Os preços apresentados devem corresponder aos valores registrados para os produtos.
As quantidades do carrinho devem ser atualizadas corretamente.
Os dados dos pedidos devem ser preservados após sua confirmação.
O sistema deve validar as informações antes de registrá-las.
Critério de aceitação: As informações exibidas e armazenadas devem permanecer consistentes durante as operações realizadas.
RNF010 — Facilidade de Aprendizado
Descrição: O sistema deve permitir que novos usuários aprendam a utilizar suas funcionalidades com facilidade.
Categoria: Usabilidade.
Requisitos:
As funcionalidades devem utilizar nomes e símbolos fáceis de compreender.
A navegação entre as telas deve seguir um padrão consistente.
As mensagens de erro devem explicar o problema de maneira simples.
Critério de aceitação: Um usuário iniciante deve conseguir compreender as funções básicas do aplicativo após um breve contato com a interface.
RNF011 — Recuperação de Falhas
Descrição: O sistema deve lidar adequadamente com falhas, evitando a perda desnecessária de informações importantes.
Categoria: Confiabilidade.
Requisitos:
O sistema deve informar quando uma operação não puder ser concluída.
Os pedidos já confirmados devem ter seus registros preservados em caso de falha posterior.
O sistema deve evitar a duplicação de pedidos causada por tentativas repetidas de envio.
Critério de aceitação: Uma falha não deve provocar alterações indevidas nos pedidos ou confirmar operações que não foram concluídas.
RNF012 — Privacidade
Descrição: O sistema deve respeitar a privacidade dos usuários e utilizar seus dados pessoais apenas para finalidades adequadas ao funcionamento da plataforma.
Categoria: Privacidade.
Requisitos:
O sistema deve solicitar apenas os dados necessários para suas funcionalidades.
Os dados pessoais não devem ser exibidos para outros usuários sem autorização.
O tratamento dos dados deve respeitar a legislação aplicável, incluindo a Lei Geral de Proteção de Dados (LGPD).
Critério de aceitação: Os dados pessoais devem ser acessíveis somente conforme as permissões e finalidades previstas pelo sistema.
Resumo dos requisitos não funcionais
Código
Requisito
Categoria
RNF001
Usabilidade
Usabilidade
RNF002
Desempenho
Desempenho
RNF003
Segurança
Segurança
RNF004
Compatibilidade
Compatibilidade
RNF005
Disponibilidade
Disponibilidade
RNF006
Confiabilidade
Confiabilidade
RNF007
Facilidade de manutenção
Manutenibilidade
RNF008
Acessibilidade
Acessibilidade
RNF009
Integridade dos dados
Integridade
RNF010
Facilidade de aprendizado
Usabilidade
RNF011
Recuperação de falhas
Confiabilidade
RNF012
Privacidade
Privacidade

Observação para o trabalho: os critérios de aceitação e os valores de desempenho são metas propostas para o sistema, não características que já foram comprovadas pelo Figma. Como o protótipo representa principalmente a interface visual, esses requisitos deverão ser verificados quando as funcionalidades forem implementadas.







RN001 — Cadastro de Usuário
Descrição: Cada usuário deve possuir uma conta própria para acessar as funcionalidades que exigem autenticação.
O e-mail deve possuir um formato válido.
Não deve ser permitido cadastrar duas contas com o mesmo e-mail.
A senha deve atender aos critérios mínimos de segurança do sistema.
RN002 — Autenticação
Descrição: O acesso às funcionalidades restritas deve ser realizado por usuários autenticados.
O usuário deve informar credenciais válidas para entrar na conta.
Caso as credenciais estejam incorretas, o acesso deve ser negado.
O usuário somente poderá visualizar seus próprios dados pessoais e pedidos.
RN003 — Exibição de Produtos
Descrição: Os produtos apresentados no aplicativo devem corresponder aos itens disponíveis no catálogo da Ecodar.
Cada produto deve possuir nome e informações básicas.
Os produtos devem apresentar seus preços quando essa informação estiver disponível.
Produtos indisponíveis não devem ser oferecidos para compra.
RN004 — Pesquisa de Produtos
Descrição: A pesquisa deve apresentar produtos relacionados ao termo informado pelo usuário.
A pesquisa deve considerar os nomes e as informações disponíveis dos produtos.
Caso nenhum produto corresponda à pesquisa, o sistema deve informar que não foram encontrados resultados.
A pesquisa não deve apresentar produtos inexistentes no catálogo.
RN005 — Adição de Produtos ao Carrinho
Descrição: O usuário poderá adicionar produtos disponíveis ao carrinho de compras.
Somente produtos existentes no catálogo poderão ser adicionados.
A quantidade de cada produto deve ser um número inteiro positivo.
A quantidade solicitada não poderá ultrapassar o estoque disponível, quando houver controle de estoque.
A inclusão de um produto no carrinho não significa que a compra foi concluída.
RN006 — Remoção de Produtos do Carrinho
Descrição: O usuário poderá remover produtos que não deseja mais comprar.
Somente produtos presentes no carrinho poderão ser removidos.
Após a remoção, o valor total deve ser atualizado.
A remoção de um produto não deve alterar os demais itens do carrinho.
RN007 — Cálculo do Valor da Compra
Descrição: O sistema deve calcular corretamente o valor dos produtos selecionados.
O subtotal de cada produto deve corresponder ao preço unitário multiplicado pela quantidade.
O valor total deve corresponder à soma dos subtotais dos produtos.
Caso exista frete ou outro custo aplicável, ele deverá ser incluído no valor final.
Os valores devem ser apresentados ao usuário antes da confirmação da compra.
RN008 — Finalização da Compra
Descrição: A compra somente poderá ser concluída quando os requisitos necessários forem atendidos.
O carrinho deve conter pelo menos um produto.
Os produtos devem estar disponíveis para compra no momento da confirmação.
O usuário deve revisar os itens e os valores antes de confirmar o pedido.
O sistema deve registrar o pedido após a confirmação da compra.
Uma compra não poderá ser considerada paga sem a confirmação do pagamento, caso essa funcionalidade seja implementada.
RN009 — Lista de Entregas
Descrição: O usuário poderá consultar as informações de entrega de seus pedidos.
Cada entrega deve estar associada a um pedido.
O usuário somente poderá consultar entregas relacionadas à sua própria conta.
A situação da entrega deve corresponder às informações disponíveis no sistema.
Pedidos ainda não enviados devem ser identificados com sua situação atual, sem indicar que já foram entregues.
RN010 — Perfil do Usuário
Descrição: As informações do perfil devem ser acessíveis somente ao usuário correspondente.
O usuário deve estar autenticado para acessar seu perfil.
Os dados apresentados devem corresponder à conta autenticada.
Alterações nos dados devem ser validadas antes de serem salvas, caso a edição de perfil seja implementada.
RN011 — Navegação do Aplicativo
Descrição: O usuário deve conseguir acessar as funcionalidades pelas opções de navegação disponíveis.
Cada ícone ou botão deve direcionar para a funcionalidade correspondente.
A opção de carrinho deve abrir a tela do carrinho.
A opção de perfil deve abrir a tela de perfil.
A opção "Sobre nós" deve apresentar as informações institucionais da Ecodar.
RN012 — Informações sobre a Ecodar
Descrição: As informações institucionais apresentadas devem corresponder à empresa e à finalidade do aplicativo.
A página "Sobre nós" deve apresentar informações relacionadas à Ecodar.
O sistema não deve apresentar informações institucionais falsas como se fossem verdadeiras.
RN013 — Integridade dos Pedidos
Descrição: Os pedidos registrados devem preservar as informações referentes à compra realizada.
Cada pedido deve possuir uma identificação própria.
Os produtos, as quantidades e os valores devem corresponder ao pedido confirmado.
Os pedidos concluídos devem permanecer disponíveis no histórico, caso essa funcionalidade seja implementada.
Uma tentativa repetida de confirmação não deve gerar pedidos duplicados indevidamente.
RN014 — Proteção de Dados
Descrição: O sistema deve proteger as informações pessoais dos usuários.
As senhas devem ser armazenadas de forma segura.
Os dados pessoais não devem ser disponibilizados a outros usuários sem autorização.
As informações devem ser utilizadas conforme as finalidades do aplicativo e a legislação aplicável.
