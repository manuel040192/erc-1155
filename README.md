# erc-1155
ERC1155

Datos relevantes:

- safeTransferFrom se usa para las transferencias delegadas y las transferencias normales de tokens. Como en el caso del ERC721, al transferir tokens es necesario especificar el id de los tokens que se vayan a transferir, y también se puede enviar algo de datos al recipiente si se enviará a un contrato inteligente. En todos los casos se requiere que si el recipiente es un smart contract, ese contrato debe implementar la interfaz receptora de ERC1155, la cual se llama ERC1155TokenReceiver, y la cual contiene dos funciones, onERC1155Received y onERC1155BatchReceived.

- La función balanceOf da el balance de un token id específico en una dirección específica. 

- La función balanceOf Batch da un balance conformado por un array de direcciones y un array de token id's. Eso es útil cuando se quiere saber el balance de un conjunto de tokens en cada una de las direcciones de un conjunto de direcciones.

- La función setApprovalForAll da permiso usando un boolean a un operador a que gaste los tokens de un propietario.

- La función isApprovedForAll dice usando un boolean si es que una dirección de un operador ha sido aprobada para poder gastar los tokens de la dirección de un propietario. Una vez que un operador ha sido aprobado, éste llamará a la función safeTransferFrom o a la función safeBatchTransferFrom. 

- En la interfaz ERC1155Metadata_URI, está la función uri que toma como argumento a un token id y da una URL que lleva a un json que tiene la metadata de unos tokens, y esa metadata uno la definirá afuera de la blockchain.
No hay metadata global para los tokens ERC1155, es decir, no hay funciones de nombre, de símbolo, o de decimales de los tokens, y eso es manejado individualmente para cada token afuera de la blockchain. 

Highlighted facts:

- safeTransferFrom is used for delegate transfers and normal transfers of tokens. As is the case with ERC721, when transferring tokens it's necessary to specify the ID of the tokens that will be transferred, and some data can also be sent to the recipient if one will send to a smart contract. In all cases, it's required that if the recipient will be a smart contract, that contract must implement the ERC1155 recipient interface called ERC1155TokenReceiver, which contains two functions, onERC1155Received and onERC1155BatchReceived.

- The balanceOf function returns the balance of a specific token id at a specific address.

- The balanceOf Batch function returns a balance made up of an array of addresses and an array of token id's. This is useful when you want to know the balance of a set of tokens in each of the addresses of a set of addresses.

- The setApprovalForAll function gives permission to an operator, using a boolean, to spend an owner's tokens.

- The isApprovedForAll function, using a boolean, tells whether an operator's address has been approved to spend tokens from an owner's address. Once an operator has been approved, they will call the safeTransferFrom function or the safeBatchTransferFrom function.

- In the ERC1155Metadata_URI interface, there's the uri function that takes a token ID as an argument and returns a URL where there's a json that has the metadata of some tokens, and that metadata will be defined outside of the blockchain. There's no global metadata for ERC1155 tokens, i.e. no functions of token name, symbol or decimals, and those things are handled individually for each token outside of the blockchain. 
