## Add a new font

1. Go to [Google Fonts](https://fonts.google.com/) and pick a cool one, for example monserrat.
1. Click on _Download Family_ and save the zip in `fonts` fondler.
1. Unzip the within a folder with the same name, ie `Monserrat`, the `fonts` structure is something like this:
   ```
   ├── JetBrainsMono
   │   ├── JetBrainsMono-BoldItalic.ttf
   │   ├── JetBrainsMono-Bold.ttf
   │   ├── JetBrainsMono-Italic.ttf
   │   ├── JetBrainsMono-Regular.ttf
   │   └── OFL.txt
   ├── Kanit
   │   ├── Kanit-LightItalic.ttf
   │   ├── Kanit-Light.ttf
   │   ├── Kanit-ThinItalic.ttf
   │   ├── Kanit-Thin.ttf
   │   └── OFL.txt
   └── Montserrat
      ├── Montserrat-BlackItalic.ttf
      ├── Montserrat-Black.ttf
      ├── Montserrat-BoldItalic.ttf
      ├── Montserrat-Bold.ttf
      ├── Montserrat-ExtraBoldItalic.ttf
      ├── Montserrat-ExtraBold.ttf
      ├── Montserrat-ExtraLightItalic.ttf
      ├── Montserrat-ExtraLight.ttf
      ├── Montserrat-Italic.ttf
      ├── Montserrat-LightItalic.ttf
      ├── Montserrat-Light.ttf
      ├── Montserrat-MediumItalic.ttf
      ├── Montserrat-Medium.ttf
      ├── Montserrat-Regular.ttf
      ├── Montserrat-SemiBoldItalic.ttf
      ├── Montserrat-SemiBold.ttf
      ├── Montserrat-ThinItalic.ttf
      ├── Montserrat-Thin.ttf
      └── OFL.txt
    ```
1. Create a file with the same font name that you've chosen in the root folder with the extension `.fontspec`. eg: `Monserrat.fontspec`
1. Fill the content of `Monserrat.fontspec` with the following:
   ```tex
   \defaultfontfeatures[Monserrat]{
       Path= ./fonts/Monserrat/,
       Extension = .ttf,
       UprightFont=*-Regular,
       BoldFont=*-Bold,
       ItalicFont=*-Italic,
   	   BoldItalicFont=*-BoldItalic,
   }
   ```
1. Finally, replace in `main.tex`: `\setmainfont{Kanit}` to `\setmainfont{Monserrat}` and it's ready to use! 😄
   


## Examples 

Find out more at [Google Fonts](https://fonts.google.com/)

### Kanit

![image](https://user-images.githubusercontent.com/41640423/129288409-fe38ef66-ce41-48e9-b37d-04ca4a517e07.png)


### JetBrains Mono

![image](https://user-images.githubusercontent.com/41640423/129288563-90c4b8e2-7f22-46db-90ba-575b1e03a43b.png)


# Compile

	pdflatex -synctex=1 -interaction=nonstopmode -output-directory out %.tex

# Format

	 latexindent -m file.tex -w -l style.yaml -s

