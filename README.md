# DuckAndCover Introduction

**sa.duckandcover** is a Titanium Studio plugin that can be used to auto generate Alloy project documentation with JSDuck.


## Prerequisites

JSDuck should be installed. Please see [https://github.com/senchalabs/jsduck](https://github.com/senchalabs/jsduck) for more details.


## Installation

copy the *sa.duckandcover* directory into the **plugins** directory of your Alloy project then enable it by adding the following to the tiapp.xml file.

before enabling sa.duckandcover

```
    <plugins>
        <plugin version="1.0">ti.alloy</plugin>
    </plugins>
```

after enabling the plugin

```
   <plugins>
        <plugin version="1.0">ti.alloy</plugin>
        <plugin version="1.0">sa.duckandcover</plugin>
    </plugins>
```

## Configuration


### Output directory

The default output directory specified in *sa.duckandcover* is the *docs* directory in the project root. This is defined in the plugin code here

```
//change this to specify where the docs will be generated
var doc_output_dir = './docs';
```

by changing the variable *doc_output_dir* you can modify where the documentation is generated.

### Configuration options

All files mention in the configuration section should be placed in the root directory of the project to be included in the documentation process.

As installed *sa.duckandcover* will generate default JSDuck documentation, but if other files are detected then the documentation can be enhanced.

#### Welcome Page
 
If the project has a **README.md** this will be added to the documentation as the welcome page (by default there is no welcome page).

#### Guides

If a **jsduck-guides.json** file exists then it will be picked up and used to add the defined guides to the documentation. See [https://github.com/senchalabs/jsduck/wiki/Guides](https://github.com/senchalabs/jsduck/wiki/Guides) for more details.

#### Categories

When a **jsduck-categories.json** file is detected it is used in the generation of the documentation. See [https://github.com/senchalabs/jsduck/wiki/Categories](https://github.com/senchalabs/jsduck/wiki/Categories) for more information on JSDuck categories.

## Credits

 - Ronald Treur on TiDev (http://www.tidev.io/2014/05/14/duckumentation/)
 - Fokke Zandbergen on TiDev (http://www.tidev.io/2014/06/18/documenting-a-new-widget/)
