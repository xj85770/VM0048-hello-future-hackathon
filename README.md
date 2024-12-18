# VM0048, VMD0055, VT0001

Submission for Hello Future Hackathon by Hedera

## Project Description

This project aimed to [improve upon a digitized version of VM0048](https://github.com/hashgraph/guardian/tree/main/Methodology%20Library/Hackathon/VM0048) REDD methodology by leveraging on Hedera's Guardian Service, which enables quantification and monitoring of emissions reductions from Verra REDD projects. It incorporates the VMD0055 module for precise unplanned deforestation impact assessments and integrates a separate VT0001 additionality tool to validate VCS AFOLU projects. Utilizing detailed schemas for carbon stock and land use calculations, the policy automates workflows for data collection, validation, and reporting. With decentralized storage via IPFS and immutability through Hedera, VM0048 ensures transparency, reliability, and alignment with international standards for generating high-integrity carbon credits.

## Improvements and progress

1. **Separate VT0001 Additionality Tool**

>- ***Importance of separate tool:***
>   - Now separated as a .tool file for modularity and reusability; enables use across future policies and methodologies.
>   - Previously implemented as a basic Excel schema, the tool now includes improved schemas with multiple embedded analyses, guiding users through appropriate steps to determine additionality.
>- [Further details available on GitHub with comprehensive README](https://github.com/xj85770/guardian/tree/main/Methodology%20Library/Verra/Tools/VT0001)
>- [Pull request](https://github.com/hashgraph/guardian/pull/4491) for VT0001 into hashgraph/guardian GitHub

2. **Seperation of VM0048 project description and VMD0055 project description into 2 schemas for clarity**

3. **VM0048 Improvements**

>- VT0001 Tool added as a tool and not as a schema.
>- VCS Non-Permaneence Risk Report added.
>- Monitoring Plan and Monitoring Report schemas added.
>- Final VCU calculations now minting correct number of tokens.

4. **VMD0055 Updates**

>- Alignment with version 1.1, released October 2024.
>- More accurate and expanded upon Standard Operating Procedures schema.
>- More accurate and streamlined VMD0055 Potential Verified Carbon Units from Unplanned Deforestation calculations including:
>   - Removal of "Activity Data" schema
>   - Expansion of uncertainty, leakage, ex-ante project scenario estimations, previously missing GHG sources, non-CO2 GHG emissions, and more.

- [Further details available for VM0048/VMD0055 on GitHub with comprehensive README]()
- [Pull request]() for VM0048 & VMD0055 into hashgraph/guardian GitHub

## List of Tech Stack Used

- Microsoft Excel (for schema & calculations)
- [Hedera Guardian Service](https://hedera.com/guardian)

   - Policy Manager & Policy Workflow Engine
      - VM0048 Policy
   - Tool Manager
      - VT0001 Tool 
   - Schema Manager
  
  ![Schema Tree](https://github.com/user-attachments/assets/8a27ec64-a4d2-4972-a971-ad36699e9de5)
  Figure 1. Schema Tree for VM0048 Monitoring Report, including schemas for VT0001 (Policy Design schema follows the same tree architecture)


## Testing Instructions

This policy can be imported via Github (.policy file) or IPFS timestamp.

| Version | IPFS Timestamp | Policy File Link | Version Differences |
|---|---|---|---:|
| VM0048 2.0.0  | | [Link]() | Verra Methodology |
| VT0001 1.0.0  | 1734352827.528167545 | [Link](https://github.com/xj85770/VM0048-hello-future-hackathon/blob/main/Verra%20VT0001%20Tool.tool) | Verra Tool |

1. **Access the Policies Tab**  
   Log in to the [MGS interface](https://guardianservice.app/) and navigate to **Manage Policies** under the **Polices** tab.

2. **Initiate the Import Process**  
   Click the **Import** button.

### **Option 1: Import a `.policy` File**

3. **Select `.policy` File**  
   - Choose the option to upload a policy file.
   - Browse your local files and select the `.policy` file you want to import.

4. **Review and Confirm**
   - Once the .policy file is selected, we get the Policy Import Review screen.
   - Review and ensure all referenced resources (schemas, tools) are correctly mapped or linked.
   - Once everything looks good, click on Import Button.

5. Once the file is successfully imported and reviewed, the policy will now appear in the **Policies** tab.

### **Option 2: Import Policy via IPFS**
3. **Obtain IPFS Timestamp**  
   - Retrieve the IPFS Timestamp in the table above.

4. **Choose the IPFS Option**  
   - Select the option to import a policy from IPFS.
   - Enter the IFPS Timestamp in the provided field.

5. **Retrieve and Map Resources**  
   - MGS will fetch the policy file from the IPFS network.

6. **Review and Confirm**  
   - Preview the imported policy details.
   - Review and ensure all referenced resources (schemas, tools) are correctly mapped or linked.
   - Once everything looks good, click on Import Button.

7. Once the file is successfully imported and reviewed, the policy will now appear in the **Policies** tab.
8. Test via a [Dry Run](https://docs.guardianservice.io/learn/important-concepts/about-dry-run).
9. Compare calculations and VCUs minted using the "VM0048 Project Design" spreadsheet provided in the [VM0048 VMD0055 REDD Template v2](https://github.com/xj85770/VM0048-hello-future-hackathon/blob/main/VM0048%20VMD0055%20REDD%20Template%20v2.xlsx).

## Selected hackathon track

- Sustainable and Green Finance
- Hashgraph Trailblazers (Open Track) 
