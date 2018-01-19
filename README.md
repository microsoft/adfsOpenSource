# ADFS Open Source Guidance

## What Belongs on ADFS Open Source?

All public scripts or tools related to ADFS diagnosability, debugging, management, etc. that are not strictly part of the ADFS codebase

All pluggable components that are not strictly part of the ADFS codebase
    Authentication adapters, relying parties, web customizations, etc. 

If a customer might want to use it, and it can be shipped out-of-band with ADFS, we should put it on GitHub 

## Release Requirements

    ### * Code:
        Must have core functionality working 
            Okay to have items marked as "TODO", "bug", etc. in dev branch (must be resolved before merging to release branch) 
        
    ### * Documentation:
        Must have basic documentation covering the following:  
    
            i. Project Overview (what is this project?)
            ii. Requirements to install (what do I need to have to run this project?)
            iii. Steps to install (how do I install/deploy this project?
            iv. Usage steps and examples (how do I use this project?)
            v. Contributing changes (how do I make changes to this project? How do I validate I didn't break anything?) 
            vi. Any special notes that are important for this project, where applicable 
        
    ### * Tests:
    
        All projects must have a base level of test coverage, or a proposed plan for implementing test coverage. 
        Test coverage can include: internal DFTs or internal production deployment. However, this is discouraged, as tests should allow contributors to validate that changes they have made did not break existing behavior
    
    ### * Code review:
    
        Every change must be reviewed in accordance with the review process (see below) 

## Code Review Process

Must have at least one reviewer sign-off when doing a pull request to a dev branch
Must have mattbo sign-off on pull request going from dev branch to release (master) 

## Project Structure for Repositories 

Main repository for collection of similar items 
Individual projects under top-level 

## Branching

Release branch (master), with tags at each major release 
Dev branch for pre-release 
Feature branch off of dev branch for any bug fix, feature addition, doc change, etc. 
Debug branch where appropriate (for example, maintaining JavaScript with verbose logging) 

![Branchest](./images/branches.png)

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Legal Notices

Microsoft and any contributors grant you a license to the Microsoft documentation and other content
in this repository under the [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode),
see the [LICENSE](LICENSE) file, and grant you a license to any code in the repository under the [MIT License](https://opensource.org/licenses/MIT), see the
[LICENSE-CODE](LICENSE-CODE) file.

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation
may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries.
The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks.
Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all others rights, whether under their respective copyrights, patents,
or trademarks, whether by implication, estoppel or otherwise.