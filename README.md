<p align="center">
  <img src="assets/wave.svg" width="100%" alt="">
</p>

### hey, I'm Charan

I'm a mechanical engineer who got lost in data and never looked back.

I care about two things that sound different but feel the same to me:

1. **what a product is actually doing** when a user clicks something  
2. **what a system is actually doing** in the two seconds before the answer shows up

Most tutorials show you how to call an API. I want to know why the pipeline failed, which layer lied, and whether the feature was even the right thing to ship.

At Flipkart I worked on seller funnel analytics and search personalization - behavioral data into product decisions. Outside of that I build the layers under intelligent systems: retrieval, memory, closed-loop forecasts, agents that can say how much to trust themselves.

---

### currently

AI systems · retrieval · inference  
memory · evaluation · product experiments

---

### what I'm curious about

**01** Where does the latency actually go?  
**02** What should an AI system remember - and prove it remembered from the source?  
**03** When is a forecast wrong because of the model, and when because of the place?  
**04** Why do technically good products still fail distribution?  
**05** Which problems are worth automating, and which only look that way?

---

### things I've built

**[IntelliRAG](https://github.com/charan-rathore/IntelliRAG)**  
*I wanted to know where RAG actually breaks.*

ingestion → chunking → hybrid retrieval → rerank → citations → evaluation → observability  
An experimental platform for measuring failure modes, not a claim of production SOTA. Eval stays honest: small deterministic corpus for CI, mock vs real Ollama labeled separately.

[read the investigation →](https://github.com/charan-rathore/IntelliRAG)

**[memoRABLE](https://github.com/charan-rathore/memoRABLE)**  
*What if documents became memory?*

Six source-linked blocks. Click a memory, the original lines light up. Publish once to email / web / doc without rewriting the truth. Local-first.

[try it →](https://memo-rable.vercel.app)

**[ThermoSense](https://github.com/charan-rathore/Time-Series-Temperature-Modelling)**  
*Can a forecast know your rooftop?*

Ground truth → commercial API bias → ensemble forecast → public leaderboard → retrain. The product is the loop, not the model name.

[see the experiment →](https://thermosense-black.vercel.app)

**[Finsight](https://github.com/charan-rathore/agentic-finance-advisor)**  
*Can an AI answer also explain how much it should be trusted?*

Multi-agent research with freshness, source agreement, versioned knowledge, and a confidence score you can inspect.

[inspect the system →](https://github.com/charan-rathore/agentic-finance-advisor)

---

### product things I keep taking apart

**Search** - what actually happens between a query and the ranked result (Flipkart search personalization was the first place this got real for me)  
**Funnels** - where discovery leaks: the step users drop, not the dashboard average  
**Trust UX** - when a product should show confidence, provenance, or “I don’t know yet”  
**Distribution** - why a technically solid system still fails to get used  
**The invisible middle** - [the 2 seconds you never see](https://charanrathore.substack.com/p/the-2-seconds-you-never-see): auth, memory, routing, the work that makes complexity feel effortless

I go system → product → business. Same habit: open the black box, name the failure mode, then decide what to ship.

---

### one thing I wrote

**[The 2 seconds you never see](https://charanrathore.substack.com/p/the-2-seconds-you-never-see)**  
I thought I knew what happened after you hit enter. I was wrong.

More when I have something worth saying → [Substack](https://charanrathore.substack.com)

---

### how I work

measure → build → break → learn → repeat

Write the tradeoff down. Keep eval next to the code. Prefer systems that fail in known ways. Same rule for product: if I can’t explain the funnel step, I don’t trust the feature yet.

---

### currently investigating

→ what actually determines RAG latency (retrieval vs rerank vs generation vs cold start)  
→ how memory systems should preserve provenance without becoming another summary blob  
→ when local inference is the right constraint vs when it just feels pure  
→ closed-loop evaluation: leaderboards that force the model to face ground truth  
→ why technically good products fail distribution

*I update this when the questions change.*

---

<p align="center">
  <a href="https://github.com/charan-rathore">GitHub</a>
  ·
  <a href="https://charanrathore.substack.com">Substack</a>
  ·
  <a href="https://charan-rathore.github.io">Portfolio</a>
  ·
  <a href="mailto:ra7hore.charan@gmail.com">Email</a>
</p>

<sub>BITS Pilani · dual degree · class of 2026 · ex-Flipkart product analytics  
Older experiments stay public. The four above are the ones that still feel like me.</sub>
