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

## Screenshots

Here are some screenshots of the setup, testing, and different components:

* Samples of calling the LLM and different responses ![AI Gateway Sample Responses](<Azure AI Gateway - Testing.png>)
* Sample Testing in the Testing Window ![AI Gateway - Test](<Azure AI Gateway - API Test.png>)
* Sample Testing Response ![AI Gateway - Test Result](<Azure AI Gateway - API Test Confirmed.png>)
* AIRS API Secret ![AI Gateway - AIRS Secret](<Azure AI Gateway - AIRS Secret.png>)


* For newbie, this is where you define the API's for your AI Gateway ![AI Gateway Setup Screen](<Azure AI Gateway - API Step 1.png>) 
* Setup screen for setting up the Language Model API ![AI Gateway Step 1](<Azure AI Gateway - API Step 2.png>)
* Settings after Setup ![Azure AI Gateway - API Settings](<Azure AI Gateway - API Settings.png>)
* LLM Backend Configuration (Automatically Done) ![AI Gateway - LLM Setup](<Azure AI Gateway - LLM Setup.png>)
* LLM Credentials Setup (Automatically Done) ![AI Gateway - LLM Authorization](<Azure AI Gateway - LLM Authorization.png>)
* LLM API Key Secret (Automatically Done) ![AI Gateway - LLM Secret](<Azure AI Gateway - LLM Secret.png>)
