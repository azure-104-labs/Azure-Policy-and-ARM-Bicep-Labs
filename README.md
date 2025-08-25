# Azure-Policy-and-ARM-Bicep-Labs
This repository documents my hands-on practice with **Azure Policies, ARM Templates, and Bicep**.   The goal of this lab was to enforce compliance with Azure Policies, deploy resources manually with ARM JSON templates, and create an automated deployment using Bicep.  

---

## 🔹 Lab Highlights  

### ✅ Azure Policy
- Created and assigned a policy that restricts resource creation to **specific regions**.  
- Applied this policy only to one resource group for testing purposes.  
- Verified policy effect by attempting deployments outside the allowed region.  

### ✅ ARM Template Deployment
When deploying a VM manually via ARM JSON template, I had to edit the following:  
1. Remove:  
   ```json
   "requiredGuestProvisionSignal": true
   
"adminPassword": "Pass-Code@2k25"

targetScope = 'subscription'

@description('Accepted location based on Azure Policies')
param region string = 'South Africa North'

resource BicepGroup 'Microsoft.Resources/resourceGroups@2025-04-01' = {
  name: 'BicepGroup'
  location: region
}

## Screenshots  

0. ![Step 0](./Images/Account_Setup.png)  
1. ![Step 1](./Images/1.png)  
2. ![Step 2](./Images/2.png)  
3. ![Step 3](./Images/3.png)  
4. ![Step 4](./Images/4.png)  
5. ![Step 5](./Images/5.png)  
6. ![Step 6](./Images/6.png)  
7. ![Step 7](./Images/7.png)  
8. ![Step 8](./Images/8.png)  
9. ![Step 9](./Images/9.png)  
10. ![Step 10](./Images/10.png)  
11. ![Step 11](./Images/11.png)  


📸 Screenshots

All screenshots (1–11) are available in the /images folder.
They capture policy creation, ARM JSON editing, and successful Bicep deployments.


