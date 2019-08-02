## Understanding the Codebase structure

This describes the app directory structure & conventions.

```
.                               # project root directory
├── node_modules                # project dependencies directory
│   ├── .bin                    # node_modules bin directory
│   ├── casperjs                # casperjs executable
│   ├── phantomjs               # phantomjs executable
│   └── ...                     # etc
├── bin                         # bin directory
│   ├── phantomjs               # local phantomjs executable
│   └── ...                     # etc
├── src                         # source files
│   ├── scripts                 # directory contains all casperjs scrapping scripts.
│   │   ├── sample-script.js    # sample casperjs script
│   │   └── ...                 # etc
│   ├── runner.js               # dynamic casperjs script runner
│   ├── utils.js                # utility functions inside here.
│   └── ...                     # etc
├── test                        # directory contains test files
│   ├── basic.js                # sample basic test
│   └── ...
├── .env                        # it is where you place your AWS deployment configuration
├── .gitignore                  # exclude files/etc to be tracked & pushed on git (i.e., local configuration, credentials, dependencies, etc.)
├── deploy.env                  # it has the same format as `.env`, but is used for holding any environment/config variables that you need to be deployed with your code to Lambda but you don't want in version control (e.g. DB connection info)
├── event.json                  # it is where you mock your event
├── index.js                    # app main entry point
├── package.json                # project details (i.e., version, author info, dependencies, etc.)
├── README.md                   # project documentation guide.
└── ...                         # etc
```
