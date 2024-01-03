# Cryptocurrency for Salesforce

## Overview
[Web3 Enabler](https://web3enabler.com) empowers enterprise users to send and accept crypto payments on the world’s leading CRM, ERP and BI software, with just one click. We handle the complexities of Web3 so that our users can reap the benefits of cryptocurrencies, without the steep learning curve. 

## Technical Architecture


[Web3 Enabler Admin Flowchart](https://github.com/MuKnSys/cryptocurrency-for-salesforce/blob/main/assets/web3_enabler_admin_flowchart.png)



## Integration Plan / Project Roadmap

Milestone 1 - Initial Build Out

* Building of cryptocurrency admin UI/UX
* Cryptocurrency payments for Salesforce admin UI/UX
* Building of cryptocurrency user UI/UX
* Cryptocurrency payments for Salesforce user UI/UX
* Initial Apex integration to the blockchain 
* Unit tests for Apex integration

Milestone 2 - Completion of Open Source

* Full Apex integration 
* User story creation
* Admin story creation
* Full testing specifications completed 

Milestone 3 - Unmanaged Package Creation 

* Unmanaged package documentation
* Unmanaged package submission
* Self Hosting of server component

## Salesforce Project and Salesforce Org Wallet Explanation and Setup

This is a basic demonstration Salesforce DX Project. Using the [SF CLI](https://developer.salesforce.com/tools/sfdxcli) tools, you can deploy to a Developer Edition Scratch Org.  Our project will allow Salesforce administrators to make crypto payments from an enterprise Salesforce Org that resembles this one.

Now that you’ve created a Salesforce DX project, what’s next? Here are some documentation resources to get you started.

### Salesforce Developer Edition

You can get a free Salesforce Developer Edition account from Salesforce. Sign up at:

https://developer.salesforce.com/signup

### How To Test the App

1. Checkout the Main Branch
1. Log into the Dev Hub Org by running `sf org login web --set-default-dev-hub --alias DevHub --instance-url https://login.salesforce.com` and entering your username and password.
1. Create a Scratch Org by running `sf org create scratch -f ./config/project-scratch-def.json -a dev -d -y 30`.
    - The `-f` flag is a path to config file (no need to change it).
    - The `-a` flag is an alias of the scratch org, if you create multiple scratch orgs you can give them unique aliases to easier refer to them.
    - The `-d` flag marks the newly created scratch org as default. If you don't mark it as default you will have to reference it by username or alias, or you will have to use `sf config set target-org YourAliasOrUsername` to set is as default.
    - The `-y` flag sets the number of days before the org expires.
    - Use the `-h` flag for help.
    - For more details: [developer docs scratch orgs create](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_create.htm).
1. Push the code to the Scratch Org: `sf project deploy start`
1. Connect to the Salesforce Scratch Org: `sf org open`

Once you've set up your Salesforce Scratch Org, you can follow the steps outlined in our [user manual](https://mukn.com/wp-content/uploads/2023/07/Web3-Enabler-for-Salesforce-User-Guide.pdf) to make and receive payments using Web3 Enabler on Salesforce. You can also use our [demo](https://www.youtube.com/watch?v=lkAp2vqQVTA) as a guide.  

We launched Web3 Enabler on the Salesforce App Exchange in July, 2023.  See our [AppExchange listing](https://appexchange.salesforce.com/appxListingDetail?listingId=ee4c011b-7a5b-4a50-91fb-f28049390858) for further details.

### Submitting changes to GitHub

1. Create a feature / change branch - you will need to fork the project
1. Pull changes from Salesforce `sf project retrieve start`
1. Push changes to GitHub
1. Create a pull request

### Notes - Convert sf scratch org creation command to sfdx

`sfdx force:org:create -f config/project-scratch-def.json --setalias xrpsalesforce1 --durationdays 30 --setdefaultusername --json --loglevel fatal`

## Copyright and License

Copyright 2023 Mutual Knowledge Systems, Inc.  XRP Salesforce is distributed under the GPL licence, version 3.0.  For more information, see the [LICENSE file](LICENSE).
