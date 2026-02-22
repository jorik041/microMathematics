## Directory microMathematics/doc

This directory contains LaTeX source files for printable documentation (English, German, Russian, Brazilian Portuguese).

**Note:**
In order to build the documentation, the LaTeX (texlive) and following latex packages shall be installed on the host machine. For example, to install texlive on Fedora Workstation, perform following commands:

- as the root user:
```
# dnf install texlive
# dnf install texlive-gensymb
# dnf install texlive-lipsum texlive-sectsty texlive-t2 texlive-lastpage texlive-lettrine texlive-titling texlive-fonts-tlwg babel texlive-minifp
# dnf install texlive-cyrillic texlive-babel-russian texlive-hyphen-russian texlive-lh 
# dnf install texlive-babel-german texlive-hyphen-german
# dnf install texlive-babel-portuges texlive-hyphen-portuguese
# dnf install texlive-babel-spanish texlive-hyphen-spanish
# dnf install texlive-collection-mathextra
# fmtutil -sys --all
```
- as a local user (not root):
```
# fmtutil -user --missing
```

After LaTeX is installed, call 
```
# chmod +x build-doc.sh 
# ./build-doc.sh <version_code>
```

AVD configuration used to export documentation (../avd/<Your_AVD_Name>.avd/config.ini): Nexus 4, 768 x 1280, 320 dpi:
hw.device.name=Nexus 4
hw.lcd.density=320
hw.lcd.height=1280
hw.lcd.width=768

On the device, generated documentation is placed here: /data/data/com.mkulesh.micromath.plus/files/doc