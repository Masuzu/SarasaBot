# Who is サラーサボット (Sarasa bot)?

Sarasa is a bot for Granblue Fantasy designed to automatically track raids, join them, collect the loot, and then do the same again!
```
raids_to_track = <user defined>
while (continue) do
  new_raid = wait for new raid in raids_to_track to pop
  join new_raid
  run <user defined Lua script>  
  if Sarasa can't join a new raid then
    collect loot
  end
end
```

It can:
- track raids **in real time** faster than Tweetdeck
- join raids **faster** than a human can. First come first serve!
- parse user scripts to **[use skills and summons](https://www.youtube.com/watch?v=SwWNsTNXWSc)** and customize the sequences of actions performed during fights, the same was as [Zooey Bot](https://github.com/Masuzu/ZooeyBot). This offers a plethora of possibilities to help you tackle the harder quests.
- join another raid mid-fight without having to wait for the end of the battle
- choose summons among a user-defined list of preferences, and refresh summons when some are not available
- refill BP on its own when needed
- stop automatically when the captcha screen appears, when X AP potions were used or when Y minutes were elapsed
- ignore raids below X% remaning HP (as this raid is more likely to end by the time you join and press a button)
- retreat from raids which drag too long (High Level Chevalier for instance)
- minimize the number of clicks when collecting raid rewards to maintain a high raid participation throughput during peak hours

Last but not least, it **never gets tired**.

It is compatible with Viramate skill and summon hotkeys, should you use it. It is generally faster to use the hotkeys instead of clicking on the character whose ability you want to use, then on that ability icon.

Sarasa Bot consists in an executable program and a Chrome Extension. Contrary to Chrome Web Store extensions which can be tracked by ID (such as Viramate or AnCheera), the Sarasa Bot extension has no fixed ID: its ID is generated randomly at installation and can be easily *[regenerated on demand](https://github.com/Masuzu/SarasaBot/wiki/Regenerating-your-Sarasa-extension-ID)*. Sarasa does not inject any Javascript code or HTML contents tampering with the original GBF webpage. In the same fashioin as [Zooey Bot](https://github.com/Masuzu/ZooeyBot), Sarasa controls your mouse and keyboard inputs in the same way as a human would do: click positions, mouse trajectories and delays are all randomized.

Sarasa Bot does not store any personal information about the user account.


# [Download website](https://gbtools.azurewebsites.net/SarasaBot/en/Home)

## Why Viramate or (insert here any other extension name which can be found on the Chrome store) can be easily detected?

By design from Google, the only way to know whether a Chrome extension is used is to know its ID. As stated above, Chrome Web Store extensions have a fixed ID from the first day they are released on the store. Sarasa is not available on the Chrome Web Store and is installed by loading it manually. Therefore, regenerating its ID on demand and at any time makes it untrackable.

## Why tampering with frame per seconds and other similar hacks can be easily detected?

Just to give you some context, this allowed players to increase the speed of the animations by a significant amount, resulting in faster turns and thus much more damage dealt than regular players. This was achieved by *modifying* some of the Javascript variables on the GBF webpage. Detecting that a variable has an impossible value in your webpage is easy, isn't it? Bingo!

**Sarasa does not mess with any of the elements of the HTML page, neither does it try to modify any of the Javascript variables on the GBF webpage.**

# Resources

[Setup and installation](https://github.com/Masuzu/SarasaBot/wiki/Setup-and-installation)

[Getting down to business: first run](https://github.com/Masuzu/SarasaBot/wiki/Getting-started)

[Raid selection](https://github.com/Masuzu/SarasaBot/wiki/Raid-selection)

[Lua scripts](https://github.com/Masuzu/SarasaBot/wiki/Lua-scripts)

[Regenerating your Sarasa extension ID](https://github.com/Masuzu/SarasaBot/wiki/Regenerating-your-Sarasa-extension-ID)

[Summon selection](https://github.com/Masuzu/SarasaBot/wiki/Summon-selection)

[Frequently Asked Questions](https://github.com/Masuzu/SarasaBot/wiki/FAQ)

Current version patch notes [2.13.6](https://gbtools.azurewebsites.net/SarasaBot/en/Home/PatchNotes#2-13-6)

