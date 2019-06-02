# Tools
* Notepad++
	When you use the Notepad++ zip package version, you can import [this](./Notepad++.reg) to add Notepad++ in the right click menu.
	> :warning: Change the path of the Notepad++ before you import it.
* Extract JDK8.exe (How to use the JDK without installation on Windows)
	1. Download the JDK.exe
	2. Open the .exe file via 7-Zip
	3. Extract .rsrc/1033/JAVA_CAB10/111 to your disk (like: c:\temp_jdk)
	4. Open the terminal (win + R -> cmd)
		```
		cd c:\temp_jdk
		extrac32 111
		```
	5. Then extract the tools.zip to your disk (like: c:\jdk) via 7-Zip 
	6. Run below in the terminal
		```
		cd c:\jdk
		for /r %x in (*.pack) do .\bin\unpack200 -r "%x" "%~dx%~px%~nx.jar"
		```
