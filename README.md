Unity WII nuspacker template
===========================

use these files and overwrite them over your existing precompiled Unity project.

How to compile Unity project with Wii U license
================================================

Make sure to have the official SDK, MULTI and the related license files for it.
Also snag Unity 2017.1.2p3 as well as the support files for WiiU.

Project Export settings options

- Build Debug Level = Master [not network]
- Build output = Download Image
- Boot mode = NAND

Then grab the files in the "SD" folder and decrypt them with CDecrypt.

Put the code, meta, content files in another folder "inputDir" (in NUSPacker's directory).

Then use my files to overwrite the two folders.

Then re-pack it with NUSPacker :
java -jar NUSPacker.jar -in "inputDir" -out "outputDir" -skipXMLParsing -encryptKeyWith "wii u commom key"

Feel free to change the header, name... later once you confirmed it installs properly on the console.
