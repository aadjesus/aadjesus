# Landing Page do Boné do Código Fonte TV

Landing page criada com a ferramenta Hostinger Horizons e demonstrada no vídeo do canal Código Fonte TV.

- Vídeo: [https://youtu.be/1hGK0oH65bE](https://youtu.be/1hGK0oH65bE)
- Site em produção (100% funcional para venda): [https://bone.codigofonte.com.br](https://bone.codigofonte.com.br)

## Tecnologias

- Vite 4 + React 18
- Tailwind CSS 3 (PostCSS + Autoprefixer)
- React Router, Radix UI, Framer Motion, Lucide Icons
- Scripts e plugins de desenvolvimento para integração com o editor visual do Hostinger Horizons

## Pré-requisitos

- Node.js 18+ (recomendado LTS)
- npm 9+ (ou pnpm/yarn, se preferir)
- Git (para clonar o repositório)

Verifique sua versão do Node e npm:

```powershell
node -v
npm -v
```

## Instalação

```powershell
# clonar
git clone https://github.com/gabrielfroes/bone.codigofonte.com.br.git
cd bone.codigofonte.com.br

# instalar dependências
npm install
```

## Rodar em desenvolvimento

```powershell
npm run dev
```

- Um servidor Vite será iniciado e o terminal mostrará a URL local (por padrão, <http://localhost:5173>).
- Em desenvolvimento, plugins extras habilitam a experiência do editor visual (Hostinger Horizons) e tratadores de erros no navegador.

## Build de produção

```powershell
npm run build
```

O processo de build executa dois passos:

- Geração automática do arquivo `public/llms.txt` a partir dos metadados definidos via `<Helmet>` nas páginas (script `tools/generate-llms.js`).
- Empacotamento do app para produção na pasta `dist/` via Vite.

Dica: não edite `public/llms.txt` manualmente — ele é recriado a cada build.

## Pré-visualizar a build

```powershell
npm run preview
```

Isso sobe um servidor somente para checar a pasta `dist/` localmente.

## Estrutura do projeto (resumo)

- `src/` — código-fonte React (páginas em `src/pages`, componentes em `src/components`)
- `public/` — arquivos estáticos (inclui o `llms.txt` gerado no build)
- `plugins/visual-editor/` — plugins usados durante o desenvolvimento com o Hostinger Horizons
- `vite.config.js` — configuração do Vite e injeções para captura de erros em dev
- `tailwind.config.js` e `postcss.config.js` — configuração do Tailwind CSS
- `tools/generate-llms.js` — script que inspeciona as páginas e cria `public/llms.txt`

## Deploy

O resultado da build é estático (pasta `dist/`) e pode ser hospedado na Hostinger publicado automaticamente através do Hostinger Horizons.

## Prompt (COSTAR)

A aplicação foi gerada a partir do seguinte prompt, estruturado no formato COSTAR:

### Context

Você é um assistente especialista em criação de landing pages impactantes, com foco em UX/UI, copywriting e marketing digital.

### Objective

Crie uma landing page profissional e altamente persuasiva para a venda de um Boné exclusivo do Código Fonte. Edição limitada com apenas 20 unidades disponíveis. A página deve ser visualmente impactante, transmitir autoridade da marca e gerar desejo imediato de compra.

### Style

Para o estilo visual, use cores escuras com toques vibrantes inspiradas na identidade visual da marca (cor de fundo `rgb(23 23 28)`). A estética deve ser moderna, limpa, responsiva, com animações sutis e de alto impacto, transmitindo exclusividade e desejo de compra.

### Tone

Persuasivo, direto e envolvente, transmitindo exclusividade e urgência.

### Audience

Desenvolvedores e apaixonados por tecnologia, fãs do Código Fonte TV e da cultura dev.

### Response

Requisitos de estrutura:

1. Menu de navegação fixo no topo com rolagem suave, contendo links para: Sobre o Boné, Detalhes, FAQ e Comprar Agora.
2. Seção principal (hero): destaque do boné com imagem do Gabriel e Vanessa usando o boné, slogan chamativo e botão de CTA “Garanta o Seu Agora”.
3. Seção de detalhes: benefícios do produto, descrição clara, materiais de alta qualidade e carrossel de imagens em diferentes ângulos.
4. Seção de exclusividade/urgência: destaque de edição limitada, apenas 20 unidades e chamada de ação para gerar escassez.
5. FAQ com respostas curtas para dúvidas comuns (material, envio, pagamento, devoluções). Use respostas genéricas para poder ser alteradas depois.
6. Seção de compra: botão de destaque com preço (R$ 99,00), opções de pagamento (em até 2x sem juros) e frete grátis para todo Brasil.
7. Rodapé com links para redes sociais do Código Fonte TV: YouTube ([https://youtube.com/@codigofontetv](https://youtube.com/@codigofontetv)) e Instagram ([https://instagram.com/codigofontetv](https://instagram.com/codigofontetv)).
8. Página extra na rota "/obrigado" informando que assim que o pagamento for confirmado, o cliente deve enviar um email.
9. Página extra na rota "/esgotado" para que possa ser redirecionado quando o total de bonés já estiver sido vendido (sold out).

Requisitos de design:

1. Design responsivo para todos os dispositivos.
2. Animações sutis para gerar engajamento (hover em botões, fade-in das imagens).
3. Tipografia profissional, legível e moderna.
4. Botões CTA bem destacados e sempre visíveis em momentos estratégicos.
5. Layout otimizado para alta taxa de conversão, com foco em destacar benefícios e escassez.

## Suporte e créditos

- Conceito e demonstração: Código Fonte TV
- Ferramenta utilizada: Hostinger Horizons
- Vídeo da criação: [https://youtu.be/1hGK0oH65bE](https://youtu.be/1hGK0oH65bE)
- Produção: [https://bone.codigofonte.com.br](https://bone.codigofonte.com.br)
