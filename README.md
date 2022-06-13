# The `settingslisted` DaNIS3H Capsule Directive
The `settingslisted` DaNIS³H Capsule indicates which capsule settings should be documented in the class and capsulename attributes of the HTML Element containing the rendered DaNIS3H capsule.

## Reference example: an HTML Element in a DaNIS³H Markup CodeSheet

```json
{
  "element": "div",

  "classList": [

    "test-class-1",

    "test-class-2"
  ],

  "attributes": {

    "test-attribute-1": "test-value-1",
    
    "test-attribute-2": "test-attribute-2",
    
    "test-attribute-3": "",

    "test-attribute-4": "⊤"
  },

  "dataSet": {

    "test-data-1": "test-value-1",
    
    "test-data-2": "data-test-data-2",
    
    "test-data-3": "",

    "test-data-4": "⊤"
  }
}
```

______

## For comparison: a nested DaNIS³H Capsule in a DaNIS³H Markup CodeSheet

```json
{
  "Capsule": true,

  "CapsulePublisher": "Ash",

  "CapsuleName": "Ash_Toggle_Input",

  "classList": [

    "test-class-1",

    "test-class-2"
  ],

  "attributes": {

    "test-attribute-1": "test-value-1",
    
    "test-attribute-2": "test-attribute-2",
    
    "test-attribute-3": "",

    "test-attribute-4": "⊤"
  },

  "dataSet": {

    "test-data-1": "test-value-1",
    
    "test-data-2": "data-test-data-2",
    
    "test-data-3": "",

    "test-data-4": "⊤"
  },

  "Directives": {

    "pagecontext": "pagefix",

    "settingslisted": [

      "StrongModifiers",
      "Classes",
      "Attributes",
      "DataSet",
      "Directives",
      "LightModifiers"
    ]
  },

  "StrongModifiers": {

    "Position": "Off"
  },

  "LightModifiers": {

    "theme": "light"
  }
}
```
_______
## settingslisted Directive

```json
"Directives": {

  "settingslisted": [

    "StrongModifiers",
    "Classes",
    "Attributes",
    "DataSet",
    "Directives",
    "LightModifiers"
  ]
},
```
