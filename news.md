---
layout: page
title: お知らせ
---

<section class="section">
    <div class="container">
        <h1 class="section-title">お知らせ</h1>
        
        {% assign news = site.news | where_exp: "item", "item.draft != true" | sort: "date" | reverse %}
        
        {% if news.size == 0 %}
        <div class="card">
            <div class="card-content">
                <p>現在お知らせはありません。</p>
            </div>
        </div>
        {% else %}
        
        <div style="display: flex; flex-direction: column; gap: 1.5rem;">
            {% for item in news %}
            <a href="{{ item.url | relative_url }}" style="text-decoration: none; color: inherit;">
                <div class="card" style="transition: box-shadow 0.3s; cursor: pointer;">
                    <div class="card-content" style="padding: 1.5rem;">
                        <div style="display: flex; justify-content: space-between; align-items: start; margin-bottom: 0.75rem;">
                            <h3 style="font-size: 1.2rem; margin: 0; color: #333;">{{ item.title }}</h3>
                            <span style="color: #757575; font-size: 0.9rem; white-space: nowrap; margin-left: 1rem;">
                                {{ item.date | date: "%Y年%-m月%-d日" }}
                            </span>
                        </div>
                        
                        {% if item.category %}
                        <span style="display: inline-block; background: #f5f5f5; padding: 0.25rem 0.75rem; border-radius: 4px; font-size: 0.85rem; color: #666; margin-bottom: 0.75rem;">
                            {{ item.category }}
                        </span>
                        {% endif %}
                        
                        <p style="margin: 0; color: #666; line-height: 1.6;">
                            {{ item.content | strip_html | truncate: 150 }}
                        </p>
                        
                        <div style="margin-top: 0.75rem;">
                            <span style="color: #1976d2; font-size: 0.9rem;">
                                詳細を見る →
                            </span>
                        </div>
                    </div>
                </div>
            </a>
            {% endfor %}
        </div>
        
        {% endif %}
    </div>
</section>

<style>
.card:hover {
    box-shadow: 0 4px 12px rgba(0,0,0,0.15) !important;
}
</style>