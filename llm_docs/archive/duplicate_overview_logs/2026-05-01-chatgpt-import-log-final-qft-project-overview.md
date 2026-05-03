---
created_at: "2026-05-01T22:10:40-04:00"
updated_at: "2026-05-01T23:45:36-04:00"
generated_by: "chatgpt_import"
timestamp_source: "filesystem_birthtime"
project: "QFT"
log_type: "generated_session"
---

# you asked

i want the section structure to be as simple as possible i think this might be a bit too much? like we were thinking
part i: theoretical construction
1. introduction
(what is this about, what r the motivations etc)
2. have all of the required math in one area (this way it can always be referenced later, and if people want to skip and just come back as needed thats better--its better to have it centralized rather than scattered bc im always kind of frustrated at having something mathy defined and then not being able to see any consequences of that definition until pages of physics)
3. perturbative qft and topological stuff, going into chern simons
4. defining what a tqft is formally and different kinds of tqfts
5. calculable observables

part 2: experimental stuff (??)
here idk, maybe like fractional quantum hall, axions, eta prime,??? im not sure a good way to structure this, but i want all of the like "so what" physics and computations to live here. this is especially a guide to routard for starting to do work in any of these subfields but im not sure how to organize

whats a good simple low # of subsection structure that can help w this? especially for experiment?

could you also do an extensive literature review on the kinds of observables i talked abt and provide a downloadable md file with any sources (reviews or papers or otherwise) that are relevant? schwartz in lecture discussed some observables and also some of the iffiness that might source them (ie like all of the assumptions baked into writing these things down)--i want to touch on that somewhere

---

# chatgpt response

Yes — I would simplify it more.

Your instinct is right that the paper should have a centralized math block and then a clean “so what?” block. Your current draft already naturally clusters into a math foundation, an anomaly-to–Chern–Simons bridge, and an applications/response block, so the right move is mostly to merge and compress, not to redesign from scratch. See your current draft modules here: [draft modules PDF](sandbox:/mnt/data/tex_docs_compile_wrapper_v3.pdf).

The simplest structure I would recommend is:

Part I. Construction

1. Introduction

2. Mathematical toolkit

3. From ordinary gauge theory to Chern–Simons

4. TQFT and its observables

Part II. Physics

5. Topological response in $2+1$ dimensions

6. Topological sectors in $3+1$ dimensions

7. Defects, caveats, and outlook

That is already enough.

The logic is:

Section 2 is your centralized math chapter.

Section 3 is where you start from the Schwartz-level material — instantons, $F\tilde F$, large gauge transformations, anomaly descent, Wilson lines — and show why those ideas force Chern–Simons language.

Section 4 is where you finally say what a TQFT is formally, but only after the reader already wants that definition.

Then Part II is not “experiment” in a vague sense. It is “physics organized by observable family.”

That is the key simplification.

So I would make Section 5 the entire FQHE / anyon / edge / degeneracy story:

5.1 Hall response

5.2 Fractional charge and braiding

5.3 Edge modes, anomaly inflow, and topological degeneracy

That works because these really are one observable package in the standard literature: transport, charge, braiding, and edge structure are the canonical Chern–Simons observables for topological phases of matter. The modern review/expt backbone for that package is Stern’s pedagogical review, Nayak et al.’s nonabelian-anyon review, the Halperin–Stern–Neder–Rosenow review on fractional charge/statistics, and the 2020 Nature and Science experiments on braiding/collision signatures. ([ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0003491607001674?utm_source=chatgpt.com))
Then make Section 6 the whole $3+1$d gauge-theory consequences story:

6.1 $\theta$ vacua, topological susceptibility, and the $U(1)_A$ problem

6.2 The $\eta'$ and Witten–Veneziano

6.3 Strong CP, neutron EDM, and axions

That is also one observable package. In the standard reviews, these topics are treated as one chain: topology controls vacuum structure, susceptibility controls $E(\theta)$ and the $\eta'$ story, neutron EDM constrains physical $\bar\theta$, and the axion is the dynamical response to that same $\theta$-dependence. Hook’s TASI notes, Dine’s older TASI notes, Marsh’s axion review, and lattice/topological-susceptibility literature all organize the subject this way. ([arXiv](https://arxiv.org/abs/1812.02669?utm_source=chatgpt.com))
Then Section 7 should absorb everything that otherwise makes the paper feel too fragmented:

7.1 Monopoles, line operators, and global structure

7.2 When the observables are really topological, and when they are only effective

7.3 Outlook / guide du routard

This is where you put the “iffiness” from lecture. That material belongs in the paper, but not as apologetics scattered everywhere. It should be a dedicated subsection. For example:

- $F\tilde F$ is locally a total derivative, yet globally nontrivial.
- Instantons are a semiclassical language, not the whole strong-coupling story.
- Topological susceptibility is a clean field-theory observable but not something you directly “detect” in a detector.
- Interferometry in Hall devices is not pure TQFT in the lab because of Coulomb effects, edge reconstruction, slow quasiparticle dynamics, and other mesoscopic complications.
- Monopoles are topological defects in a theory with specific asymptotic structure; that is different from saying the full theory is topological.

That last chapter is also the natural home for monopoles, because the monopole literature itself is usually framed as a defect/global-structure story rather than the same kind of response observable as Hall transport or EDM constraints. The current PDG monopole review and recent theory overviews treat it that way. ([Particle Data Group](https://pdg.lbl.gov/2025/reviews/rpp2025-rev-mag-monopole-searches.pdf?utm_source=chatgpt.com))
So the compact version is:

Part I:
1. Introduction
2. Mathematical toolkit
3. From ordinary gauge theory to Chern–Simons
4. TQFT and its observables

Part II:
5. Topological response in $2+1$d
6. Topological sectors in $3+1$d
7. Defects, caveats, and outlook

I also made the literature-review/source-map markdown file, with a concrete section plan, observable families, landmark reviews/papers, and a dedicated “what is clean vs what is only effective” section:

[Download the literature review markdown](sandbox:/mnt/data/tqft_observables_literature_review.md)

If you want the shortest possible takeaway: do not make Part II “experiments by subfield.” Make it “observable packages,” and then let each package gather the relevant systems under it.
