# Chapter 3: Representation: A Map With No Master Plan

Here's the answer, and there's no reason to make you wait for it: what the system holds, internally, is *position*.

Every token (every piece from the LEGO kit you met last chapter) gets *placed*: assigned a location in a vast space with far more directions in it than the three you can picture standing in a room. Every token the system has encountered corresponds to a specific point in that space. "Paris" is a location. So is "France." So is "capital," and "the," and the period at the end of this sentence. The knowledge lives in the geometry, not as stored facts or database entries.

That's the term, and here's its plain-language definition in one sentence: an **embedding** is a token's position in this space: a long list of numbers that amounts to a set of coordinates, the same way "three blocks east and two blocks north" is a position, just with many more directions than a person can hold in their head at once. "The capital of France is Paris" isn't stored anywhere as a sentence or a record. It's a consequence of where "Paris," "France," and "capital" sit relative to each other, and to everything else, in a structure built from nothing but the patterns in everything the system has read.

That's the headline. Everything that follows is what it actually means to say a word is a *place*.

## A Piece You Pick Up Becomes a Spot You Set It Down

Go back to the LEGO kit for a moment, because you're about to find out it was hiding something.

Last chapter, the kit explained what the *pieces* are: whole words, fragments, single characters, all of it broken down and reassembled one token at a time. What it didn't tell you, because the moment hadn't come yet, is what happens the instant a piece gets picked up. It doesn't stay a labeled brick with a name printed on the side. It becomes a location. Picking up a piece from this kit and reading it is the same act, inside the system, as setting it down at one specific spot on an enormous table; where it lands isn't random, and isn't fixed by the piece's shape alone. It's determined by everything the system absorbed about how that piece tends to show up: alongside which other pieces, in which situations, across the entire mountain of text it trained on.

The kit told you what the vocabulary is. This is what happens the moment that vocabulary gets used: each piece becomes a coordinate, and the coordinate carries information the symbol by itself never could. "Bank" the brick just sits there, inert, identical to every other "bank" in the box. "Bank" the *position* — well. We'll come back to that. For now, hold onto this: a token isn't only a symbol the system recognizes. It's also a spot on a map the system is constantly redrawing.

## A City With No Master Plan

So picture a map (an enormous one, with far more than the usual two directions to get lost in) where every concept has an address. And here's the part worth stating plainly, up front, rather than slipping in later as a footnote: addresses that sit close together on this map tend to belong to concepts that are close in *meaning*. "Dog" and "puppy" land near each other. "Dog" and "cat" land closer to each other than either lands to "asteroid." Zoom out further, and you'd find whole neighborhoods (clusters of words about cooking, about grief, about software, about weather), each one occupying its own region, each one nearer to the regions it's related to than to the ones it isn't.

This part is not a simplification the rest of the chapter is going to need to walk back. It is, at this point, about as settled and uncontested as anything in this book gets: positions in this space genuinely do encode relationships, and geometric closeness genuinely does track conceptual closeness. State it with exactly the confidence Chapter 2 used for "next-token prediction is the entire training objective," because it deserves exactly that much.

Now stop here for a second, because something genuinely strange just slid past, and walking on without noticing it would be a kind of waste.

Nobody sat down and decided where "dog" should go on this map. Nobody drew a border around "animals" and another one around "vehicles" and a third around "emotions," then assigned addresses inside each. The entire structure (every location, every neighborhood, every distance between one point and the next) assembled itself, with no one drafting it, out of nothing but the requirement to get a little better at guessing the next token, repeated across that staggering mountain of text Chapter 2 walked you through. A structure that looks, from the outside, exactly like something a careful cartographer must have drawn turns out to have had no cartographer at all. Sit with that for a moment before we move on. It's the kind of thing worth not rushing past.

## A Famous Demonstration, Checked

You may have come across this next claim already; it's been around for over a decade, repeated in articles, conference talks, and more than a few textbooks, usually as the single cleanest illustration of "meaning as geometry" anyone could ask for.

The claim goes like this: take the position of "king." Subtract the position of "man." Add the position of "woman." What you land on, supposedly, sits remarkably close to the position of "queen," as if the system had captured something like *analogy itself*, in pure arithmetic, on a map it built without anyone telling it to. King is to man as queen is to woman, and you can apparently prove it by doing subtraction. It's a wonderful claim. And by now, this book has been training you to ask exactly one question about wonderful claims: has anyone gone back and checked it?

Someone has. And here's what they found: the trick only worked because of a thumb quietly placed on the scale. The classic demonstrations didn't search the entire map for the closest match to "king minus man plus woman." They searched the entire map *minus the three words you started with*, quietly excluding "king," "man," and "woman" themselves from the running before checking what came out closest. Leave that exclusion in place, and "queen" often does turn up nearby. Take it away (let the arithmetic land wherever it actually lands, including back on the words you began with) and "queen" frequently isn't the answer at all. One detailed review published recently went so far as to call the popular version of the claim, in plain language, "fake news."

Sit with what that means for a second, because it's worth letting register fully: a claim that has been confidently repeated for more than ten years (quite possibly somewhere you yourself encountered it) turns out, on close inspection, to have been a party trick wearing a lab coat.

## What Survives the Correction

Now comes the single most important sentence-level move in this entire chapter, and it has to be made with total clarity: the correction lands on the *demonstration*. Not on the underlying idea.

It would be very easy, at this exact moment, to walk away thinking: oh, so the geometry thing isn't real after all, it was just a magic trick the whole time. That would be exactly the wrong lesson, and exactly the kind of overcorrection this book exists to head off, trading one misconception for another in the act of fixing the first one. So let's be precise about what actually got disproved and what didn't.

What survives, fully intact, is the part that actually does the work: relationships between concepts really are encoded as directions and distances in this space. That is settled. That is foundational. That is not, in any serious sense, in question; it's the second of this chapter's two claims you can take with full, unhedged confidence, every bit as solid as the first. What does *not* survive is something much narrower and much flashier: the specific, tidy, almost magical-feeling promise that you can run clean schoolbook arithmetic on meaning and pull a textbook-perfect answer out the other side, on demand, no asterisks. That promise was always too neat for what this structure actually is. The real geometry is messier, more tangled, and far less obliging than the famous version implied; that messiness, far from being a disappointment, is closer to what you'd actually expect from something built out of billions of overlapping patterns rather than handed down from a tidy rulebook. The honest version is more interesting than the false one. It usually is.

## No Drawer Marked Paris

So, return, now, to "Paris," and go the one layer deeper you're owed.

You already know, from Chapter 2, that "Paris" gets produced because the pattern "the capital of France is ___" is overwhelmingly dense in the text the system trained on, and that this isn't retrieval from some labeled cell. Fine; but granted that, what *kind of thing*, mechanically, is doing the producing? If there's no drawer with a card inside it reading "Paris = capital of France," what's actually there instead?

Here's the answer the geometry gives you: there is no record. No entry. No drawer. What exists instead is a *region* of that enormous space (a neighborhood) where "Paris," "France," "capital," and a great many other related positions all sit close enough to each other, in a consistent enough configuration, that landing anywhere nearby tends to nudge the system toward producing exactly that word next. The "fact" isn't stored in any one place. It's a *standing relationship between locations*, distributed across an almost incomprehensible number of these positions and the billions of settings that placed them there in the first place. Asking "where, exactly, is the Paris-is-the-capital-of-France fact kept?" is a little like asking which specific neighborhood of a city is responsible for the fact that people there tend to eat dinner around seven in the evening. There isn't a building you could point to. It's a pattern that exists *across* the structure, not *inside* any one part of it.

Which brings us back to that map with no master plan, because this is exactly where it earns its keep.

Picture an old city, the kind that grew up over centuries with no central planning office. No one ever sat down with a blueprint and decided "the bakeries go on this street, the print shops on that one." And yet walk through a city like that today, and you'll find the print shops clustered in one quarter and the food stalls bunched in another, not because anyone zoned it that way, but because each small decision (a baker setting up shop near other bakers, a customer learning where to look first) nudged the next decision just slightly, millions of times over, until a structure emerged that looks, from above, exactly as if someone had planned it. Nobody did. That's what this space looks like from the inside: a structure with every appearance of design, built entirely out of accumulated small adjustments, with no blueprint and no architect anywhere in the process, only the requirement repeated an astronomical number of times, to get a little better at guessing what comes next. You've now watched this same shape (pattern without a pattern-maker) pay off twice. It's the same "novelty is scale, not kind" idea wearing a new coat.

That's what a **distributed representation** is, in plain terms: information that exists as a pattern spread across a structure, with no single piece of it responsible for the whole, the way a city's character lives in the relationships between its neighborhoods, and not inside any one building you could point a finger at.

## What "Knowing" Means Here

So where does that leave the word "knowledge," because at some point this chapter has to actually use it, and it owes you an honest account of what it means when it does.

In a *functional* sense: yes. The system can fairly be said to "know" that Paris is the capital of France, in that it reliably produces the right answer when asked, combines that fact correctly with others, and does so across an enormous range of phrasings it has never once encountered before. That's genuinely impressive, and this book isn't going to pretend it's anything less.

But it is not knowledge in the way a filing cabinet holds it, or a database holds it, or (for that matter) the way a person who once stood in the Place de la Concorde holds it. There's no record in there that could be located, printed out, edited, or deleted. There's only a structure, shaped entirely by patterns, that produces the right behavior when the right question lands in the right neighborhood of the map.

Whether that distinction actually *matters* (whether "produces correct answers reliably, for purely structural reasons, with nothing behind it that resembles a memory" amounts to a *lesser* kind of knowing, a genuinely *different* kind, or a sign that our own definitions of "knowing" were never as crisp as we assumed they were) is not a question this book is going to resolve for you. It can't. Nobody currently can. What's worth naming plainly is that this is the *same* fault line as the stochastic-parrots debate from Chapter 2: the same disagreement, viewed one level further down, now that you can see the geometry underneath the fluency. It was unresolved there. It stays exactly that unresolved here. The only difference is that you can now feel, with much more precision than before, exactly what the question is actually asking.

## Where Does All of This Actually Live?

Stand back for a second and take in what you're now holding.

You know, in real and concrete terms, what the system is holding internally: not facts, not records, but *positions*, an enormous structure of locations and distances, where relationships between concepts live as directions you could, in principle, point to. You know that the famous arithmetic trick built on top of that structure doesn't survive close inspection; and, just as importantly, exactly what *does* survive it. You know what kind of thing actually produces "Paris," mechanically, at the level beneath pattern density: not a drawer, but a standing relationship distributed across a city that built itself, with no architect, out of nothing but the pressure to guess a little better each time.

But notice what hasn't been explained yet, because it's sitting right there, in plain view, the moment you look for it. A position, on this map, isn't fixed. "Bank" doesn't sit in one single, permanent spot, the way "Paris" mostly does. "Bank" lands near "river" in one sentence and near "interest rate" in another; it isn't that there are two different words that happen to look alike. It's the same starting point, *relocated*, on the fly, depending on what surrounds it this time.

Something has to be doing that relocating. In real time. For every word, in every sentence, all at once, every single time the system reads something and produces what comes next. That something lives inside an architecture this book hasn't named yet, hasn't even gestured at. So here's the question this chapter is handing forward, and it's the one worth carrying with you into the next one: what is the *thing*, precisely, that reads a sentence and decides, word by word, where everything in it actually belongs: this time, and not the last time, and not the time after that?

That's the architecture. And that's where we go next.
