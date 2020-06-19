<h1 align="center">Skore Development Process</h1>

<h5 align="center">Nothing here is carved in stone</h5>

## I. Epic

Epic project is presentend to team by PO's showing it's value to skore,
this discussion is time-free can be done in an hour as in three days whatever it takes,
the goal of it is explain what the project and have a clear understanding by POs and Devs the value of it as it challenges.

From this discussions spikes and poc can emerge to validate some ideas.

This meeting is the place that some cards born, not all, but a good amount of it.

With all discussions collected by POs the cards can be created with some criterias.

## II. Cards

Cards are not prescriptives, here some suggestions:
  - Good portuguese (always respecting ubiquituous language **everybody using the same terms across areas**);
  - Necessity of this card;
  - Value that this card brings to Skore;
  - Acceptance criteria (whice **role** can validate and **how** to do it).
  
## III. Boards

We suggest 5 lanes:

  - TODO: Tasks to be done in this sprint (**implies that team is commited to deliver it**)
  - Doing: Tasks that are in progress (**No one can be in 2 cards at the same time in this lane**)
  - Code Review: Your pull request is opened and attached to card (can be *n* pr's)
  - QA: ...
  - Done: Card which has (#QA) comment by roles defined on acceptance criteria can be here

<h2 align="center">Cerimonies</h2>

## I. Planning

The idea of this cerimony is define the development team **commitment** for sprint. All cards proposed by PO will be here
according to cards guideline, to be discussed, refined/improved if necessary, and in some cases denied by the team.

## II. Daily meeting

Keep it simple (same time, same place, time box):

  - What I did yesterday;
  - What I'm gonna do today;
  - Anything is blocking me;

<h2 align="center">Other Resources</h2>

## RFC (request for comments)

Sometimes We're planning to do some substantial changes or create new features for our architecture/product,
for this situations is good collect ideas and document discussions with team.

Inspired in [Vuejs RFCs](https://github.com/vuejs/rfcs) we suggest you to create a RFC describing your change and open a PR to discuss with team.

This PR should have ~24h life time.

Take a look at our [RFCs repository](https://github.com/skore-io/rfc)

## Contributing

This document **must be** alive and reflect our day to day processes, and it's responsibility of everyone make sure that
what is written here reflects our reality
