![alt text](https://i.imgur.com/8D5JcGn.png "Chatty")

# Chatty (Bukkit plugin)

[![Build Status](https://travis-ci.org/Brikster/Chatty.svg?branch=master)](https://travis-ci.org/Brikster/Chatty)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/8463f0bb652842d4a5676ce4fd54f65c)](https://www.codacy.com/manual/Brikster/Chatty?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=MrBrikster/Chatty&amp;utm_campaign=Badge_Grade)
[![JitPack](https://jitpack.io/v/Brikster/Chatty.svg)](https://jitpack.io/#Brikster/Chatty)

Chatty is the unique Bukkit-plugin, that supports all modern Bukkit-servers, such as Thermos, Cauldron, Spigot, PaperSpigot e t.c. This plugin doesn't have any non-switchable options. It's simple, stable and lightweight.

-   Chats, such as local and global chats. Also you can add another chat.
-   Chats separation by permission. For example, if you have permission "chatty.chat.local", but have "chatty.chat.global", your message will sent at global chat.
-   Spy-mode permission. Players with "chatty.spy" permission can see all messages from all chats.
-   Vault API support.
-   Advancements announcements system.
-   Cooldowns for chats.
-   Auto-messages system.
-   Private messages system.

## Permissions

    chatty.chat.<chat> (chatty.chat.<chat>.see or chatty.chat.<chat_mode>.send) - grants access for chat.
    chatty.spy.<chat> or chatty.spy - allows to see all messages from chat-modes.
    chatty.command.spy - allows to use "/spy" command for enabling/disabling spy-mode.
    chatty.command.reload - allows to use "/chatty" command for reloading configuration.
    chatty.command.msg - allows to use "/msg" command.
    chatty.command.reply - allows to use "/reply" command.
    chatty.style.<style> or chatty.style.<style>.<chat> - allows to use styles in chat
        (styles: colors, bold, magic, reset, italic, underline, strikethrough).
    chatty.notification.chat.<list> - allows to see messages from Chat notification list.
    chatty.notification.advancements.<list> - allows to see messages from Advancements notification list.
    chatty.notification.actionbar - allows to see messages from ActionBar notification.
    chatty.moderation.advertisement - bypass advertisement moderation.
    chatty.moderation.caps - bypass caps moderation.
    chatty.cooldown or chatty.cooldown.<chat-mode> - allows to bypass cooldown of chat.

## Comparison with ChatEx

| Feature                                  | ChatEx | Chatty |
| ---------------------------------------- | ------ | ------ |
| Vault support                            | +      | +      |
| Advertisement protection                 | +      | +      |
| PlaceholderAPI support                   | +      | +      |
| Old versions support (1.5.2+)            | -      | +      |
| BungeeCord support                       | -      | +      |
| Replacement of AutoMessage               | -      | +      |
| Advancements and ActionBar notifications | -      | +      |
| Custom chat groups                       | -      | +      |
| Cooldowns                                | -      | +      |
| Built-in spy-mode                        | -      | +      |
| Private messages                         | -      | +      |

## Configuration

See default configuration in <b><u>src/main/java/resources/config.yml.</u></b>

### A little life-hack

You can delete all excess blocks and keep only needed features.

Plugin will work even with this simple config:

    chats:
      default:
        enable: true
        format: '{prefix}{player}{suffix}&r: {message}'
        permission: false

## Building

Chatty uses Apache Maven to handle dependencies & building.

### Requirements

-   Java 8 JDK or newer
-   Apache Maven
-   Git

### Compiling from source

```shell script
git clone https://github.com/Brikster/Chatty.git
cd Chatty/
./mvn clean package
```

You can find the output jar in `/target` directory.

## Credits

Supports by MCSTUDIO
