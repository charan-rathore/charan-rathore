# Charan Rathore

**@charan-rathore** · I build systems that make the pieces click.

I care about two things that sound different but feel the same to me:

1. **what a product is actually doing** when a user clicks something  
2. **what a system is actually doing** in the two seconds before the answer shows up

Most tutorials show you how to call an API. I want to know why the pipeline failed, which layer lied, and whether the feature was the right thing to ship.

I am an **Analyst at MiQ, working across the MENA markets**. Previously, at Flipkart, I worked on seller funnel analytics and search personalization — behavioral data into product decisions. Outside work I build and test intelligent systems: retrieval, memory, forecasts and source-aware agents.

---

## currently

**MiQ · Analyst · MENA markets**<br>
[Explore my Systris portfolio →](https://charan-tetris-portfolio.vercel.app/)

AI systems · retrieval · inference  
memory · evaluation · product experiments

<p>
  <a href="https://github.com/charan-rathore?tab=repositories"><img alt="GitHub projects" src="https://img.shields.io/badge/GitHub-Projects-181717?logo=github"></a>
  <a href="https://charan-tetris-portfolio.vercel.app/"><img alt="Play Systris" src="https://img.shields.io/badge/Portfolio-Play%20Systris-7b68ee"></a>
  <a href="https://charanrathore.substack.com"><img alt="Read the writing" src="https://img.shields.io/badge/Substack-Writing-ff6719?logo=substack&logoColor=white"></a>
</p>

---

## open source contributions

*if it isn't merged, it isn't here. the strongest fixes lead; the rest of the magpie history is folded below.*

**[hermes-agent](https://github.com/NousResearch/hermes-agent)** · the agent that grows with you

I made the gateway show an enabled platform whose adapter is missing in `hermes status`. My commit is on main with my authorship, merged through a maintainer's salvage PR that also reconnects the platform once its plugin loads. [merged via NousResearch/hermes-agent#130613 →](https://github.com/NousResearch/hermes-agent/pull/130613) · Oct 2026

I fixed every request to a llama.cpp server failing with HTTP 400 "failed to parse grammar", by dropping the `maxLength: 8000` from the clarify tool's `choices` schema; the runtime length check is untouched, and tests guard against any bound of 2000 or more. [merged in NousResearch/hermes-agent#131286 →](https://github.com/NousResearch/hermes-agent/pull/131286) · Oct 2026

**[vite](https://github.com/vitejs/vite)** · next generation frontend tooling

I stopped Vite's dependency optimizer from warning about packages that intentionally empty an import in the browser, so a `browser: false` mapping loads an empty module while genuinely unsupported imports still warn. [merged in vitejs/vite#23590 →](https://github.com/vitejs/vite/pull/23590) · Sep 2026

**[react-hook-form](https://github.com/react-hook-form/react-hook-form)** · react hooks for form state management and validation

I restored blur validation on a `Controller` after `reset()`, so a field that lost its registration without rerendering registers again on blur and validates in `onTouched` mode instead of skipping the check. [merged in react-hook-form/react-hook-form#13817 →](https://github.com/react-hook-form/react-hook-form/pull/13817) · Oct 2026

I stopped removing a row from an outer `useFieldArray` with `shouldUnregister` on from wiping the nested field array values of the row that shifts into its place, by skipping the nested unregister while the parent reindexes. [merged in react-hook-form/react-hook-form#13828 →](https://github.com/react-hook-form/react-hook-form/pull/13828) · Oct 2026

I fixed `useFieldArray.remove` so duplicated indexes like `remove([1, 1])` no longer remove extra rows, and the array you pass in is no longer sorted in place. [merged in react-hook-form/react-hook-form#13830 →](https://github.com/react-hook-form/react-hook-form/pull/13830) · Oct 2026

I made `useForm` reset an option to its default when it is left out of the props on a later render, so a dropped `resolver` stops running on submit and `mode` goes back to `onSubmit`. [merged in react-hook-form/react-hook-form#13831 →](https://github.com/react-hook-form/react-hook-form/pull/13831) · Oct 2026

**[recharts](https://github.com/recharts/recharts)** · redefined chart library built with React and D3

I fixed a lone negative bar in a `BarStack` rounding its corners at the zero line instead of the outer end, by running a single rectangle through the same normalization as a stack of several. [merged in recharts/recharts#7896 →](https://github.com/recharts/recharts/pull/7896) · Oct 2026

I kept a `Brush` start or end index from falling outside the data and drawing NaN positions, by clamping both indexes to the data range when the data or the props change. [merged in recharts/recharts#7916 →](https://github.com/recharts/recharts/pull/7916) · Oct 2026

**[kivy](https://github.com/kivy/kivy)** · open source UI framework written in Python, running on Windows, Linux, macOS, Android and iOS

I fixed `Image` crashing on data URIs without `;base64`, which handed a plain string to `BytesIO`; the payload is now percent-decoded to bytes first, per RFC 2397, and base64 handling is unchanged. [merged in kivy/kivy#9394 →](https://github.com/kivy/kivy/pull/9394) · Oct 2026

I fixed KV rules crashing on an `or` or `and` inside an f-string, such as `f"{a or b}"`, by splitting the boolean branch from the f-string branch so both operands are found and stay reactive. [merged in kivy/kivy#9393 →](https://github.com/kivy/kivy/pull/9393) · Oct 2026

**[scalar](https://github.com/scalar/scalar)** · open-source API references and API client

I fixed multipart file uploads in Scalar's generated code examples, starting with the missing `fileName` on file params. The maintainer built on it so examples keep real file bytes and matching boundaries across clients. [merged in scalar/scalar#10460 →](https://github.com/scalar/scalar/pull/10460) · Oct 2026

I escaped quotes and backslashes in the PHP cURL example bodies, so a copied snippet with an apostrophe in the body is still valid PHP. [merged in scalar/scalar#10495 →](https://github.com/scalar/scalar/pull/10495) · Oct 2026

I escaped special characters in the Dart HTTP examples and taught them to send plain text bodies, so copied Dart code compiles and includes the body it should. [merged in scalar/scalar#10496 →](https://github.com/scalar/scalar/pull/10496) · Oct 2026

I made the Python Requests and HTTPX examples send bodies for JSON media types with parameters and for text types, instead of dropping them. [merged in scalar/scalar#10497 →](https://github.com/scalar/scalar/pull/10497) · Oct 2026

I kept every value of a repeated form field in the PHP Guzzle examples, so `tag=a&tag=b` arrives with both values instead of only the last. [merged in scalar/scalar#10499 →](https://github.com/scalar/scalar/pull/10499) · Oct 2026

I escaped strings in the C# HttpClient examples, so a URL, header or form value with a quote or backslash still compiles and sends as written. [merged in scalar/scalar#10503 →](https://github.com/scalar/scalar/pull/10503) · Oct 2026

**[react-jsonschema-form](https://github.com/rjsf-team/react-jsonschema-form)** · a React component for building web forms from JSON Schema

I fixed a root value of `false`, `0` or `''` failing validation, so a boolean form with `false` no longer errors with "must be boolean" and can submit. [merged in rjsf-team/react-jsonschema-form#5423 →](https://github.com/rjsf-team/react-jsonschema-form/pull/5423) · Oct 2026

**[nitro](https://github.com/nitrojs/nitro)** · next generation server toolkit

I made the build refuse to run when cleaning the output directory would delete the public assets inside it, so it fails with an error naming both paths instead of reporting success on an empty deploy. [merged in nitrojs/nitro#4685 →](https://github.com/nitrojs/nitro/pull/4685) · Oct 2026

I fixed the Vercel preset ignoring a `redirect: false` rule without headers, so those paths no longer get pulled into broader redirects in the build output. [merged in nitrojs/nitro#4728 →](https://github.com/nitrojs/nitro/pull/4728) · Oct 2026

**[mcp-use](https://github.com/mcp-use/mcp-use)** · the fullstack MCP framework - MCP apps for ChatGPT and Claude, servers for agents

I wrapped Gemini array tool results in an object, so serialized tool output survives the round trip back to the model. [merged in mcp-use/mcp-use#2675 →](https://github.com/mcp-use/mcp-use/pull/2675) · Sep 2026

**[harness-sdk](https://github.com/strands-agents/harness-sdk)** · build an agent harness and control it end-to-end

I gave the OpenAI Responses model the location-source guard every other provider already had, so a document backed by an S3 location is skipped with a warning instead of crashing the request. [merged in strands-agents/harness-sdk#4706 →](https://github.com/strands-agents/harness-sdk/pull/4706) · Sep 2026

I stopped a finished Gemini reply from crashing token accounting, so a final response without usage metadata completes normally instead of throwing. [merged in strands-agents/harness-sdk#4724 →](https://github.com/strands-agents/harness-sdk/pull/4724) · Sep 2026

I made the Ollama model forward numeric `keep_alive` values like `0`, which were dropped as falsy, so "unload immediately" now reaches the server. [merged in strands-agents/harness-sdk#4725 →](https://github.com/strands-agents/harness-sdk/pull/4725) · Oct 2026

**[dynamo](https://github.com/ai-dynamo/dynamo)** · a datacenter scale distributed inference serving framework

I fixed the 500 on vLLM-Omni video requests that set a negative prompt, by putting it in the prompt's dict entry instead of assigning it as an attribute. [merged in ai-dynamo/dynamo#15402 →](https://github.com/ai-dynamo/dynamo/pull/15402) · Oct 2026

**[jedi](https://github.com/davidhalter/jedi)** · awesome autocompletion, static analysis and refactoring library for Python

I stopped importing Jedi from changing the process-wide recursion limit; it now raises the limit only while its own parsing and inference run, then restores it, and never lowers a higher one. [merged in davidhalter/jedi#2113 →](https://github.com/davidhalter/jedi/pull/2113) · Oct 2026

**[OpenBot](https://github.com/CopilotKit/OpenBot)** · a template for running your own agent bots, built to be cloned and made your own

I stopped a malformed percent-escape in a stream URL from crashing the server with a 500; it now falls through to normal routing. [merged in CopilotKit/OpenBot#699 →](https://github.com/CopilotKit/OpenBot/pull/699) · Oct 2026

I made the provider and Bot registries ignore inherited keys like `constructor` and `__proto__`, so a missing Bot name hits the existing startup error instead of returning undefined fields. [merged in CopilotKit/OpenBot#697 →](https://github.com/CopilotKit/OpenBot/pull/697) · Oct 2026

**[magpie](https://github.com/yetone/magpie)** · every agent's model, one place - Codex on DeepSeek, Claude Code on Kimi, from the menu bar

I stopped Gemini ANY mode and Responses allowed_tools from leaking the full tool list, so an allowed subset stays a subset. [merged in yetone/magpie#164 →](https://github.com/yetone/magpie/pull/164) · Sep 2026

I made Gemini VALIDATED mode filter declarations down to the allowed list on translated routes, so the model only sees tools it may call. [merged in yetone/magpie#170 →](https://github.com/yetone/magpie/pull/170) · Sep 2026

I made a required tool choice that filters down to nothing callable fail with a clear 400, instead of a silent plain-text 200 the caller never asked for. [merged in yetone/magpie#169 →](https://github.com/yetone/magpie/pull/169) · Sep 2026

**[openmuse](https://github.com/CopilotKit/openmuse)** · a personal agent with a browser, terminal, files, and work that keeps going

I fixed a race where the server and worker starting together on a fresh data directory could crash on the session-signing key; the key is now published with an atomic hard link and the loser reads the winner's. [merged in CopilotKit/openmuse#125 →](https://github.com/CopilotKit/openmuse/pull/125) · Oct 2026

I stopped one bad attachment filename with an unpaired surrogate from breaking the whole Gmail inbox listing and from failing sends, by replacing the bad character before encoding. [merged in CopilotKit/openmuse#121 →](https://github.com/CopilotKit/openmuse/pull/121) · Oct 2026

I made the spending analysis reject a CSV with a repeated `date`, `description`, `amount` or `category` header, so it no longer silently reports one of two conflicting amounts. [merged in CopilotKit/openmuse#114 →](https://github.com/CopilotKit/openmuse/pull/114) · Oct 2026

**[OpenDots](https://github.com/CopilotKit/OpenDots)** · your always-on AI coworkers that move between text, calls, and Slack

I made the server accept the key name the Copilotkit CLI writes, `CPK_INTELLIGENCE_API_KEY`, as well as `INTELLIGENCE_API_KEY`, so setup no longer stays incomplete after a successful CLI login. [merged in CopilotKit/OpenDots#72 →](https://github.com/CopilotKit/OpenDots/pull/72) · Oct 2026

I stopped a store error in the background runner's scheduler tick from rejecting unhandled and taking down the always-on server; later ticks now keep running. [merged in CopilotKit/OpenDots#12 →](https://github.com/CopilotKit/OpenDots/pull/12) · Oct 2026

I made the Dot turn that runs past the 90 second limit end with a clear time-limit error instead of an incomplete stream blamed on the runtime connection. [merged in CopilotKit/OpenDots#85 →](https://github.com/CopilotKit/OpenDots/pull/85) · Oct 2026

I made the "Ready for your review" card render Markdown tables as tables instead of raw pipe text, by adding GFM support. [merged in CopilotKit/OpenDots#78 →](https://github.com/CopilotKit/OpenDots/pull/78) · Oct 2026

I made a WebRTC voice call wait five seconds on `disconnected` before hanging up, so a short network blip that recovers no longer ends the call; `failed` still ends it at once. [merged in CopilotKit/OpenDots#26 →](https://github.com/CopilotKit/OpenDots/pull/26) · Oct 2026

I made the red connection banner clear once polling recovers after an API restart; action errors still need a dismiss. [merged in CopilotKit/OpenDots#73 →](https://github.com/CopilotKit/OpenDots/pull/73) · Oct 2026

I made an unknown or foreign page conversation id return a 404 instead of a generic 503 that blamed the Intelligence setup; real Intelligence errors still return 503. [merged in CopilotKit/OpenDots#14 →](https://github.com/CopilotKit/OpenDots/pull/14) · Oct 2026

I stopped a failed voice compute from staying in the cache and using up one of the six turns, so retrying with the same `toolCallId` can now succeed. [merged in CopilotKit/OpenDots#13 →](https://github.com/CopilotKit/OpenDots/pull/13) · Oct 2026

**[urwid](https://github.com/urwid/urwid)** · console user interface library for Python

I stopped `ListBox` from rendering the same items repeatedly when a short list sits on a wrapping walker, by tracking visited positions so each fill pass stops at one it has already seen. [merged in urwid/urwid#1381 →](https://github.com/urwid/urwid/pull/1381) · Oct 2026

**[pydeps](https://github.com/thebjorn/pydeps)** · python module dependency graphs

I stopped `--externals foo` from dropping `foobar`, so packages that share a name prefix with the target stay in the output while `foo.internal` stays internal. [merged in thebjorn/pydeps#290 →](https://github.com/thebjorn/pydeps/pull/290) · Oct 2026

I made pydeps warn when a dependency diagram comes out with no edges, naming the target and pointing to filters, `--include-missing` and debug logging, instead of silently drawing a blank graph. [merged in thebjorn/pydeps#291 →](https://github.com/thebjorn/pydeps/pull/291) · Oct 2026

**[simplejson](https://github.com/simplejson/simplejson)** · simple, fast, extensible JSON encoder and decoder for Python

I made `check_circular` catch cycles that run through a custom `for_json()` or `_asdict()`, so a self-returning object raises the usual circular-reference error instead of exhausting recursion, in both the Python and C encoders. [merged in simplejson/simplejson#390 →](https://github.com/simplejson/simplejson/pull/390) · Oct 2026

**[filesystem_spec](https://github.com/fsspec/filesystem_spec)** · a specification that python filesystems should adhere to

I made `DirFileSystem` report async support from the filesystem it wraps, so a directory view over a synchronous backend no longer claims `async_impl`. [merged in fsspec/filesystem_spec#2213 →](https://github.com/fsspec/filesystem_spec/pull/2213) · Oct 2026

I made `DirFileSystem` forward the `local_file` flag of the filesystem it wraps, so a directory view over local files passes the `open_local` check instead of failing it. [merged in fsspec/filesystem_spec#2212 →](https://github.com/fsspec/filesystem_spec/pull/2212) · Oct 2026

**[bottleneck](https://github.com/pydata/bottleneck)** · fast NumPy array functions written in C

I made the reducer memory test measure retained allocations with tracemalloc instead of process peak RSS, so unrelated growth stops failing it and a real leak can't hide under an old peak. [merged in pydata/bottleneck#602 →](https://github.com/pydata/bottleneck/pull/602) · Oct 2026

**[typesafe-computer-use](https://github.com/awlevin/typesafe-computer-use)** · browser agents should read the page, not just the buttons

I gave the browser loop the visible text it was missing, so Jev can see a price or error before calling the job done. [merged in awlevin/typesafe-computer-use#23 →](https://github.com/awlevin/typesafe-computer-use/pull/23) · Sep 2026

**[pydantic-extra-types](https://github.com/pydantic/pydantic-extra-types)** · extra Pydantic types

I made card number validation check the Verve ranges before the broader Discover prefix, so a Verve card in 650002 to 650027 no longer reports as Discover and a 17-digit one is rejected. [merged in pydantic/pydantic-extra-types#429 →](https://github.com/pydantic/pydantic-extra-types/pull/429) · Oct 2026

I made `S3Path` keep newlines in object keys, so a key with a newline in its prefix is no longer silently trimmed to a different last key. [merged in pydantic/pydantic-extra-types#430 →](https://github.com/pydantic/pydantic-extra-types/pull/430) · Oct 2026

I let `DomainStr` accept internal hyphens in punycode top-level domains, so delegated TLDs like `xn--vermgensberater-ctb` stop being rejected. [merged in pydantic/pydantic-extra-types#431 →](https://github.com/pydantic/pydantic-extra-types/pull/431) · Oct 2026

**[opencompany](https://github.com/tinyhumansai/opencompany)** · run a hive mind of agents to focus on a specific goal

I removed the dead `ChannelAdapter::inbound()` stream that every adapter stubbed with an empty stream and nothing read, so the trait is now an honest outbound-only sink; a deprecated default keeps out-of-tree adapters compiling. [merged in tinyhumansai/opencompany#2408 →](https://github.com/tinyhumansai/opencompany/pull/2408) · Oct 2026

I made the reserved-path test expect the right status for `/acp` (404 without the feature, 405 with it) and added the missing CI lane for `server::routes`, so the check that only failed on unscoped runs now runs in CI. [merged in tinyhumansai/opencompany#2410 →](https://github.com/tinyhumansai/opencompany/pull/2410) · Oct 2026

I stopped the empty-retry from sending the user message twice: on retry the agent reloaded the failed turn's saved transcript and re-added the message, so I suppress that autoload on the retry and added regression tests. [merged in tinyhumansai/opencompany#2421 →](https://github.com/tinyhumansai/opencompany/pull/2421) · Oct 2026

I made a setup answer cut off by the output limit report that instead of "model unreachable", and raised the setup output budget from 1,500 to 4,000 tokens so a reasoning model can think and still answer. [merged in tinyhumansai/opencompany#2556 →](https://github.com/tinyhumansai/opencompany/pull/2556) · Oct 2026

I gave a setup run that stops on the output limit its own fallback reason, `output_budget_exhausted`, and both setup screens now say the model ran out of output room and offer a retry. [merged in tinyhumansai/opencompany#2562 →](https://github.com/tinyhumansai/opencompany/pull/2562) · Oct 2026

**[click-repl](https://github.com/click-contrib/click-repl)** · subcommand REPL for click apps

I stopped `import click_repl` from crashing when stdin is unavailable (`sys.stdin` is `None`), by treating that as non-interactive and keeping the `isatty()` check for a real stream. [merged in click-contrib/click-repl#140 →](https://github.com/click-contrib/click-repl/pull/140) · Oct 2026

<details>
<summary><b>more magpie fixes</b> · the other twenty-one merged PRs</summary>

**[magpie](https://github.com/yetone/magpie)** · every agent's model, one place - Codex on DeepSeek, Claude Code on Kimi, from the menu bar

I made Gemini PDFs and audio survive text-only routes, so Magpie no longer treats every file part as an image. [merged in yetone/magpie#95 →](https://github.com/yetone/magpie/pull/95) · Sep 2026

I stopped a reply translated from a dying gateway stream from reading as complete, so a dead upstream can't pass a cut-off answer off as finished. [merged in yetone/magpie#78 →](https://github.com/yetone/magpie/pull/78) · Sep 2026

I stopped group images from being retried on text-only fallbacks, so a vision failure skips them instead of mangling the picture into text. [merged in yetone/magpie#87 →](https://github.com/yetone/magpie/pull/87) · Sep 2026

I cleared the 400 on Responses images referenced by file_id, so stored images survive translation to Chat routes. [merged in yetone/magpie#166 →](https://github.com/yetone/magpie/pull/166) · Sep 2026

I fixed usage accounting for SSE events split across data lines or missing a trailing newline, so streamed token counts stop vanishing. [merged in yetone/magpie#94 →](https://github.com/yetone/magpie/pull/94) · Sep 2026

I fixed the Codex prompt cache so two accounts saving in the same mtime tick both keep their instructions. [merged in yetone/magpie#74 →](https://github.com/yetone/magpie/pull/74) · Sep 2026

I made the long-turn router count providers hidden from the model picker, so a growing turn no longer stays pinned to the small model. [merged in yetone/magpie#86 →](https://github.com/yetone/magpie/pull/86) · Sep 2026

I stopped disabled keys from being fetched during model refresh, with a regression test proving zero requests to them. [merged in yetone/magpie#76 →](https://github.com/yetone/magpie/pull/76) · Sep 2026

I gave Gemini's session-affinity fallback a hash of the conversation to stick to, so keyless requests stop scattering across upstreams. [merged in yetone/magpie#165 →](https://github.com/yetone/magpie/pull/165) · Sep 2026

I kept Gemini session affinity when the first turn omits its role, treating it as the user turn Gemini says it is. [merged in yetone/magpie#171 →](https://github.com/yetone/magpie/pull/171) · Sep 2026

I stopped a multi-choice Chat stream from being flattened into one reply, so translation keeps the first readable choice instead of joining the rest. [merged in yetone/magpie#168 →](https://github.com/yetone/magpie/pull/168) · Sep 2026

I fixed the `TestSmartRouting` hour-boundary flake by anchoring its reset fixture within one hour, so the five-hour tie-breaker stays deterministic. [merged in yetone/magpie#77 →](https://github.com/yetone/magpie/pull/77) · Sep 2026

I kept YAML top-level strings as strings, so a model named like `null` or `true` is no longer read back as nil or bool, and single-quoted values with escaped quotes now decode whole. [merged in yetone/magpie#431 →](https://github.com/yetone/magpie/pull/431) · Oct 2026

I kept large integers exact in the Cursor gateway's tool history, so IDs and results above 2^53 are no longer rounded when a call is replayed or its result is stored. [merged in yetone/magpie#434 →](https://github.com/yetone/magpie/pull/434) · Oct 2026

I stopped inline comments from leaking into dotenv values in two readers, so `GEMINI_API_KEY=abc123 # my key` reads back as the key alone while quoted values keep their `#`. [merged in yetone/magpie#439 →](https://github.com/yetone/magpie/pull/439) · Oct 2026

I made the Kimi model picker read TOML literal-quoted keys like `[models.'kimi k2.5']`, so models with spaces in their names stop being silently skipped. [merged in yetone/magpie#446 →](https://github.com/yetone/magpie/pull/446) · Oct 2026

I escaped backslashes when quoting dotenv values on write, so a Windows path like `C:\new folder\tmp` round-trips instead of reading back with a newline and a tab. [merged in yetone/magpie#450 →](https://github.com/yetone/magpie/pull/450) · Oct 2026


I kept a CRLF file's line endings when the dotenv, TOML and top-level YAML setters add or replace lines, so a Windows config file no longer comes back with bare `\n` on every edited line. [merged in yetone/magpie#829 →](https://github.com/yetone/magpie/pull/829) · Oct 2026

I did the same for JSON and JSONC edits, so `SetJSON` on a CRLF file keeps `\r\n` on the lines it adds. [merged in yetone/magpie#830 →](https://github.com/yetone/magpie/pull/830) · Oct 2026

I did the same for the YAML round trip, so `SetYAML`, `DelYAML` and `EditYAMLStrings` no longer rewrite every line of a CRLF file as LF. [merged in yetone/magpie#831 →](https://github.com/yetone/magpie/pull/831) · Oct 2026

I made a dotenv key that appears twice read and write its last line, as dotenv does, so wiring Gemini CLI to the gateway edits the line the CLI actually uses. [merged in yetone/magpie#832 →](https://github.com/yetone/magpie/pull/832) · Oct 2026

</details>

---

## the scenic route to main

I stopped Hermes compression from copying long user messages into summaries; the maintainer carried my fix into the merged PR, with credit in its history. [merged via NousResearch/hermes-agent#124966 →](https://github.com/NousResearch/hermes-agent/pull/124966) · Sep 2026

I traced why Anthropic tool_result images died with a 400 on Chat translation; the maintainer shipped his own version of the fix in v0.1.348, crediting the find in the commit message. [fixed via yetone/magpie@504b470 →](https://github.com/yetone/magpie/commit/504b470f127c05a805093ada144e11b58376ddb0) · Sep 2026

I made unanswered user text survive the next turn's persist override; after my PR was closed unmerged, the maintainer carried all four of my commits to main with authorship intact. [merged via NousResearch/hermes-agent#126615 →](https://github.com/NousResearch/hermes-agent/pull/126615) · Sep 2026

I kept clarify and connection cards open for /btw side tasks; the maintainer's expanded take (/bg too, plus an attachment guard) carried two of my commits to main and co-credited me on his. [merged via NousResearch/hermes-agent#127051 →](https://github.com/NousResearch/hermes-agent/pull/127051) · Sep 2026

I made scaffold generation read the vendored AIP specs instead of the sibling checkout; another contributor's PR carried the approach to main, crediting it in the description. [merged via agentproto/ts#1622 →](https://github.com/agentproto/ts/pull/1622) · Sep 2026

---

## what I'm curious about

**01** Where does the latency actually go?  
**02** What should an AI system remember - and prove it remembered from the source?  
**03** When is a forecast wrong because of the model, and when because of the place?  
**04** Why do technically good products still fail distribution?  
**05** Which problems are worth automating, and which only look that way?

---

## things I've built

**[IntelliRAG](https://github.com/charan-rathore/IntelliRAG)**  
*I wanted to know where RAG actually breaks.*

ingestion → chunking → hybrid retrieval → rerank → citations → evaluation → observability  
The live browser lab exposes issue ingestion, cited retrieval traces and a lexical knowledge graph. The public demo currently uses temporary keyword/extractive mode; persistent hybrid retrieval and real-provider evaluation are next. The Python platform has separate deterministic CI benchmarks.

Graph-first vector retrieval with weighted shortest-path ranking is now in main ([PR #9](https://github.com/charan-rathore/IntelliRAG/pull/9)).

[try the live lab →](https://intellirag-live-own-track.vercel.app/) · [read the measured audit →](https://github.com/charan-rathore/IntelliRAG/blob/main/audit/REPORT.md)

**[memoRABLE](https://github.com/charan-rathore/memoRABLE)**  
*What if documents became memory?*

Six source-linked blocks. Click a memory, the original lines light up. Publish once to email / web / doc without rewriting the truth. Local-first.

[try it →](https://memo-rable.vercel.app)

**[ThermoSense](https://github.com/charan-rathore/Time-Series-Temperature-Modelling)** · hyperlocal temperature forecasting  
*Can a forecast know your rooftop?*

Ground truth → commercial API bias → ensemble forecast → public leaderboard → retrain. The product is the loop, not the model name.

[see the experiment →](https://thermosense-black.vercel.app)

**[Finsight](https://github.com/charan-rathore/agentic-finance-advisor)**  
*Can an AI answer also explain how much it should be trusted?*

Multi-agent research with freshness, source agreement, versioned knowledge, and a confidence score you can inspect.

[inspect the system →](https://github.com/charan-rathore/agentic-finance-advisor)

**[infer-tab](https://github.com/charan-rathore/infer-tab)**  
*What changes between prefill and decode?*

CPU-only KV-cache experiments write traces of attention arithmetic and tensor bytes; a Next.js visualizer replays them. No model download needed.

[run the experiments →](https://github.com/charan-rathore/infer-tab#quick-start)

---

## receipts

| Work | One thing you can check |
| --- | --- |
| [IntelliRAG](https://github.com/charan-rathore/IntelliRAG) | 31 live browser questions in the [audit](https://github.com/charan-rathore/IntelliRAG/blob/main/audit/REPORT.md); RAGAS-style rubric, not an official RAGAS score. |
| [memoRABLE](https://github.com/charan-rathore/memoRABLE) | Six source-linked memory blocks with click-through to the original lines. |
| [ThermoSense](https://github.com/charan-rathore/Time-Series-Temperature-Modelling) | Live dashboard and a public forecast leaderboard. |
| [infer-tab](https://github.com/charan-rathore/infer-tab) | CPU-only KV-cache / prefill-decode traces, replayed in a Next.js visualizer. |
| [magpie](https://github.com/yetone/magpie) | Twenty-four merged PRs: [#74](https://github.com/yetone/magpie/pull/74), [#76](https://github.com/yetone/magpie/pull/76), [#77](https://github.com/yetone/magpie/pull/77), [#78](https://github.com/yetone/magpie/pull/78), [#86](https://github.com/yetone/magpie/pull/86), [#87](https://github.com/yetone/magpie/pull/87), [#94](https://github.com/yetone/magpie/pull/94), [#95](https://github.com/yetone/magpie/pull/95), [#164](https://github.com/yetone/magpie/pull/164), [#165](https://github.com/yetone/magpie/pull/165), [#166](https://github.com/yetone/magpie/pull/166), [#168](https://github.com/yetone/magpie/pull/168), [#169](https://github.com/yetone/magpie/pull/169), [#170](https://github.com/yetone/magpie/pull/170), [#171](https://github.com/yetone/magpie/pull/171), [#431](https://github.com/yetone/magpie/pull/431), [#434](https://github.com/yetone/magpie/pull/434), [#439](https://github.com/yetone/magpie/pull/439), [#446](https://github.com/yetone/magpie/pull/446), [#450](https://github.com/yetone/magpie/pull/450), [#829](https://github.com/yetone/magpie/pull/829), [#830](https://github.com/yetone/magpie/pull/830), [#831](https://github.com/yetone/magpie/pull/831), [#832](https://github.com/yetone/magpie/pull/832). |
| [openmuse](https://github.com/CopilotKit/openmuse) | [#45](https://github.com/CopilotKit/openmuse/pull/45) fixes duplicate artifacts on interrupted file steps - open, awaiting merge. |

---

## product things I keep taking apart

**Search** - what actually happens between a query and the ranked result (Flipkart search personalization was the first place this got real for me)  
**Funnels** - where discovery leaks: the step users drop, not the dashboard average  
**Trust UX** - when a product should show confidence, provenance, or “I don’t know yet”  
**Distribution** - why a technically solid system still fails to get used  
**The invisible middle** - [the 2 seconds you never see](https://charanrathore.substack.com/p/the-2-seconds-you-never-see): auth, memory, routing, the work that makes complexity feel effortless

I go system → product → business. Same habit: open the black box, name the failure mode, then decide what to ship.

---

## one thing I wrote

**[The 2 seconds you never see](https://charanrathore.substack.com/p/the-2-seconds-you-never-see)**  
I thought I knew what happened after you hit enter. I was wrong.

More when I have something worth saying → [Substack](https://charanrathore.substack.com)

---

## how I work

measure → build → break → learn → repeat

Write the tradeoff down. Keep eval next to the code. Prefer systems that fail in known ways. Same rule for product: if I can’t explain the funnel step, I don’t trust the feature yet.

---

## currently investigating

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
  <a href="https://charan-tetris-portfolio.vercel.app/">Portfolio</a>
  ·
  <a href="mailto:ra7hore.charan@gmail.com">Email</a>
</p>

<sub>BITS Pilani · dual degree · class of 2026 · MiQ analyst, MENA · ex-Flipkart product analytics<br>
Older experiments stay public. The four above are the ones that still feel like me.</sub>
