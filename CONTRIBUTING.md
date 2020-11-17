# Contributing

So you'd like to help add to the Verum Archives here? Awesome. Nearly everything you find here is contributed by the community and more help is always welcome.

Whether you just want to help proof-read some sections, fix some typos, or add full transcripts for campaign sessions or boss/encounter breakdowns all help is appreciated.

Large sweeping changes of organization are also welcomed as the goal here is to make this information as accessible as possible to as many people as possible. After all, in a similar vein to Arcadum's goal to bring DnD to as many people as possible, making the lore of Verum easy to jump into helps that goal as well.

Below you'll find some helpful advice and general standards we try to adhere to in all the various documents found within this Archive.

## Submitting Changes / New Files

Since this is a Git repository and not everyone has the knowledge of using Git some changes will most easily be done by going to the particular file you wish to edit, opening it up in the browser here, and clicking the little pencil icon in the top-right of the bar:

<img src="https://imgur.com/icvGhV2.png" alt="File edit pencil icon button" width="450px"/>

This will open up the markdown editor live on the page and you can make your changes, additions, and edits.

When you're done go down to the bottom of the page, give a title to the changes you made and any description you can give about what changed. Then choose to submit your changes as a new branch and pull request:

<img src="https://imgur.com/j2vqbWQ.png" alt="Submitting changes to a file in the browser-based markdown editor" />

Do not ever choose to "commit directly to the `master` branch", this has the problem of potentially overwriting files when you don't mean to.

Click the green "Propose Changes" button when you're ready.

---

For those of you familiar with Git and GitHub, feel free to clone down the repo and make whatever changes you need in a new branch and submit a PR for review/merging. Ideally your PR should detail what you added or changed so reviewers can more quickly approve the PR.

## Style Guide

A few pointers on formatting so we can have a consistent look and feel to all the various pages.

### Transcripts / Quotes

When compiling what has been said by any character in a game, whether in Maptool's chatbox as text RP or spoken aloud by a character the general format used is:

```md
> **CharacterName**: What they said.
```
This will end up looking like this:<br>
> **CharacterName**: What they said.

---

For when a character emotes something:
```md
> ***CharacterName** picks up a bag.
```
This will end up looking like this:
> ***CharacterName** picks up a bag.

---

For when you need to contain text across multiple lines for readability or to represent a pause in the conversation, or just a dramatic break:

```md
> **CharacterName**: What they said<br>
Something else they said after a pause.

# Alternatively if you need more space
> **CharacterName**: What they said.
>
> Something else they said.
```
This will end up looking like this:
> **CharacterName**: What they said<br>
Something else they said after a pause.

Alternatively if you need more space:
> **CharacterName**: What they said.
>
> Something else they said.

---

When multiple characters are speaking be sure to use the HTML line-**br**eak element (`<br>`) to help space things out:
```md
> **Character01**: Upon further thought, no.<br>
**Character02**: But why not?
```
This will look like:
> **Character01**: Upon further thought, no.<br>
**Character02**: But why not?

<br>

If you forget to use the `<br>` it ends up less ideal:
> **Character01**: Upon further thought, no.
**Character02**: But why not?

You may think, but why not just use another `>` to help?
```md
> **Character01**: Upon further thought, no.
> **Character02**: But why not?
```
> **Character01**: Upon further thought, no.
> **Character02**: But why not?

Using more `>`'s will only end up spacing out the conversation too much:
```md
> **Character01**: Upon further thought, no.
>
> **Character02**: But why not?
```
> **Character01**: Upon further thought, no.
>
> **Character02**: But why not?

### Dice & Dice Rolls

When representing an item and what power it has it is customary to specify what particular dice it uses, how many of them and what modifiers apply. To show that here we use square brackets:

```md
Long sword is a [2d6+5] slashing weapon.
```

Sometimes what a character rolled in a situation, or what Arcadum himself may role in a situation is important to what happened. For these situations we use the back-ticks to help highlight the roll. Also, unless there is good reason to incude it within the conversation (e.g. a player says it out loud) most rolls will go on their own line separate from the conversation:

```md
> **CharacterName**: Can I see if he's lying?<br>
> **Arcadum**: Sure, give me a perception check.

(CharacterName/PlayerName rolls a perception check of `23(19)`)

> **Arcadum**: With a 23 you see this man is full of it. Lying through what few teeth still remain in his mouth after a lifetime of such lies.
```
This will give us:

> > **CharacterName**: Can I see if he's lying?<br>
> > **Arcadum**: Sure, give me a perception check.
>
> (CharacterName/PlayerName rolls a perception check of `23(19)`)
>
> > **Arcadum**: With a 23 you see this man is full of it. Lying through what few teeth still remain in his mouth after a lifetime of such lies.

### Dividing Sections Within A Session/File

Sometimes a particular session transcript, lore block, or singular archive of a particular importance can grow rather long. To help break this up it's best to try and break these up with separate headings or even just a plain horizontal line.

#### Headings

The basics of markdown are the headings via the hash (`#`) character. The more you use the smaller and more nested the heading:

```md
# Main Heading

## Sub-Heading

### Lower Heading Than That
```

> # Main Heading
>
> ## Sub-Heading
>
> ### Lower Heading Than That

It's also desired that because these are like titles of each section to use as much Capital Case as makes sense for what you might expect to see in the title of a book, movie, or video game.

#### Horizontal Lines

Within one of these sections sometimes it doesn't make sense to break it down further into sub-sections via the hash (`#`) characters so you can instead just insert a horizontal line like you see below:

```md
...ending of a previous set of text.

---

New text after a horizontal line is placed to help visually separate it.
```

> ...ending of a previous set of text
>
> ---
>
> New text after a horizontal line is placed to help visually separate it.

These are often good to use show that, for example, the party is still in a particular location, but perhaps some time has passed between to portions. Or the party has moved location but are still basically at the same location mentioned in the heading.

### Pictures & Images

As they say, a picture is worth a thousand words. So sometimes it is worth adding a picture to help with whatever entry you're working on. Maptools screenshot of the room? Token art for an NPC? Or even a screenshot from Discord/Twitch chat to be a stand-in until a transcript can be made for it? Regardless of the reason there's a basic way to add them. The HTML `<img />` tag.

But don't forget to add in the `alt` and `height` tags.

```md
[<img src="https://i.redd.it/nyb85si7yuw51.jpg" alt="Fanart of Zack from Strange Roads by squidspoken" height="250px" />](https://i.redd.it/nyb85si7yuw51.jpg)
```

[<img src="https://i.redd.it/nyb85si7yuw51.jpg" alt="Fanart of Zack from Strange Roads by squidspoken" height="250px" />](https://i.redd.it/nyb85si7yuw51.jpg)

So what's going on with the link above? Why is it there twice and what's with the extra information?

Well, first the `alt` tags are great for if a picture is broken or missing for whatever reason some text will show up in its place:
```md
#e.g.
[<img src="https://i.reddit.com/nyb85si7y--w51.jpg" alt="Fanart of Zack from Strange Roads by squidspoken" height="250px" />](https://i.redd.it/nyb85si7yuw51.jpg)
```
[<img src="https://i.reddit.com/nyb85si7y--w51.jpg" alt="Fanart of Zack from Strange Roads by squidspoken" height="250px" />](https://i.redd.it/nyb85si7yuw51.jpg)

Note the text in the `alt` tag shows up now? This can happen for a number of reasons. For example it could be because the link to the picture is either wrong or the site removed where the picture came from.

Also, for accessibility reasons the `alt` tag is great for those who need to view a webpage with a screen reader. Their screen reader software can pick up the text in the `alt` tag and read out the description of the picture to them.

Second, the `height` tag is there to control how big the picture shows up on the page. A picture is great to see, but we don't want it taking up the whole screen. The `250px` (250 pixels) is not a hard and fast rule. Feel free to change this to fit whatever you think is best for the document you're working on.

And lastly, the formatting you see above is to help turn the picture, a thumbnail if you will, into an actual clickable link. It's just combining two different forms of markdown syntax.

The basic markdown link: `[some text](http://example.com)` --> [some text](http://example.com)<br>
And replacing `some text` with the `<img />` tag instead.

So why do this? Because of how we shrink the picture to fit the page it's still nice to be able to see the whole thing. So now anyone can click on the picture and go to the original, full-sized picture. (Go ahead, click that pic of Zack to see it in its full glory 😉)

### Spelling & Words You're Unsure About

Sometimes it's hard to know how a particular word is spelt when it comes to a fantasy setting and some of them are just made up. Or sometimes it's hard to hear what exactly was spoken given microphones and Discord's audio codecs.

For those times when you're not sure exactly how to spell something it's perfectly fine to include your best guess. Just denote it's a guess. That way if someone comes along later and knows the right way to spell it we know what to look out for:

```md
> **Arcadum**: When you're traveling to Rentoss(sp?) you'll find yourself looking out up on the Astral Sea
```
Above we're saying we're not really sure about the spelling of `Rentoss` but it's close enough phonetically for now.

---

For when you aren't entirely sure what word someone said because it was garbled or someone spoke over them:

```md
> **Braktor**: Hey, Azolon, what happens if we travel to the horrifying(?) depths of the world to find some answers?
```
Above, here, we're saying that we're not entirely sure if the person said `horrifying` or `harrowing` or something else entirely but it sounded like the "horrifying".
