# Charan Rathore

I build retrieval and memory systems that let you ask **“Where did that answer come from?”** At MiQ I work on market analytics. In open source I work on a related question about software behavior. When a form loses a row or an agent repeats an action, which step broke the promise to the user?

## Try the work

**IntelliRAG** · Ask a question, open the cited passage, then follow the retrieval trace to see which evidence survived. The public demo starts with cited extracts. [Open the lab](https://intellirag-live-own-track.vercel.app/) · [Read the evaluation](https://github.com/charan-rathore/IntelliRAG/blob/main/audit/REPORT.md)

**memoRABLE** · Turn a document into six reusable memory blocks. Follow a block back to its source, then use that same material in an email or on a web page. [Explore the code](https://github.com/charan-rathore/memoRABLE)

**ThermoSense** · A hyperlocal temperature forecast keeps its score after the weather arrives. Compare the model and the API against observations to see where each runs warm or cold. [Explore the forecasts](https://github.com/charan-rathore/Time-Series-Temperature-Modelling)

## Changes that reached upstream

- **A retry should produce one artifact.** In openmuse, a file could exist even when its checkpoint was lost. I made the retry recover the original file. [openmuse #45](https://github.com/CopilotKit/openmuse/pull/45)
- **Deleting one row should leave its neighbor intact.** In React Hook Form, removing a parent row could unregister the nested fields of the row moving into its place. I fixed the interaction between removal and reindexing. [React Hook Form #13828](https://github.com/react-hook-form/react-hook-form/pull/13828)
- **One tool definition could break every request.** Hermes sent a schema constraint that llama.cpp could not compile. I removed the incompatible constraint while preserving the runtime length check. [Hermes #131286](https://github.com/NousResearch/hermes-agent/pull/131286)
- **A list should follow the page around it.** Removing content above a virtual list could leave it displaying stale rows. I fixed the missed update in react-window. [react-window #935](https://github.com/bvaughn/react-window/pull/935)

[Browse my contribution notes](CONTRIBUTIONS.md) · [See my merged PRs on GitHub](https://github.com/pulls?q=is%3Apr+author%3Acharan-rathore+is%3Amerged)

[Portfolio](https://charan-tetris-portfolio.vercel.app/) · [Writing](https://charanrathore.substack.com) · [Email](mailto:ra7hore.charan@gmail.com)
