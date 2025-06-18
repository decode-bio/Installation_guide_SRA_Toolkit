# Objective
To documnent the SRA toolkit installation

# Steps 
* Installation
* Extraction
* Configuration
* Verification & functionality

# 1. Installation
Fetching the tar file from the canonical location at NCBI:
* for Ubuntu,
```
wget --output-document sratoolkit.tar.gz https://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-ubuntu64.tar.gz
```
* Output
![image](https://github.com/user-attachments/assets/2fb65ae1-b144-47d9-acad-1bb970858566)

# 2. Extraction
In this step, the contetns of the tar file has been extracted. To extract we can use the following command
```
tar -vxzf sratoolkit.tar.gz
```
*Output

 ![image](https://github.com/user-attachments/assets/9238e553-dd68-4491-b56c-7984dd7044a4)


# 3. Configuration
we can see a README-vdb-config file in the contetns of extracted folder, which will be used to configure this SRA package
  ![image](https://github.com/user-attachments/assets/fe8bf100-33b5-4271-8ac4-9f90a5fc1333)

to configure we have already made an empty directory named SRA. to configure the contents of the toolkit, we will use the follwoing command after going to bin
```
vdb-congif -i
```
* Output
  ![image](https://github.com/user-attachments/assets/ac63c8b8-43aa-4274-91e1-b68e007c7512)

* Click on the CACHE and choose your emppty directory(for me its SRA) as new location of user-repository and save the changes
  ![image](https://github.com/user-attachments/assets/cc98114d-de5d-4307-abc1-ec311b85d19e)

#  Verification & functionality
Now we can use our SRA toolkit or not, to verify write the follwoing command
```
which fastq-dump
```
* output
```
/usr/bin/fastq-dump
```
* To check the Functionality [source: https://github.com/ncbi/sra-tools/wiki/02.-Installing-SRA-Toolkit]
Use the following command
```
fastq-dump --stdout -X 2 SRR390728
```
* which should produce the following output, and nothing else
![image](https://github.com/user-attachments/assets/f8afa255-e5a7-49c1-9d0f-b8b3c25ad420)

* can use the other SRR id also to check the funtionality of the toolkit.

THANKS! & HAPPY SCRIPTING :)


