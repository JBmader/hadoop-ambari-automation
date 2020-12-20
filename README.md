<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/alexhff/hadoop-ambari-automation">
    <img src="https://www.google.com/url?sa=i&url=https%3A%2F%2Fcommons.wikimedia.org%2Fwiki%2FFile%3AHadoop_logo.svg&psig=AOvVaw3reqoXh7iKmQ6xPxNdUa95&ust=1608547814577000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCIDDqt2x3O0CFQAAAAAdAAAAABAD" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Hadoop via Ambari automation</h3>

  <p align="center">
    Hadoop (HDP) installation via Ambari on Vagrant VMs with Ansible/Chef/Puppet to configuration VMs and work on APIs.
    <br />
    <a href="https://github.com/alexhff/hadoop-ambari-automation"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/alexhff/hadoop-ambari-automation/issues">Report Bug</a>
    ·
    <a href="https://github.com/alexhff/hadoop-ambari-automation/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
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
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://example.com)

Here's a blank template to get started:
**To avoid retyping too much info. Do a search and replace with your text editor for the following:**
`alexhff`, `hadoop-ambari-automation`, `twitter_handle`, `email`, `project_title`, `project_description`


### Built With

* []()
* []()
* []()



<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites

To continue with the project, you will need the following software installed on your machine :
* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/)

### Installation

Clone the repo
```sh
git clone https://github.com/alexhff/hadoop-ambari-automation.git
```
Navigate to the repo
```sh
cd hadoop-ambari-automation
```
Copy the private key to your home directory (or some place convenient for you) so that it’s easily accessible for uploading via Ambari Web:
```sh
vagrant
```
The above command shows the command usage and also creates a private key as ~/.vagrant.d/insecure_private_key. This key will be used in the following steps.

### Starting VMs

Copy the private key to the local repo:
```sh
cp ~/.vagrant.d/insecure_private_key .
```
Now you can start VMs with the following command:
```sh
./up.sh <number of VMs to launch>
```



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

### Manually installing Ambari

Ansible is responsible for installing Ambari. However, if you want to install Ambari manually, follow the procedures:

Log into the VM:
```sh
vagrant ssh c7401
```
Note that this logs you in as user vagrant. Once you are logged in, you can run:
```sh
sudo su -
```
to make yourself root.
Download the Ambari repository file to a directory on your installation host:
```sh
wget -nv http://public-repo-1.hortonworks.com/ambari/centos7/2.x/updates/2.7.4.0/ambari.repo -O /etc/yum.repos.d/ambari.repo
```
Install ambari:
```sh
yum install ambari-server -y
```
Run the following to set up and start ambari-server:
```sh
ambari-server setup -s
ambari-server start
```

Once Ambari Server is started, hit http://http://192.168.74.101:8080/ (URL depends on the OS being tested) from your browser on your local computer.
Note that Ambari Server can take some time to fully come up and ready to accept connections. Keep hitting the URL until you get the login page.

Once you are at the login page, login with the default username `admin` and password `admin`.



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



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements

* [Alexander Hoffmann](https://github.com/alexhff)
* [Adrien Bourget](https://github.com/adritoo)
* [Jean-Baptiste Mader](https://github.com/jbmader)

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/alexhff/repo.svg?style=for-the-badge
[contributors-url]: https://github.com/alexhff/repo/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/alexhff/repo.svg?style=for-the-badge
[forks-url]: https://github.com/alexhff/repo/network/members
[stars-shield]: https://img.shields.io/github/stars/alexhff/repo.svg?style=for-the-badge
[stars-url]: https://github.com/alexhff/repo/stargazers
[issues-shield]: https://img.shields.io/github/issues/alexhff/repo.svg?style=for-the-badge
[issues-url]: https://github.com/alexhff/repo/issues
[license-shield]: https://img.shields.io/github/license/alexhff/repo.svg?style=for-the-badge
[license-url]: https://github.com/alexhff/repo/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/alexhff