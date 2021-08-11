## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/tyl811/milkdrop-web/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/tyl811/milkdrop-web/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

tylerlawhorn633@gmail.com

import butterchurn from 'butterchurn';
import butterchurnPresets from 'butterchurn-presets';

// initialize audioContext and get canvas

const visualizer = butterchurn.createVisualizer(audioContext, canvas, {
  width: 800,
  height: 600
});

// get audioNode from audio source or microphone

visualizer.connectAudio(audioNode);

// load a preset

const presets = butterchurnPresets.getPresets();
const preset = presets['Flexi, martin + geiss - dedicated to the sherwin maxawow'];

visualizer.loadPreset(preset, 0.0); // 2nd argument is the number of seconds to blend presets

// resize visualizer

visualizer.setRendererSize(1600, 1200);

// render a frame

visualizer.render();

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

