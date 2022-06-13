# The `settingslisted` DaNIS3H Capsule Directive
The `settingslisted` DaNIS³H Capsule indicates which capsule settings should be documented in the `class` and `capsulename` attributes of the HTML Element containing the rendered DaNIS3H capsule.

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

## Examples of outputs from settingslisted Directive

### All Settings:

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
}
```

### Output:
`<danis3h-capsule class="ash-toggle-input•position▸off○class▵test-class-1▵test-class-2○test-attribute-1♢test-value-1○test-attribute-2♢test-attribute-2○test-attribute-3♢○test-attribute-4○data-test-data-1♢test-value-1○data-test-data-2♢data-test-data-2○data-test-data-3♢○data-test-data-4●pagecontext♦pagefix●settingslisted♦strongmodifiers|classes|attributes|dataset|directives|lightmodifiers◦theme▹light test-class-1 test-class-2" capsulename="Ash_Toggle_Input::Position:Off++class:test-class-1:test-class-2++test-attribute-1:test-value-1++test-attribute-2:test-attribute-2++test-attribute-3:++test-attribute-4++data-test-data-1:test-value-1++data-test-data-2:data-test-data-2++data-test-data-3:++data-test-data-4&&pagecontext:pagefix&&settingslisted:StrongModifiers..Classes..Attributes..DataSet..Directives..LightModifiers#theme:light" capsulepublisher="Ash" test-attribute-1="test-value-1" test-attribute-2="test-attribute-2" test-attribute-3="" test-attribute-4 data-test-data-1="test-value-1" data-test-data-2="data-test-data-2" data-test-data-3="" data-test-data-4 ﹠pagecontext="pagefix" ﹠settingslisted="StrongModifiers Classes Attributes DataSet Directives LightModifiers" °theme="light">`


### Selected Settings:

```json
"Directives": {

  "settingslisted": [

    "Classes",
    "DataSet",
    "LightModifiers"
  ]
}
```

### Output:
`<danis3h-capsule class="ash-toggle-input○class▵test-class-1▵test-class-2○data-test-data-1♢test-value-1○data-test-data-2♢data-test-data-2○data-test-data-3♢○data-test-data-4◦theme▹light test-class-1 test-class-2" capsulename="Ash_Toggle_Input++class:test-class-1:test-class-2++data-test-data-1:test-value-1++data-test-data-2:data-test-data-2++data-test-data-3:++data-test-data-4#theme:light" capsulepublisher="Ash" test-attribute-1="test-value-1" test-attribute-2="test-attribute-2" test-attribute-3="" test-attribute-4 data-test-data-1="test-value-1" data-test-data-2="data-test-data-2" data-test-data-3="" data-test-data-4 ﹠pagecontext="pagefix" ﹠settingslisted="Classes DataSet LightModifiers" °theme="light">`

### Default Settings:
When the `settingslisted` Directive is not explicitly declared or is declared as an empty array, the value defaults to:

```json
"Directives": {

  "settingslisted": [

    "StrongModifiers"
  ]
}
```

### Output:
`<danis3h-capsule class="ash-toggle-input•position▸off test-class-1 test-class-2" capsulename="Ash_Toggle_Input::Position:Off" capsulepublisher="Ash" test-attribute-1="test-value-1" test-attribute-2="test-attribute-2" test-attribute-3="" test-attribute-4 data-test-data-1="test-value-1" data-test-data-2="data-test-data-2" data-test-data-3="" data-test-data-4 ﹠pagecontext="pagefix" °theme="light">`

### A Capsule with one StrongModifier and one LightModifier
The examples above reference a capsule with lots of settings: `StrongModifiers`, `classes`, `attributes`, `dataset`, `Directives` and `LightModifiers`.

It's generally unlikely that a DaNIS³H Capsule will include more than two types of setting, never mind all of them.

Here's a more realistic example capsule with one `StrongModifier` and one `LightModifier` and no classes, no attributes, no dataset and no `Directives`:

```json
"Directives": {

  "settingslisted": [

    "StrongModifiers"
  ]
}
```

### Output:
`json
<danis3h-capsule class="ash-toggle-input•position▸off" capsulename="Ash_Toggle_Input::Position:Off" capsulepublisher="Ash" °theme="light">
`
