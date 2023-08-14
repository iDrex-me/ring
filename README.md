## Documentação: Ring - iDrex.me

### Descrição

O projeto Ring - iDrex.me é um webapp simples que, ao ser acessado, exibe uma pergunta ao usuário: "Você quer namorar comigo?" (ou sua tradução, dependendo do idioma do navegador). O usuário tem a opção de responder "Sim" ou "Não". Ao selecionar "Sim", é exibido um segundo modal que permite ao usuário enviar uma mensagem via Telegram ou WhatsApp.

### URL Estrutura

A URL segue o seguinte formato:

```
https://ring.idrex.me/?type=TIPO&number=XXXXXXXXXXXXX
```

- `TIPO`: Pode ser `tg` (para Telegram) ou `wa` (para WhatsApp).
- `XXXXXXXXXXXXX`: É o número de telefone associado à conta do Telegram ou WhatsApp.

#### Exemplos

- Para o WhatsApp: `https://ring.idrex.me/?type=wa&number=0123456789`
- Para o Telegram: `https://ring.idrex.me/?type=tg&number=0123456789`

### Funcionalidades Principais

1. **Detecção de Idioma**: O webapp detecta automaticamente o idioma do navegador do usuário e exibe a pergunta e as opções de resposta no idioma detectado. Atualmente, suporta Inglês (en), Português (pt) e Espanhol (es). Novos idiomas podem ser facilmente adicionados ao objeto `translations`.

2. **Manipulação do Modal**: Quando o usuário clica em "Não", é exibida uma mensagem de erro. Quando clica em "Sim", o primeiro modal é ocultado e o segundo modal é exibido, com um link para enviar uma mensagem pelo meio de comunicação escolhido na URL.

3. **Integração com WhatsApp e Telegram**: Ao clicar para enviar uma mensagem no segundo modal, o usuário é redirecionado para o WhatsApp ou Telegram (conforme especificado na URL) com uma mensagem predefinida.

### Personalização e Extensão

1. **Adicionando Novos Idiomas**: Para adicionar um novo idioma, basta adicionar as traduções no objeto `translations`. Por exemplo, para adicionar francês:

```javascript
fr: {
  greeting: "Voulez-vous sortir avec moi?",
  // ... outras traduções
}
```

2. **Modificação do Design**: O design pode ser facilmente modificado através do código CSS presente no arquivo. O ícone central é um SVG e também pode ser personalizado.

3. **Integração com Outros Apps de Mensagem**: Se você deseja adicionar suporte a outros aplicativos de mensagens além do WhatsApp e Telegram, você precisará modificar a função JavaScript que lida com os parâmetros da URL e adicionar a lógica de redirecionamento para o novo app.

### Conclusão

Este é um webapp simples, mas eficaz para fazer uma proposta única. Pode ser facilmente personalizado e estendido conforme necessário. Se você tiver alguma dúvida ou precisar de assistência adicional, sinta-se à vontade para perguntar.
