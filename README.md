# SASCO Games Portal - Integration Plan

This folder coordinates the integration of Daniel's games into Victor's school portal.

## Games Overview

### 1. MathCrush2 (Unity WebGL)
**Status**: In active integration with Victor
**Location**: Azure DevOps MathGame repo
**Type**: Educational - equation solving
**Integration**: Complex (JS Interop, progress tracking, Victor's API)
**Purpose**: Core learning tool - earns students "free time" credits

### 2. Kangaroo Hop (Phaser.js)
**Status**: Ready for integration
**Location**: https://github.com/dannyboy166/my-kangaroo-game
**Live URL**: https://dannyboy166.github.io/my-kangaroo-game/
**Type**: Free time reward - endless runner
**Integration**: Simple iframe embed
**Purpose**: Free time reward game

### 3. Wordle (React)
**Status**: Ready for integration (teacher customization needed)
**Location**: https://github.com/dannyboy166/wordle-game
**Live URL**: https://dannyboy166.github.io/wordle-game/
**Type**: Educational - vocabulary/spelling
**Integration**: Medium complexity - needs teacher word selection feature
**Purpose**: Homework/vocabulary practice

### 4. 2048 (Vanilla JS)
**Status**: Ready for integration
**Location**: https://github.com/dannyboy166/2048-game
**Live URL**: https://dannyboy166.github.io/2048-game/
**Type**: Free time reward - puzzle
**Integration**: Simple iframe embed
**Purpose**: Free time reward game

### 5. Memory Game (Vanilla JS)
**Status**: SASCO branding applied, ready to deploy
**Location**: https://github.com/dannyboy166/memory-game (to be created)
**Live URL**: https://dannyboy166.github.io/memory-game/ (pending)
**Type**: Free time reward - card matching (educational potential with themed cards)
**Integration**: Simple iframe embed
**Purpose**: Free time reward game (can be educational with letter/number/vocab cards)

## Integration Roadmap

### Phase 1: Get Mum's Approval ✓
- [x] Show Mum all 4 browser games (Kangaroo, Wordle, 2048, Memory)
- [ ] Confirm which games to include
- [ ] Discuss Wordle teacher customization feature
- [ ] Discuss Memory Game educational themes (letters, numbers, vocab)

### Phase 2: Optimize Games (Current)
**Kangaroo Hop:**
- [ ] Add mobile responsive scaling (currently fixed 800x600)
- [ ] Add URL parameter support (studentId, sessionId, token)
- [ ] Add "Return to Portal" button
- [ ] Optional: Add basic progress tracking (high score, coins)

**Wordle:**
- [ ] Add teacher word list customization feature
- [ ] Add URL parameter support for custom word sets
- [ ] Add "Return to Portal" button
- [ ] Decide: Daily words vs. teacher-assigned words vs. both?

**2048:**
- [ ] Add URL parameter support (studentId, sessionId, token)
- [ ] Add "Return to Portal" button
- [ ] Optional: Track high scores

**Memory Game:**
- [ ] Deploy to GitHub Pages
- [ ] Add URL parameter support (studentId, sessionId, token)
- [ ] Add "Return to Portal" button
- [ ] Add "Play Again" button
- [ ] Optional: Create educational card themes (letters, numbers, vocabulary)
- [ ] Optional: Track completion time and matches

### Phase 3: Victor Integration Planning
- [ ] Email Victor about the 4 browser games
- [ ] Clarify iframe requirements (size, aspect ratio)
- [ ] Determine progress tracking needs
- [ ] Decide on "Free Time" vs "Homework" categorization
- [ ] Discuss Memory Game educational potential (themed cards)
- [ ] Get JS Interop code if progress tracking needed

### Phase 4: Implementation
- [ ] Implement agreed features
- [ ] Test iframe embedding locally
- [ ] Provide Victor with URLs and integration docs
- [ ] Test in Victor's staging environment

### Phase 5: Launch
- [ ] Deploy to production
- [ ] Monitor for issues
- [ ] Gather teacher/student feedback

## Technical Notes

### URL Parameter Format (matching MathCrush2):
```
?studentId=12345&sessionId=abc-def-ghi&token=xyz123
```

### Iframe Embedding Example:
```html
<iframe 
  src="https://dannyboy166.github.io/my-kangaroo-game/?studentId=12345&sessionId=abc&token=xyz"
  width="800" 
  height="600"
  frameborder="0"
></iframe>
```

### Return to Portal Button:
```javascript
// Option 1: Close iframe (if parent controls it)
window.parent.postMessage({ action: 'closeGame' }, '*');

// Option 2: Navigate back
window.location.href = 'PORTAL_URL_HERE';
```

## Game Repositories

- **my-kangaroo-game**: `/Users/danielsamus/my-kangaroo-game`
- **wordle-game**: `/Users/danielsamus/wordle-game`
- **2048-game**: `/Users/danielsamus/2048-game`
- **memory-game**: `/Users/danielsamus/memory-game`

## Contact Info

- **Victor**: Victor@eStreet.com.au (Portal integration)
- **Julie (Mum)**: juliesamus@bigpond.com (Educational requirements)
- **Daniel**: samus.daniel@gmail.com

## Next Steps

1. Get Mum's approval for all 4 browser games
2. Deploy Memory Game to GitHub Pages
3. Optimize games based on this plan
4. Email Victor with game demos and requirements
5. Coordinate integration timeline with Victor's MathCrush2 work

---

*Last updated: 2025-11-24*
