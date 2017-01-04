This FAQ is for general users who are new to steno. If you're a steno
professional, read the [[FAQ for Stenographers]]. For troubleshooting, see [[Troubleshooting: Common Issues]].

**Table of Contents**

- [What is Plover?](#what-is-plover)
- [What is stenography?](#what-is-stenography)
- [How does it work?](#how-does-it-work)
- [Why was Plover written?](#why-was-plover-written)
- [Why "Plover"?](#why-plover)
- [How is Plover different from commercial steno programs?](#how-is-plover-different-from-commercial-steno-programs)
- [Why learn steno? And how?](#why-learn-steno-and-how)
- [What hardware is needed to use Plover?](#what-hardware-is-needed-to-use-plover)
- [What can Plover do right now?](#what-can-plover-do-right-now)
- [What does Plover look like in action?](#what-does-plover-look-like-in-action)
- [Who's responsible for Plover's development?](#whos-responsible-for-plovers-development)
- [Does the Plover Project accept donations?](#does-the-plover-project-accept-donations)

### What is Plover?

Plover is the world's first free, open-source stenography program. It is
available on Windows, Mac and Linux. See the
[Releases](https://github.com/openstenoproject/plover/releases) page.

### What is stenography?

Stenography is a form of shorthand typing done on a special machine. It was invented in early 1900s.

Real-time machine stenography is a code translation system that lets users enter words and syllables by pressing multiple keys simultaneously in a chord, which is then instantly translated into English text. 

This makes steno the fastest and most accurate text entry method currently available.

| Method | Typical Speed |
| ----------|-----------|
| Handwriting | 31 wpm |
| Average Typist | 40 wpm |
| Top QWERTY Typist | 120 wpm |
| Top Dvorak Typist | 140 wpm |
| Voice Writer | 180 wpm |
| Average Speech | 200 wpm |
| Amateur Stenographer | 160-200 wpm |
| Professional Stenographer | 225-300 wpm |
|Steno World Record | 360 wpm |

 In the first semester of steno school, nearly all students learn to exceed 100 words per minute. By comparison, top qwerty typists can do 120 WPM, top Dvorak typists around 140 WPM, and voice writers dictating to voice recognition software around 180 WPM. But experienced stenographers can enter text at up to 300 words per minute (the world record is actually 360, but that's an outlier). Conceivably, with practice, amateur steno users could reach 160-200 words per minute.

### How does it work?

See the [comparison
table](Comparison_between_QWERTY_and_Steno "wikilink") between qwerty
(or dvorak, etc) and steno for more details.

Most likely, you are using a qwerty or dvorak keyboard layout to type
everything out character by character. However, Plover—and other steno
systems—use keyboard "chords" to type syllables, words, or entire
phrases. If you ever practiced piano, it might be helpful to liken them
to certain piano pieces common in a pianist's repertoire. The
"typewriter-style" systems (qwerty, dvorak, etc.) are like Chopin's
Fantasie Impromptu:

[![Yundi Li - Chopin "Fantasie" Impromptu, Op. 66](https://img.youtube.com/vi/tvm2ZsRv3C8/0.jpg)](https://www.youtube.com/watch?v=tvm2ZsRv3C8)

Notice how this piece—like typing—is mainly runs of single fingers. When
you learn and practice this piece, you often do many finger exercises to
strengthen certain fingers to increase your speed. However,
"steno-style" systems (NYCI, StenoEd, Phoenix, etc.) are like
Rachmaninoff's Prelude in G Minor:

[![Rachmaninoff Prelude in g minor op. 23 #5](https://img.youtube.com/vi/4QB7ugJnHgs/0.jpg)](https://www.youtube.com/watch?v=4QB7ugJnHgs)

Unlike the Chopin, this piece is almost entirely chorded. When learning
a piece like this, you learn how to block your chords. So your approach
to learning steno may be completely different than learning a different
keyboard layout, since it's a completely different system. Explore this
site if you wish to learn more about "Rach-style" keyboard computer
entry.

### Why was Plover written?

A professional stenographer, forced to buy proprietary (and DRM-riddled)
steno software for $4,000 plus an annual $700 upgrade fee after
shelling out for a $3,000 steno machine, looked around and saw that
most of the people who made their living and their free time putting
text up on a screen were crawling along at around 60 words per minute
because they were using qwerty instead of steno. She realized that the
only way to spread the wonders of high speed efficient text entry to the
geeks, hackers, writers, and internet addicts who desperately needed it
was to make the software free and the hardware cost less than $60. She
found a Python programmer who was also a hardware maven, and they both
got down to work. Eleven months later, Plover was ready for prime time.

### Why "Plover"?

The short answer is that it's a two-syllable, six-letter word that can
be written in a single stroke on a steno machine. The longer answer is
[here](http://plover.stenoknight.com/2010/03/why-plover.html).

### How is Plover different from commercial steno programs?

Well, first off, it's free. Free to distribute, free to modify. No
dongles, no upgrade fees, no constraints. That's already a $4,000
difference. To the developer's knowledge, it's also the only steno
software that works on a buffer-based system rather than a timer-based
system, and that has direct access to the OS rather than filtering
everything into a steno-specific word processor. This means it's
lightweight, powerful, and doesn't require a 1.5-second wait time
between when a stroke is entered and when the translation appears in an
external program. In Plover, the translation appears instantly, and the
software isn't cluttered up with file managers, printer handlers, and
other court-reporting flimflam that an amateur stenographer will never
use. Instead, it's a direct conduit between the steno keyboard and the
OS. Plover, as of version 2.1, can do everything a qwerty keyboard can
do – but much, much faster.

### Why learn steno? And how?

Mirabai Knight has broken the answer to the first question into six parts:

1. [How to Speak With Your Fingers](http://stenoknight.com/SpeakFingers.html): for people who
can't use their voice to speak but want to communicate in real-time using
a steno-enabled text to speech device.
1. [Writing and Coding](http://stenoknight.com/WritingCoding.html): for people whose
fluency of thought depends on ease and efficiency of text input.
1. [The Ergonomic Argument](http://stenoknight.com/ErgonomicArgument.html): for people
who want to avoid wasted effort and repetitive stress injuries.
1. [Mobile and Wearable Computing](http://stenoknight.com/MobileWearable.html): for people who
want to input text and control their computers while walking around,
with a minimum of dorkitude.
1. [Raw Speed](http://stenoknight.com/RawSpeed.html): for people who have to be the fastest, no matter what.
1. [CART, Court, and Captioning](http://stenoknight.com/CARTCourtCaptioning.html): for
people who want to provide live verbatim transcription professionally.

For learning, the best resource is [Learn Plover!](https://sites.google.com/site/ploverdoc/home) by Zack Brown.

### What hardware is needed to use Plover?

See the [[supported hardware|Supported Hardware]] page.

### What can Plover do right now?

Plover can write properly capitalized and punctuated text into any
window as if it were an ordinary keyboard. It can send command strokes
such as Enter or Escape, giving it complete equivalence to the Qwerty
keyboard. It's also a robust and convenient text entry system, suitable
for writing, coding, chatting, and kicking people's butts at online
typing games.

### What does Plover look like in action?

Here's a video of me kicking someone's butt in
[TypeRacer](http://play.typeracer.com/), an online typing game that lets
people race against each other by hammering out random snippets of text
at high velocities:

[![Plover Wins the Race!](https://img.youtube.com/vi/jkUyg_uoidY/0.jpg)](https://www.youtube.com/watch?v=jkUyg_uoidY)

And here's a demonstration of Plover with eSpeak, a free text-to-speech
engine, which can be a way to talk at a normal conversational pace by
people who don't use their voices to speak, as discussed in [How to
Speak With your Fingers](http://stenoknight.com/SpeakFingers.html).

[![Realtime Text to Speech with Plover](https://img.youtube.com/vi/K3MYFT6VZk8/0.jpg)](https://www.youtube.com/watch?v=K3MYFT6VZk8)

This is Mirabai's demonstration. It shows the keys pressed along with
their resulting output. Read more about it [from her blog
post](http://plover.stenoknight.com/2011/10/split-screen-demonstration.html)

[![Demonstration of Plover with Qwerty Keyboard](https://img.youtube.com/vi/JXQQzW99cAI/0.jpg)](https://www.youtube.com/watch?v=JXQQzW99cAI)

### Who's responsible for Plover's development?

Plover was originally created by [Mirabai
Knight](http://www.blogger.com/profile/16494847224950297255) and [Joshua
Harlan Lifton](http://launchpad.net/~joshua-harlan-lifton), and is the
software arm of [The Open Steno Project](http://openstenoproject.org/),
an umbrella organization for open source steno tools. The current lead
developer is Theodore Morin.

### Does the Plover Project accept donations?

Absolutely. Contributions of money, code, testing, documentation,
publicity, or TypeRacer cannon fodder are [gratefully
accepted](http://stenoknight.com/plover/donatepage.html).
