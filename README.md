
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
<!-- [![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url] -->



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <!-- <a href="https://github.com/DAMONYLY/readme_template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a> -->

  <h3 align="center">Peppa-With-AI</h3>

  <p align="center">
    A PIG with AI, namely, Peppa!
    <br />
    <a href="https://github.com/DAMONYLY/readme_template"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/DAMONYLY/readme_template">View Demo</a>
    ·
    <a href="https://github.com/DAMONYLY/readme_template/issues">Report Bug</a>
    ·
    <a href="https://github.com/DAMONYLY/readme_template/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#Design-Overview">Design Overview</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
This repo aims at correcting student homework automatically based on OCR engine and template matching strategy. 

Now the repo support correcting questions with fixed answer area because of the limitations of template matching method via perspective transform. 

Three steps are contained:
1. Find matching template and anchor positions 
2. Find answer positions in homework
3. Correct answer in homework based on ocr engine.

### Design Overview

```mermaid
graph LR

modules[modules:作业批改模块]-->common[common:通用模块组]
common-->api_service[api_service:网络调用类]
common-->geometry[geometry:几何结构]
common-->function[functino:小型函数]

modules-->io[io:IO模块组]
io-->json_io[json_io:JSON相关的IO函数]
io-->image_io[image_io:图像相关的IO函数]

modules-->utils[utils:辅助函数]
modules-->globals[globals:单例模块]

modules-->matcher[matcher:核心匹配模块组]
matcher-->match_assistant[match_assistant:手写印刷辅助模块]
matcher-->slice[slice:切题模块]

modules-->marker[marker:核心批改模块组]
marker-.->fixed[固定答题区域题型]
marker-.->unfixed[非固定答题区域题型]
```

<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

1. Get a free API Key at [https://example.com](https://example.com)
2. Clone the repo
   ```sh
   git clone https://github.com/your_username_/Project-Name.git
   ```
3. Install NPM packages
   ```sh
   npm install
   ```
4. Enter your API in `config.js`
   ```JS
   const API_KEY = 'ENTER YOUR API';
   ```



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/DAMONYLY/readme_template/issues) for a list of proposed features (and known issues).



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

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Img Shields](https://shields.io)
* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Pages](https://pages.github.com)
* [Animate.css](https://daneden.github.io/animate.css)
* [Loaders.css](https://connoratherton.com/loaders)
* [Slick Carousel](https://kenwheeler.github.io/slick)
* [Smooth Scroll](https://github.com/cferdinandi/smooth-scroll)
* [Sticky Kit](http://leafo.net/sticky-kit)
* [JVectorMap](http://jvectormap.com)
* [Font Awesome](https://fontawesome.com)





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/DAMONYLY/readme_template.svg?style=for-the-badge
[contributors-url]: https://github.com/DAMONYLY/readme_template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/DAMONYLY/readme_template.svg?style=for-the-badge
[forks-url]: https://github.com/DAMONYLY/readme_template/network/members
[stars-shield]: https://img.shields.io/github/stars/DAMONYLY/readme_template.svg?style=for-the-badge
[stars-url]: https://github.com/DAMONYLY/readme_template/stargazers
[issues-shield]: https://img.shields.io/github/issues/DAMONYLY/readme_template.svg?style=for-the-badge
[issues-url]: https://github.com/DAMONYLY/readme_template/issues
[license-shield]: https://img.shields.io/github/license/DAMONYLY/readme_template.svg?style=for-the-badge
[license-url]: https://github.com/DAMONYLY/readme_template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/DAMONYLY
[product-screenshot]: images/screenshot.png
