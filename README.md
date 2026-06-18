# FAQ

## Usage

**Q: How long does a full run take?**  
A: Roughly 30–60 minutes end-to-end. Stage 1 (Idea) takes ~5 min, Stage 2 (Plan) ~10 min, Stage 3 (Paper) ~20–40 min depending on topic complexity.

**Q: Can I submit multiple topics at the same time?**  
A: No. The system processes one job at a time. If a job is already running, you will see a "server busy" message. Wait for it to finish and try again.

**Q: Do I need to keep the browser open?**  
A: Yes. If you close the browser tab while the pipeline is running, the job will be cancelled. Keep the tab open until you have downloaded your results.

**Q: Can I use a topic in Chinese?**  
A: Yes. Both English and Chinese topics are supported. The pipeline will generate content that matches the language of the topic.

---

## Authentication

**Q: Where do I get a passphrase?**  
A: Contact the maintainer or open a GitHub Issue in this repository to request access.

**Q: What if I don't have a passphrase?**  
A: You can use your own Anthropic API Key instead. Get one at [console.anthropic.com](https://console.anthropic.com). Enter it in the **API Key** field on the main page.

**Q: How much will it cost with my own API key?**  
A: A full pipeline run uses Claude claude-sonnet-4-6 and typically costs **$5–15 USD** in Anthropic API credits, depending on topic length and model responses.

---

## Results

**Q: My job failed halfway. Can I resume it?**  
A: Not currently. Re-submit the same topic to start a fresh run from Stage 1. Stages that already completed are not saved for resumption.

**Q: How long are my results stored?**  
A: Results are stored on the server but storage is not guaranteed long-term. **Download your files immediately after the pipeline completes.**

**Q: The PDF looks incomplete or has placeholder text. What happened?**  
A: This can happen if the writing stage ran out of time or encountered a LaTeX compilation error. The plan and idea outputs (Stages 1–2) are usually still intact and valid.

**Q: Can I get the raw LaTeX source?**  
A: Not through the web interface. Only the compiled PDF is available for download.

---

## Errors

**Q: I see "another job is running" but nothing seems to be happening.**  
A: A previous job may have crashed without releasing the lock. Wait ~5 minutes. If the issue persists, contact the maintainer to restart the server.

**Q: The page loads but clicking Launch does nothing.**  
A: Make sure your passphrase or API key is valid (a green checkmark should appear). Also check that you have filled in a research topic.

**Q: The site is unreachable.**  
A: The service runs on a home server and may be offline. Try again later or open a GitHub Issue.
