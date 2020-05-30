# e5x-json
Automatically download and generate all needed files for working with [RIT-E5X](http://e5xvalidator.jrc.ec.europa.eu) reporting file format in a json  and python context.

The xsd-json bridge generation is powered by [jsonix](https://github.com/highsource/jsonix)

See [ECCAIRS site](https://eccairsportal.jrc.ec.europa.eu) and [RIT-E5X Website](https://e5xvalidator.jrc.ec.europa.eu) for more information.
## Installation

Install the package from github
```
pip install git+https://github.com/einarhuseby/e5x-json.git
```

Install required node packages
```
npm install jsonix circular-json --save
```

## Usage
```
$ python rit.py -h
usage: rit.py [-h] -v RIT_VERSION [-b BINDINGS] [-s SPECIAL_ATTR_XSD]
              [-u API_URL] [-k API_KEY] [-d] [-m] [-r] [-f]
              [-o OUTPUT_DIRECTORY]

E5X-JSON: Download, parse, generate and update the E5X-Json bridge for valid
versions of the RIT-XSD Schema File found at:
https://e5xvalidator.jrc.ec.europa.eu/E5Xwebsite/Documentation.aspx

optional arguments:
  -h, --help            show this help message and exit
  -v RIT_VERSION, --rit-version RIT_VERSION
                        Valid E5X RIT version number, ex. '4.1.0.6'
  -b BINDINGS, --bindings BINDINGS
                        Specify bindings file for generation, defaults to
                        './assets/bindings.xjb'
  -s SPECIAL_ATTR_XSD, --special-attr-xsd SPECIAL_ATTR_XSD
                        Specify bindings file for generation, defaults to
                        './assets/special_attributes.xsd'
  -u API_URL, --api-url API_URL
                        Specify the api url
  -k API_KEY, --api-key API_KEY
                        A valid api key/token
  -d, --api-delete      Delete all api entries for this version
  -m, --mongodb         Store directly in mongodb using pymongo
  -r, --mongodb-remove  Remove collections before insert
  -f, --force           Force download and generation overwriting existing
                        files
  -o OUTPUT_DIRECTORY, --output-directory OUTPUT_DIRECTORY
                        Output directory, default './'

Einar Huseby (c) 2019-2020 | https://github.com/einarhuseby/e5x-json
```


