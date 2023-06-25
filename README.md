# Jsons.ahk-for-AHKv2
The lazy man's json. Inspired by: https://pypi.org/project/jsons/

Forked from TheArkive https://github.com/TheArkive/JXON_ahk2

This is a normal Json library, with a built in function to convert Objects to Maps. Feed anything into Dump, and it should return a proper serialized string. 

# Use

Serialize 
```autohotkey
var := Jsons.Dump(obj, indent:=0)
```

Convert to obj
```autohotkey
obj := Jsons.Load(&text)
```

In the future, I'll look to try to convert to objects a la https://github.com/Jim-VxE/AHK-Lib-JSON_ToObj

test input:
```autohotkey
class Test
{
    __New(){
        this.valA := "valA"
        this.valB := "valB"
    }
}
ClassObj := Test()
ObjB := {1:2}
MapA := Map("test", {ObjB:"x"})
x := {
    ClassObjects: [ClassObj,ClassObj],
    1: 2,
    4: [1, ClassObj],
    z: Map(1,2),
    ObjB:ObjB,
    y:MapA
}
jdata := Jsons.Dump(x, indent:=2)
```

output:

```json
{
  "1": 2,
  "4": [
    1,
    {
      "valA": "valA",
      "valB": "valB"
    }
  ],
  "ClassObjects": [
    {
      "valA": "valA",
      "valB": "valB"
    },
    {
      "valA": "valA",
      "valB": "valB"
    }
  ],
  "ObjB": {
    "1": 2
  },
  "y": {
    "test": {
      "ObjB": "x"
    }
  },
  "z": {
    "1": 2
  }
}
```
