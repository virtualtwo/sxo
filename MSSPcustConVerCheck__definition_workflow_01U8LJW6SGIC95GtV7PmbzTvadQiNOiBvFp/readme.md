## Problem Statement.
Secure Endpoint MSSP partners need to operate with efficiency at scale.  “Simple” tasks like verifying compliance for standard operating conditions on all customer endpoints deployed can be time consuming.

## Key Customer/Partner outcomes:
Automation to improve operational efficiency from hours to seconds.  This particular workflow can be leveraged to identify “non-standard” endpoint connector versions across all MSSP customers.  A simple starting framework for other use cases that require common action across multiple MSSP Secure Endpoint customers.  Also provides a framework for other Secure Endpoint QA & policy compliance element verification.

## Pre-Requisites
* Acquire each tenant/customer API keys from Secure Endpoint MSSP Console
* Utilize Copy-AMP-MSSP-CREDS.json workflow to add Secure Endpoint customer tenant API keys into Group Target

## Worflow Operation
Loop through each MSSP customer and do the following:
1. Get all Computers
1. Remove input standard hosts
1. Create Table with non-standard hosts
1. Outputs non-standard hosts to table & Webex Teams room

![Workflow](/Run_Wf_Input.png)


## Required Global Variable
Create Global Variable MSSP customer credentials using Copy-ADD-AMP-MSSP-CREDS.json to aggregate MSSP customer API account keys used in this workflow.

## Required Targets
* AMP Target
* AMP MSSP Target Group - contains all MSSP customer targets

## Required Account Keys
* Account keys for each individual AMP-MSSP Customer
* Global MSSP Account Keys

## Setup Information
Browse to your SecureX orchestration instance. This will be a different URL depending on the region your account is in:

* US: https://securex-ao.us.security.cisco.com/orch-ui/workflows/
* EU: https://securex-ao.eu.security.cisco.com/orch-ui/workflows/
* APJC: https://securex-ao.apjc.security.cisco.com/orch-ui/workflows/

Import both workflows.
* Copy-ADD-AMP-MSSP-CREDS.json
* AMP MSSP Customer Block List.json

## Running Workflow

* SecureX Orchestration directly
![SXO_RUN](/SXO_Run.png)

* Threat Response context menu in SecureX Threat Response
![SX_CTR](/SX_TR_ResponseAction.png)

* SecureX browser plug-in.
![SX_BROWSER](/SX_Browser_Response.png)

* Secure Endpoint Customer/Tenant console
![ENDPOINT_CONSOLE](/Endpoint_ResponseAction.png)


## Notes
*
