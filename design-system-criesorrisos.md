# Design system: Crie Sorrisos Odontologia

Base: a logo (hashtag azul-turquesa com sorriso magenta e carinha amarela) e a faixa da fachada (ondas amarela, magenta e turquesa sobre azul-claro). A marca é alegre; o site precisa ser alegre para a criança e confiável para quem decide, o pai e a mãe.

## Tom visual (3 linhas)
1. Claro, arejado e colorido, com as ondas da fachada como forma assinatura, sem virar desenho infantil.
2. Turquesa para identidade, magenta para a ação principal e amarelo só como toque de alegria.
3. Cantos bem arredondados, fotos reais em formas suaves e pequenas ferramentas divertidas (idade e escovação) que mostram cuidado.

## 1. Cores

| Papel | Token | Hex | Uso |
|---|---|---|---|
| Turquesa da marca | --teal-500 | #00A8C0 | Formas, ícones, fundos decorativos (texto escuro sobre ele) |
| Turquesa texto | --teal-700 | #066E80 | Links, destaques e texto sobre fundo claro (contraste 5,9:1) |
| Turquesa escuro | --teal-900 | #0C3A47 | Seções escuras, rodapé |
| Aqua claro | --aqua-100 | #E3F6F7 | Seção alternada |
| Aqua muito claro | --aqua-50 | #F4FBFB | Fundo padrão |
| Magenta (ação) | --magenta-600 | #B83C86 | Botão primário (texto branco, contraste 5,3:1) |
| Magenta escuro | --magenta-700 | #9A2E6E | Hover do botão primário |
| Magenta claro | --magenta-100 | #FBE4F0 | Fundos suaves e chips |
| Amarelo | --yellow-400 | #F6DF4F | Toques de cor, selo, ondas (sempre com texto escuro) |
| Tinta | --ink | #0C2F3A | Texto de corpo |
| Texto secundário | --muted | #3F5F6B | Apoio |
| Linha | --line | #CFE6E8 | Bordas e divisores |
| WhatsApp | --wa-500 | #25D366 | **Exclusivo** do botão e do flutuante de WhatsApp (texto escuro #0C2F3A) |
| Alerta | --alert-600 | #C23A2B | Erro de formulário |

Regras: o verde do WhatsApp nunca é decorativo e o texto dele é escuro (o branco não passa no contraste AA). O amarelo nunca é cor de texto sobre fundo claro. Texto de corpo com contraste mínimo de 4,5:1.

## 2. Tipografia

| Uso | Fonte | Peso |
|---|---|---|
| Títulos | Fredoka | 600 e 700 |
| Corpo | Nunito | 400, 600 e 700 |

Link de fontes: `https://fonts.googleapis.com/css2?family=Fredoka:wght@500;600;700&family=Nunito:wght@400;600;700&display=swap`

Hierarquia (desktop / mobile):
- H1: 56 px / 34 px, peso 700, entrelinha 1,08
- H2: 42 px / 30 px, peso 600, entrelinha 1,12
- H3: 22 px / 19 px, peso 600, entrelinha 1,25
- Corpo: 18 px / 16 px, peso 400, entrelinha 1,7
- Botão: 16 px, peso 700

## 3. Componentes

**Botão primário:** magenta, texto branco, 56 px de altura, raio 999 px (pílula). Hover: magenta escuro e sobe 2 px.
**Botão WhatsApp:** verde #25D366 com texto escuro, pílula. O CTA principal de cada dobra é um só; os demais botões de WhatsApp (cartão de dúvida, rodapé) são de apoio.
**Botão secundário:** contorno turquesa escuro, fundo transparente.
**Card:** fundo branco, borda de 2 px na cor da linha, raio 24 px. Hover: sobe 4 px e a borda fica turquesa.
**Controle de idade (slider):** trilho turquesa com bolinha grande de 36 px, foco com anel magenta; número da idade gigante em Fredoka.
**Campos de formulário:** fundo branco, borda de 2 px, raio 16 px, 56 px de altura. Foco: borda turquesa e anel. Erro: borda vermelha e mensagem abaixo.
**Placeholder de pendência:** borda tracejada com o texto "[A CONFIRMAR]", sempre visível.

## 4. Estética
- Raios: 16 px (campos), 24 px (cards), 999 px (botões e chips), foto em arco no hero.
- Sombras: suaves e coloridas (turquesa a 15%), nunca pretas pesadas.
- Espaçamento (base 8): 8, 16, 24, 32, 48, 64, 96 px.
- Forma assinatura: as ondas da fachada (amarela, magenta e turquesa) nas transições entre seções.
- Movimento: bolhas flutuando devagar, ondas, brilho no fim da escovação. Tudo desligado com `prefers-reduced-motion`.

## Mascote "Dentinho"
- Personagem criado pela agência para a demo: dente branco com contorno turquesa, bochechas rosa e sorriso magenta. Piscada, balanço e aceno são animados e desligam com `prefers-reduced-motion`.
- Figurinos por fase: bebê (chupeta e topete), infância (laço), pré-adolescência (fone) e adolescência (óculos escuros).
- Aparece no hero, na ferramenta de idade, na jornada da primeira visita, na equipe e no fim. Não substitui a logo da clínica.

## 5. Conversão para WhatsApp
- CTA no topo, no hero, na ferramenta de idade (já com a idade na mensagem), depois das especialidades, na clínica, no formulário e no fim.
- A ferramenta "Quantos anos tem o seu filho?" leva a conversa para o WhatsApp com a idade preenchida.
- O formulário coleta o nome da criança, a idade e o interesse, e abre o WhatsApp com a mensagem pronta.
- Autoridade: CRO e EAPO visíveis, nota 5,0 do Google, fotos reais da clínica.
- Publicidade odontológica (CFO): sem preço, promoção, antes e depois ou promessa de resultado.

## Tokens prontos (CSS)

```css
:root{
  --teal-500:#00A8C0; --teal-700:#066E80; --teal-900:#0C3A47;
  --aqua-50:#F4FBFB; --aqua-100:#E3F6F7;
  --magenta-600:#B83C86; --magenta-700:#9A2E6E; --magenta-100:#FBE4F0;
  --yellow-400:#F6DF4F;
  --ink:#0C2F3A; --muted:#3F5F6B; --line:#CFE6E8;
  --wa-500:#25D366; --alert-600:#C23A2B;
  --font-display:'Fredoka',system-ui,sans-serif;
  --font-body:'Nunito',-apple-system,'Segoe UI',sans-serif;
  --r-field:16px; --r-card:24px; --r-pill:999px;
}
```
