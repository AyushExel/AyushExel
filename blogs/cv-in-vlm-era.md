# Re-thinking modern AI frameworks in context of LLMs and VLMs

..particularly CV frameworks

## What we know
Pre-LLM era CV algorithms, both non-parameteric and DNN-based, are great at doing certain tasks **quickly** and **in parallel** with a decent degree of competence. 

Let's unpack that a bit because it can be confusing. Isn't it the default expection that neural net based CV algorithms are better than human vision at some specialised tasks
like detection and tracking? It might appear so, but let's look at it from a different approach.

## Object Detection
![images](https://github.com/user-attachments/assets/83cda04d-13a0-4add-8c0f-a04d2a696abc)

Let's take object detection for example. Saying that a realtime CV model will surpass adult human vision intelligence in detecting and labelling objects correctly on a stream
of such video would be incorrect. With sufficiently large attention span, and no limitations on time, a human would almost always beat SOTA vision models. 

### Human contextual intelligence vs CV algorithms
It is because humans work with **contextual understanding** and (most) CV algorithms simply work on frames independently. Although sometimes there is an attempt to capture
history via parameters in case of tracking algorithms, it is still nowhere close to contextual understanding of humans. 

### Skill issue
But humans are slow as they **can't vectorize** their thinking to parallelize it. So, let's say in the given stream from which the above pic is taken, a human will be able to
recognise and detect one object at a time. A tiring and time-taking process. A deep learning model on the other hand, can simply parallelize the detection process and 
accelerate it to be orders of magnitude faster than humans.

### So, what do we know about AI algorithms
![9aoe3k](https://github.com/user-attachments/assets/3d5a0319-de7d-4d84-bfa9-67c8af853d44)

There are a few universal truths in AI. 2 of them are relevant here:
- On the extreme left, we have human intelligence that is very capable but comparitively slow
- One the extreme right, we have DL models that are very fast but not as capable.

## Enter VLMs
VLMs represent a new paradigm of compuing altogether, multimodal contextual understanding. Let's unpack again - having contextual memory either in form of prompting or in
retreival augmented fashion (VectorDBs), can allow LLMs and VLMs to be temporal in nature by default. Which means vision models can go from treating one image frame as the
smallest individual processable unit to videos as a smallest processable unit. 
This'll solve many problems in the existing CV pipelines, but we're still in very early days. Most VLMs are not video native and performance wise nowhere close to replacing
existing CV models. But there models are still very promisingand can be used to augment existing CV systems.

Today's VLMs lie somewhere in the middle of humans and DNN-based CV models. They're faster than humans and a lot more intelligent than the standalone frame-based CV algorithms.

### Contextual information is a superpower, even at frame level
One of the most challenging CV tasks is object tracking. And the most challengeing subset of problem in realtime object tracking is dealing with occlusion. In short, 
occlusion is when an object being tracker dissappears behind another object and re-apprears again after a few frames. This make consistent re-id difficult and most models 
struggle with this.

### Enter VLMs
Before we get into architectural analogies, let's understand some assumptions that we'll make regarding VLMs for the sake of simplicity. VLMs are multimodal LLMs, and like LLMs,
they are kind of a world model. This means that a sufficiently powerful VLM trained on a sufficiently large corpus, can be assumed to have a general understaning of the world.
This makes them excellent retreivers as they can represent objects pretty well in their embedding space. Here, I'm making a case that a VLM that exceeds a certain threshold of 
performance on a multi-modal benchmark, can be assumed to have a human-level multimodal world understanding. Now, obviously this isn't true, but this assumption has to be made
when using a VLM for downstream task (like in this case) and has to be rejected when pre-training a VLM itself for beating those benchmarks.

Okay if you're convinced by the above argument, then we've established that we can use VLMs analogous to human feedback (not RLHF but yes, its same direction). We can now
create powerful CV architecutres augmented by VLMs

### Back to downstream tasks
Okay let's get back to tracking. 

---------[TBC]----------------


