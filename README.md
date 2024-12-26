- 👋 Hi, I’m @jojo5882
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
jojo5882/jojo5882 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
{
    "name": "ZUOYA  GMK26",
    "vendorId": "0x28E9",
    "productId": "0x3014",
    "matrix": {"rows": 6, "cols": 6},
    
    "layouts":{
      
      "keymap":[
            ["0,0\n\n\n0,0\n\n\n\n\n\ne0",{"x":0.5},"0,2","0,3","0,4\n\n\n1,0","1,5\n\n\n1,0",
            "0,1\n\n\n0,1",{"w":2},"0,5\n\n\n1,1"],
            ["1,0",{"x":0.5},"1,1","1,2","1,3","1,4"],
            ["2,0",{"x":0.5},"2,1","2,2","2,3",{"h":2},"2,4"],
            ["3,0",{"x":0.5},"3,1","3,2","3,3"],
            ["4,0",{"x":0.5},"4,1","4,2","4,3",{"h":2},"5,3"],
            ["5,0",{"x":0.5},{"w":2},"5,1","5,2"]
        ],
        "labels": [   
        "Encoder",
        "Split Backspace"
      ]
    },
  
    "keycodes": ["qmk_lighting"],
    "customKeycodes": [
      {"name": "2.4G", "title": "2.4G Host", "shortName": "2.4G"},
      {"name": "Bluetooth Host 1","title": "Bluetooth Host 1", "shortName": "BLE1"},
      {"name": "Bluetooth Host 2","title": "Bluetooth Host 2", "shortName": "BLE2"},
      {"name": "Bluetooth Host 3","title": "Bluetooth Host 3", "shortName": "BLE3"},
      {"name": "Reset","title": "Mcu Reset", "shortName": "Reset"},
      {"name": "Battery Level", "title": "Battery Level", "shortName": "Batt"}
      ],
    "menus": [
    {
      "label": "Lighting",
      "content": [
        {
          "label": "Backlight",
          "content": [
            {
              "label": "Brightness",
              "type": "range",
              "options": [0, 255],
              "content": ["id_qmk_rgb_matrix_brightness", 3, 1]
            },
            {
              "label": "Effect",
              "type": "dropdown",
              "content": ["id_qmk_rgb_matrix_effect", 3, 2],
              "options": [
                "\u5168\u7184All Off",
                "\u5355\u8272Solid Color",
                "\u4e0a\u4e0b\u6e10\u53d8Gradient Up/Down",
                "\u5de6\u53f3\u6e10\u53d8Gradient Left/Right",
                "\u547c\u5438Breathing",
                "\u9971\u548c\u5ea6\u6761Band Sat.",
                "\u4eae\u5ea6\u6761Band Val.",
                "\u9971\u548c\u5ea6\u98ce\u8f66Pinwheel Sat.",
                "\u4eae\u5ea6\u6761\u98ce\u8f66Pinwheel Val.",
                "\u9971\u548c\u5ea6\u87ba\u65cbSpiral Sat.",
                "\u4eae\u5ea6\u6761\u87ba\u65cbSpiral Val.",
                "\u5168\u5faa\u73afCycle All",
                "\u5de6\u53f3\u5faa\u73afCycle Left/Right",
                "\u4e0a\u4e0b\u5faa\u73afCycle Up/Down",
                "\u5185\u5916\u5faa\u73afCycle Out/In",
                "\u5185\u5916\u53cc\u5faa\u73afCycle Out/In Dual",
                "\u5f69\u8679Rainbow Moving Chevron",
                "\u5faa\u73af\u98ce\u8f66Cycle Pinwheel",
                "\u5faa\u73af\u87ba\u65cbCycle Spiral",
                "\u53cc\u706f\u5854Dual Beacon",
                "\u5f69\u8679\u706f\u5854Rainbow Beacon",
                "\u5f69\u8679\u98ce\u8f66Rainbow Pinwheels",
                "\u9971\u548c\u5ea6\u547c\u5438Hue Breathing",
                "\u9971\u548c\u5ea6\u706f\u6446Hue Pendulum",
                "\u9971\u548c\u5ea6\u6ce2\u6d6aHue Wave",
                "\u70ed\u5ea6Typing Heatmap",
                "\u6570\u5b57\u96e8Digital Rain",
                "\u7b80\u5355\u6309\u952eSolid Reactive Simple",
                "\u6309\u952eSolid Reactive",
                "\u6309\u952e-\u5bbdSolid Reactive Wide",
                "\u6309\u952e-\u591a\u5bbdSolid Reactive Multi Wide",
                "\u6309\u952e-\u5341\u5b57Solid Reactive Cross",
                "\u6309\u952e-\u591a\u5341\u5b57Solid Reactive Multi Cross",
                "\u6309\u952e-\u8054\u7ed3Solid Reactive Nexus",
                "\u6309\u952e-\u591a\u8054\u7ed3Solid Reactive Multi Nexus",
                "\u98de\u6e85Spash",
                "\u591a\u98de\u6e85Multi Splash",
                "\u5355\u8272\u98de\u6e85Solid Splash",
                "\u5355\u8272\u591a\u98de\u6e85Solid Multi Splash"
              ]
            },
            {
              "showIf": "{id_qmk_rgb_matrix_effect} != 0",
              "label": "Effect Speed",
              "type": "range",
              "options": [0, 255],
              "content": ["id_qmk_rgb_matrix_effect_speed", 3, 3]
            },
            {
              "showIf": "{id_qmk_rgb_matrix_effect} != 0 && {id_qmk_rgb_matrix_effect} != 24 && {id_qmk_rgb_matrix_effect} != 28 && {id_qmk_rgb_matrix_effect} != 29 && {id_qmk_rgb_matrix_effect} != 32",
              "label": "Color",
              "type": "color",
              "content": ["id_qmk_rgb_matrix_color", 3, 4]
            }
          ]
        }
      ]
    }
  ]
}
  

  
