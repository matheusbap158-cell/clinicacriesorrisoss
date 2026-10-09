# Crie Sorrisos Odontologia (demo)

Landing page de demonstração, HTML único (`index.html`), sem dependências além das fontes do Google Fonts. Não publicada.

## Estrutura
- `index.html`: o site, com o mascote "Dentinho", faixa em movimento, jornada animada da primeira visita e mapa da boca no temporizador (hero com a fachada, ferramenta "Quantos anos tem o seu filho?", especialidades, a clínica, "Hora de escovar" (temporizador), primeira visita, avaliações, equipe, formulário que abre o WhatsApp, dúvidas, contato com mapa)
- `Copy.txt`: texto da página
- `design-system-criesorrisos.md` / `.html`: design system
- `assets/`: logo ampliada e sem fundo (`logo.png`), fotos otimizadas, favicon e imagem de compartilhamento
- `Logo/`, `Imagens/`, `Fotos/`, `Info maps.txt`, `bio insta.txt`: materiais de origem

## Mascote
O "Dentinho" é um personagem criado pela agência para esta demo (SVG no próprio `index.html`, função `MASCOT`). Muda de roupa por faixa de idade. A clínica deve aprovar, trocar ou pedir a retirada.

## Como visualizar
Na pasta da agência: `node "_ferramentas/preview-local.mjs" "4. Meus Clientes/2. Demos e propostas/clinicacriesorrisos"` e abrir o endereço mostrado.

## Antes de publicar
- O `index.html` tem `<meta name="robots" content="noindex, nofollow">` para a demo não aparecer no Google. Remover ao publicar o site definitivo.
- Os itens `[A CONFIRMAR]` aparecem no site com borda tracejada; a lista completa está na ficha em `4. Meus Clientes/_Fichas/Crie Sorrisos.pdf`.
- A equipe da clínica precisa revisar as faixas de idade, as descrições das especialidades e a orientação de escovação.
- A foto de atendimento (`Fotos/atendimento.png`) mostra uma criança paciente e não foi usada. Só usar com autorização dos responsáveis.
- Publicidade odontológica (CFO): conferir as regras com a clínica antes de publicar (avaliações, registros, ausência de preço e promessa).
- A logo veio com 150 px (a demo usa uma versão ampliada, com o fundo de fora removido); pedir o arquivo em alta resolução.
- Ao publicar: conferir de novo as avaliações com a clínica. A nota não entra no código estruturado, porque avaliação da própria empresa não gera destaque no Google.
