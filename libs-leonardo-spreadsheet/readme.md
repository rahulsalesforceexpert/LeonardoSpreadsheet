# Leonardo Spreadsheet

Leonardo Spreadsheet is a javascript library that provides an advanced HTML5 based spreadsheet interface. It is an advanced content-type which can be used in eBooks, training and assessments.

## Getting setup

##### Dependencies: ``jQuery v3.1.1``
Please include the dependencies in your application where you intend to use Leonardo Spreadsheet

### 1. Using NPM
The Leonardo Spreadsheet library can be downloaded with npm using the npm install command. You would need to add the following dependency to your “package.json” to ensure the install command works. 

>“libs-leonardo-spreadsheet" library is available in the Leonardo private npm repository. To access this repository, user need to execute following commands
> 1. npm config set registry http://npm.leonardodls.com
> 2. npm set //npm.leonardodls.com/:_authToken=< token >


Use package.json file to specify library dependencies

```
"dependencies": {
      "libs-leonardo-spreadsheet":"<version>"
}
```

>Where:
>
>version: represents the version of the released leonardo spreadsheet library.

##### Run the install command
```
npm install
```

##### Import JS present at this location:
```
import { LeonardoSpreadsheet } from "libs-leonardo-spreadsheet";
```
```
<rootnode>/node_modules/libs-leonardo-spreadsheet/dist/ribbon-bundle-msOfficeRibbon.js
```

##### Import CSS present at this location:
 ```
 <rootnode>/node_modules/libs-leonardo-spreadsheet/dist/leonardoSpreadsheet.min.css
 ```
```
<rootnode>/node_modules/libs-leonardo-spreadsheet/dist/ribbon-bundle.css
```

##### Copy assets present at this location:
```
<rootnode>/node_modules/libs-leonardo-spreadsheet/dist/assets
```

Leonardo Spreadsheet needs the assets present at above mentioned location in order to render it's UI. User needs to paste these assets in their application parallel to the location where they have imported ```leonardoSpreadsheet.min.css``` file

## How to use


### Initialization

In order to use spreadsheet widgets in the application, the first step is to create the instance of “LeonardoSpreadsheet”.

```
var leonardoSpreadsheet = new LeonardoSpreadsheet(uid, container, {config, events, uiStyle});
```

>where,
>
>uid - A unique identifier for the widget.
>
>container - Container in the webpage where the widget is to be hosted.
>
>config - It contains preferences and data to render the leonardo widget. Discussed in detail below.
>
>events - Events to be attached with the leonardo widget.
>
>uiStyle - UI styles to be applied on widget. Discussed in detail below.

##### Sample configuration to render the leonardo widget is available here:

<http://jsoneditoronline.org/?id=03ce70c630ae45ac9e7142caa908ed92>

### Create the Spreadsheet
Once you have the instance of leonardoSpreadsheet, it can now be used to create the spreadsheet using the init method.

```leonardoSpreadsheet.init()```