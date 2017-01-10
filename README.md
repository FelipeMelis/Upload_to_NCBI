## Upload to NCBI

![NCBI Logo]
(https://www.ncbi.nlm.nih.gov/corehtml/logo256.gif)


**Protocol for upload genomic data to NCBI**

1. Create a SRA project (thi)
  * https://submit.ncbi.nlm.nih.gov/subs/sra/ [New Submission]
  
2. Create new BioProject and Biosamples in the same SRA project (**later you can access to theirs respective ids**)
  * Fill the excel data for the pathogens and save as a tab delimited file
  * Fill the excel with the SRA Metadata and save as a tab delimited file
 
3. ftp upload for the reads (>300 mb)
  * Access to NCBI ftp server: ``` ftp -i ncbi_ftp_server ``` (**the user and password are in the login page of your submission portal**)
  * cd to upload folders and create a subfolder with a meaningful name (mkdir) 
  * ``` mput *files ``` (this upload the files to ftp server)
  * Wait

4. Create a WGS project
  * https://submit.ncbi.nlm.nih.gov/subs/wgs [New Submission]
  * Register de Bioproject and Biosample ID, one WGS project for Biosample ID (this data are in the SRA submission portal)
  * Upload the contig fasta file (min contig len > 200) (use perl script: ```./removesmalls.pl 200 contigs.fasta > contigs_200.fasta ```)
  * Register authors and a reference title
  
