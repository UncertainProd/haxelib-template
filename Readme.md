# Haxelib template
#### A template you can follow when making your own haxelibs

## Usage
You can create your own version of this template for your haxelib, on Github by clicking the `Use this template` button at this top of this repo, then clicking `Create a new repository`.

This template contains the following files, here's what to do with them:
- `haxelib.json` : This is the main file that contains some metadata about your haxelib and must be present at the root of your haxelib's folder when making a haxelib. It contains the following fields:
    - name : The name of your haxelib. It must be at least 3 characters long and must only use the following symbols: [A-Za-z0-9_-.]
    - url : A URL to where more information about the library can be found (usually the github repo link)
    - license : The open source license under which the library is released. Can be one of: `GPL`, `LGPL`, `BSD`, `Public` (for Public Domain), `MIT`, or `Apache`.
    - tags : A list of tags describing your haxelib
    - description : A short description of the haxelib
    - version : The current version of the haxelib. Must follow Semantic Versioning.
    - classPath : (Optional) The path to where your source files are located. If your source files are in a folder with the same name as your haxelib, then this field can be removed.
    - releasenote : A release note of the current release of your library.
    - contributors : A list of usernames, which identify the contributors to the library. The first name in this list is considered the owner of this haxelib.
    - dependencies : (Optional) A JSON object describing the dependencies of your library.
    - main : (Optional) The class whose `main` method will be executed if the commmand `haxelib run <your-haxelib-name>` is run.

    Check out [Creating a haxelib](https://lib.haxe.org/documentation/creating-a-haxelib-package/) at [lib.haxe.org](https://lib.haxe.org/) for more info.

- `extraParams.hxml` : If your library needs its own compiler flags that have to be included when a project uses your haxelib, then those must be specified here.

- `LICENSE-*` : Just choose the license most appropriate for your haxelib, rename that file to just `LICENSE` and then delete the other license files. The link to obtain licenses for public domain and creative commons are in [public-domain.txt](./public-domain.txt)

- `Readme.md` : A Readme file, which serves as a basic overview of your haxelib, what it does and how to use it. (basically this file you're reading right now. Replace it's contents with your haxelib's readme)

- `libname/` : Rename this folder to the name of your haxelib (or to the `classPath` attribute in your haxelib.json file, if you've provided one). And put your `.hx` files in there

- `.gitignore` : A file containing the names of any files or folders that need to be ignored when making pushing your commits to git and github. [docs](https://git-scm.com/docs/gitignore)

- `include.xml` (optional) : This file can specify additional XML entries that must be added onto the `Project.xml` file of any application that uses your library in say, a `lime` project. It follows the same format as the [Project.xml format](https://github.com/openfl/lime.openfl.org/blob/master/_docs/project-files/xml-format.md)