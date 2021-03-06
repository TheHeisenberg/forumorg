# forumorg

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/9434218caecf4ca08121ec60ed4accea)](https://www.codacy.com/app/app65382894/forumorg?utm_source=github.com&utm_medium=referral&utm_content=ForumOrganisation/forumorg&utm_campaign=badger)
[![Website](https://img.shields.io/website-up-down-green-red/http/shields.io.svg)](https://www.forumorg.org)
[![GitHub repository](https://img.shields.io/badge/GitHub-ForumOrganisation%2Fforumorg-blue.svg)](https://github.com/ForumOrganisation/forumorg)

This is the repository of [Forum Organisation](https://www.forumorg.org)'s official website.

## Getting Started

These instructions will get help get your own copy of the project running on your local machine for development and testing purposes.

### Requirements

To get your development environment running, you need:

- python 3.6
- bower
- mongodb

### Install

To install the necessary dependencies:

```sh
git clone https://github.com/ForumOrganisation/forumorg.git
cd forumorg
pip install -r requirements.txt
bower install
```

### Configuration
To start the project, you need to provide the following environment variables:

```sh
export MONGODB_URI="mongodb://host:port/dbname" # Required: running mongodb instance
export BUCKET_NAME="bucket_name" # Required: S3 bucket name
export DEBUG=True # Optional: Nice for debugging
export SENDGRID_API_KEY="sendgrid_key" # Optional: for emailing events
```

### Run
```sh
python runserver.py
```

## Deploying
We use Heroku for Cloud hosting and Continuous Integration.

On ```git push origin master```:

- The code is pushed to this repository (on `master`).
- A build is triggered on our [staging app](https://forumorg-staging.herokuapp.com) (useful for testing in a production-like environment).

On ```any approved PR request```:

- A review app is created, which can be live tested.
- If everything is working OK, the PR can be merged to `master`.
- If the app is ready for production, it is promoted to [production](https://www.forumorg.org).

## Contributions

Contributions are very welcome! If you find a bug or some improvements, feel free to raise an issue and send a PR! Please see the [CONTRIBUTING](CONTRIBUTING.md) file for more information on how to contribute.

## Authors

* **Mehdi BAHA** - [mehdibaha](https://github.com/mehdibaha)
* **Juliette BRICOUT** - [jbricout](https://github.com/jbricout)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
