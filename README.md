## LLM API key

AI recommendations use Claude (`claude-sonnet-5-5`) and read the key from the `ANTHROPIC_API_KEY` environment variable. The key is optional: without it the app falls back to rule-based recommendations.

The key is the shared secret `Demo-Apps-Share-API-Key` in Azure Key Vault `kv-demo-apps-shared` (subscription "Demo Apps"). Fetch it with:

```bash
az keyvault secret show --vault-name kv-demo-apps-shared --name Demo-Apps-Share-API-Key --subscription "Demo Apps" --query value -o tsv
```
