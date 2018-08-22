# GRM/Servicom Brazil Financial and Tax Files
Collection of Documents and Scripts to generate Brazil's Financial and Tax Files for GRM/Navigator and Servicom Accounts.

# Working Directories
* A: Servicom Financial Directory: `\\prodfs1b\grm\Brazil\FinancialFiles\ServicomFinancialFiles`
* B: Servicom Tax Directory: `\\prodfs1b\grm\Brazil\Taxfiles\SrvcmTaxFiles`
* C: Navigator Financial Directory: `\\prodfs1b\grm\Brazil\FinancialFiles\`
* D: Navigator Tax Directory: `\\prodfs1b\grm\Brazil\Taxfiles\`

# Current Process (main steps)
* Cleanup working directories A, B, C, D (`del *.*`)
* Get Servicom Tax and Financial Zip files
* Expand the Servicom Tax Zip file to the working directory `B`
* Expand the Servicom Financial Zip file to the working directory `A`
* Convert the Servicom Tax `D` files from ASCII to UTF8
* Correct Transaction Type for over credits (credits > charges on billing cycle)
* Set the print date on invoices whose type is `online`
* Correct addresses with pending `city++district` values
* Validate Brazil Muni Codes on the addresses for the current billing cycle
* Validate BTNs for current billing cycle
* Generate Navigator Tax Files (output goes to `D`)
* Process Servicom Tax Files (output goes to `D`)
* Generate Combined Tax Files (Navigator+Servicom) (output goes to `D`)
* Convert The Combined Tax Files `D` from UTF8 to ASCII
* Create Version Directory and copy the Combined tax files there
* Create Zip file for Combined Tax Files to send to Gilberto for verification
* Generate the Navigator to Servicom Sequence Number Mapping on XLS
* Generate Navigator Financial Files (output goes to 'C')
* Process Servicom Invoice Financial Files (output goes to 'C')
* Rename Servicom Clients Financial Files from `A` to `C`
* Generate Combined Financial Files (Navigator+Servicom)
* Create Version Directory and copy Combined Financial Files there
* Create Zip file for Combined Financial Files to send to Gilberto for verification
* Send the Combined Zip files to Gilberto and wait for verification results.



## Cleanup working directories
* Delete the files from the financial servicom directory: `\\prodfs1b\grm\Brazil\FinancialFiles\ServicomFinancialFiles`
* Delete the files from the navigator/combined files directory: `\\prodfs1b\grm\Brazil\FinancialFiles\`
* Delete the files from the tax servicom directory: `\\prodfs1b\grm\Brazil\Taxfiles\SrvcmTaxFiles`
* Delete the files from the navigator/combined files directory: `\\prodfs1b\grm\Brazil\Taxfiles\`

## Get the Servicom Tax and Financial Files for Servicom
Get the Tax and Financial files for Servicom from Gilberto either via e-mail or from Jira ticket.

## Extract Servicom Tax and Financial Files
* Extract the Financial Servicom files to `\\prodfs1b\grm\Brazil\FinancialFiles\ServicomFinancialFiles`
* Extract the Tax Servicom files to `\\prodfs1b\grm\Brazil\Taxfiles\SrvcmTaxFiles`

## Prepare Servicom Tax ND files for Oracle Use
* Convert the Servicom Tax ND files on `B` from ASCII to UTF8 (`\\prodfs1b\grm\Brazil\Taxfiles\SrvcmTaxFiles`)




