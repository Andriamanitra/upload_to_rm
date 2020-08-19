# upload_to_rm
A simple script to upload stuff to reMarkable cloud

The script takes file names (png, jpg, tiff, pdf) as argument and uploads them to reMarkable cloud. The first time you run the script it will ask for a code (which can be found from [my reMarkable](https://my.remarkable.com/connect/remarkable)) to register with a reMarkable account. It will then store the bearer token in a configuration file (in the same folder as the script) so next time it can run fully autonomously allowing you to automate things.

I made this script mainly with [Greenshot](https://getgreenshot.org/)'s external command plugin in mind but you can use it on its own too.

## Usage

`python upload_to_rm.py image1.png [image2.jpg document1.pdf...]`

## Dependencies

See requirements.txt; basically [img2pdf](https://pypi.org/project/img2pdf/) and [requests](https://pypi.org/project/requests/) along with their own dependencies.

## Working example configuration for Greenshot

![this](https://i.imgur.com/rsGRaeX.png)

One caveat is that img2pdf throws an exception with Greenshot's .png screenshots because they have an alpha channel. Might look into it later, for now configuring Greenshot to use .jpg instead is a good workaround.

-----

If you find any issues (I'm sure there are many) please let me know and I might try to fix things. Or feel free to fix it yourself, you're free to use my code however you like.
