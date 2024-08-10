<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
<div align="center">

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

</div>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/mboyov/TasksProgressBar">
    <img src="images/logo.png" alt="Logo" width="30%" height="auto">
  </a>

<h3 align="center">Obsidian ProgressBar</h3>

  <p align="center">
    Tracking tasks with a progress bar with Obsidian
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About

[![Product Name Screen Shot][product-screenshot]]()

I recently started using the Obsidian software. After configuring it to my preferences, I found that I was missing a visual overview of my task progress.

After some research, I found a way to integrate it, and now I would like to share this procedure.


### Built With

[![Obsidian][Obsidian.md]][Obsidian-url]

### Prerequisites

#### Plugins

* [DataView](https://blacksmithgu.github.io/obsidian-dataview/)
* [MetaEdit](https://github.com/chhoumann/MetaEdit)


### Installation

After installing both plugins, I'll let you configure them like this:

**Dataview**

***Dataview is a live index and query engine over your personal knowledge base. You can add metadata to your notes and query them with the Dataview Query Language to list, filter, sort or group your data. Dataview keeps your queries always up to date and makes data aggregation a breeze.***
 
![dataview_config][dataviewconfig-screenshot]

- **To reduce the refresh time, I'll let you change the value of the 'Refresh Interval' field from 2500 to 150 milliseconds.**

***If these options are not enabled, the JavaScript code we will edit later will not be able to be interpreted.***

**MetaEdit**

By [Christian B. B. Houmann aka chhoumann](https://github.com/chhoumann/MetaEdit) MetaEdit for Obsidian

Progress Properties that automatically update properties/fields  

![metaedit-config][metaeditconfig-screenshot]

I'll let you add these three fields and values as shown in the screenshot.

***It's important to maintain the association between names and types, otherwise synchronization won't be possible.***

It is now time to create your note page and add this header, specifying the property names.

![header][header-screenshot]

To finish, we will now add our dataviewjs script.

![dataviewjs][dataviewjs-screenshot]

```js
let myPage = dv.current()
    let total = myPage.total;
    let status = ((myPage.completed / myPage.total) * 100).toFixed();
    const progress = "![pb|500](https://progressbar-guibranco.vercel.app/" + status + "/?scale=" + "100" + "&width=400)";
    dv.header(3, "Objectif du jour"); dv.paragraph(progress);
```

We can now add our tasks and see the progress bar update automatically in read mode

![progressbar][progressbar-screenshot]

<!-- USAGE EXAMPLES -->
## Usage

```shell
git clone git@github.com:mboyov/TasksProgressBar.git
```
- In the Obsidian application, open a folder as a vault.
- Select the location where you cloned the repository.
- Trust the author and enable plugins.

Et voilà !


See the [open issues](https://github.com/mboyov/TasksProgressBar/issues) for a full list of proposed features (and known issues).

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.


<!-- CONTACT -->
## Contact

v__nova - [@mboyov](https://twitter.com/mboyov) - mboyov@arcadev.ch 

Project Link: [https://github.com/mboyov/TasksProgressBar](https://github.com/mboyov/TasksProgressBar)

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Snifer - Tracking Project in Obsidian with ProgressBar](https://github.com/Snifer/Curso-obsidian-desde-0/blob/main/TrackingProjects%20Obsidian.md)
* [Othneil Drew - Best-README-Template ](https://github.com/othneildrew/Best-README-Template) 

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/mboyov/TasksProgressBar.svg?style=for-the-badge
[contributors-url]: https://github.com/mboyov/TasksProgressBar/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/mboyov/TasksProgressBar.svg?style=for-the-badge
[forks-url]: https://github.com/mboyov/TasksProgressBar/network/members
[stars-shield]: https://img.shields.io/github/stars/mboyov/TasksProgressBar.svg?style=for-the-badge
[stars-url]: https://github.com/mboyov/TasksProgressBar/stargazers
[issues-shield]: https://img.shields.io/github/issues/mboyov/TasksProgressBar.svg?style=for-the-badge
[issues-url]: https://github.com/mboyov/TasksProgressBar/issues
[license-shield]: https://img.shields.io/github/license/mboyov/TasksProgressBar.svg?style=for-the-badge
[license-url]: https://github.com/mboyov/TasksProgressBar/blob/main/LICENSE.txt
[product-screenshot]: images/screenshot.png
[dataviewconfig-screenshot]: images/dataview_config.png
[metaeditconfig-screenshot]: images/metaedit_config.png
[header-screenshot]: images/header.png
[dataviewjs-screenshot]: images/dataviewjs.png
[progressbar-screenshot]: images/progressbar.png
[Obsidian.md]: https://img.shields.io/badge/Obsidian-black?logo=Obsidian&logoColor=purple
[Obsidian-url]: https://obsidian.md/
[Dataview-url]: https://blacksmithgu.github.io/obsidian-dataview/
[MetaEdit-url]: https://github.com/chhoumann/MetaEdit
