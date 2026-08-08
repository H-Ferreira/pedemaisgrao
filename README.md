# PEDE MAIS GRÃO — publicação do site e aplicativo

Esta versão funciona como site responsivo e também como aplicativo instalável no celular.

## Arquivos que devem ser publicados no GitHub Pages

Mantenha esta estrutura na raiz do repositório:

```text
index.html
manifest.webmanifest
service-worker.js
backup-pede-mais-grao-2026-08-08.rcbackup
icons/
  apple-touch-icon.png
  icon-192.png
  icon-512.png
  icon-maskable-512.png
```

O arquivo `Code.gs` deve permanecer no projeto do Google Apps Script. Ele não é necessário no GitHub Pages.

## Instalação no celular

Ao abrir o endereço publicado pelo celular, aparece uma faixa **Instale o PEDE MAIS GRÃO**.

- Android: toque em **Instalar agora** e confirme.
- iPhone: toque em **Ver como instalar**. No Safari, use **Compartilhar → Adicionar à Tela de Início**, ative **Abrir como App** e confirme.

Depois da instalação, o sistema ganha um ícone na tela inicial e abre em uma janela própria. O aviso de instalação deixa de aparecer dentro do aplicativo instalado.

## Dados e sincronização

O endereço e a chave do Google Apps Script estão incorporados ao `index.html`. Configurações antigas guardadas pelo navegador são substituídas automaticamente pela conexão atual.

Os registros continuam sendo salvos de forma criptografada no aparelho e sincronizados pelo Google Apps Script. Quando estiver sem internet, o aplicativo continua abrindo e permite trabalhar com os dados locais; a sincronização é retomada quando a conexão voltar.

Em um navegador sem dados locais, o backup inicial é carregado e solicita a senha usada na criação dele. Um navegador que já possui dados não é substituído pelo backup inicial.

## Antes de publicar uma atualização

1. No aparelho com os dados mais recentes, use **Backup e segurança → Baixar backup atualizado**.
2. Se quiser atualizar também a base inicial, substitua o arquivo `.rcbackup` mantendo exatamente o mesmo nome.
3. Publique todos os arquivos e a pasta `icons` na mesma estrutura mostrada acima.
4. Abra o endereço publicado, atualize a página e confira **Sincronização em nuvem → Sincronizar agora**.

Quando o código do site for atualizado, o aplicativo instalado recebe a versão nova ao ser aberto novamente com internet.
