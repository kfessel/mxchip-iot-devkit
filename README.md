
Links: this page is at https://kfessel.github.io/mxchip-iot-devkit/
its source is at https://github.com/kfessel/mxchip-iot-devkit/

# mxchip-iot-devkit
This Repo combines https://github.com/microsoft/devkit-sdk and build-tools released by Arduino

## This Repo might be moved away ##

## why ?

At the Time (22-10-07) this is created neither:

https://github.com/microsoft/devkit-sdk/blob/master/package_azureboard_index.json

(see: https://github.com/microsoft/devkit-sdk/issues/1089)

nor

https://github.com/VSChina/azureiotdevkit_tools/blob/master/package_azureboard_index.json

(see: https://github.com/VSChina/azureiotdevkit_tools/issues/60)


is working with Arduino IDE 2 or Arduino-cli

This fixes that and uses the toolchains provided by arduino

the `AZ3166-2.0.0-a.zip` is a slightly modified version of https://github.com/microsoft/devkit-sdk/releases/download/2.0.0/AZ3166-2.0.0.zip

The modifications (small changes) are done to make this work with the tools provided by Arduino

[small_changes.diff.txt](small_changes.diff.txt)

If either of the upstream sources is working for you please use them.

## why 2 ?

By using the tools provided by Arduino this can be used on platforms not supported by upstream like compiling on a Raspberry Pi

## usage

If you still want to use this:

Add https://kfessel.github.io/mxchip-iot-devkit/package_mxchip-iot-devkit_index.json to the additional_urls arduino board manager

for arduino-cli:
```
arduino-cli config init #if not allready initialized
arduino-cli config add board_manager.additional_urls https://kfessel.github.io/mxchip-iot-devkit/package_mxchip-iot-devkit_index.json
```
and install "AZ3166:stm32f4"

```
arduino-cli update
arduino-cli core install AZ3166:stm32f4
```

for Arduino-IDE 2.0.0:

```
> File > Preferences
Additional Boards Manager URLs
add https://kfessel.github.io/mxchip-iot-devkit/package_mxchip-iot-devkit_index.json
```
see: https://support.arduino.cc/hc/en-us/articles/360016466340-Add-or-remove-third-party-boards-in-Boards-Manager

and install the board:

https://support.arduino.cc/hc/en-us/articles/360016119519-Add-boards-to-Arduino-IDE

# help

please visit:

https://microsoft.github.io/azure-iot-developer-kit/

https://microsoft.github.io/azure-iot-developer-kit/docs/faq/

https://microsoft.github.io/azure-iot-developer-kit/docs/apis/arduino-language-reference/

https://github.com/microsoft/devkit-sdk/

https://github.com/VSChina/azureiotdevkit_tools
