

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]




<br />
<p align="center">
  <h3 align="center">AstroLauncher Dedicated Server Launcher</h3>

  <p align="center">
    <a href="https://github.com/ricky-davis/AstroLauncher/issues">AstroLauncher Bugs</a>
    ·
    <a href="https://github.com/ricky-davis/AstroLauncher/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

- [Table of Contents](#table-of-contents)
- [What does it do?](#what-does-it-do)
- [TODO](#todo)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Building an EXE](#building-an-exe)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)




## What does it do?
1. Checks to see if the IP:Port combo is registered with Playfab, if so, Deregisters it.
2. Starts the server, and waits for it to register
3. Starts a loop to check for and display players joining/leaving, using the remote console port
4. Keeps a log of everything in the logs folder
5. Restarts the server if it closes, unless it closes before it registers.


## TODO
1. Create a watcher process to determine if the launcher is closed, to close the Dedicated Server
2. Implement Save-backups with adjustable intervals
3. Auto Public IP checking / NAT Loopback detection


<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* Python 3.7
* pip / pipenv

### Installation
 
1. Clone the AstroLauncher repository
```sh
git clone https://github.com/ricky-davis/AstroLauncher.git
```
2. Install python modules using pip or pipenv
```sh
pip install requirements.txt
```
```sh
pipenv install
```

<br />

<!-- USAGE EXAMPLES -->
## Usage

Run the server launcher using one of the following commands
```sh
python Run-Server.py
```
```sh
pipenv run python AstroLauncher.py
```

<br /><br />
If not placed in the same directory as the server files, you can specify a server folder location like so

```sh
python AstroLauncher.py --path "steamapps\common\ASTRONEER Dedicated Server"
```
```sh
pipenv run python AstroLauncher.py -p "steamapps\common\ASTRONEER Dedicated Server"
```

<br />

### Building an EXE

1. If you want to turn this project into an executable, make sure to install pyinstaller using one of the following methods
```sh
pip install pyinstaller
```
```sh
pipenv install -d
```
2. Run pyinstaller with the all-in-one flag
```sh
pyinstaller AstroLauncher.py -F
```
3. Move the executable (in the new `dist` folder) to the directory of your choice. (You can now delete the `dist` and `build` folders, as well as `AstroLauncher.spec`)
4. Run AstroLauncher.exe
```sh
AstroLauncher.exe -p "steamapps\common\ASTRONEER Dedicated Server"
```




<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/ricky-davis/AstroLauncher/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Ricky Davis - Discord: @Spyci#0001

Project Link: [https://github.com/ricky-davis/AstroLauncher](https://github.com/ricky-davis/AstroLauncher)




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/ricky-davis/AstroLauncher.svg?style=flat-square
[contributors-url]: https://github.com/ricky-davis/AstroLauncher/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ricky-davis/AstroLauncher.svg?style=flat-square
[forks-url]: https://github.com/ricky-davis/AstroLauncher/network/members
[stars-shield]: https://img.shields.io/github/stars/ricky-davis/AstroLauncher.svg?style=flat-square
[stars-url]: https://github.com/ricky-davis/AstroLauncher/stargazers
[issues-shield]: https://img.shields.io/github/issues/ricky-davis/AstroLauncher.svg?style=flat-square
[issues-url]: https://github.com/ricky-davis/AstroLauncher/issues
[license-shield]: https://img.shields.io/github/license/ricky-davis/AstroLauncher.svg?style=flat-square
[license-url]: https://github.com/ricky-davis/AstroLauncher/blob/master/LICENSE.txt