# Guia de Ícones para PWA - Nestle Unity WebGL

## Estrutura de Pastas
Crie a pasta `icons` na raiz do projeto e adicione os seguintes ícones:

```
RGSNestle/
├── icons/
│   ├── icon-32x32.png
│   ├── icon-72x72.png
│   ├── icon-96x96.png
│   ├── icon-120x120.png
│   ├── icon-128x128.png
│   ├── icon-144x144.png
│   ├── icon-152x152.png
│   ├── icon-167x167.png
│   ├── icon-180x180.png
│   ├── icon-192x192.png
│   ├── icon-384x384.png
│   └── icon-512x512.png
```

## Tamanhos de Ícones Necessários

### Android/Chrome (obrigatórios)
- **192x192px** - Ícone padrão para Android
- **512x512px** - Ícone de alta resolução para Android
- 72x72px, 96x96px, 128x128px, 144x144px, 384x384px (opcionais)

### iOS/Safari (obrigatórios)
- **180x180px** - iPhone e iPad Pro
- **167x167px** - iPad Pro 10.5"
- **152x152px** - iPad, iPad mini
- **120x120px** - iPhone

### Favicon
- **32x32px** - Favicon padrão para navegadores

## Como Criar os Ícones

### Opção 1: Ferramenta Online (Recomendado)
1. Acesse: https://www.pwabuilder.com/imageGenerator
2. Faça upload de uma imagem quadrada de pelo menos 512x512px
3. Baixe todos os tamanhos gerados
4. Coloque os arquivos na pasta `icons/`

### Opção 2: Photoshop/GIMP
1. Crie ou abra sua logo em alta resolução (pelo menos 1024x1024px)
2. Exporte para cada tamanho listado acima
3. Use o formato PNG com fundo transparente ou sólido
4. Mantenha a nomenclatura: `icon-[tamanho].png`

### Opção 3: ImageMagick (Linha de Comando)
```bash
# Instale o ImageMagick primeiro
# A partir de uma imagem fonte de 1024x1024px chamada logo.png

magick logo.png -resize 32x32 icon-32x32.png
magick logo.png -resize 72x72 icon-72x72.png
magick logo.png -resize 96x96 icon-96x96.png
magick logo.png -resize 120x120 icon-120x120.png
magick logo.png -resize 128x128 icon-128x128.png
magick logo.png -resize 144x144 icon-144x144.png
magick logo.png -resize 152x152 icon-152x152.png
magick logo.png -resize 167x167 icon-167x167.png
magick logo.png -resize 180x180 icon-180x180.png
magick logo.png -resize 192x192 icon-192x192.png
magick logo.png -resize 384x384 icon-384x384.png
magick logo.png -resize 512x512 icon-512x512.png
```

## Requisitos dos Ícones

1. **Formato**: PNG com transparência ou fundo sólido
2. **Proporção**: Quadrados (1:1)
3. **Área segura**: Mantenha o conteúdo importante dentro de 80% da área central
4. **Fundo**: Use cores sólidas ou transparência
5. **Qualidade**: Alta resolução, sem pixelização

## Teste a PWA

### Desktop (Chrome)
1. Abra o DevTools (F12)
2. Vá em Application > Manifest
3. Verifique se todos os ícones aparecem
4. Teste o botão "Instalar App"

### Mobile (Android)
1. Acesse via Chrome mobile
2. Menu > "Adicionar à tela inicial"
3. Verifique se o ícone aparece corretamente

### Mobile (iOS/Safari)
1. Acesse via Safari
2. Botão compartilhar > "Adicionar à Tela de Início"
3. Verifique o ícone e o nome do app

## Problemas Comuns

**Ícones não aparecem:**
- Verifique o caminho no manifest.json
- Confirme que os arquivos existem na pasta icons/
- Limpe o cache do navegador

**App não oferece instalação:**
- Verifique se está rodando em HTTPS (ou localhost)
- Confirme que o service-worker.js está registrado
- Veja o console para erros

**Ícone aparece com qualidade baixa:**
- Use imagens em alta resolução
- Não redimensione imagens pequenas para tamanhos maiores
- Mantenha a proporção 1:1
