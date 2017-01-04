## Upload to NCBI

![NCBI Logo]
(https://www.ncbi.nlm.nih.gov/corehtml/logo256.gif)


Protocol for upload genomic data to NCBI

1. Create a SRA project
  * https://submit.ncbi.nlm.nih.gov/subs/sra/ [New Submission]
  
2. Create new BioProject and Biosamples in the same SRA project
  * Fill the excel data for the pathogens and save as a tab delimited file
  * Fill the excel with the SRA Metadata and save as a tab delimited file
 
3. ftp upload
  * Access to NCBI ftp server: ``` ftp -i ncbi_ftp_server ```
  * cd to upload folders and create a subfolder with a meaningful name (mkdir) 
  * ``` mput *files ```
  * Wait
     
