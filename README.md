# Jsons.ahk-for-AHKv2

### Forked from https://github.com/TheArkive/JXON_ahk2

The lazy man's json. Inspired by: https://pypi.org/project/jsons/

This is a normal Json library, with a built in function to convert Objects to Maps. Feed anything into Dump, and it should return a proper serialized string. 

For a detailed read me, visit the creators page:

https://github.com/TheArkive/JXON_ahk2/edit/master/README.md

# Use

Serialize 
```autohotkey
var := Jsons.Dump(obj, indent:=0)
```

Convert to map 
```autohotkey
obj := Jsons.Load(&text)
```

In the future, I'll look to try to convert to objects a la https://github.com/Jim-VxE/AHK-Lib-JSON_ToObj
