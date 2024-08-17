# Projeto de Comunicação WebSerial e WebSocket

Este repositório configura um sistema de comunicação que integra uma porta serial, um servidor WebSocket e um cliente Unity WebGL. O objetivo é permitir que dados da porta serial sejam transmitidos para um cliente Unity WebGL por meio de um servidor WebSocket intermediário.

## Estrutura do Projeto

- **HTML/JavaScript**: Conecta à porta serial usando a API Web Serial e envia os dados para um servidor WebSocket.
- **Servidor WebSocket Python**: Recebe os dados do cliente HTML e os repassa para todos os clientes conectados.
- **Cliente Unity WebGL**: Conecta ao servidor WebSocket e recebe os dados transmitidos.

## Requisitos

- Python 3.x
- Node.js (se usar o WebSocket com Node.js)
- Navegador com suporte à API Web Serial (por exemplo, Google Chrome)
- Unity com suporte WebGL

## Configuração

### 1. Configuração do Servidor WebSocket

1. Certifique-se de ter o Python e a biblioteca `websockets` instalados. Você pode instalar a biblioteca com o seguinte comando:

    ```bash
    pip install websockets
    ```

2. Salve o código do servidor WebSocket Python em um arquivo, por exemplo, `server.py`.

3. Execute o servidor com:

    ```bash
    python server.py
    ```

### 2. Configuração do HTML/JavaScript

1. Salve o código HTML/JavaScript fornecido em um arquivo, por exemplo, `index.html`.

2. Abra o `index.html` em um navegador que suporte a API Web Serial para testar a comunicação com a porta serial e o servidor WebSocket.

### 3. Configuração do Cliente Unity WebGL

1. Crie um novo projeto Unity ou use um existente.

2. Adicione o código C# para WebSocket ao seu projeto Unity.

3. Compile o projeto para WebGL.

4. Certifique-se de que o cliente Unity WebGL está configurado para se conectar ao servidor WebSocket Python.
5. Melhor recurso pra tal: https://github.com/endel/NativeWebSocket?tab=readme-ov-file

## Uso

1. Conecte o dispositivo à porta serial e inicie o servidor WebSocket Python.

2. Abra o `index.html` no navegador e conecte à porta serial.

3. Inicie o cliente Unity WebGL e verifique se ele está recebendo mensagens do servidor WebSocket.

## Troubleshooting

- **Mensagens Fragmentadas**: Verifique se o terminador de mensagem está sendo usado corretamente e se a concatenação dos fragmentos está funcionando.
- **Conexão WebSocket**: Certifique-se de que o endereço do servidor WebSocket está correto e que o servidor está em execução.
- **Permissões de Porta Serial**: O navegador pode precisar de permissões para acessar a porta serial.

## Contribuição

Sinta-se à vontade para contribuir com melhorias, correções de bugs ou novas funcionalidades. Para contribuir, faça um fork do repositório, crie uma branch para suas alterações e envie um pull request.
