# Multiquine structure

For any language of our multiquine, we will adopt the following structure

```
/** HEADERS section **/
All the code needed to start a program, and start declaring a map of integer lists

/** DATA section **/
Add an entry "CS" in the map with CS code as integer list (to be replaced)
Add an entry "JS" in the map with JS code as integer list (to be replaced)
Add an entry "BF" in the map with BF code as integer list (to be replaced)

/** CODE section **/
Read target language (by default : current language)
If it is CS : 
   print CS hearders section (to be replaced later)
   for each data map entry, add a map entry declaration in CS way
   print map[CS] values as chars
If it is JS : 
   print JS hearders section (to be replaced later)
   for each data map entry, add a map entry declaration in JS way
   print map[JS] values as chars
If it is BF : 
   print BF hearders section (to be replaced later)
   for each data map entry, add a map entry declaration in BF way
   print map[BF] values as chars

```

# Process

* First, write such program (with placeholders) for all our target languages
  * Headers parts are ready now
* Then, insert the (now written) headers section of all our target languages into all our program stubs
  * Code parts are ready now
* Finally, converts code parts into integer lists and insert into the data section
  * Multiquines are ready now
