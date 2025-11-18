# SASCO Games Portal - Claude Context

## Project Overview
Daniel is integrating 4 games into Victor's school portal platform:
1. MathCrush2 (Unity) - Currently in integration with Victor
2. Kangaroo Hop (Phaser.js) - Ready, needs optimization
3. Wordle (React) - Ready, needs teacher customization feature
4. 2048 (Vanilla JS) - Ready, needs optimization

## Current Status (2025-11-18)
- All 3 browser games are live on GitHub Pages and working
- MathCrush2 integration with Victor is in progress (Phase 1: launch testing)
- Waiting on Mum's approval before emailing Victor about browser games
- Games need optimization before Victor integration

## Key People
- **Daniel**: Developer
- **Julie (Mum)**: Educational requirements, teacher perspective
- **Victor (eStreet.com.au)**: Portal platform developer

## Integration Approach
- **MathCrush2**: Complex (Unity WebGL, JS Interop, Victor's API, progress tracking)
- **Browser games**: Simple (iframe embed, URL parameters, optional progress tracking)

## Game Repositories
Each game is in a separate repo with its own GitHub Pages deployment:
- `/Users/danielsamus/my-kangaroo-game` → https://dannyboy166.github.io/my-kangaroo-game/
- `/Users/danielsamus/wordle-game` → https://dannyboy166.github.io/wordle-game/
- `/Users/danielsamus/2048-game` → https://dannyboy166.github.io/2048-game/

## What Each Game Needs

### Kangaroo Hop (Free time reward)
- Mobile responsive scaling (currently fixed 800x600)
- URL parameter support (studentId, sessionId, token)
- "Return to Portal" button
- Optional: Basic progress tracking (high score via localStorage or Victor's API)

### Wordle (Educational/Homework)
**Key feature**: Teachers can assign custom word lists
- Teacher word list customization (needs design discussion)
- URL parameter support for custom words
- "Return to Portal" button
- Mode selection: Daily words vs. teacher-assigned vs. both?

### 2048 (Free time reward)
- URL parameter support (studentId, sessionId, token)
- "Return to Portal" button
- Optional: High score tracking

## Victor's Integration Pattern (from MathCrush2 emails)
1. Iframe embedding with URL parameters: `?studentId=X&sessionId=Y&token=Z`
2. JS Interop for progress tracking (Victor provides the service)
3. Data stored in Victor's database (structured fields + JSON blob)
4. Token-based auth for API calls
5. Small steps approach - get launch working first, then add features

## Next Immediate Steps
1. Get Mum's approval for all 3 browser games
2. Optimize games per roadmap in README.md
3. Draft email to Victor with game demos
4. Coordinate timeline with Victor's MathCrush2 work

## Recent Work (2025-11-18)
Fixed Kangaroo Hop background loading issue on GitHub Pages:
- Problem: parallax folder images returned 404 on GitHub Pages
- Solution: Moved images to `assets/images/outback-background/` folder
- Result: Game now loads perfectly with backgrounds

## Important Notes
- Keep game repos separate (don't merge into monorepo)
- This folder is for coordination/planning only
- Each game maintains its own documentation (CLAUDE.md, README.md)
- Follow Victor's pattern from MathCrush2 for consistency

## When Working on Games
Always check the game's own CLAUDE.md/README.md first for specific architecture details.
This file provides the cross-project integration context.
