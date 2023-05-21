# cmcl-bat
::cmcl.bat&nbsp;
@echo off
set APATH=%cd%
set ADISK=%cd:~0,2% 
::set ADISK=%~d0
D:
cd D:\new_minecraft

if "%1" == "ds0" (
  java -jar D:\new_minecraft\cmcl.jar config downloadSource 0
) else if "%1" == "ds1" (
  java -jar D:\new_minecraft\cmcl.jar config downloadSource 1
) else if "%1" == "ds2" (
  java -jar D:\new_minecraft\cmcl.jar config downloadSource 2
) else if "%1" == "pon" (
  java -jar D:\new_minecraft\cmcl.jar config proxyEnabled true
) else if "%1" == "poff" (
  java -jar D:\new_minecraft\cmcl.jar config proxyEnabled false
) else (
  java -jar D:\new_minecraft\cmcl.jar %1 %2 %3 %4 %5 %6 %7 %8 %9
)

%ADISK%
cd %APATH%
