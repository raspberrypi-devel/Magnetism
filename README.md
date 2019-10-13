# Magnetism
test theory of magnetism

Here's how it works: A magnetic field pulls and pushes electrons in certain objects closer to them, making them move. 
Metals like copper have electrons that are easily moved from their orbits. 
If you move a magnet quickly through a coil of copper wire, the electrons will move - this produces electricity.

simple  description of how  magnets  work:
In magnets the molecules are uniquely arranged so that their electrons spin in the same direction. 
This arrangement of atoms creates two poles in a magnet, a North-seeking pole and a South-seeking pole. 
The magnetic force in a magnet flows from the North pole to the South pole.

check this link:https://sciencing.com/things-do-rare-earth-magnets-6065303.html

electrons = move the  create the  electricity
cell    =  cells  hold the   electrons   they move  from  negative to positive
voltage =  measurement = VOLTS

_________________________________________________________________________________________________________________________________________

plan is  to move  objects  with magnetism:

setup.py_tmpl is a template (it ends with the _tmpl suffix) that will be used to create a setup.py file:

#!/usr/bin/env python

from distutils.core import setup


PROJECT = {module_name!r}
VERSION = '0.1'
AUTHOR = {author!r}
AUTHOR_EMAIL = {author_email!r}
DESC = "A short description..."

setup(
    name=PROJECT,
    version=VERSION,
    description=DESC,
    long_description=open('README.rst').read(),
    author=AUTHOR,
    author_email=AUTHOR_EMAIL,
    py_module=[{module_name!r},],
)
By default, Skeleton uses python 2.6+ string formatting.

basic-module/{module_name}.py
{module_name}.py is the module file for which the name will be set dynamically at run time.

Note

All file names are formatted using Skeleton.template_formatter method. Watch out for special characters (with the default formatter, use {{ to render { and }} for } - unless you want to render a variable).

Extra
skeleton includes a skeleton for a basic package layout, you can run it with:

python -m skeleton.examples.basicpackage <dst_dir>
or with virtualenvwrapper.project. Install it:

pip install skeleton[virtualenv-templates]
Configure virtualenvwrapper and virtualenwrapper.project; then, create a new project:

mkproject -t package <project name>
Todo:
add more examples.
Development
Report any issues and fork squeleton at http://github.com/dinoboff/skeleton/ .

History
0.6 (Mai 12, 2010)
Add skeleton.insert_into_file().
Add skeleton.Bool.
Rename Skeleton.skel_dir to Skeleton.real_dir.
Rename Skelton.vars to Skeleton.variables.
Rename Skeleton.check_vars to Skeleton.check_variables.
Skeleton constructor can take any mapping object not just Skeleton.
Add Var.valiadte(response) to validate user imput.
Rename Var.prompt() to Var.do_prompt(). Var.prompt is now a property returning the message to prompt.
0.7 will be the last minor release before version 1.0. Any backward incompatible changes between versions 0.6 and 1.0 will be marked by warnings in 0.7.

0.5.1 (Mai 11, 2010)
Fix syntax error in the package virtualenvwrapper.project extension.
0.5 (Mai 10, 2010)
Drop Python 2.5 support (might get basic support back).
Various internal changes prior to 1.0 release.
Improve error related to unexpected variable names in templates and file names
0.4 (Mai 8, 2010)
Convert Var names to lower_case_with_underscores.
improve Var name display in command
improve long string option for Vars in command line.
fix bug in setup.py_tmpl of the mkmodule.py example.
0.3 (Mai 6, 2010)
New class method, Skeleton.cmd to create the logger and optparser.
Skeleton.run doesn’t set the logger and optparser anymore.
Skeleton.write raises a KeyError exception if a key is missing instead of prompting the user.
Removed the pre_run, post_write and pre_write methods. Overwrite the write and run instead.
Added configure_parser() to configure the parser set by Skeleton.cmd.
Add required_skeleton attribute to Skeleton. These skeleton will be run before the main. They all share the same entries.
Added verbose options to the Skeleton optparser.
Added a basic package template extension for virtualenwrapper.project.
0.2.1 (Mai 2, 2010):
Fix bug with Var._prompt static method which was preventing the prompt for variable assignement.
0.2 (Mai 1, 2010):
Add python 3 support.
0.1 (April 31, 2010):
first release.
