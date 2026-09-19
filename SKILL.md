---
name: zh-one-page-resume
description: Create, rewrite, or polish Chinese one-page resumes for internships, campus recruiting, or early-career applications. Use when the user asks for a Chinese resume, resume tailoring, JD customization, one-page control, less filler, more quantified results, HTML/PDF resume layout, or formatting that should be exactly one page with little wasted whitespace.
---

# 中文一页简历

## Goal

Produce a Chinese resume that is:
- exactly one page after rendering
- easy to skim in 10 seconds
- visually full but not cramped
- result-oriented, with numbers and methods behind outcomes
- faithful to the user's real resume, portfolio, JD, and source files

Use this skill as the combined method from:
- `resume-master`: Chinese HTML/PDF layout and one-page visual control
- `resume-tailoring`: target-role matching and section prioritization
- `resume-quantifier`: metrics, scale, before/after, and defensible impact

## Source Rules

Read the user's provided resume, portfolio, JD, website, DOCX/PDF, or notes before drafting.

Do not invent:
- companies, titles, dates, tools, awards, metrics, user counts, revenue, or seniority
- results that are not in the source material or reasonably inferable

If a number is inferred from source context, phrase it conservatively, e.g. "累计", "近", "约", "覆盖", "触达".

## Content Strategy

Lead with the user's strongest target-fit evidence, not chronology alone.

For brand, content, marketing, social media, or operations resumes, prioritize:
1. growth metrics: exposure, likes, CTR, saves, conversion proxy, followers, reach
2. method: content framework, channel strategy, workflow, analysis dimensions
3. business relevance: brand tone, KOL/KOC, campaign coordination, competitor insight
4. execution ownership: built from 0, independently owned, coordinated agency/team

Rewrite bullets using:

`Action + object + method/tool/process + measurable result + scale/context`

Examples:
- "搭建 AI 辅助内容流程，围绕基金卖点和投资热点日均产出 50+ 条营销文案，分发至投顾平台，累计带来近 200 万次品牌曝光。"
- "用“情绪共鸣 x 强观点”模型做选题和封面测试，6 个月自然触达 260 万+曝光，产出 3 篇万赞、11 篇千赞内容。"

Avoid:
- "负责", "参与", "协助" as the main verb unless ownership is genuinely limited
- generic claims like "沟通能力强", "学习能力强", "认真负责"
- repeating the same verb pattern across many bullets

## Recommended One-Page Structure

Use 4-6 modules:

1. Header: name, target role, phone, email, portfolio/link
2. Summary: 1 compact paragraph, usually 2-3 rendered lines
3. Metrics strip: 4-5 quantified proof cards if the source supports them
4. Experience: internships or work, strongest first when target-fit requires it
5. Projects / portfolio: only high-signal projects with metrics
6. Skills + education: compact bottom block, not a tall narrow list

For students, always include education. Place it at the bottom unless school/major/GPA is the primary selling point.

## Layout Method

Prefer HTML as the editable source for new visual Chinese resumes, then render to PDF. Use `assets/chinese-resume-template.html` as a starting point when useful.

For DOCX editing, preserve the user's existing content and style. Adjust:
- page margins
- table column widths
- line spacing
- paragraph spacing
- cell padding
- section spacing

Do not rewrite the user's updated text unless they ask.

## Visual Standards

Target A4 one page.

Good density:
- body text: about 13.5-15 px in HTML, or 8-10 pt in dense DOCX layouts depending on font/rendering
- line-height: generally 1.25-1.45
- margins: usually 8-12 mm for HTML/PDF visual resumes
- bottom whitespace: small breathing room is fine; large blank lower third is not

For top summary:
- keep it compact and wide
- avoid narrow columns that force 4-5 short lines
- keep the photo from stealing too much text width

For core skills:
- use a two-column or label-detail grid
- left label narrow, right content wide
- avoid a narrow nested table that wraps every phrase into separate short lines

## Experience Count And Density Presets

Select internships by target-role relevance. Do not force every internship into every version. Use 2-3 internships unless the user requests otherwise, and use reverse chronological order within the experience section.

Choose the preset before drafting:

### Two-internship version

Use a visibly larger, more spacious hierarchy:
- body: 14.4-14.7 px
- line-height: 1.39-1.43
- section title: 16.0-16.3 px
- company/project title: 15.0-15.2 px
- date: 12.8-13.1 px
- item spacing: 2.4-3.0 mm
- bullet spacing: 1.1-1.4 mm

### Three-internship version

Keep it compact but clearly readable:
- body: 13.7-14.0 px
- line-height: 1.38-1.42
- section title: 15.4-15.8 px
- company/project title: 14.2-14.5 px
- date: 12.2-12.6 px
- item spacing: 1.7-2.2 mm
- bullet spacing: 0.8-1.05 mm

Treat company names and project names as scan anchors. They must be larger and heavier than bullet text; do not reuse the body size for these headings.

If a two-internship version is sparse, first add a high-signal, truthful project or an additional relevant result/method bullet. Only then increase vertical rhythm. Do not add a weak third internship merely to fill space.

If a three-internship version is crowded, first remove low-signal bullets and duplicated methods. Do not shrink below the preset merely to preserve every detail.

## Page-Fill Calibration

Calibrate page fill from the latest rendered PDF, not from the HTML or an application preview.

- Target approximately 12-22 mm between the bottommost visible content and the A4 page edge.
- Treat more than 25 mm as visibly underfilled and less than 8 mm as a clipping/printing risk.
- At a known render DPI, calculate: `bottom_blank_mm = blank_pixels / dpi * 25.4`.
- Compare related resume versions at the same DPI and zoom.
- Keep the QR code, education text, and final skills row fully visible; `overflow: hidden` can conceal clipping while the PDF still reports one page.

When underfilled, adjust in this order:
1. add target-relevant evidence already present in the source material
2. enlarge body and company/project headings within the selected preset
3. increase line-height, item spacing, and section rhythm
4. re-render and measure again

When overfilled, reverse that order and remove duplicated or low-signal text before reducing readability.

PDF viewers such as WPS may cache an older rendering when a same-named PDF is overwritten. If the preview appears unchanged, verify the newly rendered PNG or reopen the file. Export a versioned filename when necessary; do not keep enlarging the resume based on a stale viewer screenshot.

## Render And Iterate

Always render before delivery.

For HTML/PDF:
1. Render to PDF with Chrome/headless or the available PDF workflow.
2. Check page count with `pdfinfo` or an equivalent tool.
3. Convert the PDF page to PNG and visually inspect.
4. Measure the bottommost visible content and compare it with the page-fill target.
5. Iterate until it is exactly one page, visually balanced, and free of hidden clipping.

For DOCX:
1. Render DOCX to PNG/PDF with the documents skill renderer.
2. Check page count.
3. Inspect the PNG.
4. Iterate until complete, readable, and exactly one page.

If it overflows:
- first reduce section spacing, line-height, or repeated bullets
- then shorten low-signal content
- avoid making the whole resume unreadably small

If it has too much whitespace:
- increase line-height or section rhythm
- widen narrow text areas before adding filler
- add a metrics strip only when supported by source evidence

## Deliverables

When creating a visual resume, provide:
- editable source: `.html` or `.docx`
- final submission file: `.pdf` when requested or useful

Name outputs clearly with the candidate name and version, e.g. `钟懿_中文一页简历.pdf`.
