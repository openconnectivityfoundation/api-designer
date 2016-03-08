# api-designer console for github hosted raml/json-schema files.

A graphical, web based tool from [MuleSoft] (https://www.mulesoft.com/platform/api/api-designer) that has been adapted to pull content directly from github and documents the APIs in a human friendly interactive console making it easy to engage fellow application developers.

API Designer is a standalone/embeddable editor for RAML (RESTful API Modeling Language) written in JavaScript using Angular.JS. By default, the editor uses an in-browser filesystem stored in HTML5 Localstorage. This version has been modified to pull content directly from github instead.

## Usage

The console has also been modified to take some parameters from the query string.
Currently supported keys are:
* 'gitRepo' : The path to the repo which is constructed as :owner/:repo. 
  * Example: OpenInterConnect/IoTDataModels
* 'gitPath' : the content path under which the content will be pulled recursively (usually empty).
  * Example: .
* 'gitRef' : The name of the commit/branch/tag. Default: the repository’s default branch (usually master).
  * Example: OIC-Release-1.0.0

## Resulting examples:
* [The 'OIC_API_1.0.0' tagged version of the OIC data model] (https://cdn.rawgit.com/openconnectivityfoundation/api-designer/master/raml-designer-4-git.html?gitRepo=OpenInterConnect/IoTDataModels&gitRef=OIC-Release-1.0.0).
```
https://rawgit.com/openconnectivityfoundation/api-designer/master/raml-designer-4-git.html?gitRepo=OpenInterConnect/IoTDataModels&gitRef=OIC_API_1.0.0
```
* [The 'api_core' branch version of the OIC core data model] (https://cdn.rawgit.com/openconnectivityfoundation/api-designer/master/raml-designer-4-git.html?gitRepo=OpenInterConnect/IoTDataModels).
```
https://rawgit.com/openconnectivityfoundation/api-designer/master/raml-designer-4-git.html?gitRepo=OpenInterConnect/IoTDataModels&gitRef=api_core
```
* Some [example raml] (https://cdn.rawgit.com/openconnectivityfoundation/api-designer/master/raml-designer-4-git.html?gitRepo=mulesoft/api-console&gitPath=dist/examples) files hosted under the 'mulesoft/api-console' repo at the 'dist/examples' path.
```
https://rawgit.com/openconnectivityfoundation/api-designer/master/raml-designer-4-git.html?gitRepo=mulesoft/api-console&gitPath=dist/examples
```
## License
[CPAL-1.0] (https://opensource.org/licenses/CPAL-1.0)

## Known limitation:
* Currently the tool only pulls content from github. Pushing back content would require OAuth implicit grant support for accessing the github api's requiring authorization. Implicit grant is not supported by Github at the time of writing.
