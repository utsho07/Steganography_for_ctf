# Steganography_for_ctf

# Staganography

Steganography is a process that is use for hiding information inside of image,video or any other digital object..

**Tools:**

`strings`

`exiftool`

`steghide`

`zsteg`

`stegoveritas`

`binwalk`

`stegsolver`

`Foremost`

`Xiao`

`Openstego`

`outguess`

**To hide a file in an image:**

To make a file we can use nano commad:

`nano file_name`

**Hide data:**

We use “steghide” command to hide any file within a image..

`steghide  embed -cf image_file -ef text_file`

**To open an image using the terminal we can use:**

`eog image_name.`

**To extract that file we can use:**

`steghide extract -sf image_name`

**To hide some message in an audio:**

we can use deep sound software to hide message..it is a window based software..

Then we need to download our audio.

Then we need our message.

Then we can easily encrypt data using that software..

**Use of various tools:**

**strings:**

We use strings command to know the meta data of a file

command:

           `strings file_name`

**exiftool:**

ExifTool is a free and open-source software program for reading, writing, and manipulating image, audio, video, and PDF metadata. It is platform independent, available as both a Perl library and command-line application.

How to use:

           `exiftool file_name`

**zsteg:**

zteg is atool which is use for hide data for the png file..It is like the
steghide tool..

command:

           `zsteg image.png`


**outguess:**

Outguess is a another tool to extract the hidden message from a image [file.](http://file.To) To use this tool we need to install it  and we can use it by using below command:

      `outguess -r pic.jpg result_file_name`
      
**stegoveritas**

stegoveritas is a very fantastic tool to work with.It extract all the file of a
image and another thing is it supported every image file..

command:

           `stegoveritas Image_file_name`

This command create a result folder in the folder. In this folder all the
the analysis file can be found.

### **Binwalk**:

Binwalk is a powerful command-line tool used for analyzing and extracting
data embedded within binary files in the Linux environment. It is
specifically designed for firmware images, executable files, and
other binary data. Binwalk is a valuable utility for reverse
engineering, security auditing, and forensics tasks, as it helps
identify hidden content and structures within binary files.

Command:

        `binwalk -e image_name`

### **Stegsolver**:

This tool changes color combination of a image and then we can find our
flag.

Install:

`wget http://www.caesum.com/handbook/Stegsolve.jar -O    stegsolve.jar`

`chmod +x stegsolve.jar`

`mkdir bin`

`mv stegsolve.jar bin/`

how to open:

`java -jar  stegsolver`

### **Foremost:**

Foremost is a  data recovery tool for Linux. It is used to recover files using
their headers, footers, and data structures through a process known
as file carving. It create a file called output..Inside this file we
can find our data..

command:

`foremost image_file`

**Xiao:**

Xiao Steganography is free software that can be used to hide secret
files in BMP images or WAV files. Using the tool is easy: you can
just open the software and load any BMP image or WAV file to its
interface. Then add a file you want to hide. It also supports
encryption.

**OpenStego**

OpenStego is a free and open-source steganography tool that can be used to hide
data in images, audio files, and video files. It is a Java-based
tool.

Command:

```python
java -jar openstego.jar
```

### **Process for solving Steganography image Challenges(collected):**

Step
1: check file type using file command

Step2:use
exiftool command

Step3:use
strings command

Step4:use
steghide command if you have password for extract otherwise use
binwalk (But luckly you can try steghide without password)

Step5:zsteg
tools

Step6:open
stegsolve.jar file using java –jar stegsolve.jar ( then , try to
use it according to its uses )

Step7:use
magic eye solver

Step8:use
diit-1.5.jar and try to extract information

### **Process for solving Steganography wav Challenges :**

Step
1 :open file and listen it .

Step
2 :If target audio file is morse code try to extract information
using online morse code decode tools .If not , follow step 3

Step
3 :open sonic visualizer and try to extract information from it .

Step
4 : If above all step are failed . Try to extract data using steghide
as it has ability to extract audio file.
