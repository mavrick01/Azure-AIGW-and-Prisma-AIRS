# Azure-AIGW-and-Prisma-AIRS
This repository has the components for integrating Prisma AIRS into Azure AI Gateway (or APIM with LLM's)

The fragments handle failure in different ways. Those that end if open will fail open and allow the LLM prompt and response to be returned even if the scanner is unavailable.

### NOTE 
This refers to a named variable called airs-api with your API key. 

