# Jsons.ahk-for-AHKv2

### forked from https://github.com/TheArkive/JXON_ahk2

The lazy man's json. Inspired by python's Jsons found on pypi. It takes objects, and converts to maps. 

For a detailed read me, visit the creators page:

https://github.com/TheArkive/JXON_ahk2/edit/master/README.md

# Use

Serialize 
```autohotkey
var := Jsons.Dump(obj, indent:=0)
```

Convert to map (and in the future, I'll look to try to convert to objects)
```autohotkey
obj := jxon_load(&text)
```
