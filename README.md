# Fahad Jaseem · DevOps Portfolio

An immersive, single-page portfolio for **Fahad Jaseem**, DevOps Engineer. A live 3D particle swarm sits behind the page, morphs as you scroll, and reacts to your mouse.

- **Role:** DevOps Engineer at Azeosoft Web Technologies, Noida
- **Focus:** AWS, Kubernetes, Terraform, CI/CD, GitOps, observability, DevSecOps
- **Contact:** fahadjaseem2@gmail.com · 8299688301
- **LinkedIn:** https://www.linkedin.com/in/fahad-jaseem-devops
- **GitHub:** https://github.com/fahadjaseem2

---

## Features

- **Particle hero.** Thousands of dots drawn on a `<canvas>` form a sphere behind the name. Drag to rotate, click to pulse, scroll to morph.
- **Seven shapes.** Swarm, sphere, helix, knot, galaxy, grid and wave, plus an AUTO mode that changes shape per section.
- **Design.** Dark theme, blue → violet → pink gradient, glass panels, outlined hero type, floating pill nav and a ring cursor.
- **Spotlight cards.** A gradient border and glow follow the cursor over each panel.
- **Typing terminal.** A terminal in the About section types out key facts when scrolled into view.
- **Experience ledger.** Number tiles for the impact figures from the resume.
- **Delivery Flow diagram.** An animated SVG of Git push → GitHub Actions → security gates → ECR → ArgoCD → EKS, with Terraform below and observability above.
- **Resume section.** A clickable preview of the resume that opens the PDF.
- **Scroll progress bar, reveal-on-scroll and a loading screen.**
- **Responsive and accessible.** Works down to phone width. Respects `prefers-reduced-motion`. Keyboard focus is visible.

## Sections

| Section | Content |
| --- | --- |
| Home | Name, role, summary, stats, particle shape controls |
| About | Summary, education, current status, terminal |
| Skills | Cloud, containers, CI/CD, IaC, monitoring, Linux, DevSecOps, data |
| Experience | Azeosoft role with impact tiles and bullets |
| Projects | AWS Terraform and observability, CI/CD on EKS with ArgoCD |
| Flow | Animated delivery pipeline diagram |
| Security | Gitleaks, Hadolint, Semgrep, Trivy gates |
| CV | Resume preview and PDF link |
| Contact | Email, mobile, LinkedIn, GitHub and a message form |

## Tech

No framework and no build step.

- HTML, CSS and vanilla JavaScript in a single `index.html`
- Canvas 2D for the particle system
- Inline SVG for the delivery flow diagram
- Google Fonts: Outfit, Manrope and JetBrains Mono

## Files

```
portfolio/
├── index.html                 # the whole site: markup, styles, script
├── Fahad_Jaseem_DevOps.pdf    # resume (linked from the nav and Resume section)
├── resume-preview.webp        # image of the resume page shown in the CV section
└── README.md
```

## Run locally

Open `index.html` in a browser. To serve it properly, run this in the project folder and open http://localhost:8000:

```bash
python3 -m http.server 8000
```

## Customize

| What | Where in `index.html` |
| --- | --- |
| Colors | `:root` tokens at the top of `<style>` (`--blue`, `--violet`, `--pink`, `--grad`) |
| Particle colors | `BAND` array in the script |
| Particle count | `targetCount()` in the script (higher looks denser but costs more GPU/CPU) |
| Shape per section | `SECTION_SHAPE` in the script |
| Text and links | The HTML body: edit the section content directly |
| Fonts | The Google Fonts `<link>` and the `--display`, `--body`, `--mono` tokens |

### Update the resume

1. Replace `Fahad_Jaseem_DevOps.pdf` with the new file, keeping the same name.
2. Regenerate the preview image:

   ```bash
   pdftoppm -r 130 -png Fahad_Jaseem_DevOps.pdf resume-page
   # then convert resume-page-1.png to resume-preview.webp
   ```

3. Update any numbers or bullets in the Experience and Projects sections to match.

## Deploy

Because it is plain static files, it works on any static host.

- **GitHub Pages:** push the folder to a repo, then Settings → Pages → deploy from the `main` branch.
- **Netlify or Vercel:** drag the folder in, or connect the repo. No build command is needed.
- **Custom domain:** point your domain at the host and add it in the host's settings.

## Notes

- The contact form does not send email, because there is no backend. It copies your message so you can paste it into an email. To receive messages directly, connect a form service such as Formspree or Netlify Forms.
- Particle count adapts to screen width (about 10,500 on desktop, 7,200 on tablet, 4,600 on phone).

## License

Personal portfolio. All content belongs to Fahad Jaseem.
