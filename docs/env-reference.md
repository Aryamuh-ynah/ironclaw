# Environment variable reference

This page lists the environment variables read by IronClaw.

Do not put secret values in documentation, logs, issues, or pull requests. This page lists variable names only.

## Providers

| Variable                       | Description                                                                            | Default                              | Applies to |
| ------------------------------ | -------------------------------------------------------------------------------------- | ------------------------------------ | ---------- |
| `ANTHROPIC_API_KEY`            | API key used to enable the Anthropic provider.                                         | Not set                              | Provider   |
| `GEMINI_API_KEY`               | API key used to enable the Gemini provider when `GOOGLE_API_KEY` is not set.           | Not set                              | Provider   |
| `GOOGLE_API_KEY`               | API key used to enable the Gemini provider.                                            | Not set                              | Provider   |
| `GOOGLE_CLOUD_LOCATION`        | Fallback Google Cloud location for Vertex AI when `GOOGLE_VERTEX_LOCATION` is not set. | Not set                              | Provider   |
| `GOOGLE_CLOUD_PROJECT`         | Fallback Google Cloud project for Vertex AI when `GOOGLE_VERTEX_PROJECT` is not set.   | Not set                              | Provider   |
| `GOOGLE_VERTEX_ACCESS_TOKEN`   | Access token used for Vertex AI authentication.                                        | Not set                              | Provider   |
| `GOOGLE_VERTEX_LOCATION`       | Location used for Vertex AI requests.                                                  | Not set                              | Provider   |
| `GOOGLE_VERTEX_PROJECT`        | Project used for Vertex AI requests.                                                   | Falls back to `GOOGLE_CLOUD_PROJECT` | Provider   |
| `GOOGLE_VERTEX_USE_GCLOUD`     | Uses gcloud credentials for Vertex AI when set to `1`.                                 | Not set                              | Provider   |
| `IRONCLAW_LOCAL_MODEL`         | Local model name used by the local model provider.                                     | Not set                              | Provider   |
| `IRONCLAW_LOCAL_MODEL_KEY`     | Optional API key sent to the local model provider.                                     | Not set                              | Provider   |
| `IRONCLAW_LOCAL_MODEL_URL`     | Upstream URL for the local model provider.                                             | Not set                              | Provider   |
| `IRONCLAW_MODEL_GATEWAY_HOSTS` | Comma-separated model gateway host allowlist or routing list.                          | Not set                              | Provider   |
| `IRONCLAW_MODEL_GATEWAY_URL`   | Upstream URL for the model gateway provider.                                           | Not set                              | Provider   |
| `OPENAI_API_KEY`               | API key used to enable the OpenAI provider.                                            | Not set                              | Provider   |
| `OPENROUTER_API_KEY`           | API key used to enable the OpenRouter provider.                                        | Not set                              | Provider   |

## Control plane

| Variable             | Description                                           | Default | Applies to         |
| -------------------- | ----------------------------------------------------- | ------- | ------------------ |
| `IRONCLAW_API_TOKEN` | API token used by the control plane and CLI requests. | Not set | Control plane, CLI |
| `IRONCLAW_CONFIG`    | Path to the IronClaw configuration file.              | Not set | Control plane, CLI |

## Sandbox and containment

| Variable                  | Description                                                | Default | Applies to |
| ------------------------- | ---------------------------------------------------------- | ------- | ---------- |
| `IRONCLAW_DOCKER_BINDS`   | Comma-separated Docker bind mounts added to sandbox runs.  | Not set | Sandbox    |
| `IRONCLAW_DOCKER_NETWORK` | Docker network mode used for sandbox runs.                 | Not set | Sandbox    |
| `IRONCLAW_SANDBOX_IMAGE`  | Sandbox image used by onboarding and sandbox setup checks. | Not set | Sandbox    |

## Channels

| Variable                          | Description                                                     | Default | Applies to    |
| --------------------------------- | --------------------------------------------------------------- | ------- | ------------- |
| `IRONCLAW_IMESSAGE_ENABLE`        | Enables the iMessage channel on macOS when set to `1`.          | Not set | Control plane |
| `IRONCLAW_MATTERMOST_WEBHOOK_URL` | Mattermost webhook URL used to enable Mattermost notifications. | Not set | Control plane |
| `IRONCLAW_SIGNAL_CLI_URL`         | Signal CLI URL used to enable Signal notifications.             | Not set | Control plane |
| `IRONCLAW_SIGNAL_NUMBER`          | Signal phone number used by the Signal adapter.                 | Not set | Control plane |
| `IRONCLAW_TEAMS_WEBHOOK_URL`      | Microsoft Teams webhook URL used to enable Teams notifications. | Not set | Control plane |

## CLI and development

| Variable                       | Description                                                               | Default                                | Applies to    |
| ------------------------------ | ------------------------------------------------------------------------- | -------------------------------------- | ------------- |
| `IRONCLAW_DEV_MODEL`           | Development model override used by development provider configuration.    | Not set                                | Control plane |
| `IRONCLAW_DEV_PROVIDER`        | Development provider override used by development provider configuration. | Not set                                | Control plane |
| `IRONCLAW_DEV_VERTEX_LOCATION` | Development Vertex AI location override.                                  | Falls back to `GOOGLE_VERTEX_LOCATION` | Control plane |
| `IRONCLAW_DEV_VERTEX_PROJECT`  | Development Vertex AI project override.                                   | Falls back to `GOOGLE_VERTEX_PROJECT`  | Control plane |
