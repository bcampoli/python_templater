How-To:
=====

first import:

`import templater`

to use the templater module simply do:

`templater.replace(input_file, properties_file)`

where `input_file` is the path to the file that needs replacements and `properties_file` is the path to the file storing the dictionary in yaml format.

What it Does:
=============

Python Templater replaces keys or tags surrounded by (( )) with their corresponding value which is found in .yaml file. There is no support for nested tags at this time.

Example:

let the following be a dictionary defined by a yaml file:

`my-credentials: foo`

`my-name: bar`

let the follwing be an input file:

`hello world!
I am a walrus!
My name is ((my-name)) and I love to tell everyone my password which is ((my-credentials))
`
then the output after running the replace function is:

`hello world!
I am a walrus!
My name is bar and I love to tell everyone my password which is foo`
