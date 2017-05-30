# Breaking the Monolith by using hapi 
## Background
Let me get the disclaimer out of the way: I am not an expert on Hapi
I started looking into Hapi's ability to break components out.
This is my attempt to follow other tutorials from a hello world to a true component system.
I have broken this down into the following steps

| Project  | Description | Link |
|---|---|---|
|hapi-tut-monolith-01|A simple hello world hapi project| [01](https://github.com/quapaw/hapi-tut-monolith-01)|
|hapi-tut-monolith-02a|Add services - customers and products| [02A](https://github.com/quapaw/hapi-tut-monolith-02a)|
|hapi-tut-monolith-02b|Adding Glue and externalizing config| [02B](https://github.com/quapaw/hapi-tut-monolith-02b)|
|hapi-tut-monolith-02c|Moving services into their own folders| [02C](https://github.com/quapaw/hapi-tut-monolith-02c)|
|hapi-tut-monolith-03-main|Moved service into own project. Instructions here| [03-main](https://github.com/quapaw/hapi-tut-monolith-03-main)|
|hapi-tut-monolith-03-customer|Just the customer service| [03-customers](https://github.com/quapaw/hapi-tut-monolith-03-customers)|
|hapi-tut-monolith-03-products|Just the produce service| [03-products](https://github.com/quapaw/hapi-tut-monolith-03-products)|
|hapi-tut-monolith-04a-customer|Movement of some files| [04a-customers](https://github.com/quapaw/hapi-tut-monolith-04a-customers)|
|hapi-tut-monolith-04b-customer|New methods| [04b-customers](https://github.com/quapaw/hapi-tut-monolith-04b-customers)|
|hapi-tut-monolith-04c-customer|Validation and Error Handling|[04c-customers](https://github.com/quapaw/hapi-tut-monolith-04c-customers)|
|hapi-tut-monolith-04d-customer|Unit Testing|[04d-customers](https://github.com/quapaw/hapi-tut-monolith-04d-customers)|
|hapi-tut-monolith-04e-customer|Add Mongo and API Docu|[04e-customers](https://github.com/quapaw/hapi-tut-monolith-04e-customers)|
|hapi-tut-monolith-05-customer|Combine work with products for full deployment|[05-customers](https://github.com/quapaw/hapi-tut-monolith-05-customers)|
|hapi-tut-monolith-05-product|Combine work with products for full deployment|[05-products](https://github.com/quapaw/hapi-tut-monolith-05-product)|
|hapi-tut-monolith-05-main|Combine work with products for full deployment|[05-main](https://github.com/quapaw/hapi-tut-monolith-05-main)|
|**hapi-tut-monolith-06-customer**|**Move from npm to yarn**|**[06-customers](https://github.com/quapaw/hapi-tut-monolith-06-customers)**|
|hapi-tut-monolith-07-customer|Customer project to go with 07-main|[07-customers](https://github.com/quapaw/hapi-tut-monolith-07-customers)|
|hapi-tut-monolith-07-product|Product project to go with 07-main|[07-products](https://github.com/quapaw/hapi-tut-monolith-07-products)|
|hapi-tut-monolith-07a-main|Catch up with 06 changes|[07a-main](https://github.com/quapaw/hapi-tut-monolith-07a-main)|
|hapi-tut-monolith-07b-main|Change in configuration|[07b-main](https://github.com/quapaw/hapi-tut-monolith-07b-main)|




#HAPI Tutorial - Monolith - 6 - customer
This step moves from using npm as the build tool to yarn.
I am moving away from using npm because it does not lock the dependencies.
So a build two days apart could get different set of dependencies.

* Installing yarn
    * to install you can run the following command ```npm install yarn -g```
        You can also find detail on installs here (https://blog.risingstack.com/yarn-vs-npm-node-js-package-managers/)
* Use yarn
    Use yarn in the same way you use npm.  Just replace npm with the work yarn.
    * So the initial build of a project would be ```yarn install```
        This will create the following output
        ```
        yarn install v0.24.4
        info No lockfile found.
        warning customers@1.0.0: No license field
        [1/4] Resolving packages...
        [2/4] Fetching packages...
        [3/4] Linking dependencies...
        [4/4] Building fresh packages...
        success Saved lockfile.
        ✨  Done in 7.00s.
        ```
    A good article on yarn is (https://yarnpkg.com/lang/en/docs/migrating-from-npm/)
    