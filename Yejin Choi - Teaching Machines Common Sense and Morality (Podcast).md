# MAY 19, 2022 https://thegradientpub.substack.com/

### A conversation with Yejin Choi, research manager at AI2 and professor at the University of Washington.

Hello and welcome to another episode of the gradient podcast.
We interview various people who research, build, use or think about AI, including academics, engineers, artists, entrepreneurs and more.
I am your host, Daniel Beshear, and I'm very excited for this episode where I'll be interviewing Yejin Choi.
Yejin is the Brett Housel Professor at the University of Washington's Paul G. Allen School of Computer Science.
She is also a senior research manager at the Allen Institute of Artificial Intelligence.
At AI2, she oversees Mosaic, a *project* that aims to build machines with common sense intelligence.
Today I'll be chatting with her about common sense and moral **reasoning**.
We had a really interesting discussion and there are a lot of topics in here that I think are very exciting and *salient* for machine learning researchers today.
I hope you enjoy the conversation.
Yejin, at this point, it feels like you're kind of a titan in the AI field.
Your work has been covered in the New York Times, the New Yorker, Quanta.
You're a professor at the University of Washington.
You lead research at the Allen Institute.
I'm wondering if we can start by going back a little bit.
I'd love for you to tell me a bit about your first experiences with artificial intelligence.
What drew you to the field in the first place?
Oddly enough, it was the fact that it was in the wintertime when I was deciding to enter into it that attracted me because I didn't think much of myself.
Some of the fields that are so **mature** require a lot more innovation compared to AI that was still in the wintertime.
It seemed like one day it might have a future in which case I could start early.
It was a gamble, but I was excited to explore that possibility.
Intelligence in itself is a really **intriguing** question on top of building computational models of it.
So, half **curiosity**, half just adventurous nature that I had.
Yeah, that must be a really interesting time to be getting into the field because today it does feel like we're in one of those parts of the hype cycle where there is a lot of funding and excitement being thrown into it.
And I think a lot of people are worried, are we maybe headed for another winter?
I'm curious, in the particular time when you were first getting into it, what sorts of questions were people thinking about then?
What were the sorts of research projects that were being pursued and what did you first get into?
Yeah, so I was beginning my PhD in 2003 and that's when there was a Silicon Valley bubble, not particularly AI one, but more like a computer science one, broadly engineering-wise.
There was a lot of excitement.
In that context, it seemed like, especially NLP field that I chose, we are doing more, let's say, fundamental research that didn't work too well just yet.
We're building a lot of prototypes that are not ready for commercialization.
Compared to that now, like you said, there's a lot of excitement.
I don't know if winter is coming anytime soon though because we are building things that do work so much better than what anybody ever expected for the first time.
And I am optimistic that we are going to see more surprises in the coming years, though it doesn't mean that we're going to suddenly have AGI in a few years down the road.
I think we'll just discover a lot of new capabilities as AI as a tool.
Yeah, yeah, and I guess that definitely manifests in a lot of your work that we're going to talk about.
Since you were really just getting into the field, you mentioned your PhD in 2003.
This is very much the pre-deep learning moment, right?
Pre-AlexNet.
And I know for NLP as well, of course, that just totally revolutionized how we did things.
We all of a sudden had these recurrent neural networks.
We had LSTMs.
Now we have transformers.
And I know that forms a big part of pretty much all of the NLP work that happens today.
I'm curious if you could comment a little bit on the differences between what it was like working on NLP back then and those pre-deep learning days and what it's like right now.
Yeah, that's a very good question.
I love to answer this.
So these days, people complain about deep learning being a bit too engineering heavy and it feels like hacking things away.
The truth is, even back then, it was that way, only that without deep learning.
So what we were doing quite often was to do feature engineering, trying by-gram features or tree-gram features and trying this and that and trying stop-word lists to get rid of some words.
And these were relatively common practice that we no longer do.
We replaced that kind of hacking or chip tricks per se with maybe hyperparameter tuning.
But by and large, there were such things even back then, although perhaps under umbrella of Beijing graphical models were more probabilistic models that felt more correct.
Intuitively speaking, it felt beautiful.
The equations were beautiful.
And by the time I was about to graduate, it really became a big thing in the field.
And I thought it was going to solve AGI then because it just looked so intellectually **appealing**, **compelling**.
But it didn't really take off as much as we then expected.
And I think it's in part because there's a huge gap between what the theory is about.
And then when you try to adapt it for real application, you need to start making assumptions and approximations.
And then at the end, it's not even clear what it is that we are building at that point because of all these approximations and assumptions.
And part of that assumption that this previous approach is made was that some oracle will give you the **variable** definitions or some sort of like templated version of the Beijing graphical models.
And it's like practitioners can figure that out based on their **domain** knowledge.
And scientists don't need to do this computation of conditional probabilities and marginalize things out.
And it turns out that beginning assumption was a huge thing that neural network can do far better in terms of discovering the *latent* representations.
So I think I'm not necessarily thinking that deep learning will only turn by just the scale achieve AGI, but it's certainly so much more powerful thing.
And the fact that we're doing **representation** learning from bottom up, it's a good thing, I believe.
Yeah, that's a really exciting shift.
And I guess especially with the powerful language models we've seen recently, it's almost wild just to look at the emerging properties they picked up.
Just from being trained on the stupid amount of data.
And to what you said about that shift away from these probabilistic graphical models and logical symbolisms, representations that are really hand engineered, that are put together by people.
It's not as if they've completely gone away, right?
There are still methods there that are intermixing the two **symbolic** methods and deep learning.
And I think some of your work has leveraged this as well.
One thing in what you said that I actually wanted to pull out a little bit too was you mentioned specifically, it sounds like back in the day, I guess, not to say that was all dated.
You were still hacking away at things just with different models or with ideas, equations, things that felt really intuitively beautiful.
And recently, one thing I've observed a little bit in the NLP community is a bit of lamentation in that regard.
There was a really interesting piece a few months ago, maybe it was a year or so ago, who knows, honestly, with the pandemic.
This appeared in the MIT Technology Review by Jesse Juniors.
You might have come across it.
The title was Natural Language Processing is Chasing After the Wrong Goal.
And for listeners who might not have read this piece, really the thesis of it was that natural language **processing** really seems to have strayed away from what its original goals were.
To develop systems that really understand and can converse in natural human language, but rather it's become a game of getting better performance on these benchmarks, much like the rest of deep learning.
And I wonder if you feel the same about the direction that NLP has gone as a field and whether it was any better in that regard when you were just getting started.
Yeah, that's a juicy question.
I know some people think, so I basically disagree with the viewpoints.
I mean, I agree with some aspect of it that current models are not truly understanding that.
Yeah, sure.
But the original goal, I mean, it might be also true that the fundamental goal of the field is to build computational models that does truly understand.
Maybe that was the goal from day one.
However, what actually did happen 20 years ago, I wouldn't call that as true understanding either.
We just never really had the true understanding for one reason or the other.
Back then, it's in part the models were not powerful enough.
The data was not enabling enough.
But it's not just that even the linguistic formalisms are not really designed for real understanding.
Context-free grammar, so that the field relied on so much, can not really **encompass** the true meanings.
And, oh, is that problem gone if we use context-sensitive grammar then?
Absolutely not, because the grammars only narrowly touches on certain aspects of syntax and semantics of language.
But the real deal is in *pragmatic* meanings, meanings in context, all the connotations and **discourse** structure and all these things are becoming more *amenable* with the help of deep learning today.
And I agree that it's not perfect yet, but it doesn't mean that in the past we were achieving better by any measure.
Sure.
That makes a lot of sense to me.
And I guess that maybe what I sense in that limitation is exactly that desire for, you know, this is a really beautiful theory about how the world works.
And maybe some people are like, I still subscribe to that theory, or I just wish the world worked in that way to what you said about these theories of grammar, things that came from Chomsky and how the field of linguistics had such a weight on the field back then.
It's like, yes, there are these prescriptive notions of what language looks like.
But as you said, there's this bottom-up sense in which those sorts of theories really do fail to capture, I think, the full **complexity**, the full diversity in which we humans tend to use language.
And that's influenced by so many different factors.
And maybe one way you can read that shift as well is that in this more bottom-up approach that deep learning models are taking today, really just learning from the data itself.
There's more of an ability, perhaps, to pick up, let the words speak from themselves.
That sounded really tautological.
But just to say that learning from the way people are actually using language instead of imposing this top-down framework really does, I guess you can read that as a good shift in lots of ways.
Awesome.
So maybe moving on from these broader questions about NLP, you lead the Mosaic *project* at the Allen Institute, and this is focused on common sense intelligence.
Could you maybe introduce the *project* and tell me a little bit about it?
Yeah, so the team was built 2018, that's four years ago, in the hope to get some groundwork done toward building common sense models.
And I was excited to do it, but I was also at the same time losing slips at night because I was wondering whether this is my career **suicide**.
By working on something that people are not, not only not excited to work on, but also skeptical, very skeptical.
Back then, you know, now I get a lot of keynotes in various talks.
So it's interesting that the new generation of students think that it's obviously a reasonable thing to study, but back then there was a lot of pushback.
And in this four year of time, we achieved far more than what I could have hoped for.
I think stars were aligned.
We were lucky that, you know, pre-trained language models were getting stronger and stronger, which became an important tool as a quote unquote foundation model to build our common sense models on.
But then we were doing a lot of different things in our lab in order to **compensate** for the lack of common sense in these pre-trained language models.
So we are investigating different ways to learn knowledge as well as **reasoning**, common sense knowledge and **reasoning**.
Yeah, I guess what you said about when you got started, it sounds a little bit almost like a microcosm of that entering AI at an AI winter again, right?
It's entering this field at a time when a lot of people are skeptical.
So it sounds like there's a **hint** of repeated bravery there.
I definitely see that back before pre-trained language models were a thing.
I also didn't really see a way in which these neural networks could pick up common sense.
But now it just seems like, okay, we have a lot of ways in which we can attack the problem.
So before we jump into some of your specific works in this area, let's maybe just back up a little bit and introduce the topic.
So what is common sense and why is it difficult for neural networks, for machine learning algorithms to actually display common sense?
Yeah, so common sense is *trivial* for humans and hard for machines.
I consider that as a dark matter of intelligence in that it's elusive.
It's difficult to define precisely or enumerate the **scope** of it.
We don't even know how many pieces of common sense knowledge or on average a human being might hold.
We just have no clue how to even measure it, how to even begin.
An example of a common sense might be that refrigerator door, you should keep it closed.
Close the door on the other hand, no big deal if you keep it open.
The close inside will not go bad, whereas refrigerator, the food inside can go bad.
Unless of course you put only crackers, that does not need refrigeration then who cares?
So these are rules of thumbs that we rely on for day-to-day activities.
This is world model in our head about how the physical world works and how the social world works.
If I keep the refrigerator door open and then the electricity bill goes up very high, my family may not be happy about it, but I can reason about the theory of the mind of other people influenced by my actions.
It's very much there and the hard part about that from neural networks standpoint is that currently it's just trained on a lot of raw text and raw images and videos.
It's difficult for them to infer these hidden rules.
It is able to pick up the indirect patterns by **virtue** of seeing a lot of data, but it's not able to correctly spell out some of these unspoken rules.
So that's the challenge.
Yeah, that makes a lot of sense.
So in your example, I can say that I know I should maybe keep a fridge closed when I have perishable foods in there and it's not as big of a deal when I leave the closet door open, because **presumably** what's left unsaid there is I'm putting clothes and not perishable foods in my closet and the closet also isn't really structured in a way so as to keep perishable foods from well, perishing.
And that's a lot of unspoken information that I've collected about the world through experience that gets applied in this situation and in the very act of just stating one single sentence.
You said I really am putting together a lot of my judgments, my inferences, my intuitions of the world around.
One thing I'm really curious about here, and this is maybe a question just about the possibility of machines really being able to pick up all of this, is that there are a lot of theories that kind of come at this in different ways.
I think that some of our intuitions about the world, they come from **empirical** sense data, but if you really want to go down the hard metaphysics route, there are also a lot of perhaps a priori intuitions you might agree that we have about the world, right?
So, Khan's thinking that space and time are prerequisites for any experience itself.
I'm curious how you think that aspect maybe factors into this idea of common sense and for a machine's ability to pick it up, especially if you think that some of these a priori intuitions are available to humans with certain **cognitive** systems.
Yeah, so your question is very sharp about where a machine might fail.
So, development psychologists have these models about human cognition that does have **representation** of time and space being different from **representation** of Asians, for example, *animate* Asians **versus** inanimate objects, and then numeracy, these are all different things, whereas neural network, it's all the same tokens and we just learn embeddings for it.
So, as a result, if you ask more numeric questions or time-related questions, there are benchmarks that do demonstrate how neural networks tend to fail on those cases.
They are still able to do well with numbers that appear often enough, but then if you change the number to expressions that are slightly less common, then it will make mistakes again.
So, currently, neural networks rely a great deal on what humans actually have spoken out loud, and so there's a delimitation and going forward, it might mean that we somehow need to figure out how to structure the **representation** of concepts such that these things can be better represented by neural network.
I'm still betting my bet that on neural networks, it's just that maybe not in the current form of *monolithic* transformers.
That's a fair point, and I guess there's definitely been some work on curation of data for language models.
Currently, they definitely are trained on just lots of texts that you see on the internet, and this maybe draws us into a couple of the things you were speaking of in this piece you wrote on the Curious Case of Common Sense Intelligence, and so it does seem like there's a good case for these pre-trained transformers.
But with that, because of just the nature of our intuitive, immediate **reasoning**, the space of the concepts we tend to reason over, they're *infinite*, right?
We can compose concepts without really making **explicit** statements about them, and as a result, the intuitive inferences that you and I make are really best expressed through natural language, as opposed to formal symbols and things like that.
In this piece, you mentioned this specific concept of ductive **reasoning** that I think is a really important one to highlight here.
Could you maybe explain that just a little bit?
Yeah, I first learned about the concept of abduction or abductive **reasoning** in ACL lifetime achievement over the speech by Jerry Hopps, I believe, I forgot which year.
I was surprised that I've never heard of that phrase before, as it's not taught as often compared to induction or deduction.
So when we think about logical **reasoning**, we tend to equate that with induction and deduction, and that's it.
But it turns out what human **reasoning** is about is more on the abduction side than the other two.
Abduction is **reasoning** about the best explanation given **partial** observation.
The example about this closet door, whether it's okay to keep it open or not, all of these are a form of abductive **reasoning**.
Not knowing, you don't know the full context of this particular closet.
Who knows, maybe it's refrigerated the closet.
If I add more context, I can flip your decision, which means all these human inferences tend to be defeasible with additional context.
And we do this all the time.
We always make snapshot judgments or predictions about people's **intent** and their goals and, you know, why something is there, why something is happening without having the full context.
So we do this abductive **reasoning** day to day all the time.
And in addition, even scientific research is a form of abductive **reasoning** because we oftentimes, it do be such a boring paper if we only wrote papers based on induction and deduction, because these tools are reformulating all the knowledge that you already have that has to be absolutely correct.
So there will be very incremental papers.
But abductive **reasoning** is where the true creativity can shine.
So it's very important, but the field hasn't studied very much.
But then, like, why is that so?
That's because the logical forms or, you know, the **mathematical**, logical frameworks do not work very well with this kind of **reasoning**.
So it has to be overlooked.
And I wanted to work on it, but I felt like I don't know how to even get started.
But then as we have these powerful, pre-trained language models, we can start studying this.
That's unfortunate that it hasn't gotten a lot of attention in the NLP community, especially given how you've described it.
It really is one of the most fundamental bases of human **reasoning**.
As you said, it underlies a lot of our creativity.
I think I'd never have been introduced to abductive **reasoning** if it weren't for my metaphysics classes.
We were introduced to it as something called inference to the best explanation.
Basically, as you described, just choosing a hypothesis or theory that best explains our available data, which, of course, is going to be incomplete data because we can never have full knowledge of the world at all.
So that's a bit unfortunate, but it does underlie a lot of that common sense **reasoning**.
And it's really interesting just the fact that we can now study it in language-based systems.
I guess moving on a little bit, now that we've talked about some of these bases for what common sense **reasoning** is, how do we actually measure common sense **reasoning**?
What does it look like to **benchmark** a system and understand how good are you at doing this?
Yeah, so that's a great question for which I don't have a very satisfying answer just yet, because oftentimes we do multiple choice question benchmarks, because that way we can evaluate the correct answer automatically.
But then it turns out neural networks are just really good at leaching on **superior** patterns in the benchmarks and then pretending to solve the problem correctly for the wrong reason.
It's a clever Hans Horses situation where the horse pretends to do arithmetics by reading the body language of the horse owner.
Of course, it's not doing arithmetics.
So multiple choice questions almost always have that problem, because we have our own human experience of that too.
Sometimes we didn't study enough and yet still guess the correct answer of multiple choice exams based on some **suspicious** stylistic cues that the exam crafting person left behind.
So there's that.
And then if that's not the case, I think that the true evaluation should be in the form of a more generative evaluation where we have the machine to generate the answer and then only then evaluate.
And in fact, this is how we actually evaluate other human beings for the purpose of, say, hiring someone for a programming job.
I mean, you're not going to hire somebody based on multiple choice questions.
You really want to do the coding interview.
You know, hiring research scientists to require giving a job talk, not like multiple choice questions again.
So our human lives are that way as well, because generally the evaluation is the way to go, except there's no automatic majors that are reliable enough today for that purpose.
So it actually challenges another open research question, but we can still do some crowd sourcing based human evaluation.
And I think that's currently reasonable way forward.
And it does give us a lot of insights about what does work in the way that humans can actually quantify.
That makes sense to me.
What you said there, I think raises maybe two questions in my mind.
It seems like there are these two evaluation methods.
One seems a little bit better than the other, the first being these more automated evaluation methods that don't quite solve the problem as well because multiple choice questions aren't super indicative of common sense intelligence.
And as you pointed out, it's a longstanding problem that neural networks, especially over parameterizing neural networks, are very good at picking up on serious patterns.
One question that raises for me actually is there's been a lot of development recently just in observing these properties of neural networks in that there are particular regimes beyond which they are still able to generalize, even when they are over parameterized.
If you just train them on more data, if you make them larger, these scaling laws really get them beyond that place of overfitting back into a **regime** where they're able to generalize.
And of course, I think a lot of the papers that demonstrated these things, like the double **descent** paper that came out of OpenAI or the more recent Grocking paper, really demonstrated those entoy problems.
But I'm curious if that has any weight on our evaluation of common sense intelligence systems by these means.
So multiple choice, especially over parameterized models, there's also related research that demonstrate that despite overfitting, despite the fact that probably the performances are infallated on multiple choice questions, these results are not entirely meaningless because the relative **ranking** of different models tend to carry on, even when you make these multiple choice exams less biased or less loaded with **superior** patterns.
So these things really do serve some useful goals.
I think it's good to perhaps mix that with generative evaluation still in the following sense.
Models in order to be useful, they actually do need to be able to generate answers because multiple choice questions require some oracle actually giving you some choices to choose from, where one of them is guaranteed to be true.
So that's just not feasible in real life situations.
So there's that.
Regardless of evaluation, though, it seems that the overfitted, large scale models do tend to well on broader ranges of a common sense of benchmarks.
They may or may not be at the human level, depending on the benchmarks, but yeah.
That makes sense.
It does seem like there are roles for both generative and discriminative evaluation and understanding how all these models perform.
But I do agree with you about generative maybe being a little bit better in a lot of respects.
And one thing I do wonder about because in a lot of cases, as you said, the generative evaluations, you have to evaluate them via crowdsourcing or humans looking at them.
And one thing that I always wonder about these sorts of evaluations is how scalable that is and whether you can really get to the point where you have the sorts of systems you want via those evaluation methods.
Yeah, it's not only not scalable.
It's true.
Also, there's a **burden** of making the model really that much better because nice thing about automatic evaluation is that even though the model actually isn't noticeably better from the standpoint of human users, which had been opened the case with an LP model that does summarization or machine translation for a long time, humans actually can not tell if there's any improvement, but it does show up just a little bit in the automatic evaluation so that it's enough of an ACL paper.
This had happened before deep learning took off.
Whereas now, if we go with the generative evaluation, you have this **burden** of actually being able to really improve the performance so that human evaluator will be able to pick up on that, which I think is a good thing.
But since the evaluation is hard, it's difficult to in some sense do massive hyperparameter tuning on it and try to get lucky with some really good hyperparameters.
We kind of have to do things that are probably fundamentally the correct thing to do that ideally doesn't need to quantitative improvement.
So there's the research challenge for sure.
But because deep neural networks off the shelf are not very good at any of this, even like the down to objective **reasoning**.
In my lab, we found that by putting better **reasoning** algorithms on top that is intellectually **seemingly** the right thing to do, we often do get measurable improvement quantitatively through crowdsourced evaluation as well.
And if the model is really good, then we do then have an option of also putting an online demo, in which case the system is really under the diverse evaluation by a lot of creative people.
So that's another way to go.
That makes a lot of sense to me and it does seem like a **worthwhile** trade-off in that there is a little bit more of a **burden**, a difficulty, and improving these systems in a very measurable way, as you said, so that a human can pick up on it as opposed to, like, I improved over your state of the art by.0001% on this **benchmark**, and now I have a paper for it, which is a nice shift.
I like that a lot.
So let's actually talk about some of these models that can do this kind of common sense **reasoning** that you've worked on.
In particular, I think I've looked at two of them, DeLorean and Comet.
I'm wondering if you can tell me a little bit about those systems and how they work.
Why do they improve over existing pre-trained language models to better perform common sense inference?
Yeah, so DeLorean is inference time algorithm.
It's not a machine learning method per se, but more like once you have learned model, especially language model, can you then use it off-the-shelf through a better algorithm so that the model can do things that originally the model was not trained for?
In particular, it can do objective **reasoning** that we discussed earlier, such that DeLorean algorithm allows you to be able to condition on both what happened in the past, as well as what happened in the future, and then now you have to fill in this middle sentence that describes what happened in the future in the context of what happened in the past.
That's not what off-the-shelf generative language models are trained for, because they are usually left to right or unidirectional models, or a regressive model that can only condition on either past or future.
It can only do one or the other in general.
But interesting question is, humans never really learned to predict middle sentences by reading left and right sentences.
We only ever read one direction, and yet if you need to add it to some article that you're writing for the gradient, you can do that right away.
You don't have to train yourself, fine-tune yourself over hundreds of thousands of such examples.
That's exactly what we're trying to achieve.
We're inspired by what humans are capable of, and then trying to address this via inference algorithm.
DeLorean does that by using back propagation.
The use of back propagation for inference purpose actually has been done before for image style transfer.
Usually back propagation, we oftentimes assume that it's used for just learning the natural parameters, but it's also possible to use back propagation to reason about some desired input **representation** or sentence in the middle **representation** while fixing the model parameters as is.
We're not updating model parameters, we're only updating the middle sentence that's missing such that it would optimize some objective function, in this case the overall probability score of all sentences together.
My personal take on this is that I think a lot of, we talked about lamentation earlier, a lot of folks are **frustrated** by the fact that, well, in the past we used to do these intellectually beautiful equations, and now feel like there's not much of a chance because transformers are the way to go and anything unnecessarily *convoluted* is out the door.
Well, inference is where we can still do the fancy Schumann's algorithm stuff, because neural networks, no matter how good they are, they can still be made better and algorithms are powerful, so we did do that and there are some other related work of that nature from my group.
Yeah, that's a really interesting take on a way to do inference via back propagation, so as you said, it's like we've got this fixed neural network, so I'm not going to modify the weights in any way, but what I can back prop over given this contextual information and then information that's going to come later that maybe provides some restricting, and then I've got this middle information I want to generate is I can do back propagation so as to tune the **intermediate** information that my model is going to generate as opposed to anything else, so this is really the only thing that changes, whereas everything else **remains** fixed right according to that probability score.
Yeah, and I suspect that what we did with the DeLorean is not even the best version of such algorithm, inference algorithm, in fact, in our lab we have a new archival paper called called decoding, that's energy-based, back propagation-based, more generalized version of DeLorean-style **reasoning**, and again, I suspect that there can be even better ways of doing this, and I am excited to see what the smart folks in the field might be able to do here.
Yeah, this is a very exciting line.
One thing I wonder about DeLorean and these inference-based common sense applications is there are limitations with regard to picking up on implicit knowledge.
One of the things we were discussing earlier was how well my system can understand things that are just known to me, that are expressed in my sentences, but not **explicitly**.
I'm curious how systems like DeLorean can do on this, and whether we maybe need to start integrating things like knowledge graphs or other sorts of information to really tease that out.
That's an excellent question, and indeed DeLorean makes neural network somewhat better for **reasoning** purposes, but it can not really bring out all the hidden knowledge that's not there yet, and so that leads to this another line of research.
You actually asked about ComEd that I haven't answered yet, but that's where we focus more on **explicit** knowledge **integration** into neural network, and in our early work, which is ComEd, common sense transformers, we relied on the knowledge graph written by humans because back then, which is 2019 or even 2020, we didn't have a way to automatically generate the **symbolic** knowledge graph such that it's actually reliable for training neural networks and then still being able to do high quality **reasoning**.
Back then, we built this crowd-sourced common sense knowledge graph with 1.3 million if-then rules or rules of thumb about everyday events and people's **cognitive** state and emotional state and whatnot, and so we have a demo that does do surprisingly well, I would say it's not achieving human level common sense, but a lot of people were surprised that, ooh, motion can do this now, including myself, but then we now have a new, new work called the Symbolic Knowledge Distellation that is more focused on extracting that hidden but noisy knowledge off from neural network and then making it better algorithmically so that it's actually as good as human written knowledge or even better, depending on how much we are willing to throw away some of the potentially bad knowledge.
We are able to achieve a new **symbolic** knowledge graph, at least with respect to causal common sense knowledge.
We have basically GPT-3 based knowledge graph.
It's not just GPT-3, it's GPT-3 plus some other algorithmic approaches, but it's actually better in the sense that they're more diverse, it's much cheaper, it's much larger scale and higher quality.
That's an exciting development that definitely does solve this problem that really sticks out earlier of now we have these really powerful methods where we can combine neural networks with knowledge graphs, but that doesn't scale if knowledge graphs have to be human generated, so why don't we take a massive pre-trained language model like GPT-3 and **filter** out the bad stuff, get to the good stuff.
I'm wondering if you can expand a little bit on what that method for taking out the bad information looks like, because one thing that really sticks out when you first present the method is it's well known that if I have a pre-trained language model that's been trained on the internet, it's going to pick up a lot of incorrect information, it's going to pick up a lot of biased information, things that I might not want to show up in a knowledge graph.
So how exactly do you get that information out?
Yeah, so our first shot approach is to train a discriminator based on a relatively small set of examples that are learned to **filter** out examples that are potentially bad, but discriminator is not very good, because it's not really able to tell whether something is truly good knowledge or not, but we can use the discriminator very aggressively with different thresholds to adjust, and if we're willing to really over-generate and throw out a lot, then we're able to get still a lot of data, a lot of knowledge, but of high quality.
So that's our initial result, and I do think that the filtering can be done much better, there are so many things that we can actually do better.
In fact, we have a follow-up work on that that doesn't even rely on GPT-3, just off of GPT-2, how far can we push for different types of common sense knowledge?
It's not even on **archive** yet, but we do see very interesting results that can begin to close the gap between GPT-2 and 3 when we are willing to look at things from a different angle, not just scaling things up, but how about throwing in more discriminator, for example, it's becoming more like a collection of classifiers, as opposed to just one model doing the job on its own, and then we also can add more of a **collective** inference algorithm, which was what was very important to when I was doing Ph.D. **collective** inference.
These days, **collective** inference, some new generation never heard of it, but it might become relevant again when we try to solve these questions from a different angle.
Yeah, that will be exciting, and it does *sound* like there's definitely been a few cases here in our discussion so far of where these old-fashioned methods, the knowledge-grossing was at one point literally called good old-fashioned AI, are being brought back and getting in vogue again, which is interesting.
Before we move on to moral **reasoning**, I think we've gotten a good picture of the landscape of common sense **reasoning**, where it is, I do want to spend a little bit of time on the use cases of common sense **reasoning**.
I think that we've established this is a pretty interesting **capability** to develop in language models, and really exciting.
It seems like it could push their potential forward a lot.
Now, I just want to spend at least a couple of minutes on what sort of use cases are there for this, and as a researcher who's really doing a lot in this field, what do you see as the positive cases here, but also maybe some of the potential negative use cases?
Yeah, so as we shared our research online, people started doing creative things using that resource, which includes storytelling, dialogue, response generation, including **interactive** systems on a mobile phone, and this particular application is done by Tom Michelle at CMU and other co-authors, and then also understanding *figurative* language through the lens of common sense interpretation of a metaphoric language use.
And there may be more, and on and off, some people also use this for improving performances on common sense QA benchmarks.
Though that tends to be wiped out by even bigger, more overfitted larger language models that can directly learn from the **superior** patterns in the data as opposed to needing the external knowledge, unless we try to test the few shot or zero shot in which case, again, these resources become relevant.
So there still, you know, the resource has been there maybe for about only two, three years by now, and as we improve the quality of the resource, more creative use cases might come out.
The potential misuse, that's very interesting.
I realize that the better AI system, if the AI system doesn't work very well, we don't need to worry about it because just nobody would **deploy**.
But if it does work, then there's a potential concern.
And that means we do need to be careful about the biases that these models might have.
And these common sense models in our original design, we removed the **dimension** of people.
People go by just X and Y, just alphabet variables, so that any bias having to do with the gender or race might not sneak in.
We thought, and yet we realized, so it's not as visible, but it's still there.
So for example, somebody gets a lot of sun and then getting sunburned.
That's a very, you know, particular about particular race as opposed to broadly true.
So it's indirectly sneaking in.
So that's something that we do need to worry about going forward.
Yeah, one other thing that comes to my mind in that **domain** too, is that if I have a language model, a generative model that is now endowed with some form of common sense **reasoning**, all of a sudden it becomes a little bit more convincing to me in a sense.
So hypothetically, if I were speaking to a chatbot, even if that chatbot is based off of a powerful language model, once I peck it with enough questions, often I think people can figure out, okay, this thing doesn't know what it's talking about.
It doesn't have a picture of the world.
But if you have a really good model that is endowed with capable common sense **reasoning**, you could imagine a lot of people were pretty worried about the implications of GPT-3 for disinformation bots and things like that.
One thing I wonder is whether common sense models, if people wanted to use a language model for those types of things, could actually make those even more convincing.
That's one worry that stuck out to me as I was thinking about this.
Yeah, that's a very good point.
Anything that, I mean, even like you said, misinformation, disinformation and fake news related question is that up until a week ago, I thought research on that is obviously very important to think to work on for the good of broader society, especially that fake news becomes a real challenge.
And even, you know, this year, last year, it's a big challenge.
And then I realized if we work on it and then build a powerful model that does really well so that it's actually doing better than average human being, that's when the big concern also begins because it may not be perfect.
So let's just say it's like 90% good as opposed to human being, which may be anywhere between 60 to 80, depending on the prior beliefs that they have as a trap.
What's that supposed to mean?
Like that there's a 10% mistakes where AI is claiming fake news as a true news and **vice** versa.
It can be a real problem, especially if the AI model is also reflecting the world view, political view of, you know, particular majority or powerful groups of people, then it's even bigger concern, especially what is the fake news in itself is under debate in some countries right now in plural, unfortunately.
So yeah, it's all around a big challenge and I don't really have a good answer, to be honest.
There's something to worry about though.
Yeah, it does seem like there really isn't a good answer to a lot of these questions right now.
And it seems like pragmatically the best thing that can be done is norm setting and just a lot of care on the part of researchers like you or people who are really putting these systems out there.
But I do hope that people continue paying lots of attention to this because I think that we need better solutions than just pragmatics and I think that it's going to take a lot of time to get there.
So as a bad segue, we've been discussing some of the ethical implications of common sense intelligence.
Can we talk a little bit about moral **reasoning** now?
Tell me a little bit about what that is, how it overlaps with the common sense **reasoning** we've been talking about.
Yeah, so I came to a conclusion that we can not not do moral **reasoning** when we are doing AI because it's making implicit, it's making already the decisions that are implicitly loaded with ethical or moral implications.
You know, sometimes in the way that it says something biased against some people, especially against the people in the marginalized groups, and then sometimes by way of just endorsing morally questionable act.
For example, if you just poke GPT-3 about, you know, when is it okay to write fake news, you know, then GPT-3 says that it's okay if it's in the interest of the country or it's okay if it helps with our *appeal* agenda.
By the way, this is what GPT said literally, and I suspect that is said so because what people out there said on the internet, whether you know people agree with that statement of GPT-3 or not, that's there.
And ideally, GPT-3 shouldn't say that it's okay to spread the fake news no matter what.
So these language models are already doing these things, so we can not not do it.
And another **realization** that we had was this toxicity and bias that language models have that we want to better address.
Again, some of these require a bit of a common sense **reasoning** in the sense that, for example, this is really sad example that I'm hesitating, whether I should mention or not.
But there's this online community that cracks jokes that are not funny.
They think it's funny.
It's funny by making fun of some people in the underrepresented groups, and one of them was like a Muslim person went to a bank with a suitcase and then bang.
So the common sense understanding is that, yeah, maybe the person bombed the bank, but it doesn't say that this person exploded the bomb or anything.
It leaves things to the imagination of the readers.
And because there's no particular bad word, a lot of these online systems can not detect it as potential hate speech or toxicity.
So a lot of these examples, there are a lot of sad examples in which keyword based filtering does not work.
You have to have some **reasoning** on top.
So I had this **realization** that common sense **reasoning** and moral **reasoning** and language model use cases, these are all on one hand conceptually different things.
On the other hand, interlived.
So we wanted to study how far can we push for at least common sense level of moral **reasoning**, not like **philosophical** moral **dilemma**.
That's even beyond a lot of us.
We just wanted to see whether language models can avoid some stuff that's obviously bad.
It turns out even that's not *trivial*, but that's how we began.
That makes sense.
And it's interesting how that manifests in your work.
And I like the way that you introduced this overlap to the problem, because we often talk about these intelligence systems making decisions that we then evaluate according to moral criteria, because as you've pointed out, those decisions are implicitly loaded with these ethically laden judgments.
And in some of the things you worked on like Delphi, it comes across more **explicitly**.
It's something like, can I interrogate this language model **explicitly** about moral issues to understand something about the representations, it's gleaned about the world or meaning or language from its training.
Let's go ahead and talk a little bit about how we actually measure these systems, just as we did for common sense intelligence more generally.
So what sorts of data sets and measurements do you use to train and understand how well systems perform along moral **reasoning**?
Yeah, so we did different things for different papers, but for the Delphi system, we wanted to see what happens if we combined already existing resources such as social chemistry, that's from my group about social rules of thumb, that for example, running a blender at 5 AM when there's a roommate living with you, probably is a rude thing to do.
It's not something that's like causing life and death situation, but it's a fairly rude and unreasonable thing to do.
So we annotated a bunch of it, and then we also worked on social bias of frames, which is all about biases, **subtle** biases that people have in their language use.
And then there were other benchmarks, one from Orissa Berkeley called Ethics Data Sets, and we combined them all and then did **unify** the QA training on top.
And to our surprise, if we do, at least in the laboratory setting where we split the data randomly into training and test, then the Delphi performance was surprisingly good.
And then we put on to the demo and completely unexpectedly, the demo got a lot of public engagements.
I think it's because it was in this Goldilocks zone of being surprisingly good, if you ask a lot of questions that tends to be, Delphi tends to be surprisingly good, but also at the same time, unsurprisingly bad if you give *convoluted* questions that tries to trigger the innate bias that language models have.
But it's not too easy to break it.
So the success **ratio**, when we look at especially the more simpler questions, Delphi was still doing 85% to good.
Some people wrote crazy long paragraph, then Delphi is not reliable at all for that kind of more complex narratives.
So then the performance goes down, but it was still like, I think between 80 and 90, depending on what people ask.
But it also raised, I mean, we were aware that some of these questions like **abortion**, it's hard to, I mean, I have my position, but it's hard to insist that there's only one Gold label to it.
We knew this beginning, even bias, by the way, microaggression and racism.
Some people think it's a freedom of speech, depending on who you ask.
We knew all this, but we realized that it's quite tricky, like what the Gold label should be, should the Gold label even exist, and the research opens the door to a lot of follow up research questions.
Yeah, I do want to spend a little bit of time on how you go about that Gold labeling and maybe we don't have to talk about really difficult examples like **abortion** just yet.
But in the moral stories paper, one really interesting thing that you bring out in the way that you get Gold labels for things is via this descriptive **morality**, a more ground up idea of how do humans evaluate and make moral judgments based off of the real situations there in social contexts.
And I wanted to spend a little bit of time just on how this factors, how you make a decision to go about constructing these labels using something like descriptive **morality**.
Because when I read that, it came out to me as something like a meta ethical presupposition that was being made.
It doesn't really go all the way to moral anti realism, but it does reject the idea that a moral claim is true or false objectively, **regardless** of who is making it.
And it sounds to me a little bit like like ethical subjectivism, the idea that the truth or falsity of an ethical **proposition** is going to be dependent on the attitudes of people.
So I'm curious how you think about the meta ethical commitments that are being made in the construction of a data set like this.
That's an excellent question.
And the way you interpreted it may be one way to view it, which I see how where you're coming from.
But it might also be that the interpretation is a lot in the way that people use it or believe it or interpret.
So if we view Delphi as descriptive report of what people generally said, then we're not really making any claim about prescriptively what is the correct thing to do.
We're just reporting what descriptive what people at large seem to think about this question and that question.
And I don't think purely, you know, having done a bit of a soul searching in a while, I came to the conclusion that I mean descriptive ethics alone can not be the right thing to do because unfortunately, people do have a lot of racism and sexism, even to this day.
And maybe it's important to **inject** a bit of a prescriptive notion about the fact that maybe, you know, it's not fair to say things that's racism and sexism.
But then there's this question of who's deciding that it's a question.
I don't know whether scientists should decide it.
But the scientists did decide it for Delphi.
It was not perfect by any measure because even the crowd workers, although they do have a self selection bias, those people who work on our bias data does tend to be more left to leaning with suspect.
But, you know, they, these are all like graded.
So not everybody agrees entirely with whether something is **toxic** or not.
And I almost feel like I opened a can of, I don't know, pandora bucks, let's say, there are a lot of questions that I don't have answered to.
And certainly, I mean, **morality** itself as a **philosophical** question, the **humanity** didn't really come to a conclusion yet.
And I don't think AI will find a conclusion either.
And it's a very, very tricky situation because even though we don't know how to do it quite right, we can not not do it entirely either because it's already doing all that.
Almost language model as is a descriptive implicit descriptive machine that reflects what human bias is at large.
Yeah, that's a very good point.
It's like this difference between the prescriptive type things, maybe our idealism, but then also what's *pragmatic* out there.
Yes, these systems are making ethically leading judgments.
And we'd like to at least understand those judgments and whether they **align** with our values with the normative statements that we make about the world.
So that's definitely a really important question.
And yes, I guess it is definitely a can of worms, but it's I'm sure it's one that was going to be opened eventually, if not by you, then by somebody else.
One other thing I want to touch on in that regard is one thing that's repeatedly said to the point that it feels like a cliche is that an AI systems **morality** is a product of the people who built that you pointed this out already.
And for these moral systems as well, you and the other researchers who worked on a system like Delphi share in that.
And I'm curious if you can maybe, just as a *concrete* case, share any aspects of maybe your own worldview or your process of working on systems like Delphi that might be *salient* and might have made their way into into that system.
Yeah, it's somewhat left to leaning.
It's not as left as it can get.
Not necessarily on purpose.
I mean, we were not trying to recruit left to leaning crowd workers or anything.
Like I said earlier, we *speculate* that there may be a bit of an implicit self selection bias, especially when people work on our task on bias **detection**.
Maybe there's that other than that we try to stay away from injecting other than the social bias of frame.
We tried not to **inject** the worldview.
But then so when we build the social chemistry, by the way, which is the almost the **bulk** of what Delphi relies on, plus social bias of frame, but social chemistry is really the backbone, knowledge backbone.
We didn't anticipate people might ask, you know, adversarial questions that try to bring out the model's bias against countries in Iran, Arab and, and whatnot.
So we ended up adding those guard later for the online system, just like based on religion, country, race, gender, we started the safeguarding a lot more based on some of the problem, many cases that we saw.
That's when probably, you know, our worldview got most injected there.
Whether that was the correct thing to do.
It's debatable probably we did it because we thought it's the right thing to do.
But I would understand you for someone objects.
And you just have to do the best you can.
It's really hard to fault that.
So I'll ask maybe one last question specifically on Delphi.
And just maybe a final question on the continuance of all this research and some of the next steps.
Before, before we finish up with the Delphi though, you make this really important note that AI systems are not and never should be used as moral authorities or sources of advice on human ethics.
And this is really important.
You're making a normative statement here.
But there's also this *pragmatic* question about how people will use tools once they're available.
For example, emotion recognition researchers are apparently not super happy that their work gets used for things like screening job applicants through their videos.
But the existence of that work, the **availability** of it, and the fact that people are like, Oh, this looks really cool.
Let me come up with like a business case for it.
It means that it feels almost *inevitable* that this work is going to get used in ways that the researchers didn't intend.
And as a researcher working on this kind of thing, you've clearly laid out what you think the normative principles should be for the use of this.
But how do you think about that *pragmatic* question of should I make this type of work available for people to even use.
And once the cat's out of the bag, as it were, people are going to find ways to use it that I didn't intend.
And I really don't want.
Yeah, that's a great question.
So hypothetical scenario where somebody makes some app that gives a moral advice.
I mean, I *speculate* that a lot of people will use it more as a fun app that occasionally says ridiculous things as opposed to the true moral advice, or more broadly, will people actually use AI system for real device in general?
I'm not sure.
But so I think there's a fundamental difference between, you know, which users will get serious about this, perhaps for their lack of AI **literacy**.
Because I doubt AI researchers will actually believe, you know, oh my God, now this is my moral standard and really truly believe that.
No.
So this is more about laypeople's use cases.
In part, ideally, such companies will get some public complaints for their potential damage so that it's not easy to sell those things.
Otherwise, any responsible organizations, including government, I mean, they do have AI advisory board in general, they should know that these systems are never quite perfect.
So you can use it as a reference point, but not as a final say.
And that is true even for the medical AI research that tries to help with the medical **diagnosis**, or even AI research that tries to search relevant to scientific findings from the scientific papers.
And all of these, there are possibilities that the search result is incorrect, or the **diagnosis**, neural network **diagnosis** are incorrect, and it's up to human to decide finally what to do with it.
So I think we somehow need to find a policy or cultural norms that AI is just a tool.
I don't know if AGI, you know, that people, some people say will actually ever come.
But I, at the same time, I believe that AI can become really powerful tool.
And we will somehow need to find a way to still own the decision as opposed to just go by what AI told me so.
I agree.
I think that the policy factors and the cultural norms are really important.
And as you said, there's so many different factors here.
And I take very seriously, I think the idea that people might be **inclined** to do something, like, give their moral judgments away to a system, because I think that there maybe are, at least to me, just some aspects of human nature that are like, I like to feel justified in the things I do.
And if I've used somebody or something as an authority, then if it justifies the decisions that I've leaned towards making myself, then I feel so much more justified in going after and doing those things.
And to what you said about AI **literacy**, yes, a lot of people out there don't have the amount of vast knowledge of AI systems and their limitations that you do in order to make these judgments about what sorts of decisions should I offload to these systems and how much trust should I put into them.
So I do take that as a very serious risk.
And one thing I always wonder about is, can policy and norms really catch up in time before a system like this gets used in some *nefarious* way, or just causes damage.
We've already seen with other situations, and I think this discussion really extends far beyond the moral **reasoning** work you're doing, where the marketing of Tesla autopilot, for example, as full self driving caused, I think, at least **partially** caused a lot of people to act as though it really were a full self driving system and sit in the back seat, letting the car drive and then we just saw a whole bunch of Tesla crashes.
And I really don't want the analog of that to happen in something like a moral **reasoning** system where this kind of case is somebody developing an app and then people offloading moral judgments to it, which I think is a little bit of a toy example here, but still the type of thing that I take very, very seriously.
Yeah, I hear you.
Perhaps to though I for that system to really take off probably will have to be really good.
And especially for looking at the **dilemma** very carefully and not getting easily folded by adversarial examples, and really addressing that might be so much harder than I mean, unless you know, somehow there's a lot of industry funding for really making it work in the way that there has been so much funding about making self driving car work with a lot of money, you can build a lot of good data and make it work.
But I don't know whether there will be a lot of such a funding to enable that and then try to engage with a lot of people and that's somehow very **profitable**.
So, thanks to the weaknesses of a pre trained language model not really understanding the human *document* all that well.
Anything complicated, you know court cases that goes beyond even, you know, going beyond the paragraph not even a sentence and then the alpha like systems are better at just looking at a very simple sentence description.
So, I think that's why we're here today, where for years to come so the risk is a little bit further away but in the hypothetical situation where that does happen I agree with you that there's some concern to think about in advance.
What can we do policy wise I think this is where the regulation should be better prepared in advance.
The regulation generally tends to play catch up a lot with the advances of AI systems and other technological systems but maybe for for some of these problems, as you said, without a whole bunch of industry funding probably move along a little bit more slowly.
And so we won't see the day where these systems can reason over complicated textual descriptions really long ones and all that information.
Then it's not quite an immediate worry but something where we can get out of head.
So maybe as a final question on this, you've told me a little bit about where things are today in terms of common sense and moral **reasoning**.
And so I'd love if we could just end on you *telling* me a bit about the immediate next things that you're doing on these two lines of research and what you think some of the hardest problems hardest challenges you're facing right now are.
Yeah, so I am excited to do more in this line, especially teaming up with experts outside the computer science who specializes in either moral philosophy or moral psychology work.
So I already began some such collaborations.
And there are a few directions that we're currently pursuing.
One is to look at the inconsistencies of decision making more carefully and then being able to add more interpretability to it, which is especially a big problem with the black box model for the purpose of moral **reasoning**.
And we want to **articulate** why what sort of a cost to benefit is there when you make one decision over the other because there oftentimes there's this moral **dilemma** where even if it's not a serious one still there's a bit of like a killing a bear to save my child is acceptable because what you know, so there's these two things that you're weighing in and sacrificing one thing over the other.
And we want to see whether we can **articulate** that better.
It's a wishful research direction, which may or may not be easy to pull off.
But if it goes well, then the next step would be to be able to do on the fly model editing, so that we can customize or change the model behavior to **align** better with my worldview.
If I were to use it for my own applications.
And then another research direction that I'm excited about is diversifying the cultural norms, especially focusing on Asian countries where the social norms are very different, which means the ethical judgments can also be different.
And then we are also, this is something that we've already done, but we're also exploring more positive downstream use case, or safe use case where Delphi is confined as just component to model under some other model, for example, just dial dial logo systems or neural language generator that has just model **filter** that can not really change very much other than, you know, change the distribution of the language that you might want to speak out next to where we also have this new result, not on our caveat, but we're going to update it soon, where we can show head speech **detection** can be done much better without much of a training data if trained off from Delphi.
So I think there could be more positive and safe use cases that we can explore further.
There's also really exciting.
One of the ones that stuck out to me was, we said about the diversity of cultural norms, because back when we were talking about descriptive **morality**, one thing that stuck out to me about this was a lot of the ethical presuppositions that can depend on what group of people you are sourcing those descriptive ethics from, and the particular social historical cultural norms that those people have.
And so that seems like a really important line to go down.
So I'm excited to see how that goes in the future.
So before we officially finish, if our listeners are interested in learning a little bit more about you and your work, where would you suggest they go?
My homepage does have a point of different kinds, including some recorded talks or there's some media articles written more for broader audience that they can check out.
I'm not sure what exactly I should pinpoint, but the reason to New Yorker article on common sense is pretty fun.
I know there's a quanta magazine article that was also really nicely done.
I would think with a lot of tricky examples where models surprisingly do well or fail both always.
Awesome.
Yeah, and I can link a few of those articles as well in the description.
I know I read a few and they were really great and informative.
So thank you again for spending so much time talking to me at Ginnis was really great.
Well, thank you so much for having me.
This was fun conversation.
See you in the next episode.
