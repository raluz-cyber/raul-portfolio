# raul-portfolio
Multi-page personal portfolio built with Jekyll and pure HTML/CSS. Features auto-generated project pages via Markdown collections, responsive design, and easy customization.

Copyright (c) 2025 Raul Luzardo

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.


## Quick Start (Jekyll + Codespaces)
- Open a Codespace on this repo.
- Terminal A (server):
  ```bash
  bundle install
  bundle exec jekyll serve --host 0.0.0.0 --port 4000


## Updating the Resume (PDF)

**Where:** `assets/docs/resume.pdf`

**How to update:**
1. Replace the file with your new resume but keep the same name:
   - VS Code → right-click `assets/docs/` → **Upload…** → select PDF → rename to `resume.pdf`
   - Or via terminal if the old file exists:
     ```bash
     git mv "My New Resume.pdf" assets/docs/resume.pdf
     ```
2. Commit and push:
   ```bash
   git add assets/docs/resume.pdf
   git commit -m "chore: update resume.pdf"
   git push
