# k-goku

A configuration using GokuRakuJoudo to generate Karabiner profile.

## What is Karabiner?

[Karabiner](https://pqrs.org/osx/karabiner/) is a powerful and stable keyboard customizer for macOS.

- You can re-map any key without any restriction. 
- You can accelerate speed of the key repeat. Karabiner offers frequently used settings. 
- You can activate them by simply clicking the checkbox in the list. If the settings which you want are not in the list, you can add them by yourself. 

Karabiner has many useful features for efficient keyboard operations. 

- You can do Emacs-style operations anywhere. 
- You can do Vi-style operations anywhere. You can do Mouse operations from keyboard.

You can do everything by modifying your keyboard!

## What is GokuRakuJoudo?

[Goku](https://github.com/yqrashawn/GokuRakuJoudo) is a tool to let you manage your Karabiner configuration with ease.

Karbiner Elements uses JSON as it's config file. This leads to thousands lines of JSON (sometimes over 20,000 lines). Which makes it really hard to edit the config file and iterate on your keymap.

Goku use the [edn format](https://github.com/edn-format/edn) to the rescue.

## What is k-goku

k-goku is a configuration using GokuRakuJoudo to generate Karabiner profile, which provides a set of handy personal customised rule. ☺