# virgo - Create Golang virtual environments

## Overview

Very simple command line tool, inspired by Python's [virtualenv](https://pypi.python.org/pypi/virtualenv).

## Install

Copy the two included in the distribution files, _virgo_ and _goactivate_ to some directory and fix the __VIDIR__ line inside _virgo_:

    VIDIR="${HOME}/bin"

## Usage

Create new virtual environment with

    $ virgo ./new_proj

This will create the basic structure for a Go language project:

    bin/   # command line tools
    pkg/   # compiled binaries 
    src/   # sources    
    
Go to the new directory and activate the virtual environment:

    $ cd ./new_proj && source ./bin/activate
    
Activation will change the __GOPATH__ to the current directory and also include the project _bin/_ in the __PATH__:

    GOPATH=/path/to/your/project
    PATH=$GOPATH/bin:$PATH

When you finish working with the virtual environment, you can go back to your default Go language settings with:

    $ deactivate
    
This will restore the old __GOPATH__ and __PATH__ .
    
## Author

* [Stoyan Zhekov](https://github.com/zh)


## License

[MIT License](http://opensource.org/licenses/MIT)

## More

* Code: <https://github.com/zh/virgo>