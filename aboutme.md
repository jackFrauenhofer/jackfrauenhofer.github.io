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

<style>
  #timeline {
    position: relative;
    margin-left: 60px;
    padding-left: 40px;
  }

  /* Draw vertical line */
  #timeline::before {
    content: '';
    position: absolute;
    top: 0;
    bottom: 0;
    left: 20px; /* Aligns with circle center */
    width: 4px;
    background-color: #0c2340;
    z-index: 0;
  }

  .timeline-item {
    position: relative;
    margin-bottom: 50px;
    transition: all 0.3s ease;
    padding-left: 40px; /* spacing from the circle */
  }

  /* Circle marker */
  .timeline-circle {
    position: absolute;
    left: 20px;
    top: 0;
    width: 20px;
    height: 20px;
    background-color: #0c2340;
    border-radius: 50%;
    z-index: 2;
    transform: translateX(-50%);
    transition: transform 0.2s ease;
  }

  .timeline-content {
    transition: all 0.3s ease;
  }

  .timeline-title {
    font-size: 1.2rem;
    font-weight: 700;
    margin: 0;
    color: #0c2340;
  }

  .timeline-sub {
    margin: 4px 0 0;
    color: #555;
    font-size: 0.95rem;
  }

  .timeline-description {
    margin-top: 10px;
    display: none;
    max-width: 600px;
    line-height: 1.5;
    color: #333;
    font-size: 0.95rem;
  }

  /* Hover-expand style */
  .timeline-item.expanded {
    background-color: #f2f2f2;
    border: 1px solid #ccc;
    border-radius: 10px;
    padding: 15px 20px 15px 60px;
  }

  .timeline-item.expanded .timeline-description {
    display: block;
  }

  .timeline-item.expanded .timeline-circle {
    transform: translateX(-50%) scale(1.3);
  }
</style>

<script>
  const experiences = [
    {
      period: 'Summer 2025',
      title: 'Incoming Investment Banking Analyst',
      company: 'Morgan Stanley',
      location: 'New York, NY',
      description: 'Selected for competitive sophomore internship program.'
    },
    {
      period: 'Fall 2024',
      title: 'Team Leader',
      company: 'Morgan Stanley Strategic Advisory Project – Notre Dame SIBC',
      location: 'New York, NY',
      description: 'Led a team to advise AeroVironment (NASDAQ: AVAV) on strategic growth. Delivered final presentation to Morgan Stanley representatives.'
    },
    {
      period: 'Spring 2024 – Summer 2024',
      title: 'Intern',
      company: 'Kuttin Family Office',
      location: '',
      description: 'Worked on private wealth and estate planning research across high-net-worth portfolios.'
    },
  ];

  const container = document.getElementById('timeline');

  experiences.forEach((exp, index) => {
    const item = document.createElement('div');
    item.className = 'timeline-item';

    item.innerHTML = `
      <div class="timeline-circle"></div>
      <div class="timeline-content">
        <p class="timeline-title">${exp.period} — ${exp.title}</p>
        <p class="timeline-sub">${exp.company}${exp.location ? ' | ' + exp.location : ''}</p>
        <p class="timeline-description">${exp.description}</p>
      </div>
    `;

    item.addEventListener('mouseenter', () => {
      item.classList.add('expanded');
    });
    item.addEventListener('mouseleave', () => {
      item.classList.remove('expanded');
    });

    container.appendChild(item);
  });
</script>






