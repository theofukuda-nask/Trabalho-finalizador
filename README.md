RF001 — Fazer Cadastro
Descrição: O sistema deve permitir que novos usuários criem uma conta para acessar as funcionalidades da plataforma e realizar compras.

Atores: Usuário.

Pré-condições: O usuário não deve possuir uma conta cadastrada com o mesmo e-mail.

Entradas:
- Nome completo;
- E-mail;
- Senha;
- Confirmação de senha;
- Data de nascimento, quando necessária;
- Demais informações solicitadas pelo sistema.
Processamento:
1. O usuário acessa a opção "Criar conta".
2. O sistema apresenta o formulário de cadastro.
3. O usuário preenche os dados solicitados.
4. O sistema valida os campos obrigatórios.
5. O sistema verifica se o e-mail já está cadastrado.
6. O sistema verifica se a senha atende aos critérios de segurança e corresponde à confirmação.
7. O sistema registra a nova conta.
8. O sistema informa que o cadastro foi realizado com sucesso.
Saída: Uma nova conta de usuário é criada e fica disponível para autenticação.

Regras de negócio:
- O e-mail deve possuir um formato válido.
- O e-mail não pode estar associado a outra conta.
- A senha deve atender aos critérios mínimos de segurança.
- Todos os campos obrigatórios devem ser preenchidos.
Exceções:
- Caso algum campo obrigatório esteja vazio, o sistema deve informar o usuário.
- Caso o e-mail já esteja cadastrado, o sistema deve impedir o registro.
- Caso as senhas sejam diferentes, o sistema deve solicitar a correção.
- Caso os dados sejam inválidos, o cadastro não deve ser concluído.

RF002 — Fazer Login
Descrição: O sistema deve permitir que usuários cadastrados acessem suas contas por meio de suas credenciais.

Atores: Usuário cadastrado.

Pré-condições: O usuário deve possuir uma conta cadastrada.

Entradas:
- E-mail;
- Senha.
Processamento:
1. O usuário acessa a opção "Entrar".
2. O sistema apresenta o formulário de login.
3. O usuário informa seu e-mail e senha.
4. O sistema valida os dados informados.
5. O sistema verifica as credenciais.
6. O sistema autentica o usuário.
7. O sistema direciona o usuário para a página inicial ou para a página que desejava acessar.
Saída: O usuário acessa sua conta e pode utilizar as funcionalidades que exigem autenticação.

Regras de negócio:
- As credenciais devem corresponder a uma conta cadastrada.
- A senha deve ser verificada de forma segura.
- O sistema deve proteger a conta contra tentativas excessivas de acesso indevido.
Exceções:
- Caso os campos estejam vazios, o sistema deve solicitar o preenchimento.
- Caso as credenciais sejam inválidas, o sistema deve informar que não foi possível realizar o login.
- Caso ocorra uma falha de autenticação, o acesso não deve ser concedido.

RF003 — Recuperar Senha
Descrição: O sistema deve permitir que o usuário recupere o acesso à sua conta caso esqueça a senha.

Atores: Usuário cadastrado.

Pré-condições: O usuário deve ter uma conta cadastrada e acesso ao meio de recuperação associado a ela.

Entradas:
- E-mail cadastrado;
- Código ou link de recuperação;
- Nova senha;
- Confirmação da nova senha.
Processamento:
1. O usuário acessa a opção "Esqueci minha senha".
2. O sistema solicita o e-mail cadastrado.
3. O usuário informa o e-mail.
4. O sistema disponibiliza o procedimento de recuperação de forma segura.
5. O usuário confirma sua identidade pelo método solicitado.
6. O sistema apresenta o formulário para criação de uma nova senha.
7. O usuário informa e confirma a nova senha.
8. O sistema valida os dados e atualiza a senha.
9. O sistema informa que a senha foi redefinida.
Saída: A senha é redefinida e o usuário pode voltar a acessar sua conta.

Regras de negócio:
- A recuperação deve utilizar um método seguro de verificação.
- O código ou link de recuperação deve possuir prazo de validade.
- A nova senha deve atender aos critérios de segurança.
Exceções:
- Caso o e-mail seja inválido, o sistema deve solicitar sua correção.
- Caso o código esteja expirado ou seja inválido, o sistema deve solicitar uma nova recuperação.
- Caso as senhas sejam diferentes, o sistema deve solicitar a correção.
- Caso ocorra uma falha no processo, a senha não deve ser alterada.

RF004 — Visualizar Catálogo de Produtos
Descrição: O sistema deve permitir que os usuários visualizem os produtos de energia renovável disponíveis para consulta e compra.

Atores: Usuário e visitante.

Pré-condições: O catálogo de produtos deve estar disponível para consulta.

Entradas:
- Acesso à página de produtos;
- Categoria de produto, quando selecionada.
Processamento:
1. O usuário acessa a página de produtos.
2. O sistema consulta os produtos disponíveis para venda.
3. O sistema organiza os produtos por categorias.
4. O sistema apresenta os produtos com suas informações principais.
5. O usuário pode selecionar um produto para consultar seus detalhes.
Saída: O catálogo é exibido com os produtos disponíveis para consulta.

Regras de negócio:
- Somente produtos publicados para venda devem ser exibidos.
- Cada produto deve apresentar, no mínimo, nome, imagem, preço e disponibilidade.
- Os produtos podem ser organizados em categorias, como energia solar, eólica e acessórios.
Exceções:
- Caso não existam produtos disponíveis, o sistema deve informar que o catálogo está vazio.
- Caso ocorra uma falha no carregamento, o sistema deve informar que não foi possível exibir os produtos.

RF005 — Pesquisar Produtos
Descrição: O sistema deve permitir que os usuários pesquisem produtos específicos por meio de palavras-chave.

Atores: Usuário e visitante.

Pré-condições: O sistema deve disponibilizar um catálogo de produtos para pesquisa.

Entradas:
- Nome do produto;
- Marca;
- Modelo;
- Tipo ou categoria;
- Palavras-chave relacionadas ao produto.
Processamento:
1. O usuário acessa a barra de pesquisa.
2. O usuário informa o termo desejado.
3. O sistema realiza a pesquisa no catálogo.
4. O sistema identifica os produtos compatíveis com o termo informado.
5. O sistema apresenta os resultados encontrados.
6. O usuário pode acessar os detalhes de qualquer resultado.
Saída: Uma lista de produtos relacionados à pesquisa é apresentada ao usuário.

Regras de negócio:
- A pesquisa deve considerar os dados disponíveis dos produtos.
- Os resultados devem corresponder ao termo informado.
- O sistema deve permitir que a pesquisa seja realizada sem distinção entre letras maiúsculas e minúsculas.
Exceções:
- Caso nenhum produto corresponda à pesquisa, o sistema deve informar que nenhum resultado foi encontrado.
- Caso o campo de pesquisa esteja vazio, o sistema pode exibir o catálogo completo.
- Caso ocorra uma falha na pesquisa, o sistema deve informar o usuário.

RF006 — Filtrar e Ordenar Produtos
Descrição: O sistema deve permitir que os usuários filtrem e ordenem os produtos para facilitar a localização dos itens desejados.

Atores: Usuário e visitante.

Pré-condições: O catálogo deve conter produtos disponíveis para consulta.

Entradas:
- Categoria;
- Faixa de preço;
- Marca;
- Disponibilidade;
- Tipo de produto;
- Ordem de preço crescente ou decrescente;
- Ordem alfabética;
- Critério de relevância.
Processamento:
1. O usuário acessa o catálogo ou os resultados da pesquisa.
2. O sistema apresenta os filtros e as opções de ordenação disponíveis.
3. O usuário seleciona os critérios desejados.
4. O sistema aplica os filtros selecionados.
5. O sistema organiza os resultados conforme a ordenação escolhida.
6. O sistema apresenta a lista atualizada.
Saída: Uma lista de produtos filtrada e ordenada de acordo com os critérios escolhidos.

Regras de negócio:
- Os filtros devem considerar as informações cadastradas para cada produto.
- A ordenação deve respeitar o critério selecionado.
- O usuário deve poder remover os filtros aplicados.
Exceções:
- Caso nenhum produto corresponda aos critérios selecionados, o sistema deve informar que não foram encontrados resultados.
- Caso um filtro não esteja disponível para determinada categoria, ele não deve ser aplicado.
- Caso ocorra uma falha, o sistema deve informar que não foi possível atualizar os resultados.

RF007 — Visualizar Detalhes do Produto
Descrição: O sistema deve permitir que o usuário consulte informações detalhadas sobre cada produto disponível no catálogo.

Atores: Usuário e visitante.

Pré-condições: O produto deve existir no catálogo.

Entradas:

- Seleção de um produto no catálogo ou nos resultados da pesquisa.

Processamento:
1. O usuário seleciona um produto.
2. O sistema consulta as informações correspondentes.
3. O sistema apresenta o nome, a descrição, as imagens e o preço.
4. O sistema apresenta a marca, o modelo e as especificações técnicas disponíveis.
5. O sistema informa a disponibilidade do produto.
6. O sistema apresenta as opções de quantidade e de compra, quando aplicáveis.
Saída: A página de detalhes do produto é exibida com as informações necessárias para auxiliar a decisão de compra.

Regras de negócio:
- As informações apresentadas devem corresponder ao produto selecionado.
- O preço e a disponibilidade devem refletir os dados atuais do sistema.
- As especificações técnicas devem ser apresentadas conforme as informações disponíveis para o produto.
Exceções:
- Caso o produto não exista ou não esteja mais disponível para consulta, o sistema deve informar o usuário.
- Caso alguma informação não esteja disponível, o sistema não deve apresentar dados inventados.
- Caso ocorra uma falha no carregamento, o sistema deve informar que não foi possível exibir os detalhes.

RF008 — Gerenciar Carrinho de Compras
Descrição: O sistema deve permitir que os usuários adicionem, consultem, atualizem e removam produtos do carrinho de compras.

Atores: Usuário.

Pré-condições: O usuário deve acessar o carrinho de compras e os produtos adicionados devem existir no catálogo.

Entradas:
- Produto selecionado;
- Quantidade desejada;
- Solicitação para alterar ou remover um item.
Processamento:
1. O usuário seleciona um produto.
2. O usuário informa a quantidade desejada.
3. O sistema verifica a disponibilidade do produto.
4. O sistema adiciona o item ao carrinho.
5. O usuário pode visualizar os itens adicionados.
6. O usuário pode alterar a quantidade ou remover itens.
7. O sistema recalcula os valores dos itens e o total do carrinho.
8. O sistema apresenta o carrinho atualizado.
Saída: O carrinho de compras é atualizado e apresenta os produtos selecionados, suas quantidades e seus valores.

Regras de negócio:
- A quantidade deve ser um número inteiro positivo, respeitando as condições de venda do produto.
- A quantidade solicitada não pode ultrapassar a disponibilidade informada.
- O subtotal de cada item deve corresponder ao preço unitário multiplicado pela quantidade.
- O carrinho deve apresentar o valor total dos produtos.
Exceções:
- Caso o produto esteja indisponível, o sistema deve impedir sua inclusão.
- Caso a quantidade seja inválida, o sistema deve solicitar a correção.
- Caso a quantidade ultrapasse o estoque disponível, o sistema deve informar o limite permitido.
- Caso o produto deixe de estar disponível após sua inclusão, o sistema deve informar o usuário.

RF009 — Calcular Frete e Prazo de Entrega
Descrição: O sistema deve permitir que os usuários consultem o custo e o prazo estimado de entrega dos produtos antes de finalizar a compra.

Atores: Usuário.

Pré-condições: O carrinho deve possuir pelo menos um produto e o sistema deve dispor das informações necessárias para estimar a entrega.

Entradas:
- CEP de destino;
- Produtos do carrinho;
- Quantidades dos produtos.
Processamento:
1. O usuário acessa o carrinho ou a etapa de entrega.
2. O sistema solicita o CEP de destino.
3. O usuário informa o CEP.
4. O sistema verifica a validade do CEP.
5. O sistema consulta as opções de entrega disponíveis.
6. O sistema calcula ou consulta o custo do frete e o prazo estimado.
7. O sistema apresenta as opções encontradas ao usuário.
Saída: O usuário visualiza os valores de frete e os prazos estimados de entrega disponíveis para seu endereço.

Regras de negócio:
- O cálculo deve considerar o destino e as características dos produtos.
- O prazo deve ser apresentado como uma estimativa.
- Os custos de entrega devem ser apresentados antes da confirmação do pedido.
Exceções:
- Caso o CEP seja inválido, o sistema deve solicitar sua correção.
- Caso não exista entrega disponível para o endereço, o sistema deve informar o usuário.
- Caso o serviço de cálculo de frete esteja indisponível, o sistema deve informar que não foi possível realizar a consulta.

RF010 — Realizar Compra
Descrição: O sistema deve permitir que o usuário finalize a compra dos produtos selecionados no carrinho.

Atores: Usuário.

Pré-condições:
- O usuário deve estar autenticado.
- O carrinho deve conter pelo menos um produto.
- Os produtos devem estar disponíveis para compra.
Entradas:
- Produtos e quantidades;
- Endereço de entrega;
- Opção de frete;
- Forma de pagamento;
- Dados necessários para concluir a compra.
Processamento:
1. O usuário acessa o carrinho.
2. O sistema apresenta os produtos, as quantidades e os valores.
3. O usuário confirma os itens que deseja comprar.
4. O sistema solicita ou apresenta o endereço de entrega.
5. O usuário seleciona a opção de entrega.
6. O sistema calcula o subtotal, o frete e o valor total.
7. O sistema apresenta as formas de pagamento disponíveis.
8. O usuário seleciona a forma de pagamento.
9. O sistema apresenta um resumo da compra.
10. O usuário confirma o pedido.
11. O sistema valida novamente os preços e a disponibilidade dos produtos.
12. O sistema registra o pedido e encaminha o pagamento para processamento.
13. O sistema informa o resultado da operação e o estado do pedido.
Saída: Um pedido de compra é registrado, com seus produtos, valores, endereço de entrega, forma de pagamento e situação atual.

Regras de negócio:
- O pedido deve conter pelo menos um produto.
- O valor total deve incluir os produtos e os custos adicionais aplicáveis, como frete.
- O pedido somente deve ser considerado pago após a confirmação do pagamento.
- O sistema deve evitar a duplicação de pedidos em caso de repetição acidental da solicitação.
- O usuário deve ter a oportunidade de revisar o pedido antes de confirmá-lo.
Exceções:
- Caso o carrinho esteja vazio, o sistema deve impedir a finalização.
- Caso um produto fique indisponível, o sistema deve informar o usuário e solicitar a atualização do carrinho.
- Caso o pagamento seja recusado, o sistema deve informar o usuário sem indicar a compra como paga.
- Caso ocorra uma falha no registro do pedido, o sistema deve informar que a operação não foi concluída.
- Caso os dados de entrega estejam incompletos, o sistema deve solicitar sua correção.

RF011 — Gerenciar Endereços de Entrega
Descrição: O sistema deve permitir que o usuário cadastre, consulte, altere e remova seus endereços de entrega.

Atores: Usuário cadastrado.

Pré-condições: O usuário deve estar autenticado.

Entradas:
- Nome do destinatário;
- CEP;
- Logradouro;
- Número;
- Complemento, quando necessário;
- Bairro;
- Cidade;
- Estado;
- Identificação opcional do endereço, como "Casa" ou "Trabalho".
Processamento:
1. O usuário acessa a área de endereços.
2. O sistema apresenta os endereços cadastrados.
3. O usuário escolhe cadastrar um novo endereço ou alterar um existente.
4. O sistema apresenta o formulário correspondente.
5. O usuário preenche ou modifica as informações.
6. O sistema valida os campos obrigatórios.
7. O sistema salva as alterações.
8. O sistema apresenta a lista atualizada de endereços.
Saída: O endereço é cadastrado, atualizado, consultado ou removido conforme a solicitação do usuário.

Regras de negócio:
- Os campos obrigatórios devem ser preenchidos.
- O CEP deve possuir um formato válido.
- Um endereço associado a um pedido já realizado deve ser preservado no histórico daquele pedido.
Exceções:
- Caso existam dados obrigatórios ausentes, o sistema deve solicitar seu preenchimento.
- Caso o CEP seja inválido, o sistema deve informar o usuário.
- Caso o endereço esteja associado a um pedido e não possa ser removido, o sistema deve informar a restrição.

RF012 — Selecionar Forma de Pagamento
Descrição: O sistema deve permitir que o usuário selecione uma das formas de pagamento disponíveis para concluir a compra.

Atores: Usuário.

Pré-condições:
- O usuário deve estar autenticado.
- O carrinho deve conter produtos.
- O sistema deve disponibilizar pelo menos uma forma de pagamento.
Entradas:
- Forma de pagamento escolhida, como Pix, cartão de crédito, cartão de débito ou boleto, conforme disponibilidade;
- Dados necessários para a modalidade selecionada.
Processamento:
1. O usuário acessa a etapa de pagamento.
2. O sistema apresenta as formas de pagamento disponíveis.
3. O usuário seleciona uma modalidade.
4. O sistema solicita os dados necessários para aquela modalidade.
5. O usuário informa ou confirma os dados.
6. O sistema valida as informações.
7. O sistema encaminha a transação ao serviço de pagamento.
8. O sistema apresenta o resultado da transação.
Saída: A forma de pagamento é selecionada e a transação é encaminhada para processamento, com o resultado registrado no pedido.

Regras de negócio:
- Somente formas de pagamento habilitadas devem ser apresentadas.
- Os dados de pagamento devem ser tratados de forma segura.
- O sistema deve apresentar o estado do pagamento de forma clara.
- Dados sensíveis de cartão não devem ser armazenados de maneira insegura.
Exceções:
- Caso os dados sejam inválidos, o sistema deve solicitar sua correção.
- Caso o pagamento seja recusado, o sistema deve informar o usuário.
- Caso o serviço de pagamento esteja indisponível, o sistema deve informar que não foi possível processar a transação.
- Caso o pagamento esteja pendente, o sistema deve apresentar essa situação sem indicar aprovação.

RF013 — Visualizar Histórico de Pedidos
Descrição: O sistema deve permitir que o usuário consulte o histórico de compras realizadas em sua conta.

Atores: Usuário cadastrado.

Pré-condições: O usuário deve estar autenticado.

Entradas:
- Solicitação de acesso ao histórico;
- Filtros opcionais por período, número do pedido ou situação.
Processamento:
1. O usuário acessa a opção "Meus pedidos".
2. O sistema consulta os pedidos associados à conta autenticada.
3. O sistema organiza os pedidos por data.
4. O sistema apresenta informações resumidas de cada pedido.
5. O usuário seleciona um pedido para consultar seus detalhes.
6. O sistema apresenta os produtos, valores, data da compra e situação do pedido.
Saída: O usuário visualiza seus pedidos anteriores e os detalhes de cada compra.

Regras de negócio:
- O usuário somente pode consultar pedidos associados à sua própria conta.
- Os pedidos devem apresentar informações consistentes com o registro da compra.
- Os valores e os produtos de pedidos concluídos devem ser preservados no histórico.
Exceções:
- Caso o usuário não possua pedidos, o sistema deve informar que não existem compras registradas.
- Caso o pedido solicitado não exista ou não pertença ao usuário, o sistema deve impedir sua visualização.
- Caso ocorra uma falha na consulta, o sistema deve informar o usuário.

RF014 — Acompanhar Entrega do Pedido
Descrição: O sistema deve permitir que o usuário acompanhe a situação de entrega de um pedido realizado.

Atores: Usuário cadastrado.

Pré-condições: O usuário deve estar autenticado e possuir um pedido com informações de entrega disponíveis.

Entradas:
- Seleção de um pedido;
- Solicitação de consulta ao rastreamento.
Processamento:
1. O usuário acessa a opção "Meus pedidos".
2. O usuário seleciona o pedido desejado.
3. O sistema consulta a situação atual do pedido.
4. O sistema apresenta o estado da compra, como pagamento pendente, pagamento aprovado, em preparação, enviado ou entregue.
5. Quando disponível, o sistema apresenta o código e o link de rastreamento.
6. O sistema apresenta as atualizações de entrega recebidas.
Saída: O usuário visualiza a situação atual do pedido e as informações de rastreamento disponíveis.

Regras de negócio:
- O acompanhamento deve apresentar informações correspondentes ao pedido selecionado.
- O rastreamento somente deve ser apresentado quando existir um código ou serviço de acompanhamento disponível.
- Os estados apresentados devem corresponder às informações recebidas pelo sistema.
Exceções:
- Caso o pedido ainda não tenha sido enviado, o sistema deve informar sua situação atual.
- Caso não exista código de rastreamento, o sistema deve informar que o acompanhamento detalhado ainda não está disponível.
- Caso ocorra uma falha na consulta, o sistema deve informar que não foi possível atualizar o rastreamento.

RF015 — Cancelar Pedido
Descrição: O sistema deve permitir que o usuário solicite o cancelamento de um pedido, respeitando as condições aplicáveis à situação da compra.

Atores: Usuário cadastrado.

Pré-condições: O usuário deve estar autenticado e possuir um pedido elegível para cancelamento.

Entradas:
- Pedido selecionado;
- Solicitação de cancelamento;
- Motivo do cancelamento, quando solicitado.
Processamento:
1. O usuário acessa a área "Meus pedidos".
2. O usuário seleciona o pedido desejado.
3. O sistema verifica a situação do pedido e as condições de cancelamento.
4. O sistema apresenta a opção de cancelamento, caso disponível.
5. O usuário solicita o cancelamento.
6. O sistema apresenta as informações e as possíveis consequências da solicitação.
7. O usuário confirma a solicitação.
8. O sistema registra o pedido de cancelamento ou efetua o cancelamento, conforme as regras aplicáveis.
9. O sistema apresenta o resultado ao usuário.
Saída: A solicitação de cancelamento é registrada ou o pedido é cancelado, conforme sua situação e as regras aplicáveis.

Regras de negócio:
- O cancelamento deve respeitar a situação do pedido e as condições de compra.
- Pedidos já enviados podem exigir um procedimento diferente de cancelamento.
- Quando aplicável, o sistema deve informar o procedimento de reembolso.
- O usuário deve receber a confirmação do resultado da solicitação.
Exceções:
- Caso o pedido não pertença ao usuário, a operação deve ser impedida.
- Caso o pedido não possa ser cancelado diretamente, o sistema deve informar as alternativas disponíveis.
- Caso ocorra uma falha na solicitação, o sistema deve informar o usuário.

RF016 — Avaliar Produtos
Descrição: O sistema deve permitir que usuários que adquiriram determinado produto registrem avaliações sobre ele.

Atores: Usuário cadastrado.

Pré-condições: O usuário deve estar autenticado e atender aos critérios definidos para avaliar o produto, como possuir uma compra elegível.

Entradas:
- Produto avaliado;
- Nota;
- Comentário opcional;
- Data da avaliação, gerada pelo sistema.
Processamento:
1. O usuário acessa os detalhes do produto ou a área de compras.
2. O sistema verifica se o usuário pode avaliar o produto.
3. O sistema apresenta o formulário de avaliação.
4. O usuário seleciona uma nota e, opcionalmente, escreve um comentário.
5. O sistema valida os dados informados.
6. O sistema registra a avaliação.
7. O sistema disponibiliza a avaliação conforme as regras de publicação.
8. O sistema informa que a avaliação foi registrada.
Saída: A avaliação fica registrada e pode ser apresentada na página do produto.

Regras de negócio:
- A nota deve respeitar a escala definida pelo sistema, por exemplo, de 1 a 5 estrelas.
- O usuário deve cumprir os critérios de elegibilidade para avaliar.
- O sistema deve impedir avaliações duplicadas para a mesma compra e produto, conforme sua política.
- Os comentários devem respeitar as regras de utilização da plataforma.
Exceções:
- Caso a nota não seja informada ou seja inválida, a avaliação não deve ser registrada.
- Caso o usuário não esteja autorizado a avaliar o produto, o sistema deve informar a restrição.
- Caso ocorra uma falha no registro, o sistema deve informar que a avaliação não foi concluída.

RF017 — Visualizar Avaliações dos Produtos
Descrição: O sistema deve permitir que os usuários consultem as avaliações feitas por outros compradores para auxiliar na decisão de compra.

Atores: Usuário e visitante.

Pré-condições: O produto deve existir no catálogo.

Entradas:
- Seleção do produto;
- Filtros opcionais de nota;
- Critério de ordenação das avaliações.
Processamento:
1. O usuário acessa os detalhes de um produto.
2. O sistema consulta as avaliações disponíveis.
3. O sistema calcula ou consulta a nota média do produto.
4. O sistema apresenta as notas e os comentários publicados.
5. O usuário pode filtrar ou ordenar as avaliações, quando disponível.
Saída: As avaliações e a nota média do produto são apresentadas ao usuário.

Regras de negócio:
- Somente avaliações publicadas devem ser exibidas.
- A nota média deve ser calculada com base nas avaliações válidas.
- O sistema deve distinguir avaliações verificadas de outras avaliações, quando esse recurso existir.
Exceções:
- Caso o produto não possua avaliações, o sistema deve informar que ainda não existem opiniões registradas.
- Caso ocorra uma falha na consulta, o sistema deve informar o usuário.

RF018 — Adicionar Produtos à Lista de Favoritos
Descrição: O sistema deve permitir que o usuário salve produtos de seu interesse em uma lista de favoritos para consultá-los posteriormente.

Atores: Usuário cadastrado.

Pré-condições: O usuário deve estar autenticado e o produto deve existir no catálogo.

Entradas:
- Produto selecionado;
- Solicitação de inclusão ou remoção dos favoritos.
Processamento:
1. O usuário acessa o catálogo ou os detalhes de um produto.
2. O usuário seleciona a opção "Adicionar aos favoritos".
3. O sistema verifica se o produto já está na lista.
4. O sistema registra o produto nos favoritos.
5. O usuário pode acessar a área de favoritos para visualizar os itens salvos.
6. O usuário pode remover produtos da lista.
7. O sistema atualiza a lista e informa o resultado da operação.
Saída: A lista de favoritos é atualizada e fica disponível para consulta pelo usuário.

Regras de negócio:
- Cada usuário deve possuir sua própria lista de favoritos.
- O mesmo produto não deve aparecer duplicado na lista.
- Adicionar um produto aos favoritos não deve adicioná-lo automaticamente ao carrinho.
Exceções:
- Caso o usuário não esteja autenticado, o sistema deve solicitar o login.
- Caso o produto não exista mais no catálogo, o sistema deve informar sua indisponibilidade.
- Caso ocorra uma falha ao salvar a alteração, o sistema deve informar o usuário.

RF019 — Editar Dados do Perfil
Descrição: O sistema deve permitir que o usuário visualize e atualize as informações pessoais associadas à sua conta.

Atores: Usuário cadastrado.

Pré-condições: O usuário deve estar autenticado.

Entradas:
- Nome completo;
- E-mail, quando permitido;
- Telefone;
- Data de nascimento, quando solicitada;
- Demais informações pessoais editáveis.
Processamento:
1. O usuário acessa a área "Meu perfil".
2. O sistema apresenta os dados cadastrados.
3. O usuário seleciona a opção de edição.
4. O sistema apresenta os campos editáveis.
5. O usuário altera as informações desejadas.
6. O sistema valida os dados.
7. O sistema solicita uma confirmação adicional, quando necessária.
8. O sistema salva as alterações.
9. O sistema apresenta os dados atualizados.
Saída: As informações do perfil são atualizadas conforme os dados fornecidos pelo usuário.

Regras de negócio:
- Os campos obrigatórios devem conter informações válidas.
- O e-mail, quando alterado, deve passar pelas validações necessárias.
- Alterações em informações sensíveis podem exigir confirmação de identidade.
Exceções:
- Caso algum campo obrigatório esteja vazio, o sistema deve solicitar seu preenchimento.
- Caso o novo e-mail já esteja associado a outra conta, a alteração deve ser impedida.
- Caso os dados sejam inválidos, o sistema não deve salvar as alterações.

RF020 — Alterar Senha
Descrição: O sistema deve permitir que o usuário altere a senha de sua conta por meio de um procedimento seguro.

Atores: Usuário cadastrado.

Pré-condições: O usuário deve estar autenticado.

Entradas:
- Senha atual;
- Nova senha;
- Confirmação da nova senha.
Processamento:
1. O usuário acessa as configurações de segurança da conta.
2. O sistema apresenta o formulário de alteração de senha.
3. O usuário informa a senha atual e a nova senha.
4. O usuário confirma a nova senha.
5. O sistema verifica a senha atual.
6. O sistema valida os critérios de segurança da nova senha.
7. O sistema verifica se a confirmação corresponde à nova senha.
8. O sistema atualiza a senha.
9. O sistema informa que a alteração foi concluída.
Saída: A senha da conta é atualizada.

Regras de negócio:
- A senha atual deve ser válida.
- A nova senha deve atender aos critérios de segurança.
- A confirmação deve corresponder à nova senha.
- A senha deve ser armazenada de forma segura.
Exceções:
- Caso a senha atual esteja incorreta, a alteração não deve ser realizada.
- Caso a nova senha seja inválida, o sistema deve informar os critérios necessários.
- Caso as senhas sejam diferentes, o sistema deve solicitar a correção.
- Caso ocorra uma falha, o sistema deve informar que a alteração não foi concluída.
