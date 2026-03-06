# Token-do-zero

Para criar um Token do zero, siga estas etapas detalhadas:

# 1. Configurar a Metamask

1. Instalar a Metamask:
   - Acesse a [página da Metamask](https://metamask.io/) e faça o download da extensão.
   - Siga as instruções para instalar.

2. Criar uma Wallet:
   - Abra a extensão e clique em "Começar".
   - Selecione "Criar uma carteira".
   - Siga as instruções para definir uma senha e anote a frase de recuperação.

3. Adicionar uma Rede Personalizada (RPC):
   - Clique no ícone de conta no canto superior direito e em "Configurações".
   - Vá para "Redes" e clique em "Adicionar Rede".
   - Preencha os campos com informações da rede desejada (por exemplo, Binance Smart Chain, Avalanche, etc.).

# 2. Código Base do Token

Usaremos o padrão ERC20 como exemplo. Aqui está um código básico para um Token:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MeuToken is ERC20 {
    constructor(uint256 inicialSupply) ERC20("MeuToken", "MTK") {
        _mint(msg.sender, inicialSupply);
    }
}
```

# 3. Usando o Remix IDE

1. Acessar o Remix:
   - Vá para o [Remix IDE](https://remix.ethereum.org/).
   
2. Criar um Novo Arquivo:
   - No painel esquerdo, crie um novo arquivo chamado `MeuToken.sol` e cole o código acima.

3. Compilar o Contrato:
   - Vá para a aba "Solidity Compiler" (ícone de compilador).
   - Selecione a versão correta do compilador (deve ser compatível com a versão do código).
   - Clique em "Compilar MeuToken.sol".

4. Implantar o Token:
   - Vá para a aba "Deploy & Run Transactions" (ícone de Ethereum).
   - Selecione “Injected Web3” como ambiente para usar a Metamask.
   - Escolha o contrato `MeuToken` na lista e defina o `inicialSupply` (em unidades mínimas, como `1000000000000000000` para 1 token).
   - Clique em "Deploy" e aprove a transação na Metamask.

# 4. Confirmação e Teste

1. Verifique o Token:
   - Após o deploy, você pode ver seu token na sua wallet.
   - Para adicionar o token manualmente, use o contrato criado e insira o endereço na Metamask.

2. Teste Funcionalidades:
   - Você pode testar a transferência de tokens entre contas usando a Metamask.

# Conclusão

Seguindo esses passos, você terá criado e implantado seu próprio token na blockchain. Para aprimoramentos, considere implementar funcionalidades adicionais como queima de tokens, permissões, entre outros.
