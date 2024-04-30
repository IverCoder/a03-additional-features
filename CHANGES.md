<sup>SPDX-FileCopyrightText: 2024 IverCoder \<https://github.com/IverCoder\></sup>

<sup>SPDX-License-Identifier: CC0-1.0</sup>

Here are the modifications this module does to system files, and how it affects your deivce. Credits to [@ravindu644](https://github.com/ravindu644)'s [Samsung Additional Features 2.0 guide](https://github.com/ravindu644/Samsung_Additional_Features).

# `floating_feature.xml` tweaks
## High end launcher animations
```xml
<SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ANIMATION_TYPE>LowEnd</SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ANIMATION_TYPE>
```
is changed to
```xml
<SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ANIMATION_TYPE>HighEnd</SEC_FLOATING_FEATURE_LAUNCHER_CONFIG_ANIMATION_TYPE>
```
It makes One UI Home and other Samsung apps use the same animations as they do on the highest-end Galaxy S line. This has barely any performance impact thanks to the Galaxy A03 having a decent GPU.

## Performance profiles
```xml
<SEC_FLOATING_FEATURE_SYSTEM_SUPPORT_LOW_HEAT_MODE>TRUE</SEC_FLOATING_FEATURE_SYSTEM_SUPPORT_LOW_HEAT_MODE>
```
is added. It exposes a "Performace profiles" feature that lets you switch between Standard performance and Light performance which offers better battery life and lower temperature. Its impact to this device is untested and might be just placebo.

## Smooth scrolling
```xml
<SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SMOOTH_SCROLL>TRUE</SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SMOOTH_SCROLL>
```
is added.

## Screen recording feature
```xml
<SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SCREEN_CAPTURE_ADVANCED_EDIT_VI>TRUE</SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SCREEN_CAPTURE_ADVANCED_EDIT_VI>
<SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SCREEN_RECORDER>TRUE</SEC_FLOATING_FEATURE_FRAMEWORK_SUPPORT_SCREEN_RECORDER>
```
is added. It reenables the built-in screen recording feature which is disabled on One UI Core devices.

## Secure Wi-Fi
> **Takes effect on certain regions only** but kept for other users who live in supported regions. Confirmed to have no effect for users with the CSC `XTC` (Philippines unbranded). Theoretically activatable on all regions via CSC data modifications, which is planned for a future update.
```xml
<SEC_FLOATING_FEATURE_WLAN_SUPPORT_SECURE_WIFI>TRUE</SEC_FLOATING_FEATURE_WLAN_SUPPORT_SECURE_WIFI>
```
is added. It enables Samsung's built-in VPN service.

# System properties tweaks
The system properties
```
fw.max_users=5
fw.show_multiuserui=1
fw.showhiddenusers=1 
fw.poweruserswitcher=1
```
are set. It enables the multi-user feature.