# vmf_deserialiser
Short program that turns VMF files into Python ```dict``` objects.

In order to use it in a Python program, move ```vmf_deserialiser.py``` to the folder of your program and include
```import vmf_deserialiser```
with the rest of your imports in the file. The sole function is ```deserialise_vmf()```, which takes a string that specifies the VMF file's path as an argument. It will return a dictionary representing the VMF that includes all of its structures (e.g ```world{}```) as dictionaries and substructures (e.g ```solid{}```) as nested dictionaries within those dictionaries representing structures.

Duplicated names are handled by inserting a "&n" extension on the end of the structure's name where "n" is the number of duplicate structures (beginning with n = 1 or n = 0 if ```settings["tagFirstInstance"]``` is set to ```True```). **_The first occurrence of a structure will have no name extension if ```settings["tagFirstInstance"]``` is set to ```False```._**
