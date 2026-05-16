Satiwa Hemp Craft Spirits - Website Context & Setup

This document serves as the project context and setup guide for the Satiwa single-page promotional website. It outlines the technical stack, brand guidelines, structure, and animation logic.

1. Technical Stack

Structure: Single-page HTML5 (index.html).

Styling: Tailwind CSS (loaded via CDN for rapid prototyping and utility-first styling). Custom CSS is used for specific gradient masks, scrollbars, and animations.

Animations: GSAP (GreenSock Animation Platform) and GSAP ScrollTrigger (loaded via CDN) are used to handle complex scroll-bound animations.

Fonts: * Headings/Display: Playfair Display (Google Fonts)

Body: System UI fonts (Apple System, BlinkMacSystemFont, Segoe UI, etc.) for optimal native rendering.

2. Local Setup Instructions

To run this website locally with all assets functioning properly:

Ensure you have the index.html file saved on your computer.

Place the hero bottle image in the exact same directory as the index.html file.

Important: The image must be named satiwa-bottle.jpg to link correctly to the code.

Open index.html in any modern web browser.

3. Brand Guidelines (2026 Edition)

The design strictly follows the Satiwa 2026 Brand Guidelines:

Brand Voice: Relaxed yet refined, earthy yet aspirational.

Tagline: "The Happy High Gin"

Primary Hashtag: #GETHAPPYHIGH

Color Palette:

Backgrounds: Deep dark canvas (#0a0a0a to #1a1a2e)

Accents/CTAs: Gold/Amber (#d4a843, #c9a96e)

Text: Off-White/Cream (#f5f0e8)

Pillar Accents: Deep Green (#1a3c2a), Muted Sage (#6b7c65), Rose/Copper (#b87333)

Legal Requirement: "DRINK RESPONSIBLY. NOT FOR SALE TO PERSONS UNDER 18." must be present in the footer and age gate.

4. Page Architecture & Features

The single-page application is divided into the following sections:

Age Gate (Modal): * Requires users to confirm they are of legal drinking age before accessing the site. Prevents scrolling until confirmed.

Navigation:

Sticky header with backdrop blur. Contains anchor links to page sections. Includes a mobile responsive hamburger menu.

Hero Section (#home):

Features the primary hashtag and the uploaded satiwa-bottle.jpg.

Animation: As the user scrolls down, the bottle pins to the center, tilts (-105 degrees), and a stream of translucent liquid pours out, eventually filling the screen to transition into the next section.

Our Story (#story):

Focuses on the three brand pillars: Small Batch, Hemp Botanical, and Tropical Soul.

Animation: Cards fade and slide up sequentially as they enter the viewport.

Catalogue (#catalogue):

Displays the three core spirits: Hemp Craft Gin, Hemp Craft Rum, and Baby Pink Gin.

Features glass-morphism cards with stylized CSS bottle representations.

Mixology (#mixology):

A horizontal scrolling container (snap-x) detailing three signature cocktail recipes: The Happy High, Tropical Smoke, and Strawberry Blush.

Find Us / Contact (#contact):

Split layout featuring a mock location search input and a functional-looking contact form.

Footer:

Social links, brand typography, and legal drinking age disclaimers.

5. Animation Logic (GSAP)

The core pouring animation is handled by a GSAP Timeline bound to a ScrollTrigger on the #home section.

scrub: 1 ensures the animation smoothly follows the user's scroll wheel.

pin: true locks the hero section in place while the scroll animation completes, giving the illusion of a full-screen interactive cinematic sequence.