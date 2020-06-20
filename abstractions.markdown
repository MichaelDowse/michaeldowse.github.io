---
layout: post
---

![What my toddler taught me about abstraction](/images/abstractions/abstractions.001.png)

Thanks, good morning, welcome, I’m so excited to be here with you today.

---

![Tamagotchi](/images/abstractions/abstractions.002.png)

It's been about 10 years now since I started learning Ruby

And it's been four years since I became a parent.

The first thing I learned when my daughter Charlie was born is that babies are like puzzles. They can't talk, or walk. All they do is cry, or not cry.

And to solve the puzzle, you have to make them not cry. That's how you win.

Kind of like a tamagotchi.

This is one of the first things they teach you in ante-natal classes right.

If your baby starts crying: Here's how to figure out why they are crying.

Here is how you debug that problem.

They just don't use the word debug but it is very much a debugging process.

And then they learn to talk. Wow, this is when it gets interesting.

---

![In the beginner's mind there are many possibilities, in the expert's mind there are few](/images/abstractions/abstractions.003.png)

Children come into this world with such an open attitude. They are so curious. They have no preconceptions or biases. They are open to any possibility.

**In the beginners mind there are many possibilities, in the expert's mind there are few.**

Children start out this way, no one has told them what isn't possible, so they assume that anything is possible.

Not like us adults, with our decades of experience, slowly whittling down the set of possibilities that are open to us.

We know there are no purple elephants, or monsters in the wardrobe.

But to a toddler, almost anything is possible.

It can be hard for us as adults to step back into this mindset, to open ourselves up to these possibilities, so we talk about imagination, the skill of considering possibilities which we know not to be possible.

But for a child, this is just how they are. In a child's mind there are many possibilities, in an adults mind there are few.

---

![Why?](/images/abstractions/abstractions.004.png)

And then children take this open mind and combine it with the confidence to ask Why.

Why are blue penguins blue? I had to ask the zookeeper.

Blue penguins are blue to provide camouflage in the blue ocean.

---

![Asking why is a recursive function](/images/abstractions/abstractions.005.png)

And then they keep asking Why, recursively.

But why is the ocean blue? Why do penguins need to camouflage themselves in the ocean? And so it goes.

It turns out that it's possible to ask Why a lot more than five times in a row.

So I've been watching Charlie for a couple of years now, as she considers many possibilities, and asks Why a lot, and I've brought along a few stories that I'd like to share with you today.

---

![There are two hard things in Computer Science: Cache invalidation and naming things](/images/abstractions/abstractions.006.png)

There are two hard things in Computer Science: Cache invalidation and naming things. This isn't a joke, it's the original quote. I myself have definitely found this to be true, and Naming things well is hard. One of the hardest things in computer science as the saying goes. But naming things isn't a challenge that only relates to computer science as I learned.

---

![Ice-cream light](/images/abstractions/abstractions.007.png)

This is a light in Charlie’s room. I call it the Ice Cream Light, which seemed like a totally sensible thing to call it.

But one day Charlie got quite frustrated with me about this light

Because

She couldn't eat it. And it didn't taste like ice cream.

And for a moment I was confused, because, obviously, this is not edible.

But that's the experts mind speaking. The expert has been around a while, has seen a lot of lights and eaten a lot of ice creams.

In Charlie's mind there exists a possibility that no longer exists in mine: That this object is both an edible ice cream and a functioning light.

This was my fault really.

If I tell you something is an Ice Cream Light then to someone who has only a little experience with lights and even less experience with Ice Creams, there's an obvious interpretation.

---

![Ice-cream light class](/images/abstractions/abstractions.008.png)

An object that has the behaviours of both an Ice Cream and a Light.

What I was actually trying to express is something quite different: An object which has the behaviours of a light, with the shape of an Ice Cream.

---

![Ice-cream light class](/images/abstractions/abstractions.009.png)

This is what I had in mind.

It may be obvious to us as adults, that this object is not edible.

But the name is not clear to a toddler, or to a new developer who has just joined the team and is trying to understand these abstractions by reading the code without any real world context.

It's a bad name for a difficult to describe object.

---

![Ice-cream light class](/images/abstractions/abstractions.010.png)

Now I've renamed it to IceCreamShapedLight.

It's a longer name that accurately describes the behaviours of the object. No more disappointed toddlers.

A good name should describes what an object does at a high level, so that a fellow developer can read through some code and see `IceCreamShapedLight` and be like "Sure, yeah, I can assume that does what it says it does."

Another thing to consider is what assumptions we're making about the readers existing knowledge.

We're making an assumption here that the reader knows what an ice-cream is and knows what a light is, which I think in this case is a reasonable assumption.

---

![Ice-cream light class](/images/abstractions/abstractions.011.png)

If we tried to make less assumptions we could end up with something like this. A cold dairy based treat in the shape of a source of luminescence. This is really long, hard to understand, and at the same time manages to be an even less accurate description.

Yoghurt is also a cold dairy based treat, and ice cream can be made without dairy. So in our attempts to reduce the amount of knowledge required we've ended up with a worse name.

---

![Ice-cream light class](/images/abstractions/abstractions.012.png)

So that's the first lesson Charlie taught me. 

Naming things is hard, I agree with Phil Karlton on that one.

To avoid disappointment we should avoid ambiguous names.

And we need to consider what pre-requisite knowledge is required to understand the names we're creating.

---

![Charlie looking at ocean](/images/abstractions/abstractions.013.png)

This is Charlie, looking at the ocean. Just after I took this photo she turned to me and said: "Wow, big puddle"

---

![Charlie looking at ocean with "Wow, Big Puddle"](/images/abstractions/abstractions.014.png)

And I wasn't quite sure what to say to that. 

Is the ocean a big puddle? No, of course not, that's a silly idea.

Buy why not? That's a trickier question, because I kind of get where she's coming from.

It is water, and it kind of looks like you could stomp your feet in it and splash water everywhere.

On the other hand, it's a lot bigger than other puddles.

Hmmmm.

Ok, we can figure this out. Let’s look up what a puddle is.

---

![Puddle class](/images/abstractions/abstractions.015.png)

If our brains were written in Ruby, this is what Charlie’s mental model of a puddle might look like. It’s not an actual puddle, it’s an abstracted description of a puddle that describes the what makes a puddle a puddle.

This is what a puddle is, right? To a toddler at least. It contains Water, you can splash in it, and you can cross it by walking through it. It's a Puddle.

---

![Abstract (verb): the process of taking away or removing characteristics from something in order to reduce it to a set of essential characteristics](/images/abstractions/abstractions.016.png)

What Charlie’s done here is performed the process of abstraction: to reduce something to a set of essential characteristics. She's identified the set of essential characteristics that define a puddle: Water, splash-ability, and cross-ability. This is one of the core principles of object oriented programming.

---

![Abstraction (noun): the result of this process, a named entity made up of selected attributes and behaviour specific to a particular usage of the originating entity
](/images/abstractions/abstractions.017.png)

Then we have the Abstraction, noun: the result of this process, a named entity made up of selected attributes and behaviour specific to a particular usage of the originating entity.

This is what Charlie has ended up with: with an Abstraction named "Puddle".

Then, whenever she encounters something new, Charlie will try to match it against her existing set of abstractions and see if it fits.

---

![Charlie looking at ocean](/images/abstractions/abstractions.018.png)

Does the ocean match this existing abstract description of a puddle? It’s water, sure. You can splash in it, sure. Cross it? Maybe not by walking, but yeah sure.

When all you have is a hammer, everything looks like a nail. When you only have one abstraction, there’s a kind of gravity that pushes everything you encounter towards that abstraction.

So as Charlie contemplates the ocean, there is a temptation to take her existing Puddle abstraction, and apply it here. It just needs to be extended a bit.

---

![Puddle class](/images/abstractions/abstractions.019.png)

So the existing abstraction gets extended to cover this new really big puddle. It now looks like this. 

It's now not as useful as it used to be though. The "can splash" method is no longer correct in all cases. The crossable method just returns "maybe" which isn't very helpful.

When we want to know things about this object we can call its methods to find out things. When we find that the methods cannot return useful answers in all cases this is a sign that we have overextended the existing Puddle abstraction. In our industry we would call this a leaky abstraction.

It's starting to look like this big puddle has fundamentally different characteristics to all the puddles we've seen before.

From here, we can try separating BigPuddle out into its own object.

---

![Puddle class](/images/abstractions/abstractions.020.png)

This is better, I’ve written code like this. Now we have a BigPuddle class that inherits from Puddle. The crossable? method has been overridden to accept an array of available transport methods, which is then checked against a list of supported crossing methods to determine if the BigPuddle can in fact be crossed.

If you have a ferry, you can cross it. If you just have your gumboots, you can't.

This still isn't a good solution though. The bias towards our initial abstraction is strong, we're still viewing the Ocean as BigPuddle where really it's a lot more than that.

---

![Puddle class](/images/abstractions/abstractions.021.png)

This is where Charlie will get to eventually. She'll realise that this new thing, the Ocean, is not directly related to the Puddle, even though they initially seem pretty similar. And that what unites them, is that they both behave as bodies of water.

Now we have a nested structure of abstractions, we have a Body of Water abstraction, which has a certain set of behaviours, and then we have a Puddle, which is a separate thing, but includes the same behaviours.

And then we have another abstraction, called an Ocean, which includes the behaviours and characteristics of a Body of Water, plus, some additional behaviours and characteristics that differentiate it from the basic Body of Water and also from a Puddle. This still isn't a fully formed model of water, but it's getting there.

Charlie won't get there straight away. It's hard to make that leap with only two cases to work from: puddles and oceans, she might need to encounter a River or a Pond to begin to understand the "body of water" abstraction.

---

![Lesson: There's a bias towards extending your existing abstractions, resist](/images/abstractions/abstractions.022.png)

You will feel biased towards your existing abstractions, resist. Instead:

- Find more cases, upon seeing the ocean we should aggressively seek out more cases: Lakes, rivers, waterfalls.
- If in doubt, it's better to separate things earlier rather than kludging them in to an existing abstraction

---

![Charlie looking at the ocean](/images/abstractions/abstractions.023.png)

I've really enjoyed watching Charlie for the last couple of years as she conceptualises abstractions and then chooses the correct one. Often she gets it wrong, and has to change her abstraction as she learns more about the world around her.

I'm an adult though. I know my puddles from my Oceans, I know what a pond is. I've even seen waterfalls. I've got it all figured out.

Except for when I go to work.

---

![Charlie ocean / michael office split image](/images/abstractions/abstractions.024.png)

I've worked in various industries over the years, working with money, then language learning, then fake money, then electricity and now tax. Each domain has it's own set of unique challenges, and it's own set of concepts and abstractions.

Nowadays, working with tax, I spend my days contemplating questions like: 

what are the abstractions underlying GST?

---

![GST class](/images/abstractions/abstractions.025.png)

For anyone not familiar with it, GST is a goods and services tax that we pay here in New Zealand when we buy things. This would be a pretty minimal abstraction to describe how it works: It has a rate of 15% and to calculate the amount of tax on a purchase we multiply the amount by the tax rate.

Ah, we've got some Australians here right? You've got GST too, what's the GST rate in Australia? (10%)

Ah, right, ok.

---

![GST class](/images/abstractions/abstractions.026.png)

How about this? It works right?

We've got two classes now: New Zealand GST and Australian GST. They're mostly the same, the only difference is that they have different tax rates.

We've only got two cases, so I wouldn't say we _need_ to create any abstractions just yet, but it's a good time to start thinking about it.

At this stage I like to start by consulting the vast existing knowledge of humanity. I mean, if Charlie had just consulted an encyclopaedia she would have figured out the Ocean straight away.

In this case I can figure out pretty quickly that GST is a Sales Tax. Europe has a sales taxes called VAT, America has all sorts of sales taxes. If I were European I might have called the whole thing a Value-added tax, but I'm going to go with Sales Tax as the name of my abstraction.

---

![GST class](/images/abstractions/abstractions.027.png)

So now we've centralised the definition of what a Sales Tax is and how it works. The only unique piece of information relating to New Zealand GST is the rate. If we discover other quirks relating to how GST works in New Zealand, we can add them in here later. Much tidier.

---

![Lesson: Find existing real world abstractions in your domain and use them](/images/abstractions/abstractions.028.png)

Next lesson: Always use an existing abstraction from your domain if one exists, like we did with Sales Tax.

- This will reduce the learning curve for new team members, especially those with experience with the domain
- It's less likely to turn out to be an unsuitable abstraction six months down the line because it's been in use for many years already
- And best of all. It's less work to use an existing abstraction than to try and create one.

---

![Office party](/images/abstractions/abstractions.029.png)

I often tell Charlie stories about my day, trying to find the interesting, relatable bits. And so I told her a story about an party we had once, not really a party, just office drinks but I was embellishing the story a little.

She loved the story and said "can I come to your office party", and I was like, oh no, you wouldn't like it, very boring for a three year old.

But she became quite insistent about it, and I ended up in this position of trying to convince her that she didn't really want to come to my work office drinks. It's a lot less fun than the parties that she normally goes to, she just wouldn't like it.

I used her own trick on her, and I kept asking why. Why do you want to come to the office party.

And it turns out the reason she wanted to come to the office party is because she wanted to drink orange juice.

Yes, I am a mean parent, there is no orange juice in my house, that's not the point.

---

![Bring charlie joy method](/images/abstractions/abstractions.030.png)

The point is that Charlie has developed an abstraction in her head for a party, and based on her experiences to date, a party has juice. That's a reasonable conclusion, we do have orange juice at our office.

And orange juice makes Charlie very, very happy. So in her pursuit of happiness, she used that party abstraction to demand that she be invited to a party. And the answer was no.

---

![Bring charlie joy method](/images/abstractions/abstractions.031.png)

Instead what she should have done is be more explicit with her requirements. If she didn't really care about the party and just wanted orange juice, then she should have asked for orange juice.

---

![Lesson: Be specific with your requirements](/images/abstractions/abstractions.032.png)

Be specific with your requirements. If Charlie had asked for Orange Juice she might have got it. If your ruby object needs to know something then don't try to be to clever about it, just ask for what you need. Ask for the most specific, most precise thing that you can. Don't ask for a party if you just want Juice.

---

![Walkway decorated with paintings](/images/abstractions/abstractions.033.png)

This is a walkway just down the road from our house, it's been decorated with paintings by children from the local school which is lovely. Some of these kids are quite talented.

---

![Good paintings](/images/abstractions/abstractions.034.png)

These are a couple of my favourites, probably better than I could do.

Charlie has a very particular favourite though, it's been her favourite for a couple of years now and we always stop and look at it.

It's this one.

---

![Drippy painting](/images/abstractions/abstractions.035.png)

Now I don't mean to trash talk some kids artwork, but objectively this is the worst artwork of them all.

And at first I was like, wow, my daughter has poor taste in Art. But of course, Art is subjective, and who am I to tell her that she has bad taste.

Sometimes the exact attributes that make something appealing to me: fine details, no visible brushmarks or drips, might make it unappealing to Charlie. Maybe she likes simple shapes, with visible paint drips. Is one better than the other? Who am I to say. I would never try to convince her that a different painting should be her favourite.

And that made me thing about the role taste plays in our work.

I had some examples earlier in this talk where I changed between class inheritance and including modules, both approaches worked, and achieved a result that functioned in roughly the same way.

Is one better than the other? these kinds of decisions have pros and cons, and choosing the best approach depends on the context. This kind of thing pops up all over the place, Tabs vs Spaces, Emacs vs Vim. We all have slightly different values in our tools and in our techniques, and sometimes there's not a right answer, it just comes down to a matter of personal preference, a matter of taste.

---

![Lesson: Sometimes it's just a matter of taste](/images/abstractions/abstractions.036.png)

So that was my conclusion here, sometimes it's just a matter of taste. We need to remember to acknowledge the role taste and our personal preferences play in our work. Of course sometimes we also need to come to some sense of common agreement: A codebase can't be half tabs and half spaces.

---

![Half eaten toast](/images/abstractions/abstractions.037.png)

I've always tried to teach Charlie good manners, and for a while we focused perhaps a bit too much on saying goodbye. So when someone was leaving and they said goodbye, I would encourage Charlie to say goodbye to them. 

And the way I explained this was: When our friends are leaving, we won't see them again for a while, and they might miss us, so we say "goodbye".

I can't remember exactly how I explained this to Charlie but I can't have done a very good job. A few days later I was clearing away her half-eaten breakfast, and she said "Goodbye, toast".

Now I'm not sure exactly where she'd gone wrong in her mental model here, or in my communication with her, but she's clearly gone too broad with her abstraction.

We should only say good bye to people, not food.

---

![Say goodbye method](/images/abstractions/abstractions.038.png)

This is what I was trying to communicate. If the object is leaving and it's a person, say goodbye.

---

![Say goodbye method](/images/abstractions/abstractions.039.png)

But this is how she interpreted it: If the object is leaving, say "Goodbye". She seems to be applying the "Goodbye" behaviour to any object that leaves her, be it Toast or a Person.

---

![Say goodbye method](/images/abstractions/abstractions.040.png)

Or, since she was in the kitchen when I explained this to her, perhaps she's interpreted it like this: If I'm currently in the kitchen, and an object is leaving, then say goodbye.

---

![Lesson: Clearly communicate the intent behind our abstractions](/images/abstractions/abstractions.041.png)

We need to clearly communicate the intent behind our abstractions.

Introducing a new abstraction to a child or a codebase is usually a significant change, we need to do our best to communicate clearly so that it gets used as intended.

We have tools beyond just the name of the Class. We could add comments in the code, we have tests, pull requests, we have internal wikis and knowledge bases, we can talk to our teammates in person to help establish a shared understanding. Do whatever works for your team, but just adding the code probably won't be enough.

---

![Photo of charlie's artworks](/images/abstractions/abstractions.042.png)

The very first time Charlie brought home an artwork was a really special moment. I was trying to take a photo of it and then she picked it up, held it up to her face, and sneezed into it.

This photo doesn't include that specific artwork sorry, that one went in the bin.

Somewhere in her head Charlie has an abstraction that describes what kinds of things you can use to blow your nose. I guess she thought any kind of paper is close enough to a tissue.

---

![Photo of charlie's artworks](/images/abstractions/abstractions.043.png)

Perhaps at this point Charlie didn't even have an abstraction for Art as a separate thing from Paper. There's a deeper conversation to be had here about the entire concept of what is Art which I'm not qualified to speak on so instead I learned a simple lesson.

---

![Lesson: Abstractions will be applied in unpredictable ways](/images/abstractions/abstractions.044.png)

You can't predict how an abstraction will be applied and that's ok. It probably won't be used quite as you'd imagined.

We've talked about some things we can do to mitigate this but no matter how hard we try, we'll never get it 100% correct and that's ok.

Our abstractions will evolve. That's fine. It's part of the process. It is the process. It doesn't mean we did a bad job the first time, it just means that maybe we hadn't encountered the concept of an Ocean before, and we did the best we could at the time.

---

![Lego house](/images/abstractions/abstractions.047.png)

I've always valued software architecture, getting the big decisions right, choosing the right abstractions.

Coming up with abstractions like the ones we've been talking about is a key part of the way we architect our software. These are some of the most fundamental decisions we make as software developers. Getting the architecture right can make a whole project seem like a breeze, and getting it wrong, can cause a lot of pain down the road.

So we create these abstractions and then they enter the world. 

And other developers come along and they enter the world of our codebase with only our abstractions to guide them. And then through our abstractions they learn about the world around them, they learn the business domain. 

So this process, of observing the world and creating abstractions. And then being presented with abstractions and using them to interpret the world around us. That’s fundamental to both software development and toddlers. 

But that doesn’t make it easy. We’re always working with incomplete information, with a half formed view of the world. 

I'm certainly still learning, both from my colleagues around me and from the world outside the office.

So, what have we learned.

---

![Lesson #1: Naming things is hard, avoid ambiguity & consider pre-requisite knowledge](/images/abstractions/abstractions.048.png)

Ice-cream lights are not for eating. Naming things is hard, let's try to avoid ambiguity and consider pre-requisite knowledge.

---

![Lesson #2: Resist the bias towards extending existing abstractions](/images/abstractions/abstractions.049.png)

The ocean is not a big puddle. Resist the bias towards extending existing abstractions, you don't want to end up with a leaky abstraction.

---

![Lesson #3: Find existing abstractions in the real world and use them](/images/abstractions/abstractions.050.png)

Apologies, for having to talk about tax, but a Sales Tax is a good example of a real world abstraction that we should use in our code. Don't re-invent the wheel.

---

![Lesson #4: Be specific in your requirements](/images/abstractions/abstractions.051.png)

Be specific in your requirements. If you want Orange Juice, say so. Don't try to gatecrash a party instead.

---

![Lesson #5: Sometimes it's just a matter of taste](/images/abstractions/abstractions.052.png)

Try to recognise when a decision can't be objective and acknowledge the role of personal preferences in our choices.

---

![Lesson #6: Clearly communicate the intent behind your abstractions](/images/abstractions/abstractions.053.png)

Code itself is not enough, we need to make sure our teams understand the intentions behind the abstractions we're creating, so that we say goodbye to people, and not to toast.

---

![Lesson #7: You can’t predict how an abstraction will be applied](/images/abstractions/abstractions.054.png)

At the end of the day, you can't predict how an abstraction will be applied, even if you do a fantastic job and create a beautiful piece of code, one day someone's going to come along and use it to blow their nose.

---

![Charlie at the beach](/images/abstractions/abstractions.055.png)

I’ve learned another lesson too. A more abstract lesson.

I learned that Charlie’s work isn’t all that different from mine.

She conceptualises abstractions and then chooses the correct one. Often she gets it wrong, and has to change her abstractions as she learns more about the world around her.

This isn't so different from the process I go through when I'm designing and building software. Our work has more in common that it may seem.

In many organisations I've worked in, and even at family dinners, Tech has this mystical aura, as this deep specialty that's beyond comprehension. This is how we end up being called wizards, or magicians. As if we practice some dark art that no one else can understand.

We use so many technical terms and acronyms that it's like we're speaking a different language. The divide between "Developers" and "Non-Developers" is deeper than between other specialities, or so we tell ourselves.

It's a trap I've fallen into myself in the past.

The problem with talking this way, with thinking this way, is that we obscure the common characteristics that exist between developers and designers, between developers and project managers, between developers and three year olds.

And by thinking in that way we close ourselves off from so many opportunities to learn. 

I want to come back to that quote again...

---

![In the beginners mind there are many possibilities, in the experts mind there are few](/images/abstractions/abstractions.057.png)

In the beginners mind there are many possibilities, in the experts mind there are few

By coming here today I think we've all shown some of that curiosity, that mind that's open to many possibilities.

And I think we can take that even further, to look even beyond our industry and see what common ground we can find.

If we look underneath our jargon and our acronyms

If we entertain many possibilities instead of few

And if we remember to ask Why

Then there is always something we can learn.

Even from a three year old.

---

![Thank you](/images/abstractions/abstractions.058.png)

Thanks for having me, and let's enjoy the rest of the day.