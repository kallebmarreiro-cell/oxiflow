# OxiFlow v2
## Recursos
- Aplicativo web instalável (PWA) e cache da interface para uso após primeiro carregamento.
- Cadastro de materiais, rastreamento, custódia e alertas.
- Leitura QR pela câmera quando suportada pelo navegador, em HTTPS/localhost.
- Captura opcional de foto e GPS no formulário de custódia.
- Exportar/importar backup JSON para transferência manual de dados.
## Teste
Para PWA, câmera e GPS, abra o site via HTTPS ou localhost (não `file://`). Em um computador com Python, rode `python -m http.server 8000` dentro da pasta e abra `http://localhost:8000`.
## Publicação gratuita
Envie `index.html`, `manifest.webmanifest`, `sw.js` e `icon.svg` para a raiz de um repositório GitHub. Em Settings → Pages, selecione Deploy from a branch, `main`, `/ (root)`. Aguarde o endereço HTTPS.
## Limitações
O QR scanner lê códigos que contenham exatamente o código do lote, mas etiquetas QR reais ainda precisam ser geradas. Não há sincronização automática entre dispositivos: o backup é manual. Foto e GPS ficam no navegador. Não há login, backend ou banco compartilhado. O cache offline funciona depois de visitar o site uma vez online.
