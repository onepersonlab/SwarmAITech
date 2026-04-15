---
layout: page
title: "Framework Comparison"
description: "Detailed comparison of multi-agent AI frameworks by stars, language, license, and features."
---

<section class="comparison-section">
  <div class="comparison-table-wrapper">
    <table class="comparison-table">
      <thead>
        <tr>
          <th>Framework</th>
          <th>Stars</th>
          <th>Forks</th>
          <th>Language</th>
          <th>License</th>
          <th>Type</th>
        </tr>
      </thead>
      <tbody>
        {% assign sorted = site.data.frameworks.frameworks | sort: 'stars' | reverse %}
        {% for framework in sorted %}
        <tr>
          <td class="name-cell">
            <a href="{{ framework.github_url }}" target="_blank" rel="noopener noreferrer">{{ framework.name }}</a>
          </td>
          <td class="number-cell">{{ framework.stars }}</td>
          <td class="number-cell">{{ framework.forks }}</td>
          <td>{{ framework.language }}</td>
          <td>{{ framework.license }}</td>
          <td>
            {% if framework.topics contains 'multi-agent' %}Multi-Agent{% elsif framework.topics contains 'autonomous-research' %}Research{% elsif framework.topics contains 'assistant' %}Assistant{% else %}Framework{% endif %}
          </td>
        </tr>
        {% endfor %}
      </tbody>
    </table>
  </div>
</section>

<section style="margin-top: var(--space-3xl);">
  <h2>Key Metrics Comparison</h2>
  
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(400px, 1fr)); gap: var(--space-xl); margin-top: var(--space-lg);">
    <!-- Stars Chart Placeholder -->
    <div style="background: var(--color-bg-card); padding: var(--space-lg); border-radius: var(--radius-lg); border: 1px solid rgba(255,255,255,0.05);">
      <h3 style="font-size: var(--font-size-lg); margin-bottom: var(--space-md);">GitHub Stars Distribution</h3>
      <p style="font-size: var(--font-size-sm); color: var(--color-text-secondary);">
        OpenClaw leads with 357K stars, followed by AutoGPT (183K) and Hermes Agent (85K).
        The distribution shows clear market leaders in the personal assistant and autonomous agent categories.
      </p>
      <div style="margin-top: var(--space-lg);">
        {% assign sorted = site.data.frameworks.frameworks | sort: 'stars' | reverse %}
        {% for framework in sorted limit:5 %}
        <div style="display: flex; align-items: center; margin-bottom: var(--space-sm);">
          <span style="width: 120px; font-size: var(--font-size-sm);">{{ framework.name }}</span>
          <div style="flex: 1; height: 20px; background: rgba(255,255,255,0.1); border-radius: var(--radius-sm); overflow: hidden;">
            <div style="height: 100%; width: {{ framework.stars | divided_by: 357447 | times: 100 }}%; background: var(--color-accent-gradient);"></div>
          </div>
          <span style="width: 80px; font-size: var(--font-size-sm); font-family: var(--font-mono); text-align: right;">{{ framework.stars }}</span>
        </div>
        {% endfor %}
      </div>
    </div>
    
    <!-- License Distribution -->
    <div style="background: var(--color-bg-card); padding: var(--space-lg); border-radius: var(--radius-lg); border: 1px solid rgba(255,255,255,0.05);">
      <h3 style="font-size: var(--font-size-lg); margin-bottom: var(--space-md);">License Distribution</h3>
      <p style="font-size: var(--font-size-sm); color: var(--color-text-secondary);">
        MIT License is the dominant choice (11/13 frameworks), reflecting the open-source ethos of the AI agent community.
        Apache-2.0 is used by 2 frameworks.
      </p>
      <div style="margin-top: var(--space-lg); display: flex; gap: var(--space-md);">
        <div style="flex: 1; text-align: center;">
          <div style="font-size: var(--font-size-3xl); font-weight: 700; color: var(--color-accent-primary);">11</div>
          <div style="font-size: var(--font-size-sm); color: var(--color-text-muted);">MIT License</div>
        </div>
        <div style="flex: 1; text-align: center;">
          <div style="font-size: var(--font-size-3xl); font-weight: 700; color: var(--color-accent-secondary);">2</div>
          <div style="font-size: var(--font-size-sm); color: var(--color-text-muted);">Apache-2.0</div>
        </div>
      </div>
    </div>
    
    <!-- Language Distribution -->
    <div style="background: var(--color-bg-card); padding: var(--space-lg); border-radius: var(--radius-lg); border: 1px solid rgba(255,255,255,0.05);">
      <h3 style="font-size: var(--font-size-lg); margin-bottom: var(--space-md);">Primary Languages</h3>
      <p style="font-size: var(--font-size-sm); color: var(--color-text-secondary);">
        Python dominates the multi-agent framework space, used by most frameworks. 
        TypeScript represents the modern web-first approach (OpenClaw).
      </p>
      <div style="margin-top: var(--space-lg);">
        <div style="display: flex; gap: var(--space-sm); margin-bottom: var(--space-md);">
          <span class="language-badge" style="flex: 1; justify-content: center;">
            <span class="language-dot python"></span>
            Python (10)
          </span>
          <span class="language-badge" style="flex: 1; justify-content: center;">
            <span class="language-dot typescript"></span>
            TypeScript (1)
          </span>
          <span class="language-badge" style="flex: 1; justify-content: center;">
            <span class="language-dot other"></span>
            Other (2)
          </span>
        </div>
      </div>
    </div>
    
    <!-- Fork Ratio -->
    <div style="background: var(--color-bg-card); padding: var(--space-lg); border-radius: var(--radius-lg); border: 1px solid rgba(255,255,255,0.05);">
      <h3 style="font-size: var(--font-size-lg); margin-bottom: var(--space-md);">Community Engagement</h3>
      <p style="font-size: var(--font-size-sm); color: var(--color-text-secondary);">
        Fork ratio indicates community contribution activity. Higher ratios suggest more active development communities.
      </p>
      <div style="margin-top: var(--space-lg);">
        {% assign sorted = site.data.frameworks.frameworks | sort: 'forks' | reverse %}
        {% for framework in sorted limit:5 %}
        {% assign ratio = framework.forks | divided_by: framework.stars | times: 100 %}
        <div style="display: flex; align-items: center; margin-bottom: var(--space-sm);">
          <span style="width: 120px; font-size: var(--font-size-sm);">{{ framework.name }}</span>
          <div style="flex: 1; height: 20px; background: rgba(255,255,255,0.1); border-radius: var(--radius-sm); overflow: hidden;">
            <div style="height: 100%; width: {{ ratio | at_most: 40 }}%; background: linear-gradient(90deg, var(--color-accent-secondary), var(--color-accent-primary));"></div>
          </div>
          <span style="width: 80px; font-size: var(--font-size-sm); font-family: var(--font-mono); text-align: right;">{{ framework.forks }} forks</span>
        </div>
        {% endfor %}
      </div>
    </div>
  </div>
</section>

<section style="margin-top: var(--space-3xl); background: var(--color-bg-secondary); padding: var(--space-2xl); border-radius: var(--radius-lg);">
  <h2>Feature Matrix</h2>
  
  <div class="comparison-table-wrapper" style="margin-top: var(--space-lg);">
    <table class="comparison-table">
      <thead>
        <tr>
          <th>Framework</th>
          <th>Multi-Agent</th>
          <th>Human-in-Loop</th>
          <th>Self-Improving</th>
          <th>Graph-Based</th>
          <th>Research Focus</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td class="name-cell">AutoGen</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
        </tr>
        <tr>
          <td class="name-cell">MetaGPT</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
        </tr>
        <tr>
          <td class="name-cell">CrewAI</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
        </tr>
        <tr>
          <td class="name-cell">LangGraph</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
        </tr>
        <tr>
          <td class="name-cell">Swarm</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
        </tr>
        <tr>
          <td class="name-cell">HiClaw</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
        </tr>
        <tr>
          <td class="name-cell">Hermes Agent</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
        </tr>
        <tr>
          <td class="name-cell">AutoResearchClaw</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">✓</td>
        </tr>
        <tr>
          <td class="name-cell">AI-Scientist-v2</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">✓</td>
        </tr>
        <tr>
          <td class="name-cell">deer-flow</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">✓</td>
        </tr>
        <tr>
          <td class="name-cell">OpenClaw</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
        </tr>
        <tr>
          <td class="name-cell">AutoGPT</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">✓</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
          <td style="text-align: center;">—</td>
        </tr>
      </tbody>
    </table>
  </div>
  
  <p style="margin-top: var(--space-lg); font-size: var(--font-size-sm); color: var(--color-text-muted);">
    ✓ = Supported | — = Not primary feature
  </p>
</section>