# The VT-May-2020-WinEXE-Image dataset

* To enable malware researchers to compare different classification approaches, we disclose how to create our dataset.

* This dataset contains 1,556 malware images from 18 different malware families. The original malware of the dataset are included in the VirusTotal malwere sample folder. 

* When your papers or articles use the dataset, please cite the following paper.

* COMPSAC

# How to create the dataset
### 1. Apply for the VirusTotal malware sample folder as an academic user

* Apply at the VirusTotal site. If you are approved for an academic account, there is no charge.
* https://www.virustotal.com/gui/home/upload
* Contact Us -> I have a commercial inquiry -> I am interested in premium services

### 2. Access to the VirusTotal malware sample folder 

* Move to 2020-05-06 folder.
* Download Win32_EXE.7z.

### 3. Unzip malware files
* See the "README - VirusTotal Academic Malware Samples.docx."
* Note that these are real malware.

### 4. Make directory and put malware files
* The following steps are confirmed in Ubuntu 20.04 LTS.
```
./00_make_directory.sh
```
* Copy unzipped malware files to "virustotal" directory.
* Check the file type. 
```
file ./virustotal/000a65b4dc39c24eda9987f2d0fd77a8f033526d3f986791598f350c2667da82
```
-> PE32 executable (GUI) Intel 80386 (stripped to external PDB), for MS Windows, PECompact2 compressed

### 5. Create dataset
```
sudo apt-get install pnmtopng
```
```
./01_binary_copy.sh
```
```
./02_malwareimage.sh
```
```
./03_image_copy.sh
```


### 6. Check the malware image samples
```
cd ./dataset
```

* 001/0aa73b88b3f3272b04599d7d834b27ae42ff1dafa2403b5dccecc6ad817da863.png
<img src="./sample01.png" width=10%>

* 002/1d6bddc4d5568ff753cfc4b9157222dbb0f2ded7378d3422c15f492810baa446.png
<img src="./sample02.png" width=10%>
