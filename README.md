# Linux Shell
We will look briefly at the LINUX command interpreter, called the SHELL, which, although not part of the operating system, makes heavy use of many operating system features and thus serves as a good example of how the system calls can be used. It is also the primary interface between a user sitting at his terminal and the operating system.
Shell has standard input and output as its terminal. Shell is started when a user begins to login. To start a command a dollar sign is typed which indicates the user that the shell is ready to accept the command.

## How it works
1. take user input 
2. allocate memory for user input 
3. create a child process using fork () command 
4. execute the input command is valid (in the child process). Parent will wait for the completion of the child process 
5. child process uses execvp() to transform user input into Linux command, and execute it 
6. Return to step 1 when success 
7. Use if-else for exception handling. Ex: Special case is “cd” command will not work with the C Unix Shell, allocation fail, fail to create a child process, fail to execute Linux command... 
8. The purpose of the program is to run Linux system command using my shell (c code) and practicing the child and parent process in Linux Shell. User input is the parent process, Linux commands execute is the child process. Please look at my diagram for further verification:

![alt](https://github.com/jackyhuynh/linuxShell-app/blob/main/src/picture/Diagram.png)

## Technology
- C Programming
- g++ compiler
- readline.h
- Multithreading (pthread.h)

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites
What things you need to install the software and how to install them
- Command-Prompt for Visual Studio: Same goes here. For this particular project, I highly recommend using Command-Prompt instead of the IDE.
- Linux: Program can be run on Linux System (if you are familiar with the Linux command line). 

### Installing

A step by step series of examples that tell you how to get a development env running

Visual Studio & Command-Prompt for Visual Studio:
* [Install Visual Studio](https://docs.microsoft.com/en-us/cpp/build/vscpp-step-0-installation?view=msvc-160#:~:text=Visual%20Studio%202019%20Installation%201%20Make%20sure%20your,...%204%20Choose%20workloads.%20...%20More%20items...) - If you haven't downloaded and installed Visual Studio and the Microsoft C/C++ tools yet, here's how to get started.
* [Developer Command Prompt for Visual Studio](https://docs.microsoft.com/en-us/dotnet/framework/tools/developer-command-prompt-for-vs#:~:text=%20Developer%20Command%20Prompt%20for%20Visual%20Studio%20,from%20inside%20Visual%20Studio.%20For%20easier...%20More) - Developer Command Prompt for Visual Studio enables you to use .NET Framework tools more easily. It's a command prompt that automatically sets specific environment variables. After opening Developer Command Prompt, you can enter the commands for .NET Framework tools such as ildasm or clrver.

Linux Ubuntu 18.4 LTS
* [Linux Ubuntu 18.4 LTS](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q?activetab=pivot:overviewtab) can be download at Microsoft Store

## Running the tests

Explain how to run the automated tests for this system:
* [Linux Compilers](https://askubuntu.com/questions/61408/what-is-a-command-to-compile-and-run-c-programs#:~:text=The%20simplest%20way%20to%20compile%20a%20C%2B%2B%20program,only%20compiler%20capable%20of%20compiling%20the%20Linux%20kernel.)- Locate the home folder that contains the program (by using the cd command). Call the g++ compiler and execute.
* [Visual Studio Command Line](https://docs.microsoft.com/en-us/cpp/build/walkthrough-compiling-a-native-cpp-program-on-the-command-line?view=msvc-160)

### Result

![alt](https://github.com/jackyhuynh/linuxShell-app/blob/main/src/picture/TrucShell.PNG)

## Deployment

Can be deployed to any embedded system without any problem. Can also make an API or library using this code. 

## Built With

* [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/) - The full-featured integrated development environment (IDE) for Android, iOS, Windows, web, and cloud.
* [.NET](https://dotnet.microsoft.com/download/dotnet-framework) -  Free. Cross-platform. Open-source. A developer platform for building the Internet of Things (IoT), Microservices, Desktop, Cloud, Mobile, Machine Learning, Web, Game.

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Truc Huynh** - *Initial work* - [TrucDev](https://github.com/jackyhuynh)

## Format
my README.md format was retrieved from
* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)
See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc


