# esp-idf-vscode-boilerplate
Boilerplate for developing ESP32 projects using ESP-IDF and VS Code

## Prerequisite
  > Install [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools) extension for VisualStudio Code.

  > Setup of the [Toolchain](https://docs.espressif.com/projects/esp-idf/en/release-v3.0/get-started/index.html#setup-toolchain) and make sure you have path to XTENSA compiler _bin_ folder needs to be present on the `PATH`.  
  
  > Install [ESP_IDF](https://docs.espressif.com/projects/esp-idf/en/release-v3.0/get-started/index.html#get-esp-idf) and make sure that you have `ESP_IDF` environment variable set.

## How to use

1. Clone repository

Open the command palette with the key combination of cmd + Shift + P.

At the command palette prompt, enter gitcl, select the Git: Clone command, and press Enter.

When prompted for the Repository URL, select clone from GitHub, then press Enter.

Enter [esp-idf-vscode-boilerplate](https://github.com/nechry/esp-idf-vscode-boilerplate.git) in the Repository URL field.

Select (or create) the local directory into which you want to clone the project.

[Not required] Change the default project name called *main* in files.
This step renames the executable file. By default, the executable file is *main.elf*.

Open CMakeLists.txt and replace main by <my_project_name>
Open Makefile and replace main by <my_project_name>
Open .vscode/launch.json and replace main by <my_project_name> (lines 11 and 19)


## Config, Build and Flash

Open the command palette with the key combination of cmd + Shift + P.

Hit CMD I P, to choose right comm port

Hit CMD I D, to build, flash and monitor

Or use integrated Terminal in Visual Studio Code

```bash
idf.py set-target (esp32 esp-s2 esp-s3)
idf.py menuconfig
idf.py build
idf.py -p (PORT) flash
idf.py -p (PORT) monitor
```

## License

[MIT](LICENSE)
