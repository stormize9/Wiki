
#### .BAT file to resize several pictures


```
@echo off

setlocal enabledelayedexpansion

  

set "folder=%~dp0"

for %%i in ("%folder%*.jpg") do (

  magick "%%i" -resize 50%% "%%~ni%%~xi"

)

  

pause
```
