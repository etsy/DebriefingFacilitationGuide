# Introduction

> “The purpose of an investigation is to understand how things usually
> go right as a basis for explaining how things occasionally go wrong.”
>
> — Erik Hollnagel, Safety-I and Safety-II

Most traditional accident investigations tend to focus on discovering things
around an event that never actually happened. In an attempt to prevent future
accidents, there is an underlying assumption (Shorrock, 2014) for this
somewhat peculiar emphasis, which is:

> Someone did not do something they should have, according to someone else.

Through this lens, what generally surfaces in investigations are “findings”
about what people did not do (pay attention, make the right decision, etc.)
rather than what they actually did. Without anyone really noticing, these
items get labeled as “human error” and through a seductive and convenient
contortion of logic, an event that never actually happened is deemed after the
fact as the “cause” of the accident. Perhaps unsurprisingly, this results in
an obvious recommendation for the future:

> “Next time, do what you should.”

Unfortunately, this approach does not result in the safer and improved future
we want. The perspective now known as the “New View” on accidents and mistakes
flips this thinking around, providing a different path to improvement and
learning (Dekker, 2002). We wholeheartedly believe in this approach at Etsy.
We’ve invested in operationalizing it on an organizational level (Allspaw,
2012) and have shared our perspective publicly:

> “Adaptability and learning. We learn through honest, blameless reflection on
> lessons and surprises. We believe that traditional rootcause analysis makes
> learning from mistakes difficult. Our blameless post-mortem process is a
> widely-cited technique that we believe is becoming best practice among
> organizations that value innovation.  Blameless postmortems drive a
> significant percentage of our development as we analyze what about our
> production environment was less than optimal and rapidly make corresponding
> adjustments.”
>
> (Etsy, Inc., 2015)

How a postmortem[1][] debriefing (hereafter “debriefing”) is done (in whatever
form it takes) is at the core of the approach, and therefore hinges on the
expertise of the debriefing facilitator. Over the years, we have developed an
internal course at Etsy focused on building a strong bench of debriefing
facilitators. At the time of writing, this course is comprised of:

- Three seminars covering the theoretical and empirical foundations of
  accident models, historical case studies, topics of “Just Culture” and
  Safety-I/II (with readings and written exercises)
- An interactive workshop for facilitators to practice core skills
- Shadowing and feedback for new facilitators
- Regular follow-up discussion groups

This guide is intended to be a lightweight set of techniques and tactics
distilled from the full course, designed to help facilitators develop and
sharpen their debriefing facilitation skills.



1 Postmortem in this sense could be seen as an ‘after-action review’ or
‘incident review.’ The term is unfortunately inaccurate and confusing across
domains (such as medicine), but is nevertheless part of the software domain
lexicon at the current time.

## What Brought Us to Write This
Modern businesses critically rely on software, and that reliance will continue
to grow more critical.  This is not a revelation. We believe, along with a
growing number of organizations, that the current and prevailing paradigm of
accident investigation in software-rich environments is fundamentally flawed,
confused, and dangerous in the long term.

In Etsy’s corner of Internet commerce and marketplaces, we believe we can
contribute to an emerging dialogue about what “safety” is really made of: the
presence of people’s expertise, not simply the absence of accidents.

We first began practicing and developing expertise in facilitating debriefs
within the Engineering group at Etsy. Over the years, as we have evolved our
understanding of this work and its value, the greater organization (beyond the
technical side) became interested in this new source of learning.  As a
result, we have adapted what was originally custom-made for an engineering
audience to be a more generalized and accessible set of materials. We think
this has been successful; to date, more non-engineers than engineers have
taken the course at Etsy, and some of the most insightful debriefings have
been facilitated by non-engineers.

After four years of developing and evolving the internal course, we considered
that other organizations might benefit from what we’ve put together. While we
have attempted to make the material as generalizable as possible, we do
acknowledge that it has been developed on the job and we are a company that
operates an online business, which influences what we have produced here.
Nevertheless, we very much hope that other organizations (online and offline)
find it useful.

## Who This Guide Is for
This guide is intended to serve as a starting point for debriefing
facilitators in organizations that rely on the successful design and operation
of software. It has been written with the assumption that multiple
non-technical stakeholders are involved in the dialogue around understanding
and improving the use of tools, processes, and practices in the organization.

### Influences and Inspiration
As the original Code As Craft blog post (Allspaw, 2012) reveals, we have come
to these ideas, concepts, practices, and techniques through the expertise and
assets of the psychology, cognitive systems engineering, and safety science
communities. The text that we use in the internal course is *The Field Guide to
Understanding Human Error* by Sidney Dekker. We reference a number of passages
in these texts as well:

- *Behind Human Error*, by David Woods, Sidney Dekker, Richard Cook, Leila
  Johannesen, and Nadine Sarter
- *Pre-Accident Investigations: An Introduction to Organizational Safety*, by
  Todd Conklin
- *Safety Differently*, by Sidney Dekker
- *Engineering a Safer World*, by Nancy Leveson
- *Safety-I and Safety-II: The Past and Future of Safety Management*, by Erik
  Hollnagel
- *Normal Accidents: Living with High-Risk Technologies*, by Charles Perrow
- *The Challenger Launch Decision*, by Diane Vaughan
- *Working Minds: A Practitioner’s Guide to Cognitive Task Analysis*, by Beth
  Crandall, Gary Klein, and Robert Hoffman

Many of the techniques and approaches to interviewing and debriefing
facilitation in this guide can be seen as a specific translation of the
*Critical Decision Method*, which is a cognitive task analysis method designed
to draw out how people make decisions; how they pick up and understand cues in
their environments; and how they judge whether their actions are likely to be
fruitful or not. Essentially, it’s a semi-structured interview approach using
targeted questions, focusing on decision making and cognition with people
trying to solve problems. Scenarios are broken down into critical junctures,
and we ask questions about those. Developed by Gary Klein and his colleagues
in the late 1980s, we have found it to be an invaluable foundation for
facilitators when they approach a debriefing.

## Why We Focus on Facilitation Skills

### Because there are stories to uncover
A key idea in the ‘New View’ perspective is that people do (notice, pay
attention, act on, solve, etc.) what makes sense to them at the time, given
their experience and familiarity with their tools, and their understanding of
the current situation.

The facilitator’s job is not to discover the things that people *didn't* do, but
what they actually *did*, and how they perceived their world at that time.

Productive debriefing facilitation is about getting people to tell their
stories. A facilitator does this by asking pointed, open-ended questions that
help to draw out descriptive details from people that they might not otherwise
say out loud. The debriefing exists to hear (and ask about) people’s
*descriptions*, not their *explanations*.

In other words: As facilitators, we are not looking for causes.

Finding cause is easy, and we don’t need a group interview to find it. In
contrast, finding all the things people actively do to keep the system running
effectively is quite difficult, so an accident provides a unique opportunity
for these underlying factors to be revealed.

### Because each story is essential
Like the parable of the blind men and the elephant (see below), there is no
singular, omniscient perspective on an event involving work in complex
systems. There are only multiple perspectives, sometimes overlapping and
sometimes not.

> #### The parable of the blind men and the elephant
> Six blind men were asked to determine what an elephant looked like by feeling
> different parts of the elephant’s body. The blind man who feels a leg says the
> elephant is like a pillar; the one who feels the tail says the elephant is
> like a rope; the one who feels the trunk says the elephant is like a tree
> branch; the one who feels the ear says the elephant is like a hand fan; the
> one who feels the belly says the elephant is like a wall; and the one who
> feels the tusk says the elephant is like a solid pipe.
>
> None of them is wrong, but at the same time, none of the descriptions alone
> are sufficient to describe an elephant holistically.

For example: In an outage or otherwise surprising scenario, it’s clear that a
network engineer will likely have a different view of the event than an
engineer familiar with the application code, a database engineer, a customer
support agent, a product manager, a security engineer…the list could go on.
The facilitator’s challenge is to gather these diverse perspectives and
construct an aggregate narrative of how an event unfolded.

That being said, our goal as facilitators is not to consolidate different
accounts into a unified story of cause and effect.

It’s very tempting (and quite easy) to take the perspectives that people
provide in a debriefing to create a singular, omniscient, and comprehensive
view of the accident, which we can (from our comfortable and hindsight-driven
seats) use to reveal precisely where people went wrong. However, even if such
an account could be constructed, it would be an inherently inaccurate
reflection of the complex realities in which the people existed at the time,
and will continue to find themselves in as work continues and new incidents
take place.

As facilitators, we are not looking to somehow merge these multiple
perspectives into a single story.  Quite the contrary—the value in gathering
multiple narratives is to ask questions that shed light on the contrasting and
complementing parts of the different accounts shared in the debriefing.

### Because everyone truly is an expert
When we ask people for descriptions of their work, we hear about their
expertise. We hear about the tips and tricks they’ve developed over their
careers, like the shortcut shell aliases, special bookmarks, one-liner
scripts, and the go-to graphs they always look at when diagnosing certain
problems.

We hear about the procedures they always follow, and the ones they sometimes
skip because if they followed them blindly and to the letter they’d have a bad
day, guaranteed. We hear about what they usually do when that alert goes off
and everything is fine again. When “this” and “that” happens, they do “these
things,” but only in certain circumstances. We coax out the hidden nuances
underlying their actions, decisions, and rationales.

A debriefing is where you learn how the mechanic can just lift the hood of the
car, listen to that faint hum of the engine, and intuit that it needs new
valves.

A debriefing is where you discover what makes people’s work difficult, and
what makes them good at it, despite the difficulty.

## The Benefit to Others: Vicarious Experiences
Expertise develops in large part from having a diverse knowledge-base to lean
on when trying to solve problems under time pressure (such as diagnosing and
resolving an outage). In our domain, this means that part of getting good at
handling incidents that have a high degree of uncertainty depends largely on
how many different types of incidents you’ve been exposed to in your career.

One way to accelerate or augment training is through what Gary Klein and
Robert Hoffman called “vicarious experiences”—the shared and explored stories
of perspectives (Klein, G. & Hoffman, 1993).  When we’re facilitating a
debriefing, one of the primary benefits is the emergence of these “thick”
descriptions, which provide a rich source of learning for others in the
company, and can help fill a gap in their training that can’t otherwise be
filled.

We know this to be true, as “war stories” told at conferences or in the
hallways of successful companies are always very compelling. The sharing of
these stories is critically important, and we tend to remember them quite
well.

What Klein and Hoffman (and others) strongly suggest is that these
descriptions in and of themselves can serve as training materials for staff,
which means that debriefing documents should be made available, searchable,
and shareable.

The question then becomes: How does a facilitator get good at eliciting these
descriptions?

> The Goal Is to Learn, Not to Produce Remediation Items “The problem comes
> when the pressure to fix outweighs the pressure to learn.”
>
> —Todd Conklin, Pre-Accident Investigations

When we ask software engineers to think about how to make their environments
“safer”, we cannot be surprised that their response is to adapt existing
software, or build new software.

In some cases, this can indeed help, but employees should capture the
rationale for it and validate when it’s a constructive thing to do, while
being open to the idea that it might not be.

Our experience at Etsy is that identifying new tools (or modifying existing
ones) to “fill in the gaps” is one of the many outcomes from a debriefing, and
perhaps not always the most important one.

In particular, it’s important to be wary of the “dashboard trap”, where the
outcome of your debriefing simply adds another graph to an ever-increasing
number of graphs on yet another dashboard someone needs to check before they
can feel confident about taking an action, like pushing code. The introduction
of more input on a dashboard will ultimately make it difficult for people to
discern signal from noise (making their jobs harder), so this is an example of
a superficial solution. If you find yourself falling into the dashboard trap,
take it as a sign that now’s the time to dig deeper.

The goal of a debriefing is not to produce recommendations or remediation
items. Yes, you read that right. As we mentioned before, the goal is not to
find the cause of an accident. The goal is to seize the opportunity for an
organization to learn as much as they can, in a relatively short period of
time, about how people normally perceive and perform their work. Because the
people involved were doing their normal work on a normal day when the event in
question happened.

To reach these learnings we ask questions that allow us to understand the
myriad ways the organization prevents this sort of event from happening all
the time, not by asking what made the event happen this one time. That
prevention is taking place, even if we’re not aware of it. But we should be.
