# Azure-AIGW-and-Prisma-AIRS
This repository has the components for integrating Prisma AIRS into Azure AI Gateway (or APIM with LLM's)

The fragments handle failure in the prompt and response and different error methods.

### NOTE 
This requires a named variable called `airs-api` with your API key. 

## Files
* `All-ops-example` : This is an example policy for my LLM API. 
* `panw-airs-scan` : This is a consolidated fragment that can be used to scan  prompts and responses. It can be configured using the following variables:
    - `ScanType`: (string) "prompt" or "response". Defaults to "prompt".
    - `currentProfile`: (string) The name of the AIRS profile to use for scanning. Defaults to "example-profile".
    - `appName`: (string) The name of the application. Defaults to "Azure-APIM-Gateway".
    - `FailOpen`: (boolean) `true` to allow traffic if the scanner is unavailable, `false` to block it. Defaults to `false`.
    - `airsDescriptions`: (JObject) A JObject containing custom error messages for detected threats. If not provided, the default messages in `scanDescriptions` will be used.
