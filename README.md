# emr-vis-web 

![Screenshot](https://github.com/trivedigaurav/emr-vis-web/raw/master/screenshot.png)

emr-vis-web is the web port for the [emr-vis-nlp](https://github.com/trivedigaurav/emr-vis-nlp) project.

## Getting Started

To get started, install the pre-requisites and then clone emr-vis-web as described below:

### Prerequisites

1. You need git to clone the emr-vis-web repository. You can get it from
[http://git-scm.com/](http://git-scm.com/).

2. You must have node.js and its package manager (npm) installed. You can download them from [http://nodejs.org/](http://nodejs.org/) or get them using your favourite package manager. For example, if you are on a Mac and have homebrew installed, run `$ brew install node`.

3. We use the [Apache Tomcat](http://tomcat.apache.org/) server to deploy the app. On a Mac with homebrew you may use `$ brew install tomcat` to get it.

### Clone emr-vis-web

1. Navigate to the home directory of your tomcat server. You can use `$ catalina version` to check the value of  `CATALINA_HOME`.
2. `cd` to the _webapps/_ directory. If you are using the default tomcat setup, your present working directory would be something like _/usr/local/Cellar/tomcat/7.0.54/libexec/webapps/_.
3. Clone the emr-vis-web repository using [git][git]:

    ```
    git clone https://github.com/trivedigaurav/emr-vis-web.git
    cd emr-vis-web
    ```

### Install Dependencies

1. Make sure you have [node.js][node] installed.

    * We get the tools we depend upon via `npm`, the [node package manager][npm].
    * We get the angular code via `bower`, a [client-side code package manager][bower].

2. We have preconfigured `npm` to automatically run `bower` so we can simply do:

    ```
    npm install
    ```

3. (Skip this step to leave default settings as it is.) 
   In case you need to change the backend service's path, edit the `config.backend` variable in _package.json_ *or* or use the following commands:

    ```
    npm config set emr-vis-web:backend <relative/path/to/backend/service>
    npm start
    ```
    
    Valid examples of this path include _"http://localhost:9090/backEndService"_, _"/backEndService"_ etc.
    
    Editing package.json would be a permanent solution while using the `npm config` lets you include the config settings for the current terminal session.

### Run the Application

If you haven't built the backend project as yet, please do so now. Remember to go through step 3 to modify the default path to the backend service.

Now browse to the app at `http://localhost:8080/emr-vis-web/app/index.html` or `<your-localhost-root>/emr-vis-web/app`.


[git]: http://git-scm.com/
[bower]: http://bower.io
[npm]: https://www.npmjs.org/
[node]: http://nodejs.org
