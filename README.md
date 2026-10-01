# Podium Reveal

Tela cheia de revelação de ranking em pódio, com suspense (nomes embaralhando), coroa, medalhas e confete no 1º lugar. Um arquivo, zero dependências, abre direto no navegador.

Feito originalmente para o evento **"1 por 1"** da IASD do Jardim Europa. Reutilizável para qualquer ranking.

## Como usar

Abra `index.html` no navegador. Clique em **Revelar** (ou aperte `Espaço`/`Enter`) para revelar do último ao 1º lugar. `⛶` entra em tela cheia.

## Onde mudar (reutilizar para outro evento)

Só o bloco `CONFIG` no topo do `<script>` em [index.html](index.html):

```js
const CONFIG = {
  title:    '1 por <b>1</b>',        // aceita HTML; <b> = destaque dourado
  subtitle: 'IASD do Jardim Europa',
  teams: [
    { place: 5, name: 'Ebenezer', score: 100 },
    { place: 4, name: 'Ungidos',  score: 500 },
    { place: 3, name: 'Adonai',   score: 600 },
    { place: 2, name: 'Maranata', score: 700 },
    { place: 1, name: 'Águia',    score: 800 },
  ],
};
```

- **`title` / `subtitle`** — cabeçalho e título da aba. `title` aceita HTML.
- **`teams`** — adicione ou remova times à vontade. Layout do pódio, texto do botão e medalhas se ajustam sozinhos.
- **`place`** — posição final (1 = campeão). Pode listar em qualquer ordem.
- **`score`** — controla só a **altura** da barra, nunca aparece como texto. Maior score = barra mais alta.

Não precisa mexer em mais nada.

## Personalização visual (opcional)

- **Cores** — variáveis `--gold*` e `--ink` no `:root` do `<style>`.
- **Logos** — o `<svg class="logo-sda">` e a imagem no header são embutidos no HTML; troque-os pelos do seu evento.
