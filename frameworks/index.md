---
layout: page
title: "Frameworks"
description: "Complete catalog of multi-agent AI frameworks with detailed information and comparisons."
---

<div class="frameworks-grid">
  {% for framework in site.data.frameworks.frameworks %}
  <a href="{{ framework.github_url }}" class="framework-card animate-fade-in" target="_blank" rel="noopener noreferrer">
    <div class="framework-card-header">
      <h3 class="framework-name">{{ framework.name }}</h3>
      <div class="framework-stars">
        <svg viewBox="0 0 24 24" width="16" height="16">
          <path fill="currentColor" d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
        </svg>
        <span>{{ framework.stars | divided_by: 1000 }}K</span>
      </div>
    </div>
    <p class="framework-description">{{ framework.description }}</p>
    <div class="framework-meta">
      <span class="language-badge">
        {% if framework.language == 'Python' %}
        <span class="language-dot python"></span>
        {% elsif framework.language == 'TypeScript' %}
        <span class="language-dot typescript"></span>
        {% elsif framework.language == 'JavaScript' %}
        <span class="language-dot javascript"></span>
        {% else %}
        <span class="language-dot other"></span>
        {% endif %}
        {{ framework.language }}
      </span>
      <span class="license-badge">{{ framework.license }}</span>
    </div>
    {% if framework.topics.size > 0 %}
    <div class="framework-topics">
      {% for topic in framework.topics limit:3 %}
      <span class="topic-tag">{{ topic }}</span>
      {% endfor %}
    </div>
    {% endif %}
  </a>
  {% endfor %}
</div>

<section style="margin-top: var(--space-4xl); background: var(--color-bg-secondary); padding: var(--space-2xl); border-radius: var(--radius-lg);">
  <h2>Categories</h2>
  
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: var(--space-lg); margin-top: var(--space-lg);">
    <div>
      <h3 style="font-size: var(--font-size-lg); margin-bottom: var(--space-md);">🤖 Personal Assistants</h3>
      <ul style="list-style: none; padding: 0;">
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/openclaw/openclaw" target="_blank">OpenClaw</a></li>
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/Significant-Gravitas/AutoGPT" target="_blank">AutoGPT</a></li>
      </ul>
    </div>
    
    <div>
      <h3 style="font-size: var(--font-size-lg); margin-bottom: var(--space-md);">🔬 Research Automation</h3>
      <ul style="list-style: none; padding: 0;">
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/aiming-lab/AutoResearchClaw" target="_blank">AutoResearchClaw</a></li>
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/SakanaAI/AI-Scientist-v2" target="_blank">AI-Scientist-v2</a></li>
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/karpathy/autoresearch" target="_blank">autoresearch</a></li>
      </ul>
    </div>
    
    <div>
      <h3 style="font-size: var(--font-size-lg); margin-bottom: var(--space-md);">🏗️ Multi-Agent Frameworks</h3>
      <ul style="list-style: none; padding: 0;">
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/microsoft/autogen" target="_blank">AutoGen</a></li>
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/geekan/MetaGPT" target="_blank">MetaGPT</a></li>
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/crewAIInc/crewAI" target="_blank">CrewAI</a></li>
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/openai/swarm" target="_blank">Swarm</a></li>
      </ul>
    </div>
    
    <div>
      <h3 style="font-size: var(--font-size-lg); margin-bottom: var(--space-md);">📊 Graph-Based Agents</h3>
      <ul style="list-style: none; padding: 0;">
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/langchain-ai/langgraph" target="_blank">LangGraph</a></li>
      </ul>
    </div>
    
    <div>
      <h3 style="font-size: var(--font-size-lg); margin-bottom: var(--space-md);">🦞 OpenClaw Ecosystem</h3>
      <ul style="list-style: none; padding: 0;">
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/openclaw/openclaw" target="_blank">OpenClaw</a></li>
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/NousResearch/hermes-agent" target="_blank">Hermes Agent</a></li>
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/aiming-lab/AutoResearchClaw" target="_blank">AutoResearchClaw</a></li>
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/agentscope-ai/HiClaw" target="_blank">HiClaw</a></li>
      </ul>
    </div>
    
    <div>
      <h3 style="font-size: var(--font-size-lg); margin-bottom: var(--space-md);">🧠 Self-Improving</h3>
      <ul style="list-style: none; padding: 0;">
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/NousResearch/hermes-agent" target="_blank">Hermes Agent</a></li>
        <li style="margin-bottom: var(--space-sm);"><a href="https://github.com/aiming-lab/AutoResearchClaw" target="_blank">AutoResearchClaw</a></li>
      </ul>
    </div>
  </div>
</section>