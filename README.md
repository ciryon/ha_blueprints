# blueprints
Some Home Assistant blueprints I have created

## Cabinet lights
This blueprint is used to control lights inside a cabinet. They turn on when the door sensor triggers and turn back off once the door is closed again. Of course it can be used in other similar situations. The general setup is described in [my blog here](https://thesmarthomejourney.com/2020/07/07/diy-smart-wardrobe-lights/).

## Motion brightness light
This blueprint extends the included motion sensor automation from Home Assistant by adding a brightness sensor. The lights will only turn on if the brightness is lower than a certain threshold you can provide or if it night (after sunset, before sunrise). That way you can avoid using hardcoded times to activate your lights. There is an in-depth explanation on my blog [here](https://thesmarthomejourney.com/2021/04/19/ultimate-smart-light-system/).

There is also a version two of this blueprint here which fixes one issue: sometimes after turning on the lights the brightness level will be high enough which will in turn make the automation turn off the lights again. To fix this annoying but I added a new condition that checks if any lights are already on. Unfortunately it is difficult to use a target selector in a condition so this is just a workaround that will most likely only work if you only select entities (no conditions or groups). A full explanation can be found on my [blog here](https://thesmarthomejourney.com/2022/02/20/target-selector-in-a-condition/).