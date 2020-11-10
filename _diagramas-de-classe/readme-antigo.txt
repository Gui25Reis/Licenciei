# Diagrama
![Diagrama de Classes](https://github.com/Gui25Reis/Licenciei/blob/master/_diagramas-de-classe/diagrama-SEM-metodos.png)

# Dicionário
### Classe Pessoa
Classe responsável por ambos atores do sistema (cliente e empresa)
* Nome: Nome da pessoa ou da empresa responsável pelo perfil
* Telefone: Telefone para contato
* Pessoa: Tipo de pessoa (Física ou Jurídica)
* Endereço: Endereço de cobrança
* Email: Email para contato
###
* setPessoa(): Atribui o tipo de pessoa ao cadastro

### Classe Cliente
Classe responsável pelos métodos do cliente
* Cadastro: Classe pessoa com os dados de cadastro
* Licenças: Lista ligada de licenças adquiridas
###
* pesquisar(): Pesquisar produtos
* comprar(): Método para realizar a compra de uma licença
* cancelar(): Cancelar uma licença ativa
* renovar(): Renovar uma licença ativa
* gerenciar(): Método para gerenciar todas as licenças da conta, seja ativa ou inativa

### Classe Empresa
Classe responsável pelos métodos da empresa
* Cadastro: Classe pessoa com os dados de cadastro
* Licenças: Lista ligada de licença anunciadas
###
* adicionar_Licenca(): Adicionar uma licença para a venda
* deletar_Licenca(): Remover uma licença já existente
* atualizar_Licenca(): Atualizar dados de uma licença já existente
* gerenciar(): Método para gerenciar todas as licenças já anunciadas pela conta

### Classe Licença
Classe responsável pelo atributos de uma licença
* Nome: Nome da licença
* Valor: Valor da assinatura (mensal)
* Duração: Duração restante dessa licença
* Ativo: Booleano de verdadeiro ou falso caso a assinatura esteja ou não ativa
###
* resumo(): Retorna informações da licença
* combo(): Método responsável pelos descontos (se disponível) de assinaturas mais longas (ex: 12 meses de assinatura pelo valor de 10 meses)

### Classe Produtos
Classe responsável pela lista ligada de licenças
* lic: Classe Licença com os dados da licença
* prox_Lic: Ponteiro para a próxima licença da lista