Passo 1: Criar uma Nova Ramificação "melhorias"
No terminal ou prompt de comando, navegue até o diretório do seu projeto Git e execute os seguintes comandos: 
git branch melhorias  # Cria uma nova ramificação chamada "melhorias"
git checkout melhorias  # Muda para a ramificação "melhorias"

Passo 2: Implementar as Funcionalidades
Operação de venderProduto() em ProdutosDAO:
Dentro da classe ProdutosDAO, implemente o método venderProduto() para atualizar o status de um produto para "Vendido". Você precisará usar uma instrução SQL para atualizar o status no banco de dados.

Operação de listarProdutosVendidos() em ProdutosDAO:
Implemente o método listarProdutosVendidos() em ProdutosDAO para buscar produtos com status "Vendido" no banco de dados e retornar uma lista de produtos vendidos.

Implementar Tela de Vendas (VendasView):
Crie uma nova classe VendasView para exibir os produtos vendidos. Esta classe deve interagir com ProdutosDAO para obter a lista de produtos vendidos e exibi-los na interface gráfica.

Implementar Funcionalidade de Venda na Tela de Listagem:
Na tela de listagem existente (provavelmente na classe listagemVIEW), atualize o botão "Vender" para chamar o método venderProduto() de ProdutosDAO quando um produto for vendido.

Implementar Navegação para Tela de Vendas:
No botão "Consultar Vendas" da tela de listagem, implemente um evento para abrir a tela de VendasView.

Passo 3: Realizar Commits e Pushes
No terminal ou prompt de comando, dentro do diretório do seu projeto Git, adicione, faça commits e envie as alterações para o repositório remoto:
git add .  # Adiciona todas as alterações para o commit
git commit -m "Implementadas funcionalidades: venderProduto, listarProdutosVendidos, tela de Vendas"
git push origin melhorias  # Envia os commits para a ramificação "melhorias" no repositório remoto

Passo 4: Mesclar a Ramificação "melhorias" com a Ramificação Principal:
git checkout main  # Muda de volta para a ramificação principal
git merge melhorias  # Mescla as alterações da ramificação "melhorias" na ramificação principal
git push origin main  # Envia os commits mesclados para o repositório remoto na ramificação principal

