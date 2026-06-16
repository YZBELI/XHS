---
name: theme-picturebook-xhs
description: Create Xiaohongshu-ready children's picturebook prompt packages from user-provided themes such as festivals, animals, plants, seasons, emotions, nature, or daily-life topics. Use when the user asks to generate a complete picturebook story for ages 3-8 with fixed long-term IP characters, consistent character visuals, storyboard pages, character-reference/cover/interior image prompts, very bright luminous healing watercolor picturebook style, Xiaohongshu title/copy/tags, and a Word document deliverable. Generate actual images only when the user explicitly asks for image generation.
---

# Theme Picturebook XHS

## Overview

Create a complete themed children's picturebook prompt package for Xiaohongshu publishing. Start from the user's theme, interpret it from multiple child-friendly dimensions, build a story around the fixed long-term IP characters, then produce storyboard pages, character-reference prompt, cover prompt, interior page prompts, and publish-ready Xiaohongshu copy in a Word document.

Default package: one Word document named from the user's theme, containing only the story title, full story, character reference image prompt, cover prompt, at least 12 interior page prompts, Xiaohongshu-ready title and intro, body copy, and tags. Keep supporting planning work internal unless the user explicitly asks to include it. Treat 12 interior pages as the minimum, not the target. Let the story choose the page count, commonly 14, 16, 18, or 20 pages when the premise needs more setup, attempts, emotional change, or a softer transition, while keeping the structure publishable as a Xiaohongshu image sequence.

Prompt length default: write image prompts in compact production mode. Keep the visual result stable while reducing repeated wording. Do not paste the full style bible, full character lock sheet, or long negative list into every prompt. Use short reusable wording: one compact style sentence, abbreviated anchors only for visible characters, the page-specific action/composition, exact in-image text/page-number rules, and a compact negative constraint. Expand prompts only when the user asks for detailed prompts or when image generation repeatedly fails because a necessary detail was too compressed.

## Required References

Load these files before producing a real package:

- `references/story_rules.md`: multi-dimensional theme interpretation, light educational facts, audience adaptation, character consistency, story structure, and storyboard rules.
- `references/ip_bible.md`: fixed world, recurring characters, visual anchors, relationship dynamics, and forbidden drift.
- `references/prompt_publish_rules.md`: image prompt standards, visual styles, image generation workflow, file package rules, and Xiaohongshu publishing copy.

## Input Handling

If the user only gives a theme, proceed with these defaults:

- Audience: children ages 3-8.
- Role mode: use the fixed long-term IP characters in `references/ip_bible.md`; do not create a new lead cast for each theme.
- Length: cover + 12 interior pages minimum; expand to 14, 16, 18, or 20 interior pages when needed for natural story rhythm. Do not compress a story into 12 pages if the setup, attempts, turning point, or ending would feel rushed.
- Format: portrait 3:4 for Xiaohongshu image posts.
- Style: soft transparent watercolor children's picturebook by default. Use this compact style line in generated prompts unless more detail is needed: `柔和透明水彩儿童绘本风，治愈手绘，淡彩叠色，湿画法晕染，干净纸纹，细腻线稿，明亮高调，低对比柔光，粉蓝/奶油白/浅绿/柔粉为主，少量暖橙点缀，清新安全、低视觉噪点。` Keep dappled shadows, mottled leaf shadows, speckled light, and broken shadow patterns extremely light and local; they must not dominate the picture, cover faces, obscure page text, or create a busy/noisy surface. Avoid muddy colors, heavy oil-paint texture, dim lighting, brown/orange dominance, gray haze, dark dramatic contrast, high-contrast dappled shadows, or dense speckled shadow texture unless the user explicitly asks.
- Output depth: generate prompts and a Word document by default. Do not call `imagegen` or any image generation tool unless the user explicitly asks to generate images.

If the user provides multiple themes separated by the Chinese enumeration comma `、`, treat each segment as a separate theme. Create one independent story, prompt package, Xiaohongshu copy set, and Word `.docx` file for each theme. Use each theme as its own Word filename.

Ask at most 3 clarifying questions only when the missing choice materially changes the output, such as changing the fixed IP, changing the page count beyond the default, or using a non-child audience.

## Workflow

1. Interpret the theme from multiple dimensions and identify the audience, emotional value, parent-facing appeal, safety concerns, light educational facts, and the most visual story hook.
2. Create a theme knowledge card before writing the story. For plant themes, include name origin or alias when known, flowering/fruiting period, appearance, scent, growth habit, habitat, child-observable details, and cultural associations. For other themes, choose equivalent age-appropriate dimensions.
3. Select 2-4 facts from the knowledge card that can naturally become story events, dialogue, discoveries, or repeated visual motifs. Do not turn the book into a fact list.
4. Load the fixed IP bible and choose 2-3 recurring characters as the main cast for the current theme. Use 4 only when the story genuinely needs it.
5. Create a character lock sheet before writing image prompts. Include name, species/type, age feeling, silhouette, colors, face features, clothing or signature prop, personality, expression range, allowed theme props, and forbidden drift.
6. Write the full story before splitting pages. Include a child-scaled wish or question, a gentle obstacle, 2-3 attempts that change the character's understanding, a foreshadowed turning point, climax, resolution, and a warm takeaway. Avoid sudden reversals; each turn must grow from an earlier object, clue, promise, mistake, or emotion. Run a plausibility pass before page splitting: the problem, attempts, turning point, and solution must feel like natural consequences of the characters' earlier choices and the theme facts, not a forced moral, coincidence, or abrupt lesson.
7. Convert the full story into a story-beat allocation plan before writing page text. Each beat must answer: what changed from the previous beat, what caused this change, what the current page shows, why the next page naturally follows, and what small question or feeling pulls the child reader forward.
8. Split the story into causally connected interior pages, expanding the count when the rhythm feels rushed and merging adjacent beats when their picture content would be nearly identical. Each page must move the story forward, show an imageable moment, include child-readable page text, include a visible lower-right page number, and include explicit continuity with the previous and next page. Page text must accurately describe the story content shown on that page rather than act as a vague caption. Prefer two to three short child-readable sentences, or three to four short lines, when needed to explain the action, emotion, cause, or transition. If two adjacent beats have very high visual overlap and no meaningful composition change, combine them into one page instead of producing two near-duplicate images; in that combined page, include two separate page-text sentences and place the two text blocks in different quiet areas of the image.
9. Create a cover concept that makes the theme recognizable at Xiaohongshu thumbnail size. The cover must include the story title as visible text wrapped in Chinese book-title brackets, such as `"《故事名》"`, placed upper-center with artistic lettering.
10. Create image prompts for the character reference sheet, cover, and each interior page in compact production mode. Each prompt should usually be 5 compact parts in this order: format and compact style line; abbreviated visual anchors for visible characters only; page-specific composition/action/emotion; exact in-image text and page-number placement; compact negative constraint. Do not repeat the full style bible or full lock sheet on every page. Keep only the visual details that protect consistency: 小暖's hairpin, dress, notebook bag; 团团's bear shape, honey-brown body, cream muzzle/belly, moss-green scarf with yellow stitch; 芽芽's thumb size, pale-green body, two sprouts, translucent leaf wings, warm leaf-tip glow. Every interior prompt must still include visible page text that accurately describes what happens on the page and the exact lower-right Arabic page number such as `"1"`, `"2"`, or `"3"`. Reserve a quiet text area and require uniform same-size characters within each sentence.
11. Do not call `imagegen` by default. Only use the `imagegen` skill when the user explicitly asks to generate images, such as "生成图片", "开始生图", or "调用 imagegen". If image generation is requested, generate a character reference sheet first, then cover and interior pages. Generate at least two candidate images for every requested image target, including character reference, cover, and each interior page; if the image tool cannot produce two in one call, run separate attempts. QA all candidates, discard failed candidates, and show or package at least two passing options whenever possible so the user can choose the better one. Image generation can take a long time, so allow extended waiting and multi-round QA/regeneration instead of treating slow generation as a failure. Inspect each image for brighter healing style, character consistency, theme visibility, 3:4 composition, style consistency, exact intended text, correct lower-right page number, consistent text size within each sentence, and unwanted pseudo-text. An interior image without readable page text, without the correct lower-right page number, with a dull/dark/muddy visual style, or with any other QA failure must be regenerated or corrected before delivery. Do not display failed generated images to the user; only show final images that pass QA.
12. Produce Xiaohongshu copy: one unified-format main title, one short intro, body copy, tags, image order, and upload checklist. The main title may use an emoji for appeal but must follow the required format.
13. Use the Documents plugin to create a Word `.docx` file named from the user's theme. The Word file must include only the story title, full story, character reference image prompt, cover image prompt, every interior page image prompt, Xiaohongshu main title and short intro, body copy, and tags. Do not include theme interpretation, knowledge cards, safety notes, role mode notes, character lock sheets, beat allocation, cover concept, global visual style, publishing file lists, upload checklists, or other supporting planning sections in the Word document unless the user explicitly asks to include them. Follow the Documents skill render-and-verify workflow for the DOCX when available. If the theme contains filename-unsafe characters, keep the visible title unchanged inside the document and use the closest filesystem-safe filename. For multiple `、`-separated themes, create one separate `.docx` per theme.
14. Package the default output as `<用户主题>.docx`, or multiple `.docx` files when multiple themes are provided. Only package `character-reference.png`, `cover.png`, and `page-01.png` through the final page number when the user explicitly asks for image generation.

## Output Contract

Write only these sections into the Word document in order. Keep all other planning notes internal unless the user asks to include them. By default, the chat response should only provide a concise summary and a link to the `.docx` file, unless the user asks to see the full text in chat.

1. `故事名`
2. `完整故事`
3. `角色参考图像提示词`
4. `封面图像提示词`
5. `内页图像提示词`
6. `小红书主标题与简介`
7. `小红书正文`
8. `标签`

If the user asks for a shorter draft, include only the requested sections, but keep character lock and story continuity internally consistent.

## Non-Negotiables

- Use the fixed long-term IP characters for children's picturebooks. Do not replace the core cast unless the user explicitly asks to redesign the IP.
- Keep characters consistent across all pages by repeating the same visual anchors.
- Do not write disconnected knowledge cards; every page must be a story beat.
- Do not create independent page ideas first. Always create the complete story, then allocate that story into connected page beats.
- Do not force every story into exactly 12 interior pages. Use more pages when a child reader needs more time to understand the setup, repeated attempts, emotional turn, or ending.
- Do not use abrupt twists, unexplained rescues, forced morals, coincidence-only solutions, or hard transitions. Turning points must be prepared by earlier visual clues, character choices, repeated motifs, emotional changes, or simple theme facts. If the story would require a narrator to explain why the solution suddenly works, rewrite the middle and setup before making prompts.
- Do not make page text so sparse that the image becomes hard to understand. Interior page text should usually be fuller than a caption: use enough child-readable words to name the visible action, feeling, cause, or next transition accurately, while keeping the wording easy to read aloud and fit naturally in the picturebook layout.
- Do not create two separate interior pages when the adjacent story beats would produce almost the same image, camera angle, character pose, and background. Merge those beats into one page, keep the story causality clear, and place two separate page-text sentences in staggered quiet areas of the image.
- Do not proactively call image generation tools. Default output is a complete prompt package in Word format; generate actual images only when the user explicitly asks for image generation.
- When the user provides multiple themes separated by `、`, generate multiple independent Word files, one per theme. Do not merge multiple themes into one Word file unless the user explicitly asks.
- Interpret the theme from multiple dimensions before writing. Include light educational value, but embed facts into the story through action, discovery, dialogue, or visual motifs.
- Treat all intended in-image text as exact production text. Transcribe it character-for-character, wrap every intended string in English double quotes, and describe placement, size, material, font style, and layout when text appears on covers, signs, labels, screens, posters, menus, UI, maps, charts, or any self-added visual element.
- The cover image must include the exact story title text wrapped in Chinese book-title brackets, for example `"《七里香的秘密香气》"`, positioned upper-center, using readable artistic title lettering.
- Every interior image must include visible page text that accurately describes the current story action, action change, emotional shift, or story transition. Keep each sentence child-readable, concrete, and placed in a quiet area of the composition; do not reduce the page text to a generic label when the scene needs context. When a page intentionally combines two visually overlapping beats, include two exact quoted sentences and specify clearly staggered placements for them. Within one sentence, every Chinese character must have the same size, weight, style, and baseline; do not use mixed-size characters, decorative emphasized words, jumping letters, or uneven typography.
- Every interior image must include its exact Arabic page number in the lower-right corner, starting at `"1"` for the first interior page and continuing sequentially. Do not put a page number on the cover. Treat page numbers as exact intended text with specified placement, size, color, and style.
- Never show failed generated images to the user. Failed images may be inspected internally for QA, but user-facing previews, final responses, and output packages must include only images that pass QA or clearly mark unresolved failures without displaying the failed image.
- Create a Word document by default using the Documents plugin. The user's theme is the Word filename, and the document must include only the story title, full story, character reference image prompt, cover image prompt, all interior image prompts, Xiaohongshu main title and short intro, body copy, and tags unless the user explicitly asks for additional planning or publishing sections.
- Keep the story suitable for ages 3-8 unless the user explicitly asks for a different audience.
- Adapt scary, violent, death-related, disaster, disease, or punishment-heavy topics into care, observation, imagination, recovery, or gentle problem-solving.
- Do not imitate a living artist by name. Use broad style terms such as soft transparent watercolor children's picturebook, healing hand-drawn illustration, light fairy-tale feeling, pastel layered color, wet-on-wet watercolor blooms, delicate hand-drawn linework, warm natural atmosphere, bright high-key color, clean paper texture, and low-contrast cozy shadows. Avoid heavy painterly texture unless the user explicitly asks for it.
- Do not let dappled shadows, mottled leaf shadows, speckled light, paper grain, or texture noise become a dominant visual element. For children's picturebook prompts, keep shadows soft, low-contrast, and secondary to clear characters, clean color blocks, readable expressions, and open text areas.
- Do not make prompts unnecessarily long. Keep the compact style line, compact visible-character anchors, page-specific action, exact text/page number rules, and one compact negative sentence. Avoid repeating synonyms, full personality descriptions, full story rationale, or the entire IP bible in every page prompt.
- When actual image generation is requested, generate at least two QA-passed candidate images per requested image target whenever the tool allows it, and keep candidate naming clear so the user can compare options.
- Allow longer response time during image generation and QA. Do not stop only because generation is slow; keep waiting, checking, and regenerating until the required image set is complete or a real tool failure occurs.
- Keep Xiaohongshu output practical: strong thumbnail cover, honest title, concise body, relevant tags, and clear image order.
- Never auto-publish to Xiaohongshu.
