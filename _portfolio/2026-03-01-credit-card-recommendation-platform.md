---
title: "CardSmart — Credit Card Recommendation Platform"
collection: portfolio
section: fintech_grad
permalink: /portfolio/credit-card-recommendation-platform/
date: 2026-03-01
project_period: "Jan 2026 - May 2026"
header:
  teaser: projects/card_smart.png
excerpt: "Full-stack Flask app matching user spending patterns to optimal credit card strategies; deployed on Duke VCM with CI/CD pipeline and security scanning."
---

Group software engineering project building a personalized credit card recommendation system, developed across 5 sprints with a team of 5.

## Product

- Built a full-stack Flask web app allowing users to import transaction data (CSV/JSON), receive ranked card recommendations based on spend categories and reward structures, and commit to a card plan with tracked history.
- Implemented cashback and travel reward modes, CPP slider for interactive updates, and an admin console for user management and cross-account analytics.
- Integrated a Claude-powered AI chatbot as a persistent assistant across the product using the Anthropic API.

## Engineering

- Scaffolded the project foundation: Flask app factory, SQLAlchemy models, Blueprint structure, environment-based config, seed data scripts, and migration setup.
- Deployed to Duke VCM with PostgreSQL, Gunicorn, and Nginx; configured systemd auto-restart and a 4-stage GitLab CI/CD pipeline (build, test, SAST, deploy).
- Achieved 84% test coverage; ran Semgrep SAST (0 findings) and OWASP ZAP baseline scan (57 PASS, 0 FAIL) against the live deployment.

Links:
- [Code (GitLab)](https://gitlab.oit.duke.edu/hz362/512-pccrs)
- <a href="http://vcm-53434.vm.duke.edu/" style="color: #000; text-decoration: none;">Live Site (Duke VCM)</a>
