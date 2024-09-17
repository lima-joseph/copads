# Sistema de Resgate de Conquistas

Este projeto é uma página web para resgate de conquistas, onde os usuários podem inserir códigos para desbloquear conquistas específicas. Quando todas as conquistas são resgatadas, uma mensagem de vitória aparece na tela, juntamente com um ícone de celebração.

`Ver no GitHub Pages:` https://lima-joseph.github.io/copads/testes.html

## Funcionalidades

- **Resgate de Conquistas**: Os usuários podem resgatar conquistas inserindo códigos válidos.
- **Armazenamento Local**: As conquistas resgatadas são salvas no `localStorage` do navegador, permitindo que o progresso do usuário seja mantido mesmo ao recarregar a página.
- **Verificação de Conquistas Completas**: Se todas as conquistas forem resgatadas, a seção de resgate desaparece e uma mensagem de parabéns é exibida.
- **Efeitos Visuais**: As conquistas adquiridas são destacadas, e um efeito de preto e branco é aplicado aos cards de conquistas como indicativo de que foram desbloqueadas.

## Estrutura de Códigos de Conquista

Os códigos de conquistas válidos e seus botões correspondentes são:

- `TOURLAB` - Conquista 1
- `PROJARD` - Conquista 2
- `TCCVETS` - Conquista 3

## Como Usar

1. O usuário deve inserir um dos códigos de conquista válidos no campo de entrada.
2. Ao clicar no botão "Resgatar", a conquista será desbloqueada, e o progresso será salvo automaticamente no `localStorage`.
3. Ao desbloquear todas as conquistas, uma mensagem será exibida, parabenizando o usuário.

## Estrutura do Código

- **HTML**: Estrutura da página com seções de conquistas, input para código, e botões de resgate.
- **JavaScript**: Gerencia o resgate das conquistas, verificações, armazenamento no `localStorage` e a exibição de mensagens.
- **CSS**: Estilos para personalizar a exibição da página e efeitos visuais nos cards de conquistas.

### Funções JavaScript

- **`loadBadges()`**: Carrega as conquistas já resgatadas a partir do `localStorage` e ajusta a interface.
- **`checkAllConquests()`**: Verifica se todas as conquistas foram resgatadas e, se positivo, exibe uma mensagem de parabéns e aplica filtros de preto e branco nos cards das conquistas.
- **`submitBtn.onclick`**: Lida com o evento de resgate de conquista quando o código é inserido e o botão é clicado.

## Exemplo de Código HTML

```html
<section class="badges-section">
  <div id="btnBadge1" class="badge-card conquered">Conquista 1</div>
  <div id="btnBadge2" class="badge-card conquered">Conquista 2</div>
  <div id="btnBadge3" class="badge-card conquered">Conquista 3</div>
</section>

<section class="rescue-section">
  <input type="text" id="code-input" placeholder="Insira o código">
  <button id="submitBtn">Resgatar</button>
</section>

