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

Contact form (Web3Forms)

The contact form uses Web3Forms, a free service that emails form submissions to me. The site is static, so there is no server of my own.
