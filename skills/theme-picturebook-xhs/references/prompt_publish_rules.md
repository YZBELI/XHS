# Prompt And Publish Rules

## Visual Style

Default to soft transparent watercolor children's picturebook style with healing hand-drawn illustration:

- high-key bright watercolor washes
- fresh, luminous color with airy whites
- soft brushwork
- gentle healing mood
- rounded child-friendly shapes
- light fairy-tale feeling
- warm natural atmosphere
- pastel layered color
- wet-on-wet watercolor blooms and soft transparent washes
- delicate hand-drawn linework
- warm sunlight, soft glow, and low-contrast cozy shadows
- tactile fine paper texture
- airy, clean composition
- clean pastel palette led by powder blue, cream white, pale green, gentle pink, sky blue, and theme-specific accent colors
- small warm-orange accents for sunlight and coziness, without brown/orange dominance
- soft diffuse daylight instead of harsh directional light
- large calm color areas, clear silhouettes, and uncluttered backgrounds
- very light, low-contrast shadows that support form without becoming decorative noise
- innocent, friendly character expressions
- rounded cute animal or plush forms when animal/plush characters appear
- soft furry texture for plush or animal characters when relevant, kept subtle and hand-painted

Avoid muddy color, dim gray haze, brown/orange dominance, heavy oil-painting texture, dramatic shadows, dark editorial mood, high-contrast dappled shadows, dense mottled leaf shadows, speckled light patterns, noisy paper grain, and busy texture fields. Dappled light may appear only as a very subtle local accent when the scene genuinely needs it, never across character faces, page text, or the main focal object, and never as the dominant surface pattern. Warm oil-painting texture may appear only as a very subtle background influence when the user explicitly wants it; the default should feel brighter, lighter, cleaner, softer, more transparent, and more healing than painterly. Let the user choose or override the style. Do not imitate a living artist by name. If the user names a living artist, translate the request into broad traits such as soft transparent watercolor picturebook, healing hand-drawn children's illustration, delicate linework, airy pastel colors, wet-on-wet watercolor softness, warm natural atmosphere, and low-contrast picturebook light.

## Children's Picturebook Clarity

For every cover and interior image prompt, prioritize low-age readability:

- clean focal hierarchy with one main action per image
- simple readable character poses and facial expressions
- open quiet areas for page text and page numbers
- soft, even lighting with gentle low-contrast shadows
- broad watercolor washes and calm pastel color blocks
- delicate hand-drawn linework that clarifies forms without making the image busy
- friendly rounded characters with innocent expressions
- subtle tactile or furry detail only where it helps character warmth
- limited background detail so characters and theme objects read immediately

Keep mottled shadows and decorative texture below a small visual accent level. If the setting naturally has trees, leaves, curtains, window light, or water reflections, describe them as soft, pale, and sparse. Do not ask for strong leaf shadows, scattered dark spots, high-frequency texture, heavy stippling, or dramatic broken light.

## Global Image Prompt

Default prompt mode is compact production mode. The goal is shorter prompts that keep image stability. Every image prompt should include:

- portrait 3:4
- target audience and picturebook mood
- one compact style line, not the full style bible
- abbreviated anchors for visible characters only
- composition and camera distance
- page-specific action
- quiet text area when text is required
- exact text/page-number rules
- one compact negative constraint

Use Chinese for story and publishing copy. Image prompts may be Chinese or bilingual, but must be precise and repeat character anchors.

Use this compact style line unless the user asks for more detail:

`柔和透明水彩儿童绘本风，治愈手绘，淡彩叠色，湿画法晕染，干净纸纹，细腻线稿，明亮高调，低对比柔光，粉蓝/奶油白/浅绿/柔粉为主，少量暖橙点缀，清新安全、低视觉噪点。`

Use this compact negative line unless a page needs special constraints:

`避免写实恐怖、暗黑、厚重油画、glossy 3D、乱码水印、强斑驳树影、密集叶影、碎斑光点、高频纸纹、重颗粒和高对比破碎光影。`

Use compact character anchors instead of full lock sheets inside ordinary cover and interior prompts:

- 小暖：6岁圆脸黑色波波头女孩，红星发夹，奶油背带裙，栗色内搭，小棕色斜挎笔记本包。
- 团团：小毛绒熊朋友，蜂蜜棕身体，奶油口鼻和肚皮，纽扣眼，苔绿色围巾带黄色缝点。
- 芽芽：拇指大小淡绿叶精灵，两片头顶小芽，透明叶翅，叶尖微弱暖黄光。
- 小舟：7岁短发孩子，丹宁蓝外套，白衫，耳后黄色铅笔，小折尺。

Character reference sheet prompts may be slightly longer than page prompts because they establish continuity, but should still avoid repeating non-visual story logic or long personality descriptions.

## Character Reference Sheet

Create a character reference sheet prompt before cover and pages:

- neutral front view of each main character
- one small expression row per character
- signature prop shown clearly
- no story text
- clean light background
- same style as the final picturebook

Use the reference sheet prompt as the visual consistency anchor. Do not include it in Xiaohongshu upload order unless the user asks.

When actual image generation is requested, create at least two character-reference candidates and QA both for brightness, healing mood, and character consistency before using one as the continuity anchor.

## Text In Images

Before writing any image prompt, decide whether the final image should contain visible text. Treat all intended in-image text as exact production text.

Default for interior illustrations: every interior image must contain visible page text and a lower-right Arabic page number. The page text should accurately describe the page content, action change, emotional shift, or story transition, with enough words for a child to understand what is happening in the picture. Reserve quiet text areas in the composition from the start instead of treating text as an optional overlay. Image models often produce pseudo-text, so keep embedded interior text precise, readable, and tightly specified rather than vague.

If no text should appear, include:

`画面中不要出现任何文字、字母、符号、水印、标识或伪文字。`

If any text should appear in the image:

- Transcribe every intended string character-for-character.
- Wrap every intended string in English double quotes, for example `"七里香开花了"` or `"暖芽小院"`.
- Do not paraphrase, simplify, translate, or silently correct the user's intended text.
- Describe where each text string appears, such as top center, lower right, on a wooden sign, on a notebook page, on a phone screen, or on a shop awning.
- Describe the approximate size and hierarchy, such as title, subtitle, small label, tiny handwritten note, readable sign text, or screen header.
- Describe font or lettering style, such as rounded children's book title lettering, neat handwritten Chinese, carved wooden characters, printed menu text, soft brush lettering, or simple UI sans-serif.
- For every single sentence or page-text line, require one uniform font size, weight, style, and baseline across all characters. Do not create mixed-size Chinese characters, decorative emphasized words, jumping letters, or uneven typography inside the same sentence.
- If an interior page intentionally combines two adjacent story beats because the pictures would be too similar, include two exact quoted page-text sentences. Specify two staggered placements for the sentences, for example first sentence in the upper-left open sky and second sentence in the lower-left floor or grass margin. Do not stack both sentences into one cramped block, and do not let either sentence overlap characters, faces, important props, or the page number.
- Describe layout and material when relevant, such as centered two-line cover title, vertical signboard, chalkboard menu, paper label, cloth banner, road sign, phone UI, tablet screen, map legend, chart label, or worksheet step.
- Include text that appears on objects inside the scene, including signs,路标, labels, books, notebooks, screens, packaging, maps, posters, menus, UI panels, charts, diagrams, or classroom boards.
- Apply the same exact-text rule to any text element introduced during reasoning, including self-added charts, labels, diagrams, clue cards, recipe cards, growth timelines, or problem-solving steps.
- For interior page numbers, use the exact Arabic numeral matching the interior page order, such as `"1"` on page-01, `"2"` on page-02, and `"3"` on page-03. Place it in the lower-right corner, small but readable, with a simple rounded style that does not compete with the story text. Do not add a page number to the cover.

For poster, menu, UI, workbook, chart, map, or other design-like images, list all visible text strings before the visual description, then specify the typography and layout for each text group.

Keep generated in-image text concise but not underwritten. For interior pages, missing, unreadable, pseudo, generic, story-inaccurate, or unevenly sized page text is a QA failure; regenerate or correct the page until the final interior image contains the required readable and story-accurate text.

## Cover Prompt

The cover must be theme-specific and readable at thumbnail size. It should include:

- main characters
- strongest theme object or scene
- emotional promise of the story
- simple composition with clear focal point
- visible story title text

Avoid generic character group shots that do not reveal the theme.

Cover text is mandatory:

- Use the exact story name wrapped in Chinese book-title brackets as the only required cover title, for example `"《七里香的秘密香气》"`.
- Place the title upper-center, centered horizontally and slightly above the visual focal point.
- Use readable artistic children's book lettering. It may be hand-drawn, softly embossed, watercolor brush-lettered, or warm cream paper-cut style, but it must remain light, bright, and legible at Xiaohongshu thumbnail size.
- Describe the title size, color, material/texture, and layout. Example: large warm cream artistic lettering with soft brown shadow, centered near the upper third of the cover, printed on the illustration rather than on a separate label.
- Do not add extra cover slogans, subtitles, author names, logos, or decorative pseudo-text unless the user explicitly asks.

## Interior Prompt

Each interior prompt must preserve continuity:

- Use the same names and compact visual anchors from the lock sheet.
- State which characters are visible.
- State the exact action and emotion for this page.
- Add visible page text for every interior page. Wrap every exact sentence in English double quotes. Prefer two to three short child-readable sentences, or three to four short lines, when needed to explain the page content, action change, emotional shift, or story transition accurately. Place the text in quiet margin or open sky/floor/wall areas, and specify uniform readable children's book typography with same-size characters throughout each sentence.
- When a page combines two visually overlapping adjacent beats, add two exact quoted sentences and specify staggered placements for them so the first sentence and second sentence are visually separated.
- Add the exact lower-right page number for every interior page as a separate text element, for example `"1"` for page-01. Specify lower-right placement, small readable size, soft color, and simple rounded style. The cover must not include a page number.
- State any object carried over from previous pages.
- Avoid changing clothing, body colors, signature props, or species.

Compact interior prompt template:

`内页第N页，竖版3:4。{compact style line} 角色：{visible compact anchors}。画面：{page action, emotion, composition, carried object if any}。文字：在{quiet area}放入"{page text}"，圆润儿童绘本中文字体，同句字形大小一致；右下角页码"N"，小号柔和深绿。{compact negative line}`

## Image QA

Use this section only when the user explicitly asks for actual image generation. Do not call image generation tools by default.

For every requested image target, generate at least two candidate images. This applies to the character reference sheet, cover, and each interior page. If a tool supports multiple outputs in one call, request two or more outputs; otherwise, run separate generation attempts. Keep candidate filenames or labels clear, such as `cover-A`, `cover-B`, `page-01-A`, and `page-01-B`.

Inspect generated images for:

- very bright, luminous, healing watercolor mood
- clean pastel palette, airy whites, warm sunlight, and no muddy or dim color cast
- soft diffuse lighting, clean readable silhouettes, and no dominant dappled or mottled shadow pattern
- character consistency
- theme visibility
- correct page action
- 3:4 portrait composition
- style consistency
- no unwanted text or pseudo-text
- no busy speckled shadow texture, dense paper noise, heavy stippling, or high-contrast broken light across faces/text
- every interior page contains readable page text that accurately explains the page content, action change, emotional shift, or story transition
- every interior page contains the correct lower-right Arabic page number, and the cover contains no page number
- intended interior page text is exact, readable, and uses consistent character size within each sentence
- no extra limbs, distorted faces, or confusing objects
- suitability for children and Xiaohongshu

Regenerate only failed images. Keep successful images stable. Do not display failed generated images to the user in previews, final responses, galleries, or output packages; failed images are for internal QA inspection only. Show at least two passing candidates when available so the user can choose. If only one candidate passes after regeneration attempts, clearly mark that only one passed QA instead of pretending two are ready.

## Generation Timing

This section applies only when the user explicitly asks for actual image generation. Full image packages include a character reference sheet, cover, and at least 12 interior images; generating at least two candidates per image target can be slow. Allow extended waiting time for generation, inspection, comparison, and selective regeneration. Do not treat slow generation as a failure by itself. Continue until all required image targets have the requested candidate set passing QA, the user chooses finalists, the user cancels, or the image tool returns a real failure.

## Word Prompt Package

Default delivery is a Word `.docx` prompt package, not generated images. Use the Documents plugin to create and verify the DOCX when available.

The Word filename must be the user's theme. If the theme contains filename-unsafe characters, keep the exact theme as the visible document title and use the closest filesystem-safe filename.

If the user provides multiple themes separated by `、`, create a separate Word `.docx` file for each theme. Do not combine multiple themes into one document unless the user explicitly asks for a combined file.

The Word document must include:

- story title
- full story
- character reference image prompt
- cover image prompt
- every interior page image prompt in numeric order
- Xiaohongshu main title
- Xiaohongshu short intro
- Xiaohongshu body copy
- tags

Keep theme interpretation, knowledge cards, safety notes, role mode notes, character lock sheets, beat allocation, cover concept, global visual style, publishing file lists, upload checklists, and other supporting planning sections out of the Word document unless the user explicitly asks to include them.

Do not paste the full prompt package into the chat by default after creating the Word file. Return a concise summary and link the `.docx` deliverable unless the user asks to see the text in chat.

## File Package

When creating the default prompt package, use:

- `<用户主题>.docx`
- one separate `<主题>.docx` per theme when the user provides multiple `、`-separated themes

Only when the user explicitly asks for actual image generation, also use:

- `cover-A.png` and `cover-B.png` candidate files, or final `cover.png` only after the user chooses
- `page-01-A.png` and `page-01-B.png` candidate files, continuing the same pattern for every generated interior page, or final `page-01.png` through the final page only after the user chooses
- `character-reference-A.png` and `character-reference-B.png` if generated, or final `character-reference.png` only after the user chooses
- `publish-copy.md` if requested

The upload order is cover first, then interior pages in numeric order after the user has chosen final candidates. Keep unchosen candidates and production aids separate from the upload set.

## Xiaohongshu Copy

Produce:

- one required main title
- one short intro
- body copy
- 8-15 tags
- image order
- upload checklist

Main title format must be unified:

- `emoji + 《故事名》｜3-8岁亲子共读·主题关键词`

Use one relevant emoji at the beginning when it fits the theme, such as a flower, leaf, moon, star, lantern, book, or animal emoji. Keep the title honest and specific. Avoid exaggerated claims. Do not change the required order unless the user asks.

Intro rules:

- Write one short Xiaohongshu intro of 1-2 sentences.
- Explain the story premise and parent-child reading value.
- Mention one light educational point when it is natural.
- Keep it suitable as the visible post summary before the longer body copy.

Body copy structure:

1. one-sentence hook
2. what the story is about
3. what children can notice or learn, including 1-3 light educational facts from the theme
4. how parents can read it together
5. save/share call to action

Tags should mix broad and specific tags, such as `#儿童绘本`, `#亲子共读`, `#睡前故事`, `#小红书绘本`, and theme-specific tags.

## Publishing Checklist

Before final delivery, check:

- cover shows the theme at thumbnail size
- visual style is very bright, luminous, healing, airy, and watercolor-led unless the user explicitly requested a different style
- default delivery is a Word `.docx` prompt package named from the user's theme
- multiple `、`-separated themes produce multiple independent Word files, one per theme
- the Word file includes only the story title, full story, character reference prompt, cover prompt, all interior prompts, Xiaohongshu main title, short intro, body, and tags unless the user explicitly requested more sections
- cover prompt includes the exact story title wrapped in Chinese book-title brackets, placed upper-center with readable artistic lettering
- all interior prompts are in order and there are at least 12 pages
- characters remain consistent across prompts
- every interior prompt includes readable and story-accurate page text; page text is not too sparse or too long, and embedded text rules require uniform same-size characters within each sentence
- every interior prompt includes the correct lower-right page number, starting at 1, and the cover prompt has no page number
- story has a clear beginning, turning point, climax, and ending
- story logic passes the not-contrived test: no forced moral, abrupt turn, coincidence-only solution, unexplained helper, or sudden emotional reversal
- cover and interior prompts include exact quoted text plus placement, size, material, font style, and layout; the no-unwanted-text rule only applies to character reference sheets or production aids that intentionally contain no story text
- if image generation was explicitly requested, user-facing delivery includes only QA-passed images; failed generated images are not displayed
- if image generation was explicitly requested, each requested image target has at least two QA-passed candidates whenever possible, with clear labels for user selection
- no image generation tool was called unless the user explicitly requested image generation
- Xiaohongshu unified-format main title, short intro, body, tags, and image order are included
- no auto-publish action is taken
