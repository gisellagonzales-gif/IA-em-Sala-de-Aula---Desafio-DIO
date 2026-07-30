# image-gen-mcp — instalação neste repositório

Servidor MCP de terceiros ([Ichigo3766/image-gen-mcp](https://github.com/Ichigo3766/image-gen-mcp))
que gera imagens conectando-se a uma instância local do Stable Diffusion WebUI
(AUTOMATIC-1111/ForgeUI). O código-fonte foi vendorizado em `mcp-servers/image-gen-mcp/`
e registrado em `.mcp.json` na raiz do repositório.

## Passos necessários antes de usar

1. Instalar dependências e compilar (não versionamos `node_modules/` nem `build/`):
   ```bash
   cd mcp-servers/image-gen-mcp
   npm install
   npm run build
   ```
2. Ter uma instância do Stable Diffusion WebUI rodando com a flag `--api`.
3. Ajustar as variáveis de ambiente em `.mcp.json` (raiz do repo), principalmente
   `SD_WEBUI_URL` para apontar para a sua instância do WebUI. Variáveis opcionais
   (`SD_AUTH_USER`, `SD_AUTH_PASS`, `SD_UPSCALER_*` etc.) estão documentadas no
   `README.md` deste diretório.
4. Reabrir o Claude Code neste projeto — o servidor `image-gen` aparecerá
   automaticamente na lista de MCP servers definida em `.mcp.json`.

## Ferramentas disponibilizadas

- `generate_image`, `get_sd_models`, `set_sd_model`, `get_sd_upscalers`, `upscale_images`

Veja `README.md` neste diretório para a lista completa de parâmetros.
