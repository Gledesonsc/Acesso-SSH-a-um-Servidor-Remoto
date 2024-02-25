# Documentação: Acesso SSH a um Servidor Remoto

## Visão Geral

Este documento fornece instruções para acessar um servidor remoto via SSH usando uma chave SSH específica.

## Requisitos

- Acesso à internet.
- Uma chave SSH válida.
- Permissões para executar o comando `sudo`.
- Endereço IP do servidor remoto.

## Passos

1. Abra um terminal no seu sistema operacional.

2. Digite o seguinte comando, substituindo `/caminho/para/sua/chave/privada` pelo caminho real onde sua chave privada está armazenada e `seu_usuario@seu_endereco_ip` pelo usuário e endereço IP do servidor remoto:
   
    ```
    sudo ssh -i /caminho/para/sua/chave/privada seu_usuario@seu_endereco_ip
    ```

    Por exemplo:
    ```
    sudo ssh -i /home/tvt/Documentos/SSH/ssh-key-git.key github@110.85.381.960
    ```

3. Pressione Enter para executar o comando.

4. Se solicitado, digite a senha do usuário atual para confirmar a execução do comando `sudo`.

5. Aguarde enquanto o sistema tenta estabelecer uma conexão SSH com o servidor remoto.

6. Se a autenticação for bem-sucedida, você será conectado ao servidor remoto e verá o prompt do terminal do servidor.

## Solução de Problemas

- **Erro "Permission denied (publickey)":** Isso indica que a chave pública não foi aceita pelo servidor remoto. Verifique se a chave pública está corretamente adicionada ao arquivo `~/.ssh/authorized_keys` no servidor remoto.

- **Permissões de Arquivo e Diretório:** Verifique se as permissões do diretório `.ssh` e do arquivo `authorized_keys` no servidor remoto estão configuradas corretamente. O diretório `~/.ssh` deve ter permissões `700` e o arquivo `authorized_keys` deve ter permissões `600`.

## Considerações Finais

- Certifique-se de manter suas chaves SSH seguras e não compartilhá-las com outras pessoas.
- Se necessário, entre em contato com o administrador do servidor remoto para obter assistência adicional.

---

Esta documentação fornece um guia rápido e fácil de entender para acessar um servidor remoto via SSH usando uma chave SSH específica. Se você encontrar problemas durante o processo, consulte a seção de solução de problemas ou procure assistência adicional conforme necessário.
