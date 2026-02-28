README – Assignment Q3

------------------------------------------------------------
1. Prompt 1: Planning Prompt (no code included)
------------------------------------------------------------

My prompt to ChatGPT:
"Can you give me a plan for implementing responsive breakpoints for desktop, tablet, and mobile, and also explain how to make the hero section behave correctly on small screens? I only want a planning explanation, not any code."

Two things I accepted from the plan:
1. I accepted the idea of using three breakpoint ranges (desktop, tablet, mobile) because it matched the assignment requirements exactly.
2. I accepted the suggestion to stack the hero section vertically on mobile to prevent layout overflow and improve readability.

One thing I rejected (and why):
I rejected the suggestion to add a hamburger menu for mobile navigation. The assignment did not require a hamburger menu, only stacked and centered navigation, so adding one would have been unnecessary and outside the scope.

------------------------------------------------------------
2. Prompt 2: Debug Prompt
------------------------------------------------------------

Problem statement:
I had a bug where the navigation would not stack vertically on mobile. Even when the screen was below 600px, the links stayed in a horizontal row.

The CSS snippet I asked about:
".header { display: flex; }
.nav a { margin-right: 12px; }
@media (max-width: 600px) {
  .header { flex-direction: column; }
}"

Most important part of the AI response:
"The navigation is not stacking because only the header is changing direction. You must also change the .nav container to use flex-direction: column, and remove the right margin on the links so they can center properly."

What I changed afterward:
I added a mobile media query that sets `.nav` to `flex-direction: column`, adds a small vertical gap, and removes the right margin from `.nav a`. After doing this, the navigation stacked and centered correctly on mobile.

------------------------------------------------------------
3. Verification List
------------------------------------------------------------

Viewport sizes tested:
• 375px (mobile)
• 600px (mobile breakpoint limit)
• 768px (tablet)
• 900px (tablet breakpoint limit)
• 1200px (desktop)

What I checked visually:
• Header layout: logo left + nav right on desktop, stacked and centered on mobile.
• Container width and padding: ensured content never touched screen edges.
• Hero section: two columns on desktop, stacked vertically on mobile, hero card aligned right.
• Grid layout: 4 columns on desktop, 2 on tablet, 1 on mobile.
• Hover styles: button color change and card hover lift effect.

