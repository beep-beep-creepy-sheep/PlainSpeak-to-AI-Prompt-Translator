# PlainSpeak Prompt Translator

PlainSpeak Prompt Translator is a small static web app that turns plain-language human requests into structured, safer, prompt-engineered instructions. It shows the understood intent, request breakdown, structured prompt, missing information, safety notes, deterministic quality scores, and a JSON prompt-card preview.

The app has two compiler modes:

- Rule-based: deterministic, no setup, no API key.
- Ollama local LLM: calls a local Ollama model for GPT-style intent understanding and prompt rewriting.

It uses no hosted backend, no cloud API key, no build step, and no external frameworks.

## Use it online

Live site: https://beep-beep-creepy-sheep.github.io/Plainspeak-to-ai-prompt-translator/

## Run locally

Open `index.html` directly in a browser.

You can also serve the folder with any static file server, but that is optional.

## Use Ollama mode

1. Install and start Ollama.
2. Pull a model, for example:

```bash
ollama pull qwen2.5:7b
```

3. Make sure Ollama is running at:

```text
http://localhost:11434
```

4. Open the app, set Compiler to `Ollama local LLM`, and choose the model name.

If the GitHub Pages version cannot reach your local Ollama because of browser security rules, run the app locally instead:

```bash
python3 -m http.server 8017
```

Then open:

```text
http://localhost:8017
```

## Deploy with GitHub Pages

1. Push this project to a GitHub repository.
2. In the repository, open Settings.
3. Go to Pages.
4. Set the source to the main branch and the project root.
5. Save, then open the published GitHub Pages URL after deployment finishes.

## Safety limitations

- Use mock or public information only.
- Do not paste confidential data, client identifiers, account numbers, private portfolio holdings, employer-confidential information, or internal documents.
- Do not treat generated text as investment advice.
- Do not rely on AI-generated output without human review.
- Rule-based mode can miss nuance.
- Ollama mode depends on the local model's quality and may still misunderstand vague requests.
- The app does not include jailbreak, bypass, or unsafe prompt examples.

## Future improvements

- Prompt diff view
- Eval case generator
- YAML prompt card export
- Prompt registry integration
