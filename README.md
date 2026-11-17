# Gemini VidIQ MCP

Configuration de référence pour connecter le serveur MCP VidIQ à Gemini CLI et clients compatibles.

## 1) Fichier de configuration Gemini CLI

Fichier : `settings.json`

```json
{
  "mcpServers": {
    "vidiq": {
      "url": "https://mcp.vidiq.com/mcp",
      "oauth": {
        "enabled": true
      }
    }
  }
}
```

### Variante avec clé API

```json
{
  "mcpServers": {
    "vidiq": {
      "url": "https://mcp.vidiq.com/mcp",
      "headers": {
        "Authorization": "Bearer VOTRE_API_KEY"
      }
    }
  }
}
```

## 2) Fichier MCP générique

Fichier : `mcp.json`

```json
{
  "mcpServers": {
    "vidiq": {
      "url": "https://mcp.vidiq.com/mcp",
      "transport": "sse"
    }
  }
}
```

## 3) Validation de l’authentification

1. Ouvrir Gemini CLI.
2. Exécuter :

```bash
/mcp auth vidiq
```

3. Vérifier la connexion :

```bash
/mcp
```

4. Recharger si nécessaire :

```bash
/mcp reload
```

## 4) Important pour l’app iOS Gemini

L’application Gemini officielle sur iOS n’utilise pas un fichier `settings.json` local. Si le support MCP est disponible pour ton compte, il se configure depuis les réglages Gemini sur le Web / applications connectées, pas via un fichier dans l’app iOS.

## 5) Sécurité

- Ne jamais committer de clé API ou token OAuth réel.
- Les identifiants doivent être gérés par le flux d’authentification du client MCP utilisé.
