# Block with care

**A proposal and interactive proof of concept: a block button that asks first, and never stands between a person in danger and their safety.**

> One tap. Total exclusion. No questions asked.
> That is how blocking works on most social networks today.

**[Try the prototype →](https://innermost47.github.io/block-with-care/)**

---

## The problem

Blocking is one of the most powerful actions a social network offers. It silently cuts a person off, completely and instantly. Platforms hand it out with a single tap, no context and no follow-up.

The same button does two very different jobs:

- It protects someone from a stalker, a harasser or an abusive ex. This use is vital and must stay fast.
- It lets someone avoid an uncomfortable conversation, end a disagreement or exclude someone socially. The consequences for the other person are real.

The platform cannot tell these apart, so it learns nothing about either.

## The proposal

Pressing **Block** opens a short questionnaire. The questions become more specific as urgency rises, and the flow ends with a recommendation, and a report to the platform when the situation calls for one.

**Guiding principle: friction should scale inversely with danger.**

| Urgency  | Situation                                                            | What the flow does                                                                               |
| -------- | -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| Low      | "I just don't want to see their content"                             | Suggests lighter tools (mute, restrict, 30-day snooze). Block stays available.                   |
| Moderate | A real conflict, or contact that continues after being asked to stop | Block, with report offered.                                                                      |
| High     | Harassment, insults, repeated unwanted contact                       | Block and report recommended. The report is pre-filled from the answers.                         |
| Critical | "I feel unsafe" (threats, stalking, doxxing)                         | **Instant block. No further questions.** Priority report, evidence preserved, support resources. |

The critical path is the most important design constraint: no questionnaire may ever delay protection for someone in danger.

## Whose job is this?

A social network's job is to manage social conflict. If every dispute is handed to a one-tap exclusion button, the platform has outsourced its core function to its users.

Social is not an optional feature of a social network. A platform that does not want to handle it properly should say what it is: an advertising business with a friends list. A platform that does want to be a social network has to treat blocking as a serious act, handled carefully rather than taken lightly.

## What the research suggests

- **Blocking feels very different on each side.** A 2026 conference poster (N = 130, preliminary) reports relief and restored control for people who block, and confusion, rejection and lower need satisfaction for people who are blocked. [APS 2026 poster](https://www.psychologicalscience.org/conventions/archive/2026annual/paper/61996/)
- **Online ostracism threatens basic needs** (belonging, esteem, control, meaning), in all age groups. A silent block is therefore not a neutral act. [Summary of Abrams and Williams's findings](https://vulcanpost.com/10169/ignored-facebook-lowers-self-esteem-study-finds/)
- **Design "friction" has precedent in harassment prevention.** Civil-rights groups have welcomed prompts that make people stop and think as a complement to punitive moderation. [ADL statement on Instagram's 2019 changes](https://go.adl.org/node/38418)

This list is a starting point, not a literature review. Pointers to better sources (especially from clinical psychology, victimology and trust & safety research) are welcome.

## Open questions

This is a proposal to discuss, not a finished answer. These questions are deliberately left open:

1. **Should the blocked person be told?** A neutral notice might reduce confusion and the feeling of being silently erased. It might also escalate a dangerous situation. The prototype takes no position.
2. **Who sees the answers?** The questionnaire creates sensitive data. Retention, access and use limits would need to be designed with privacy experts.
3. **How are thresholds set, and by whom?** The scoring in this prototype is a placeholder. A real one needs evidence, testing across cultures, and an audit trail.
4. **Can it be gamed?** People could choose whichever answer unlocks the outcome they want. What keeps the flow robust without making it punitive?
5. **What is the platform's duty once it receives a report?** Collecting the signal only matters if someone acts on it.

## The prototype

A single static page, `index.html`, with no build step and no dependencies apart from two Google Fonts.

- **Proposed** tab: the new flow. Try the different answers; the colored rail on the side of the sheet tracks urgency.
- **Today** tab: the current experience (one confirmation, no questions), for comparison.

The wording, the scoring and the thresholds are **placeholders**. This is a flow prototype, not a validated clinical or safety tool.

### Run locally

Open `index.html` in a browser. Or serve the folder:

```bash
python3 -m http.server 8000
```

## Contributing

Feedback is the point of this repository. Useful contributions include:

- Critique of the flow, from people who have been harassed, who have been blocked, or who have moderated.
- Research pointers from psychology, HCI, victimology and trust & safety.
- Alternative flows and wording, as issues or pull requests.
- Translations of the prototype.

Open an issue to start a discussion.

## License

[MIT](LICENSE)
