---
tags: paper
date: 2026-07-15
---
Good and bad examples for causal coding: around fifty hand-coded examples, simple and controversial, from three publishable cases. Sister paper to [[! Evaluating AI causal coding -- prompts, models and the metrics that lied ((prompt-eval))]].

# Good and bad examples for causal coding

Not a gold standard: another coder could produce different but valid links, so no fixed list can score a coding. What examples CAN do: teach the doctrine, seed judge calibration, and mark known traps. The working metric stays n(ok links) and n(not ok links), judged per link against the text.

Format: verbatim quote, then the coding on its own line(s), then any commentary on a separate line. A package is shown as its member links in full, with the connective (AND / OR / DESPITE) on its own line between them; a DESPITE package has the successful link first and the failed one second, so it reads "A despite B". Quotes here carry only the material for the example's claim, so they do not suggest extra links; in real coding, longer quotes are fine. Layers needed are `[core]` unless marked. CONTROVERSIAL = reasonable coders differ; the commentary says what is and is not acceptable. `nothing` = a correct coder codes no link here. Never include this file in a prompt under test.

Cases:

- **M**: app project `example-original`, source MNX-1 (QuIP-style household interview).
- **N**: `notes-on-nursing-excerpt-ch-i-ii-ventilation-and-health-of-houses` (Nightingale 1859, public domain, Gutenberg #12439).
- **G**: published Garden examples (papers 005 minimalist, 015 combining-opposites) plus house doctrine.
- **H**: agents4qual loneliness corpus, Participant 19 (male, 19, Hackney); also the harness's third test text.

## M: household interview

**M1** "We changed our behaviours because we learned from Organisation 1 that the way one behaves contributes to a health status."
`Organisation 1 taught us how behaviour affects health --> We changed our hygiene behaviours`

**M2** "Our churches prohibited us from visiting the hospital and as a result five of my children are dead."
`Our churches prohibited us from visiting the hospital --> Five of my children died`
(or a two-step chain via not taking children to hospital)

**M3** "we go to church as we are prohibited of going to the hospital because of cultural issues, and beliefs ... and also going to the hospital takes longer time to be assisted."
`Cultural issues and beliefs --> We go to church instead of the hospital`
OR
`Long waiting times at the hospital --> We go to church instead of the hospital`
Two alternative or merely contributory reasons in a package, because mentioned in the same breath.

**M4** [+opposites +despite] CONTROVERSIAL "but we still do get sick even though we make use of mosquito nets."
`We use mosquito nets --> ~We get sick` failure=1
Core-only: no link. Coding `nets --> sickness` is WRONG.

**M5** CONTROVERSIAL "We do get sick because it is the way God made things to occur"
`The way God made things --> We get sick`
Code the respondent's claim, not our ontology.

**M6** "We take three baths per day, and also wash our hands after visiting the washrooms."
nothing
Description of practices; the change link is M1.

**M7** "the chicken we had all died due to sickness"
`Sickness --> Our chickens all died`

**M8** "Organisation 1 taught us how to plant and how to harvest in the best manner."
`Organisation 1 taught us to plant and harvest --> We farm in a better way`
Weak is not wrong.

**M9** "in my garden in general we plant tomatoes, vegetables, cabbage, and corn because we grow crops in our farm and that way we have no food shortages"
`We grow crops in our garden and farm --> No food shortages`
NOT links among the crops: a list is not a chain.

**M10** "We all get sick and when this happened everything is affected and put on hold."
`We all get sick --> Everything is put on hold`

**M11** "My family earns money only because of the savings that Organisation 1 has provided for us. They taught us how to save money."
`Organisation 1 taught us how to save --> Family has savings to live on`

**M12** "we were all sick and we were unable to plant almost anything"
`We were all sick --> We were unable to plant`

**M13** [+opposites] "It has changed because we do not earn as much money for many different foods."
`~We earn money --> ~We eat varied foods`
plain wording equally right.

**M14** "but with the neighbours help with giving food and the community we do eat a bit"
`Neighbours and community give us food --> We eat a bit`

**M15** "ever since a man from Organisation 1 came and spoke to him he has since changed"
`A man from Organisation 1 spoke to my husband --> My husband stopped beating us`
(context supplies "changed")

**M16** CONTROVERSIAL "our leader and Organisation 1 incriminated my husband so he does not beat women any more, or other wise he will be arrested"
`Leader and Organisation 1 incriminated my husband --> My husband no longer beats us`
adding `Threat of arrest --> ...` also fine.

**M17** CONTROVERSIAL "There has been no change as we were not able to change because we are unable to produce more."
`We are unable to produce more --> Our situation stayed the same`
Kept-as-it-was IS an effect.

**M18** [+type] "We would like to participate in the farmers group and we would also like to be able to go to the hospital and that children stop dying."
nothing
Aspiration.
Using the type extension:
`We are able to go to the hospital --> Children stop dying` type=hypothetical-future

**M19** [+sentiment] "ever since a man from Organisation 1 came and spoke to him he has since changed"
`A man from Organisation 1 spoke to my husband --> My husband stopped beating us` sentiment=1
The outcome is good for the respondent, whatever the grim subject matter.

**M20** [+emotion] "For this lady, it is sad the way they are living. ... Some end up dying as a result, five children died because of sickness."
`The family does not go to the hospital --> Five of the family's children died` emotion=2
"it is sad", deaths of children: clear emotional content in the wording.

## N: Notes on Nursing

**N1** "The air is as stagnant, musty, and corrupt as it can by possibility be made. It is quite ripe to breed small-pox, scarlet-fever, diphtheria, or anything else you please."
`Room air stagnant and corrupt --> Smallpox, scarlet fever and diphtheria breed among occupants`

**N2** [+packages] "the fireplace is carefully fastened up with a board; the windows are never opened; probably the shutters are kept always shut ... no breath of fresh air can by possibility enter into that room"
`Fireplace boarded up --> No fresh air enters the room`
AND
`Windows never opened --> No fresh air enters the room`
AND
`Shutters kept shut --> No fresh air enters the room`
Core-only: three separate links.

**N3** CONTROVERSIAL "People don't catch cold in bed. This is a popular fallacy."
nothing
The text DENIES the influence; coding `Open windows in bed --> Catching cold` inverts her.

**N4** [+packages] "With proper bed-clothes and hot bottles, if necessary, you can always keep a patient warm in bed, and well ventilate him at the same time."
`Proper bed-clothes --> Patient kept warm in bed while ventilated`
AND
`Hot bottles --> Patient kept warm in bed while ventilated`

**N5** [+packages] CONTROVERSIAL "The time when people take cold ... is when they first get up after the two-fold exhaustion of dressing and of having had the skin relaxed by many hours, perhaps days, in bed, and thereby rendered more incapable of re-action."
`Exhaustion of dressing --> People take cold on first getting up`
AND
`Skin relaxed by long bed rest --> People take cold on first getting up`
internal chain ("thereby") also fine.

**N6** "I have known a medical officer keep his ward windows hermetically closed. Thus exposing the sick to all the dangers of an infected atmosphere"
`Medical officer kept ward windows hermetically closed --> Sick exposed to an infected atmosphere`

**N7** CONTROVERSIAL "because he was afraid that, by admitting fresh air, the temperature of the ward would be too much lowered"
`The medical officer was afraid that fresh air would lower the ward temperature --> The medical officer kept the windows closed`
Always code the actor if possible; "he" is hidden in earlier text and needs bringing out.
A fear is a cause; the feared belief itself is NOT coded.

**N8** "To attempt to keep a ward warm at the expense of making the sick repeatedly breathe their own hot, humid, putrescing atmosphere is a certain way to delay recovery or to destroy life."
`Sick repeatedly breathe their own foul atmosphere --> Sick peoples' recovery delayed or life destroyed`
Generic causal knowledge is codeable.

**N9** "During sleep, the human body, even when in health, is far more injured by the influence of foul air than when awake."
`Foul air during sleep --> The body is injured`

**N10** [+packages] "hot bottles, hot bricks, or warm flannels, with some warm drink, should be made use of until the temperature is restored"
`Hot bottles --> Patient's temperature restored`
OR
`Hot bricks --> Patient's temperature restored`
OR
`Warm flannels --> Patient's temperature restored`
OR
`Warm drink --> Patient's temperature restored`
"Or" = alternatives, each sufficient.

**N11** [+despite +opposites] CONTROVERSIAL "The nurse may be trusting to the patient's diet, or to his medicine, or to the occasional dose of stimulant ... while the patient is all the while sinking from want of a little external warmth."
`The patient lacks a little external warmth --> The patient is sinking`
DESPITE
`Diet, medicine and stimulants --> ~The patient is sinking` failure=1
NOT `diet --> sinking`.

**N12** "Patients are frequently lost in the latter stages of disease from want of attention to such simple precautions."
`Nurses neglect simple warming precautions --> Patients are lost in the latter stages`

**N13** CONTROVERSIAL "This fatal chill is most apt to occur towards early morning at the period of the lowest temperature of the twenty-four hours, and at the time when the effect of the preceding day's diets is exhausted."
`Lowest temperature of the 24 hours --> Patients suffer the fatal chill`
OR
`Effect of the day's food exhausted --> Patients suffer the fatal chill`
Two contributory reasons mentioned in the same breath: a package with the packages extension, two links without. Nothing also defensible.

**N14** CONTROVERSIAL "If they are feverish at night, with burning hands and feet, they are almost sure to be chilly and shivering in the morning."
nothing
Predictive association (one cycle, two phases); `fever --> chill` is the over-reading trap.

**N15** CONTROVERSIAL "A short time ago a man walked into a back-kitchen in Queen square, and cut the throat of a poor consumptive creature ... Of course he was mad."
`The attacker was mad --> The attacker cut the victim's throat`
(offered as the explanation); nothing also fine. NOT anything about ventilation.

**N16** "It may come from a corridor into which other wards are ventilated, from a hall, always unaired ... and with this the patient's room or ward is aired, as it is called--poisoned, it should rather be said."
`Room aired from foul indoor sources --> Patient's room air poisoned`
The sources are a list, not a chain.

**N17** [+type] CONTROVERSIAL "hot bottles, hot bricks, or warm flannels, with some warm drink, should be made use of until the temperature is restored"
`Warm drink --> Patient's temperature restored` type=hypothetical-future
A recommendation is generic causal knowledge: no particular past event, so not factual-past; hypothetical-future is the least-bad fit. Unclear also defensible.

## G: Garden and house doctrine

**G1** (005) "I started to eat adequately and was feeling more lively"
`I started to eat adequately --> I felt more lively`
NOT forced into variable form (`amount eaten --> energy level`).

**G2** (005) "I was eating less and felt quite lethargic"
`I was eating less --> I felt quite lethargic`
Speaker's own words; NOT collapsed into G1 as we might with a variable-based approach.

**G3** [+opposites] CONTROVERSIAL (005)
G1/G2 MAY align as `Eating adequately --> Feeling lively` and `~Eating adequately --> ~Feeling lively`
as-said labels equally right. Use opposites form with ~X if there are other nearby codings using X.

**G4-G9** [+hierarchy +opposites] (015, the Priya interview) "I used to smoke about ten a day all through my twenties and I never really thought about vegetables. Honestly I was unfit then. I would get out of breath walking up the hill to my flat, and I was low quite a lot of the time, although I did not really join the dots back then. Things changed when I turned thirty-five. I gave up smoking and started cooking properly with lots of greens. Within about six months I was a different person. The fitness came back quite quickly once the cigarettes were out of the way, and I was in a much better mood for it. Being fit just lifts you, you feel capable."

- `~Healthy habits; smoking --> ~Good health; physical fitness`
- `~Healthy habits; ~eating vegetables --> ~Good health; physical fitness`
- `Healthy habits; ~smoking --> Good health; physical fitness`
- `Healthy habits; eating vegetables --> Good health; physical fitness`
- `~Good health; physical fitness --> ~Good health; positive mood` (CONTROVERSIAL: "did not join the dots back then" — she joins them now, so code it)
- `Good health; physical fitness --> Good health; positive mood`

**G10** [+packages] CONTROVERSIAL (005) "I went on holiday to Spain expecting to enjoy it, and indeed I did particularly enjoy it because I remembered to take my phrase book."
`Going on holiday to Spain --> Enjoying the holiday`
AND
`Remembering to take my phrase book --> Enjoying the holiday`
with packages, an AND package. Second-order (enabler) links are NOT coded.

**G11** [+opposites +despite] CONTROVERSIAL (005) "I went on holiday to Spain, but I forgot to take my phrase book so I didn't enjoy the holiday at all."
`Forgetting to take my phrase book --> ~Enjoying the holiday`
DESPITE
`Going on holiday to Spain --> Enjoying the holiday` failure=1

**G13** CONTROVERSIAL (house, 2026-07-15) "Once the stress starts it just breeds more stress."
`Family stress --> Family stress`
Same label both ends is LEGAL where the text claims the thing feeds itself; empty only with no claim behind it.

**G14** CONTROVERSIAL (house) "Rising unemployment made me lose my job"
`Rising unemployment --> I lost my job`
Sounds tautological, is not, at least not from the speaker's perspective.

**G15** CONTROVERSIAL (house) "The manager delivered coaching to the staff." (nothing more said)
`The manager delivered coaching --> Staff received coaching`
Weak is not wrong.

**G16** (house) "Training will be delivered through online guides, workshops and 1-2-1 coaching."
nothing
A common false link in plans.

**G17** [+sentiment] (015) "climate change means our crops are failing"
`Climate change --> Our crops are failing` sentiment=-1
Sentiment is the respondent's valuation of the effect, separate from opposites.

**G18** [+type] (house) "The programme will improve children's reading"
`The programme runs --> Children's reading improves` type=planned-future
A stated plan is coded against its intended effect and typed as planned.

**G19** [+sentiment +hierarchy] (015) "Being fit just lifts you, you feel capable."
`Good health; physical fitness --> Good health; positive mood` sentiment=1
Sentiment attaches to the whole hierarchical effect label; the general part does not change the valuation.


**G20** (house) "The child fell off their bike and they were injured."
`The child fell off their bike --> The child was injured`
NOT
`The child fell off their bike --> They were injured`
Each label must stand alone: no pronoun leaning on the other label.

## H: loneliness interview (Hackney)

**H1** "it makes me... it doesn't really sadden me but um... it kind of um, peaks a specific curiosity"
`Watching social groups from the outside --> My curiosity is piqued`

**H2** CONTROVERSIAL "usually people would then try to... fit in and kind of see where they could slot themselves with people they wouldn't find much... um compatibility with, but they just wouldn't like to be lonely. So... I would shy away from that and kind of find my own space"
`People don't want to be lonely --> People try to fit in with incompatible groups`
`I do not want to force incompatible friendships --> I shy away and find my own space`
Two claims, one about people in general and one about himself; code both.

**H3** [+emotion] "it makes me feel... er... I suppose over a longer period of time, irritated, and I suppose like um... uh... dissatisfied in the long run"
`I shy away from groups rather than fit in --> I feel irritated and dissatisfied in the long run` emotion=1
The disfluency is the speaker's; the emotional wording is real but mild.

**H4** [+type] CONTROVERSIAL "unless you find people like minded then... you're gonna kind of just get swept away in like the kind of um... the um... the social wave"
`You do not find like-minded people --> You get swept along in the social wave` type=hypothetical-future
A conditional generic claim; factual-present also defensible.

**H6** [+packages] "people look up to, because um... they either... um, let's say away from school they had... like a good dress sense or like they knew a lot of people"
`(Popular kids) had good dress sense --> People look up to (popular kids)`
OR
`(Popular kids) knew a lot of people --> People look up to (popular kids)`
Same-breath alternatives: an OR package. The actor type is implicit and spelt out the same way in every label.

**H7** "stigmas attached to them about things that um are out of control. So maybe like a sickness they were born with ... things that are out of their control that kind of get mocked"
`(Vulnerable people) get stigmas about conditions outside their control --> (Vulnerable people) get mocked`
The actor is implicit and needs bringing out; spell out the type of person, in the same words across links, parenthesised where the wording is ours.

**H8** "once you kind of get to that point you don't see that person too much though as a person, it's about all the things you attribute to them"
`You put someone on a pedestal --> You stop seeing (the person on the pedestal) as a person`
NOT "seeing them": the effect label must not lean on the cause label.

**H9** "I drew like a um... a head, like behind where a camera would be pointing, with like a sea of faces"
nothing
Describing the drawing; interview transcripts are full of codeable-looking description.

## X: extension combinations

Coverage of the pairs so far: hierarchy+opposites (G4-G9), opposites+despite (M4, N11, G11), packages alone (M3, N2, N4, N5, N10, H6, G10), sentiment+hierarchy (G19), type alone (M18, G18, H4, N17), emotion alone (M20, H3). The examples below fill the missing pairs.

**X1** [+hierarchy +opposites +despite] (house) "I gave up smoking but the fitness never really came back."
`Healthy habits; ~smoking --> Good health; physical fitness` failure=1
A failed influence with hierarchical labels: the failure flag and the `;` form compose without special rules.

**X2** [+despite +packages +opposites] (house) "The heavy rains made the river rise, despite all the prevention and clearance work."
`Heavy rains --> River levels rose`
DESPITE
`Prevention and clearance work --> ~River levels rose` failure=1
The DESPITE package: winner first, failed second.

**X3** [+opposites +packages] (house) "Either the strike or the bad weather kept attendance down."
`Strike --> ~Attendance`
OR
`Bad weather --> ~Attendance`
A `~` label is an ordinary package member.

**X4** [+sentiment +opposites] (house) "The medication finally brought my anxiety right down."
`Medication --> ~My anxiety` sentiment=1

**X5** [+hierarchy +packages] CONTROVERSIAL (015) "I gave up smoking and started cooking properly with lots of greens. Within about six months I was a different person."
`Healthy habits; ~smoking --> Good health; physical fitness`
OR
`Healthy habits; eating vegetables --> Good health; physical fitness`
With packages on, the same-breath rule makes G6/G7 a package: two contributory causes given in one breath, no claim both were needed, so OR. But arguably AND could work too.

## S: splitting an "and" between causes (packages) — NEW, uncurated

When a source joins influences with "and" or similar ideas, split into packaged links but only where the conjuncts are genuinely distinct influences, each of which the source could have claimed alone. A phrase that is really one influence described with two words stays as a single label with no package. Test: would the source defend each conjunct separately as its own influence on this effect?

**S1** [+packages] (house) "You need both the visa and the sponsorship letter to get in."
`Visa --> Entry to the country`
AND
`Sponsorship letter --> Entry to the country`
Two distinct things, each nameable alone; the source says both are needed.

**S2** [+packages] (house) "We got there because of the funding and because the new manager pushed it through."
`Funding --> The project succeeded`
?
`The new manager pushed the project through --> The project succeeded`
Two distinct contributory causes in one breath, not clear whether both were needed: same-breath rule, `?` says not clear whether AND or OR.

**S3** DO NOT SPLIT (strategy doc) "UoB needs to be much more innovative and strategic to gain the attention of London based national policymakers."
`UoB; being more innovative and strategic --> London-based national policymakers; paying attention to UoB`
Paired adjectives on one stance. The source is not claiming innovation alone would do it; splitting manufactures two influences out of one.

**S4** DO NOT SPLIT (house) "The staff were friendly and welcoming, so I kept coming back."
`Staff were friendly and welcoming --> I kept coming back`
Near-synonyms describing one quality.

**S5** DO NOT SPLIT (house) "The hustle and bustle of the market drew the crowds in."
`The market's hustle and bustle --> Crowds came to the market`
A set phrase is one influence.

**S6** CONTROVERSIAL (strategy doc) "Policy engagement without clear goals and strategic coordination can be rudderless."
`~Clear goals --> Policy engagement was rudderless` ?
AND
`~Strategic coordination --> Policy engagement was rudderless` ?
Two distinct noun phrases, so splittable on the test above; arguably, speaker says that both have to be absent for rudderless engagement.

**S7** [+packages] "and" on the EFFECT side (house): "The programme raised awareness and changed behaviour."
`The programme --> Awareness rose`
AND
`The programme --> Behaviour changed`
One claim fanned into two effects: the links may share a package just as joint causes do, recording that this is one joint claim rather than two independent pieces of evidence. (Ruling, Steve 2026-07-16: effect-side packages allowed; an earlier draft of this example banned them.)
