## Hi there 👋
<!-- header: text sigil + lightweight svg animation -->
<?xml version="1.0" encoding="UTF-8"?>
<svg width="1200" height="320" viewBox="0 0 1200 320" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- scanline pattern -->
    <pattern id="scan" width="4" height="4" patternUnits="userSpaceOnUse">
      <rect x="0" y="0" width="4" height="2" fill="#0b0b0b"/>
      <rect x="0" y="2" width="4" height="2" fill="rgba(0,0,0,0)"/>
      <animate attributeName="patternTransform" dur="3s" values="translate(0,0);translate(0,4);translate(0,0)" repeatCount="indefinite"/>
    </pattern>

    <!-- noise-based glitch -->
  <filter id="glitch" x="-10%" y="-20%" width="120%" height="140%">
      <feTurbulence type="fractalNoise" baseFrequency="0.006 0.006" numOctaves="2" seed="3" result="noise">
        <animate attributeName="baseFrequency" dur="6s" values="0.002 0.002;0.02 0.02;0.002 0.002" repeatCount="indefinite"/>
      </feTurbulence>
      <feDisplacementMap in="SourceGraphic" in2="noise" scale="8" xChannelSelector="R" yChannelSelector="G">
        <animate attributeName="scale" dur="6s" values="0;12;0;6;0" repeatCount="indefinite"/>
      </feDisplacementMap>
    </filter>

    <!-- subtle flicker -->
   <filter id="flicker">
      <feComponentTransfer>
        <feFuncA type="table" tableValues="1 0.9 1 0.85 1"/>
      </feComponentTransfer>
    </filter>
  </defs>

  <rect x="0" y="0" width="100%" height="100%" fill="#0a0a0a"/>
  <rect x="0" y="0" width="100%" height="100%" fill="url(#scan)" opacity="0.45"/>

  <!-- chromatic offsets for raw edge -->
  <g filter="url(#glitch)">
    <text x="50%" y="54%" text-anchor="middle" dominant-baseline="middle"
          font-family="ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
          font-size="108" letter-spacing="6" fill="#00f" opacity="0.55">AAMOSM</text>

   <text x="50.6%" y="48%" text-anchor="middle" dominant-baseline="middle"
          font-family="ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
          font-size="108" letter-spacing="6" fill="#f00" opacity="0.55">AAMOSM</text>

   <text x="50%" y="50%" text-anchor="middle" dominant-baseline="middle"
          font-family="ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
          font-size="108" letter-spacing="6" fill="#e5e5e5">AAMOSM</text>
  </g>

  <!-- low-key banner text -->
  <g filter="url(#flicker)">
    <text x="50%" y="78%" text-anchor="middle" dominant-baseline="middle"
          font-family="ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
          font-size="20" letter-spacing="2" fill="#bdbdbd" opacity="0.8">
      web design • java • ui/ux • experiments
      <animate attributeName="opacity" dur="2.8s" values="0.85;0.65;0.9;0.75;0.85" repeatCount="indefinite"/>
    </text>
  </g>
</svg>


about/
- a‑level student building on the web
- java‑first brain; html/css/js for the look & feel
- python = school grind (do what must be done)

now/
- learning: advanced java + modern web tooling
- interests: ui/ux, layout systems, coding challenges
- goal: make this profile less sterile over time

workbench/
- web design (typography, grids, motion)
- java (mini toys, cli tools, small engines)
- notes (sketches, fragments, experiments)

changelog/
- [wip] scaffolding this space
- [soon] live ui/ux sandboxes
- [soon] java animation demos (text + svg)

contact/
- open an issue here if something breaks

