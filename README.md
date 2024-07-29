# From SPSS to R: How to Make Your Statistical Analysis Reproducible

Comfortable/aware of how to run your stats in SPSS? Curious to learn how to run them in R? You've come to the right place.

In part 1 of this course, we will learn to:
- Download and navigate R.
- Work with R markdown documents.
- Conduct our trusty SPSS analysis through R.

In part 2 of this course, we will learn to:
-   Upload your own data to R.
-   Create a data tidying script.
-   Learn how to save your tidied data (in case you want to transfer analysis to other software/supervisors).
-   A reminder of our analyses.
-   Learn how to create APA ready analysis outputs - no more copy and pasting our results!

The material in this repo was developed and curated by Rhys Davies. All material collected here is free to use but is covered by a License: [![License: CC BY-NC 4.0](https://licensebuttons.net/l/by-nc/4.0/80x15.png)](https://creativecommons.org/licenses/by-nc/4.0/) license


## R Setting Up

You can either run the code on your own machine or through Posit (RStudio Online IDE) or if you are part of the University of Edinburgh through [Noteable](https://noteable.edina.ac.uk/).
Below are the instructions for setting up. 


### On Posit

1. Go to https://posit.cloud/
2. Signup either via Gmail or GitHub
3. Go on New Project
4. New Project from Git Repository
5. Copy and Paste this repository URL [https://github.com/DCS-training/From-SPSS-to-R-How-to-Make-Your-Statistical-Analysis-Reproducible](https://github.com/DCS-training/From-SPSS-to-R-How-to-Make-Your-Statistical-Analysis-Reproducible) as the Repository URL
6. The Project directory name will filled in automatically
7. Navigate to the rmd file you want to explore

### Locally

- R and RStudio are separate downloads and installations. R is the underlying statistical computing environment, but using R alone is no fun. RStudio is a graphical integrated development environment (IDE) that makes using R much easier and more interactive. You need to install R before you install RStudio. After installing both programs, you will need to install some specific R packages within RStudio. Follow the instructions below for your operating system, and then follow the instructions to install the needed packages(below)

_Windows_

- If you already have R and RStudio installed

  - Open RStudio, and click on "Help" > "Check for updates". If a new version is available, quit RStudio, and download the latest version for RStudio.
  - To check which version of R you are using, start RStudio and the first thing that appears in the console indicates the version of R you are running. Alternatively, you can type `sessionInfo()`, which will also display which version of R you are running. Go on the [CRAN website](https://cran.r-project.org/bin/windows/base/) and check whether a more recent version is available. If so, please download and install it. You can [check here](https://cran.r-project.org/bin/windows/base/rw-FAQ.html#How-do-I-UNinstall-R_003f) for more information on how to remove old versions from your system if you wish to do so.

- If you don't have R and RStudio installed

  - Download R from the [CRAN website](https://cran.r-project.org/bin/windows/base/release.htm).
  - Run the `.exe` file that was just downloaded
  - Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
  - Under _Installers_ select **RStudio x.yy.zzz - Windows Vista/7/8/10** (where x, y, and z represent version numbers)
  - Double click the file to install it
  - Once it's installed, open RStudio to make sure it works and you don't get any error messages.

_macOS_

- If you already have R and RStudio installed

  - Open RStudio, and click on "Help" > "Check for updates". If a new version is available, quit RStudio, and download the latest version for RStudio.
  - To check the version of R you are using, start RStudio and the first thing that appears on the terminal indicates the version of R you are running. Alternatively, you can type `sessionInfo()`, which will also display which version of R you are running. Go on the [CRAN website](https://cran.r-project.org/bin/macosx/) and check whether a more recent version is available. If so, please download and install it.

- If you don't have R and RStudio installed

  - Download R from the [CRAN website](https://cran.r-project.org/bin/macosx/).
  - Select the `.pkg` file for the latest R version
  - Double-click on the downloaded file to install R
  - It is also a good idea to install [XQuartz](https://www.xquartz.org/) (needed by some packages)
  - Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
  - Under _Installers_ select **RStudio x.yy.zzz - Mac OS X 10.6+ (64-bit)** (where x, y, and z represent version numbers)
  - Double-click the file to install RStudio
  - Once it's installed, open RStudio to make sure it works and you don't get any error messages.

_Linux_

- Follow the instructions for your distribution from [CRAN](https://cloud.r-project.org/bin/linux), they provide information to get the most recent version of R for common distributions. For most distributions, you could use your package manager (e.g., for Debian/Ubuntu run `sudo apt-get install r-base`, and for Fedora `sudo yum install R`), but we don't recommend this approach as the versions provided by this are usually out of date. In any case, make sure you have at least R 3.5.1.
- Go to the [RStudio download page](https://www.rstudio.com/products/rstudio/download/#download)
- Under _Installers_ select the version that matches your distribution, and install it with your preferred method (e.g., with Debian/Ubuntu `sudo dpkg -i rstudio-x.yy.zzz-amd64.deb` at the terminal).
- Once it's installed, open RStudio to make sure it works and you don't get any
  error messages.

Once you have R and R Studio installed, open R Studio

1.  Go to File>New Project> Version Control >Git
2.  Enter the Repository URL [https://github.com/DCS-training/From-SPSS-to-R-How-to-Make-Your-Statistical-Analysis-Reproducible](https://github.com/DCS-training/From-SPSS-to-R-How-to-Make-Your-Statistical-Analysis-Reproducible) 
3.  Select the Name for the directory project and where to save it
4.  Press Create Project
5.  Navigate to Day1 >DataVisWithR
6.  Click on `DataVisDHRSE.Rproj` (this is important to reset the working directory correctly)
7.  Click on `DataVis.Rmd`

### On Noteable
1. Go to https://noteable.edina.ac.uk/login
2. Login with your EASE credentials
3. Select RStudio as a personal notebook server and press start
4. Go to File >New Project>Version Control>Git
5. Copy and Paste this repository URL [https://github.com/DCS-training/From-SPSS-to-R-How-to-Make-Your-Statistical-Analysis-Reproducible](https://github.com/DCS-training/From-SPSS-to-R-How-to-Make-Your-Statistical-Analysis-Reproducible) as the Repository URL
6. The Project directory name will filled in automatically but you can change it if you want your folder in Notable to have a different name
7. Decide where to locate the folder. By default, it will locate it in your home directory 
8. Press Create Project

  
