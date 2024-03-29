# Gitignore CL Editor

This is a simple bash script that allows you to edit a `.gitignore` file right from your terminal. It saves you from having to locate the file, open it up and edit it yourself. Granted, that isn't the most difficult thing to do but this is a nice script to have nonetheless!

## Installation
In order to install the script, first clone this repository. In your terminal or bash shell, type:

`$ cd directory/to/clone/to`

`$ git clone https://github.com/aliu2/gitignore_editor.git`

Now, change directory into this project and move the script to your local bin directory. This adds the script to your PATH variable so that it can be executed from anywhere. Type the following commands into your terminal or bash shell:

`$ cd gitignore_editor`

`$ mv gitignore /usr/local/bin/`

Finally, change directories to this local bin directory and make the script executable by typing the following into your terminal or bash shell:

`$ cd /usr/local/bin`

`$ chmod +x gitignore`

You can now execute the script from anywhere you like!

## Usage

`gitignore -mode -- location/of/.gitignore "line/to/add"`

The script can be invoked with the `gitignore` command once added to your local bin directory. It has two modes, add and delete and it takes two parameters, the location of the .gitignore file you wish to edit and the line you wish to add or delete.

Modes:
  - `-add` - Add a line to the specified .gitignore file
  - `-del` - Delete a line from the specified .gitignore file

Parameters:
  - `path/to/.gitignore` - The path to the .gitignore file you wish to edit
  - `"line/you/wish/to/add"` - The string you wish to add

**Example usage**

_When at the root level of your git project:_

`$ gitignore -add -- .gitignore "*/__pycache__"`

_When deeper in the project:_

`$ gitignore -del -- ../../.gitignore "*.log"`

_When in some other directory:_

`$ gitignore -add -- location/of/git/proj/.gitignore "logs/"`
