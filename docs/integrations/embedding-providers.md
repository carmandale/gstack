# GBrain embedding providers

GBrain owns embedding-provider support; GStack only detects the common failure
mode where a launchd service cannot see `OPENAI_API_KEY`.

If you want to avoid OpenAI cost or keep embeddings local, configure GBrain's
`embedding_model` to one of the providers supported by your installed GBrain
version, then restart the GBrain service and backfill stale pages. Common
provider families include local engines such as Ollama or llama.cpp and hosted
providers such as OpenAI, Voyage, and Gemini.

For launchd services, provider credentials must be in the service environment,
not only in your login shell. See [gbrain-sync error lookup](../gbrain-sync-errors.md)
for the `embedded_count: 0` and `Timed out waiting for PGLite lock` runbooks.
