# Jsonipy
class for serializing objects into Json

### Usage

first create a simple class that inherits jsonipy, add meta class with two fields
  - model - your class name
  - fields- fields to be included in json file , use __ all__ for including every field
 
```py
 from serializers import jsonipy
 
 class MyClassSerializer(jsonipy):
    
    class Meta:
        model = Pokemon
        fields = ['name','strength']
        
```
then create an object and get your data in json, as simple as  1,2,3

```py
    charizard = Pokemon(name = 'Charizard', strength = '1500', .....)
    serialized_charizard = MyClassSerializer(charizard)
    print ( serialized_charizard.data )
    
    # {"strength": "1500" , "name":"Charizard" }
```
