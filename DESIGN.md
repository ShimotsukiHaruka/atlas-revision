---
version: alpha
name: Atlas-design-system
description: "An AI-powered IB exam preparation platform with a deep dark canvas (#0A0A0A), purple-indigo gradient accents (#4F46E5 → #7C3AED), and subtle neon glow effects. Combines Linear.app's restrained minimalism with Apple's typographic precision. Dark mode only. The system prioritizes clarity and focus — generous whitespace between sections (120px), glass-morphism navigation with backdrop blur, and accent gradients reserved for interactive elements only. Typography uses Satoshi for display headlines (700 weight, tight -0.03em tracking) and Inter for body text. Cards live on subtly elevated surfaces (#111111) with hairline borders (rgba(255,255,255,.04)). The purple-indigo gradient appears on CTAs, brand marks, focus states, and section highlights — never decoratively."
colors:
  primary: "#4F46E5"
  primary-light: "#818CF8"
  primary-dark: "#3730A3"
  accent: "#7C3AED"
  accent-light: "#A78BFA"
  gradient: "linear-gradient(135deg, #4F46E5, #7C3AED)"
  gradient-text: "linear-gradient(135deg, #818CF8, #A78BFA)"
  ink: "#FFFFFF"
  ink-muted: "rgba(255,255,255,.45)"
  ink-subtle: "rgba(255,255,255,.25)"
  ink-tertiary: "rgba(255,255,255,.15)"
  canvas: "#0A0A0A"
  surface-1: "#111111"
  surface-2: "#181818"
  surface-3: "#1C1C1E"
  hairline: "rgba(255,255,255,.04)"
  hairline-strong: "rgba(255,255,255,.08)"
  glass-bg: "rgba(255,255,255,.015)"
  glass-border: "rgba(255,255,255,.04)"
  glow: "rgba(79,70,229,.12)"
  orb-1: "rgba(79,70,229,.06)"
  orb-2: "rgba(124,58,237,.04)"
  semantic-success: "#22C55E"
  semantic-error: "#EF4444"

typography:
  display-hero:
    fontFamily: "Satoshi, Inter, -apple-system, sans-serif"
    fontSize: "clamp(36px, 5vw, 64px)"
    fontWeight: 700
    lineHeight: 1.04
    letterSpacing: -0.03em
  display-xl:
    fontFamily: "Satoshi, Inter, -apple-system, sans-serif"
    fontSize: "clamp(28px, 3.5vw, 40px)"
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: -0.025em
  display-lg:
    fontFamily: "Satoshi, Inter, -apple-system, sans-serif"
    fontSize: "clamp(32px, 4vw, 48px)"
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.025em
  headline:
    fontFamily: "Satoshi, Inter, -apple-system, sans-serif"
    fontSize: 20px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: -0.02em
  card-title:
    fontFamily: "Inter, -apple-system, sans-serif"
    fontSize: 14px
    fontWeight: 600
    lineHeight: 1.3
    letterSpacing: -0.01em
  body-lg:
    fontFamily: "Inter, -apple-system, sans-serif"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0
  body:
    fontFamily: "Inter, -apple-system, sans-serif"
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0
  body-sm:
    fontFamily: "Inter, -apple-system, sans-serif"
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: 0
  caption:
    fontFamily: "Inter, -apple-system, sans-serif"
    fontSize: 11px
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: 0.08em
    textTransform: uppercase
  button:
    fontFamily: "Inter, -apple-system, sans-serif"
    fontSize: 13px
    fontWeight: 500
    lineHeight: 1.2
    letterSpacing: 0

rounded:
  xs: 4px
  sm: 6px
  md: 8px
  lg: 12px
  xl: 16px
  xxl: 20px
  pill: 9999px

spacing:
  xxs: 4px
  xs: 8px
  sm: 12px
  md: 16px
  lg: 24px
  xl: 32px
  xxl: 48px
  section: 120px
  section-sm: 80px

easing:
  default: "cubic-bezier(.16,1,.3,1)"
  spring: "cubic-bezier(.34,1.56,.64,1)"
  hero-up: "cubic-bezier(.16,1,.3,1)"

animations:
  hero-fade-up:
    keyframes:
      from:
        opacity: 0
        transform: "translateY(32px)"
      to:
        opacity: 1
        transform: "translateY(0)"
    duration: 0.8s
    easing: "{easing.default}"
  fade-up:
    keyframes:
      from:
        opacity: 0
        transform: "translateY(24px)"
      to:
        opacity: 1
        transform: "translateY(0)"
    duration: 0.8s
    easing: "{easing.default}"
  scale-in:
    keyframes:
      from:
        opacity: 0
        transform: "scale(.96)"
      to:
        opacity: 1
        transform: "scale(1)"
    duration: 0.6s
    easing: "{easing.default}"

components:
  glass-nav:
    background: "rgba(10,10,10,.78)"
    backdropFilter: "blur(24px) saturate(1.5)"
    borderBottom: "1px solid {colors.hairline}"
    height: 56px
  glass-nav-default:
    background: "transparent"
    borderBottom: "1px solid transparent"
    backdropFilter: "none"
    height: 56px
  button-primary:
    background: "{colors.gradient}"
    color: "{colors.ink}"
    typography: "{typography.button}"
    rounded: "{rounded.md}"
    padding: "12px 24px"
    hover:
      transform: "translateY(-1px)"
      boxShadow: "0 8px 32px rgba(79,70,229,.25)"
  button-secondary:
    background: "transparent"
    color: "{colors.ink-muted}"
    border: "1px solid {colors.hairline}"
    typography: "{typography.button}"
    rounded: "{rounded.md}"
    padding: "12px 24px"
    hover:
      borderColor: "{colors.hairline-strong}"
      color: "{colors.ink}"
      background: "rgba(255,255,255,.015)"
  glass-card:
    background: "{colors.glass-bg}"
    backdropFilter: "blur(20px) saturate(1.6)"
    border: "1px solid {colors.glass-border}"
    rounded: "{rounded.lg}"
    hover:
      borderColor: "{colors.hairline-strong}"
      transform: "translateY(-2px)"
  surface-card:
    background: "{colors.surface-1}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.xl}"
    hover:
      background: "rgba(255,255,255,.015)"
      borderColor: "{colors.hairline-strong}"
  feature-card:
    background: "{colors.surface-1}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.xl}"
    padding: "{spacing.xl}"
    hover:
      borderColor: "{colors.hairline-strong}"
  testimonial-card:
    background: "{colors.surface-1}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.xl}"
    padding: "80px 48px"
  pricing-card:
    background: "{colors.surface-1}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.xl}"
    padding: "{spacing.xl}"
  pricing-card-featured:
    background: "rgba(79,70,229,.02)"
    border: "1px solid rgba(79,70,229,.15)"
    rounded: "{rounded.xl}"
    padding: "{spacing.xl}"
  input:
    background: "rgba(255,255,255,.03)"
    color: "{colors.ink}"
    border: "none"
    rounded: "{rounded.md}"
    padding: "12px 16px"
    typography: "{typography.body}"
    placeholder: "{colors.ink-subtle}"
    focus:
      background: "rgba(255,255,255,.06)"

rules:
  - "Gradient text (via {colors.gradient-text}) is reserved for hero titles, and pricing amounts."
  - "Glow orbs (fixed-position blur divs) as background atmosphere: use {colors.orb-1} and {colors.orb-2} at 400-600px with blur(100px). Only 3-4 orbs per page."
  - "Navigation has two states: transparent by default, glass-bg after scrolling past 40px."
  - "Section spacing must be exactly 120px (desktop) and 80px (mobile)."
  - "Hover cards use a radial gradient overlay at the cursor position: background: radial-gradient(600px circle at var(--mx,50%) var(--my,50%), rgba(79,70,229,.04), transparent 50%)."
  - "Animations staggered in 0.05-0.1s increments using transition-delay."
  - "Progress bars animate from 0% to target width using IntersectionObserver when scrolled into view."
  - "FAQ items animate max-height toggle — only one item open at a time."
  - "Hero section has two-column layout: left text + right visual (grid lines + glow orb + floating icon). On mobile, stack vertically."
  - "Pricing cards use a 3-column grid. Featured card has 'Most popular' badge positioned at -10px top center."
  - "Colors are defined as rgba() for transparency control — never use opacity on color tokens."
