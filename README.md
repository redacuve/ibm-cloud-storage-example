<!-- Badges -->
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-0.1-blue.svg?cacheSeconds=2592000" />
  <a href="#" target="_blank">
    <img alt="License: GPLv3 " src="https://img.shields.io/badge/License-GPL-yellow.svg" />
  </a>
  <a href="https://twitter.com/redacuve" target="_blank">
    <img alt="Twitter: redacuve " src="https://img.shields.io/twitter/follow/redacuve.svg?style=social" />
  </a>
</p>

<!-- Project Header -->
  <p align="center">
    <img alt="" src="https://firebasestorage.googleapis.com/v0/b/hackernoon-app.appspot.com/o/images%2F3QhYanjJvSgIJz7mG3iKq9qUuz72-80eo3u4u.png?alt=media&amp;token=663e5a1e-0640-4b43-8f25-899f8b1a1330" width="250">
  <h1 align="center">Basic Tutorial of How to connect to IBM Cloud Storage With Rails. </h1>
  <p align="center">
  <br>
   <a href="https://github.com/redacuve/ibm-cloud-storage-example"><strong>Explore the repo »</strong></a>
  <br>
    <a href="https://github.com/redacuve/ibm-cloud-storage-example/issues">Request Feature</a>
  </p>

<!-- TABLE OF CONTENTS -->

## Table of Contents

- [About the Project](#about-the-project)

- [Tutorial](#tutorial)

- [Built With](#built-with)

- [Getting Started](#getting-started)

- [How it Works](#how-it-works)

- [Contributing](#contributing)

- [License](#license)

- [Contact](#contact)

<!-- ABOUT THE PROJECT -->

## About The Project

This is the code from my tutorial "A Guide for Uploading and Showing Images Trough IBM CLOUD with RAILS 6", it is the most basic code to upload and retrieve images from IBM cloud, feel free to fork it. If you want to check the full "My Cats Photo" app, you can find the repo [here](https://github.com/redacuve/my-cat-photos).

## Tutorial

https://hackernoon.com/how-to-upload-and-display-images-trough-ibm-cloud-with-rails-6-xwj3um0

## Built With

- [Ruby](https://ruby-doc.org/core-2.7.0/)

- [HTML5](https://developer.mozilla.org/es/docs/HTML/HTML5)

- [IBM Cloud](https://cloud.ibm.com/docs)

- Gems used:
  - [carrierwave](https://rubygems.org/gems/carrierwave)
  - [fog-aws](https://rubygems.org/gems/fog-aws)
  - [mini_magick](https://rubygems.org/gems/mini_magick)

<!-- GETTING STARTED -->

## Getting Started

To get a local copy up and running follow these simple steps.

Clone or fork the <a href="https://github.com/redacuve/ibm-cloud-storage-example">repo</a> [git@github.com:redacuve/ibm-cloud-storage-example.git]

Note\* Ruby and Rails needs to be installed to run the code, check [here](https://www.ruby-lang.org/en/documentation/installation/) and [here](https://guides.rubyonrails.org/getting_started.html) for further steps. Also you need to setup your own IBM Cloud or AWS keys on the credentials. [credentials](https://guides.rubyonrails.org/security.html#custom-credentials) to work properly.

Attention\* If you want to setup this project locally you need to add YOUR OWN CLOUD KEYS on credientials.yml, to edit this file you NEED to run this command:

```
 $ EDITOR='nano' rails credentials:edit
```

note\* you must change the editor to your favorite, for example, gedit, vim, geany, kate, kwrite, emacs, etc.
Also, you MUST configure the file carrierwave.rb, this file is located at:

```
.
├── config
│   ├── initializers
│   │   ├── carrierwave.rb

```

The configuration of this file needs to have YOUR OWN cloud configuration:

- region: 'eu-west-1',
- endpoint: 'https://s3.example.com:8080'
- config.fog_directory = 'name_of_bucket'

<!-- HOW IT WORKS -->

## How it Works

It uses the carrierwave gem to upload files with ease, carrierwave by default is not able to send the uploaded files to the cloud, to achieve that we need to use the gem fow-aws, this gem allows to us to save the file previously uploaded with carrierwave to the cloud with the protocol S3, IBM cloud uses this protocol, so the configuration is straightforward.

## Running the code

- Navigate to the root directory of the project

- Run this command on your terminal to install all the needed gems:
  ```
  $ bundle install
  ```
- Install Yarn
  ```
  $ yarn install --check-files
  ```
- Create and migrate the database
  ```
  $ rails db:create
  $ rails db:migrate
  ```
- Add your own credentials for IBM Cloud or AWS
  ```
  $ EDITOR='nano' rails credentials:edit
  ```
- Run the develpment server with
  ```
  $ rails server
  ```
- Take a look at the app
  ```
  http://127.0.0.1:3000/
  ```

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

This project is under the <a href="https://www.gnu.org/licenses/gpl-3.0.html">GNU Public License V3</a>. For more information see <a href="https://github.com/redacuve/ibm-cloud-storage-example/blob/master/LICENSE">here</a>

<!-- CONTACT -->

## Contact

Rey David Cuevas Vela - [@redacuve](https://twitter.com/redacuve) - [redacuve@gmail.com](mailto:redacuve@gmail.com) -[linkedin.com/in/redacuve/](https://www.linkedin.com/in/redacuve/)

Project Link: [github.com/redacuve/ibm-cloud-storage-example](https://github.com/redacuve/ibm-cloud-storage-example) - IBM CLOUD Storage Example.
