
Almarai Open-Source Font

See: 
     /source/1-drawings/Almarai-Bold.ufo
     /source/1-drawings/Almarai-Extrabold.ufo
     /source/1-drawings/Almarai-Light.ufo
     /source/1-drawings/Almarai-Regular.ufo

URW Beziér Format is used as source and production file format. 
The production is done with URW program IKED and OTM.
See: 
     /source/2-production/Almarai-Bold/Almarai-Bold.be
     /source/2-production/Almarai-Extrabold/Almarai-Extrabold.be
     /source/2-production/Almarai-Light/Almarai-Light.be
     /source/2-production/Almarai-Regular/Almarai-Regular.be


For each of the four font weights the production of TTF and OTF is done with IKED 
and OTM using four additional ASCII-files as input:

arab.cha          (containing a glyph list of IKED used numbers and according UNICODES 
                  and PS names for the conversion from URW Beziér to OTF or TrueType)
loadfeature.fea   (containing the GSUB feature information and loading GPOS and name table files)
??gpos.fea        (containing GPOS feature information)
name.fea          (containing name feature information)
Almarai-Bold.ufm  (URW font metric file, which contains all necessary name 
                   and other table entry information for the final font production)


Production:

In each font directory the five ASCII files (see above) and the Bezièr file must 
be present.

1. Start program IKED and select "File/Open" and open the Bezièr file
2. Select "File/Make OpenType Font"
3. Select "Import" the layout file "arab.cha"
4. Select "More" to get the UFM Dialog
5. In the fourth entry "Export Options" select the field "TrueType raster size"
   and insert the value "1000" instead of the default value "2048"
6. Select "OK"
7. Select "Target font file"
6. Select "Make"


After production of the Basic Type format use program OTM 
to add the necessary feature files, by importing "loadfeature.fea".











