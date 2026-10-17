# Plugins sugeridos do Granite

Registro público dos plugins que o [Granite](https://github.com/vitorreus/granite) sugere para instalação.

O Granite lê [`plugins.json`](plugins.json) por HTTPS (`https://raw.githubusercontent.com/vitorreus/granite-plugins/main/plugins.json`), mostra a lista na tela de plugins e instala o escolhido com `git clone` em `~/.granite/plugins/<id>`. Plugins instalados chegam **desativados** e só rodam depois que você os ativa (com o aviso de acesso total).

## Formato
```json
{
  "format": "granite-plugin-registry",
  "version": 1,
  "plugins": [
    {
      "id": "personagens",
      "name": "Personagens",
      "description": "…",
      "author": "…",
      "repo": "https://github.com/<dono>/<repo>.git",
      "branch": "main",
      "minApiVersion": 1
    }
  ]
}
```
- `id`: igual ao `id` do `granite-plugin.json` do plugin (`[a-z0-9-]+`) e ao nome da pasta de instalação.
- `repo`: URL HTTPS clonável; o repositório deve conter na raiz o `granite-plugin.json` e o JS já compilado.
- `minApiVersion`: versão mínima da API de plugins do Granite.

## Sugerir um plugin
Abra um pull request adicionando uma entrada em `plugins.json` (mantenha a lista em ordem alfabética de `id`).
