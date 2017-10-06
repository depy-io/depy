## Install docker

version: 17.09.0-ce-mac35 (19611)

## Install python 2.7

## configure your company settings:

1. cd <depy home>/conf

2. cp -R company <your company name>

3. cd <your company name>

4. Fill in the values in aaa.json file

## Spotinst settings

1. place in your home directory file named - '.spotinst'

2. store your Spotinst API Token in the file

## Running depy:

caffeinate docker run --rm -v /Users/liora/git/depy-backend/lift:/lift -v /Users/liora/.depy:/root/.depy -v /Users/liora/.spotinst:/root/.spotinst -v /Users/liora/.ssh:/root/.ssh -v /Users/liora/.aws:/root/.aws -v /Users/liora/.vault_pass.txt:/root/.vault_pass.txt depy python /lift/up.py;say done
