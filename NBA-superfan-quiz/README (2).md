# NBA Superfan Identity Quiz 🏀

**What Type of NBA Superfan Are You?**

A web quiz I built using HTML, CSS, and JavaScript for Project 4. You answer 8 questions and it tells you what kind of NBA fan you are. There are 5 possible results.

---

## How to Run It

Just download the files and open `index.html` in your browser. No installs, no setup, nothing extra needed.

---

## What the Project Is

I chose to make a quiz for NBA superfans because I'm genuinely part of that community. I watch games, I follow the discourse, I have opinions — and I noticed that NBA fans all engage with the sport in really different ways. Some people live and die for their team. Some people only care about one player. Some people are mostly on Twitter starting arguments. I thought it would be fun to turn that into something interactive.

The quiz puts you into one of five categories:

- 📊 **The Analyst** — stats obsessed, always citing numbers
- 🏆 **The Loyalist** — one team, forever, no exceptions
- ⭐ **The Player Follower** — follows players not teams
- 🔥 **The Hot Take Machine** — lives for the debate
- 🎉 **The Casual Superfan** — shows up for the big moments

---

## Technical Requirements

- **8 questions** — each one has 5 answer choices that map to a fan type
- **Buttons and form elements** — radio inputs for each answer, next/back buttons to navigate, everything wired with event listeners
- **localStorage** — saves your answers as you go so if you close the tab and come back, it asks if you want to resume. Also saves your last result so if you retake it, you can see how you changed
- **localStorage changes the page** — the resume banner only shows up if there's a saved session, and the result screen shows your previous result for comparison. The accent color of the whole page also changes based on your result
- **Works locally** — single HTML file, open it and it just works
- **GitHub repo** — linked below
- **User testing** — done with a few friends, notes below
- **This README** — you're reading it

---

## Design

I wanted it to look like something NBA-related, not just a generic quiz. So I went with a dark background, red as the main color (NBA colors), and big bold fonts that feel like a scoreboard or a jersey. The font for the big headings is called Bebas Neue — I found it on Google Fonts and thought it looked right for this.

The background has a very faint grid pattern that's supposed to feel like a basketball court. It's subtle but I like it.

For the result screen, the accent color actually changes depending on which fan type you get. That part took me a while to figure out but I'm glad I kept it in.

---

## Challenges I Faced

**localStorage was confusing at first.** I understood the idea of it from class but when I actually had to implement it I kept running into issues. My first attempt only saved the final result, not the progress. Then I tried saving after every click but I was also updating the score at the same time as saving, which caused the score to be wrong if someone went back and changed an answer. I eventually fixed this by recalculating the scores at the very end from the saved answers instead of tracking them as I go.

**Styling the radio buttons.** The default HTML radio buttons are really ugly and I couldn't figure out how to style them the way I wanted. I ended up hiding them with CSS and styling the label instead, then using JavaScript to add and remove a `.checked` class. This is something I didn't learn in class — I found it on MDN and Stack Overflow.

**English as a second language.** Writing the question and answer text was actually one of the harder parts for me. I wanted it to sound natural and like something an NBA fan would actually say, not stiff or translated. I rewrote a lot of the answer options multiple times.

**Screen layout.** Getting the page to look decent on both my laptop and my phone took longer than I expected. I ended up using `clamp()` for font sizes which I found helpful.

---

## User Testing

I tested with three people.

**Friend 1** — watches NBA casually, not super into it
She got "Casual Superfan" and said it was accurate. She said the design looked professional. She didn't notice the localStorage resume feature so I made the banner more visible after.

**Friend 2** — really into the NBA, follows stats a lot
He got "The Analyst" on his first try and said the questions felt real. He went back and retook it trying to get a different result, which is how I found out the previous result comparison badge was useful — he asked if that was intentional.

**Friend 3** — international student who doesn't follow basketball much
He was confused by some of the NBA-specific terms like "box score" and "PER." I added a note to the answer options to make them a little more understandable but also kept the terminology because the target audience is supposed to be people who already follow the NBA.

---

## What I Would Do Differently / Next Steps

If I had more time or did a second version:

- I would add a way to share your result, maybe copy a link or generate a shareable image
- The tie-breaking logic right now just picks whichever type comes first alphabetically if two scores are equal. That's not great. I'd add a tiebreaker question
- I want to add more questions (maybe 15) with random selection so the quiz feels different each time
- Better mobile styling — it works but it's not perfect on small screens
- I'd also like to show stats at the end like "most people who took this got The Analyst" — that would need a backend though which is outside what I know right now

---

## References

- MDN Web Docs (localStorage, radio inputs, CSS variables)
- Google Fonts (Bebas Neue, Barlow)
- Stack Overflow (styling radio buttons with labels)
- Class notes and slides

---

## Repository

```
https://github.com/YOUR_USERNAME/nba-superfan-quiz
```

```bash
git clone https://github.com/YOUR_USERNAME/nba-superfan-quiz.git
cd nba-superfan-quiz
open index.html
```
