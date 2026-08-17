# Celma's Buffet — site

Abra o `index.html` com dois cliques. Não precisa de servidor, build nem internet
(só o WhatsApp e as redes sociais é que abrem online).

---

## Antes de colocar no ar — pendências

1. **Depoimentos: seção desativada.** Existe uma seção "Quem já fez a festa com a
   gente" pronta no `index.html`, mas **comentada** — não aparece no site. Os três
   textos que estão lá são fictícios, escritos só para desenhar o layout.
   Para ativar: troque pelos depoimentos reais e apague a linha de abertura e a de
   fechamento do comentário que envolve a `<section id="depoimentos">`.
   Não ative com os textos como estão — avaliação inventada apresentada como real é
   publicidade enganosa (CDC art. 37) e infração ao CONAR.
2. **Três respostas do FAQ** estão genéricas de propósito, porque eu não tenho
   a informação. Procure os comentários `<!-- SUBSTITUIR -->` no `index.html`:
   - cidades atendidas / raio / taxa de deslocamento
   - número mínimo de convidados
   - o que acompanha o serviço (louças, mesas, garçons, tempo, montagem)
3. **Facebook** — o link está chutado como `facebook.com/celmabuffet`. Confirme a URL real.

---

## Como colocar as fotos dos pratos

Coloque as fotos na pasta `img/` com **exatamente** estes nomes, em `.jpg`.
Cada prato que tiver foto passa a mostrar a foto; o que não tiver continua
com a ilustração desenhada. Pode ir colocando aos poucos.

Formato ideal: **quadrada** (ex.: 600×600), prato visto de cima, fundo claro
(o site é bordô escuro, então foto de fundo claro é o que destaca o prato).

### Fundo do topo da página
- `img/hero.jpg` — foto larga do buffet montado (ex.: 1600×900)

### Guarnições
- `arroz-branco.jpg`
- `arroz-a-grega.jpg`
- `arroz-de-forno.jpg`
- `batata-gratinada.jpg`
- `batata-recheada.jpg`
- `baiao-de-dois.jpg`
- `feijao-tropeiro.jpg`
- `farofa.jpg`
- `pure.jpg`
- `salada-tropical.jpg`
- `salada-verde.jpg`
- `salada-mista.jpg`
- `salada-de-batata-com-maca.jpg`
- `salpicao.jpg`

### Proteínas
- `bife-ao-molho-madeira.jpg`
- `bife-a-role.jpg`
- `lagarto-recheado.jpg`
- `parmegiana-de-carne.jpg`
- `estrogonofe-de-carne.jpg`
- `escondidinho-de-carne-de-sol.jpg`
- `calabresa-acebolada.jpg`
- `feijoada.jpg`
- `file-de-frango-ao-molho-branco.jpg`
- `medalhao-de-frango.jpg`
- `parmegiana-de-frango.jpg`
- `fricasse-de-frango.jpg`
- `peixada.jpg`
- `camarao-ao-alho-e-oleo.jpg`
- `camarao-internacional.jpg`
- `risoto.jpg`
- `macarronada-a-bolonhesa.jpg`
- `macarronada-ao-molho-branco-com-camarao.jpg`
- `lasanha.jpg`
- `empadao.jpg`

### Sobremesas
- `pudim.jpg`
- `pave.jpg`
- `torta-de-maracuja.jpg`
- `delicia-de-abacaxi.jpg`
- `taca-da-felicidade.jpg`
- `sorvetes.jpg`

### Extras
- `rodizio-de-pizzas.jpg`
- `rodizio-de-massas.jpg`
- `saladas.jpg`
- `comidas-tipicas.jpg`

---

## Mexer no cardápio

Todos os pratos estão na constante `STEPS`, dentro do `<script>` no fim do
`index.html`. Cada item é:

```js
{ n: "Nome do prato", d: "descrição opcional", i: "d-ilustracao", f: "nome-do-arquivo" }
```

- `n` — nome que aparece no card e vai na mensagem do WhatsApp
- `d` — linha pequena embaixo do nome (opcional)
- `i` — ilustração de fallback (os ids `d-*` ficam no `<svg class="sprite">` no topo)
- `f` — nome do arquivo em `img/`, sem o `.jpg`

Para adicionar um prato, copie uma linha dessas e mude os valores.

---

## Telefone

O número `5585996742666` aparece em 4 lugares: os dois botões do topo, o
rodapé, o botão flutuante e a constante `PHONE` no script. Se mudar, troque
em todos.
