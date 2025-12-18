# Azure-AIGW-and-Prisma-AIRS
This repository has the components for integrating Prisma AIRS into Azure AI Gateway (or APIM with LLM's)

The fragments handle failure in the prompt and response and different error methods.

### NOTE 
This requires a named variable called `airs-api` with your API key. 

## Files
* `All-ops-example` : This is an example policy for my LLM API. If you want to define the profile, you have to set the currentPromptProfile and currentResponseProfile variables
* `panw-airs-scan-prompt` : This will scan the prompt (it will use prompt-profile by default). This will fail closed if the AIRS service is not available
* `panw-airs-scan-prompt-open` : This will scan the prompt (it will use prompt-profile by default). This will fail open if the AIRS service is not available
* `panw-airs-scan-response` : This will scan the response (it will use response-profile by default). This will fail closed if the AIRS service is not available
* `panw-airs-scan-response-open` : This will scan the response (it will use response-profile by default). This will fail open if the AIRS service is not available
