# 📱 Content Viewer - Tania Bulhões Scraper

Interface web para visualizar e gerenciar o conteúdo extraído pelo scraper do site taniabulhoes.com.br.

## 🎯 Objetivo

Permitir que a equipe de negócios acesse, visualize e copie facilmente o conteúdo das páginas scraped para uso no CMS, sem precisar mexer em arquivos JSON.

## ✨ Funcionalidades

### 📋 Visualização
- **Menu lateral**: Lista todas as páginas extraídas
- **Busca**: Procure por páginas ou conteúdo específico  
- **Seções organizadas**: Conteúdo separado por seções com headings
- **Seletores CSS**: Informações técnicas para desenvolvedores

### 📋 Copy & Paste
- **Copiar texto**: Clique em qualquer bloco de texto para copiar
- **Copiar URLs de imagens**: Botão dedicado para cada imagem
- **Copiar seção completa**: Formato otimizado para CMS
- **Export JSON**: Dados estruturados para integração

### 🔍 Organização
- **Estatísticas**: Quantidade de páginas e seções
- **Filtros de busca**: Encontre conteúdo rapidamente
- **Interface responsiva**: Funciona em desktop e mobile

## 🚀 Como usar

### Localmente
1. Abra o terminal na pasta do projeto
2. Execute: `python -m http.server 8000`
3. Abra: `http://localhost:8000/viewer/`

### Deploy (Netlify/Vercel)
1. Faça push do projeto inteiro para o GitHub
2. Conecte no Netlify/Vercel
3. Configure:
   - **Publish directory**: `viewer/`
   - **Build command**: (deixe vazio)
4. A interface ficará disponível online

## 📁 Estrutura de arquivos

```
projeto/
├── src/           # Scraper
├── viewer/        # Interface web ← ESTA PASTA
├── output/        # JSONs (servidos como /output/)
└── config/
```

## 💡 Dicas de uso

### Para equipe de negócios:
1. **Selecione uma página** no menu lateral
2. **Navegue pelas seções** na área principal
3. **Clique nos textos** para copiar automaticamente
4. **Use "Copiar Seção"** para pegar conteúdo formatado
5. **"Export CMS"** gera JSON estruturado

### Para desenvolvedores:
- Os **seletores CSS** aparecem em cada seção
- **URLs das imagens** são organizadas e otimizadas
- **JSON de export** mantém estrutura original dos dados

## 🌐 Deploy recomendado

**Netlify** (mais fácil):
1. Arraste a pasta inteira do projeto
2. Configure publish directory: `viewer/`
3. Link pronto para compartilhar

**Vantagens**:
- ✅ Interface sempre atualizada com novos scrapes
- ✅ Acesso online para toda equipe
- ✅ Zero configuração de servidor
- ✅ HTTPs automático

## 🔧 Troubleshooting

**Páginas não aparecem:**
- Verifique se existem arquivos .json na pasta `output/`
- Confirme que o servidor está servindo a pasta correta

**Erro CORS:**
- Use sempre um servidor HTTP (não abra o arquivo diretamente)
- `python -m http.server` ou similar

**Deploy não funciona:**
- Confirme que publish directory está como `viewer/`
- Verifique se os JSONs estão na pasta `output/` do repositório