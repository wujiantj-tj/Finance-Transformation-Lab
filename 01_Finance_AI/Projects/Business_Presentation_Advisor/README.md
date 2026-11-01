# Business Presentation Advisor

An AI assistant for insight-driven business presentations, developed as part of the [Finance Transformation Lab](https://github.com/wujiantj-tj/Finance-Transformation-Lab).

## What it does

- **Slide title generation:** turns topic-based headings into concise, insight-led action titles.
- **Business insight extraction:** identifies the primary message in charts, tables, and metrics, explains the business implication, and suggests an evidence-based action.
- **Presentation story design:** structures management presentations using the Pyramid Principle, Situation–Complication–Resolution (SCR), and MECE.

## Principles

- Lead with the conclusion, not the topic.
- Use the numbers and facts provided. Never invent data.
- Separate facts, assumptions, and external research.
- Tailor the message to the audience.
- Keep one main message per slide.
- Use company terminology and style guides when supplied.

## Example prompts

1. “Rewrite this slide title for a CFO audience. Here are the chart and key metrics: …”
2. “Extract the primary business insight, explain the so-what, and recommend an action from this data: …”
3. “Build a 10-slide management presentation using the Pyramid Principle and SCR.”

## ChatGPT plugin

The private ChatGPT plugin is available to its owner here:

[Open Business Presentation Advisor in ChatGPT](https://chatgpt.com/plugins/plugins_6ade270ff2448191843acc07b3f5ee6a)

The plugin currently runs in ChatGPT. This GitHub folder documents its purpose and reusable instructions; it does not automatically synchronize with the installed plugin. Access to the private plugin may be limited to the owner or authorized users.

## Project files

- `plugin.json`: plugin package metadata.
- `skills/business-presentation-advisor/SKILL.md`: reusable workflow instructions.

## Scope and limitations

This assistant focuses on slide titles, insight extraction, and presentation structure. It does not automatically access private corporate systems or create a finished PowerPoint unless a suitable tool is separately available. Always check sources, data, and company-specific terminology before using outputs in management decisions.
