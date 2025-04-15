---
layout: page
title: About Me
subtitle: 95% figuring it out. 5% pretending I already did.
---


As a kid, I once secretly hoarded spoons from the kitchen and stashed them in my room not for mischief, but because I was worried we might run out one day. I think this highlights how I think: I like anticipating problems before they show up and quietly solving them in advance. That same instinct to plan, build, and prepare for the unknown still drives how I approach everything.

## My Background

I grew up in Menlo Park, California with a brother, sister, two loving parents, and a golden retriever, Cooper. I  feel incredibly lucky to have been raised in a home filled with love, support, and the kind of values that have shaped who I am today.

## Education

I’m currently pursuing a B.A. in Computer Science and Economics at the University of Notre Dame. I’ve been named to the Dean’s List every semester, currently holding a 3.98 GPA. Before college, I took a gap year through EF Education First, traveling through 13 European countries in a language immersion and internship program that expanded both my worldview and my Spotify playlist.

## Experience

<div id="timeline"></div>

<script>
  const experiences = [
    {
      year: '2025',
      title: 'Incoming Investment Banking Analyst',
      company: 'Morgan Stanley',
      location: 'New York, NY',
      description: 'Selected for competitive sophomore internship program. Worked on aerospace M&A case with cross-functional team. Presented findings to VP-level executives.'
    },
    {
      year: '2024 – Present',
      title: 'Team Leader',
      company: 'Strategic Advisory Project – Notre Dame SIBC',
      description: 'Led a team to advise AeroVironment (NASDAQ: AVAV) on strategic growth. Delivered final presentation to board.'
    }
  ];

  const timelineContainer = document.getElementById('timeline');
  experiences.forEach((experience, index) => {
    const timelineItem = document.createElement('div');
    timelineItem.className = 'timeline-item';
    timelineItem.innerHTML = `
      <div class="timeline-bubble" onmouseover="showDescription(${index})" onmouseout="hideDescription(${index})">
        <div class="bubble" id="bubble-${index}" style="display: none;">
          <h4>${experience.title}</h4>
          <p>${experience.description}</p>
        </div>
      </div>
      <div class="timeline-content">
        <h3>${experience.year}</h3>
        <h4>${experience.company} | ${experience.location || ''}</h4>
      </div>
    `;
    timelineContainer.appendChild(timelineItem);
  });

  function showDescription(index) {
    document.getElementById(`bubble-${index}`).style.display = 'block';
  }

  function hideDescription(index) {
    document.getElementById(`bubble-${index}`).style.display = 'none';
  }
</script>

<style>
  #timeline {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    position: relative;
  }
  .timeline-item {
    margin: 20px 0;
    position: relative;
  }
  .timeline-bubble {
    position: absolute;
    left: -20px;
    width: 20px;
    height: 20px;
    background-color: #007bff;
    border-radius: 50%;
    cursor: pointer;
  }
  .bubble {
    position: absolute;
    top: -10px;
    left: 30px;
    background-color: #f8f9fa;
    border: 1px solid #ddd;
    padding: 10px;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  .timeline-content {
    margin-left: 50px;
  }
</style>
</div>






