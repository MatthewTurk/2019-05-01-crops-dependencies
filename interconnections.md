<!-- .slide: class="titleslide" -->

# Interconnections
<div style="height: 6.0em;"></div>
## Matthew Turk
## Crops in Silico 2.0
<p style="text-align: right;">`mjturk@illinois.edu`</p> 

---

## Development

Assertion: we all depend on the results of each other's work for our own work
to continue, in one way or another.

<p class="fragment">
Implication: we must manage our relationships in light of our dependencies.
</p>

---

## Types of Interdependence

 * Blocking
 * Asynchronous
 * Received


---

## Blocking Dependencies

Progress on Goal A cannot proceed until Goal B has been reached.

These dependencies have a tendency to produce conflicts and delays.

<div class="fragment step-fade-in-then-out" data-markdown=true>
<p>**Example:** Matt says he will have a set of data collected for Meagan so
that Meagan can progress with training a model.
</p>

<p>Here, software development has concluded, and Meagan's work cannot proceed
to the next phase until Matt has completed what he has said he would complete.
</p>
</div>

<div class="fragment step-fade-in-then-out" data-markdown=true>
<p>**Example:** Matt's visualization work requires a set of sample data to
iterate on in order to build a framework, but as soon as he gets it working,
the format of the data changes again.
</p>

<p>This one is just frustrating!  Every time something works, the rug gets
pulled out.  The informal "contract" between collaborators is not being adhered
to.
</p>
</div>

---

## Asynchronous Dependencies

Aim for this type of dependency.

Think of these as "promises" -- at a future time, this dependency will be resolved.

<div class="fragment step-fade-in-then-out" data-markdown=true>
<p>**Example:** Matt is developing a model and needs `yggdrasil` to support a new
data type before it can be integrated into a system.</p>

<p>In this case, the dependency is straightforward: Matt can continue to develop
the model, assuming that by the time it is ready, the framework will support it.</p>
</div>

<div class="fragment step-fade-in-then-out" data-markdown=true>
<p>**Example:** Stuti is developing a model and needs photosynthetic data from a model
developed by Matt in order to test whether it functions.</p>

<p>Here, we have a more complicated situation.  Development of the model *code*
can likely proceed using sample or "mock" data, but the final verification and
validation of the *results* requires Matt's model be complete.</p>
</div>

---

## Received Dependencies

These are probably the most *frustrating* type of dependency!

"OK, you have to wait for me to do this."  In some communities, you see this
when systems are rapidly in flux.  Often, an infrastructure provider is
changing underpinnings, and so the work falls necessarily on the developer
doing the implementation on top of that infrastructure provider.

<div class="fragment step-fade-in-then-out" data-markdown=true>
<p>**Example:** Matt has built his model to use a particular version of
`yggdrasil`, but during the next set of development, Meagan changes the
fundamental interface.
</p>

<p>Here, Meagan has *inserted* a dependency into Matt's work!  This one is hard, and can potentially be *mitigated* by advance planning and communication, but likely not completely *alleviated*.
</p>
</div>

---

## Development Guidelines

 * Everything in a single place
 * Communicate about goals:
   * Identify *unavoidable* direct dependencies
   * Identify *available* asynchronous dependencies
   * Identify *potential* received dependencies

---

## Conduct in Collaborations

 * Communication!
 * Assume the best <span class="fragment">(Seriously, just assume the best.)</span>
 * Push your code frequently
 * Code of Conduct

---

## Tools

 * Slack for chat
 * Github for:
   * Source code
   * Issues (questions, bugs, planning)
   * Code review
 * SmartSheet for long-term planning
