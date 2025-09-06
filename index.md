---
layout: home
title: ホーム
---

{% include carousel.html %}

<section class="hero">
    <div class="container">
        <h1>{{ site.data.event_info.title }}</h1>
        <p class="subtitle">{{ site.data.event_info.dates }}</p>
        <div class="hero-buttons">
            <a href="{{ '/registration' | relative_url }}" class="btn btn-secondary">参加登録</a>
            <a href="{{ '/program' | relative_url }}" class="btn btn-primary">プログラムを見る</a>
        </div>
    </div>
</section>

<section class="section">
    <div class="container">
        <h2 class="section-title">開催概要</h2>
        <div class="grid grid-3">
            <div class="card">
                <div class="card-title">
                    <span class="material-icons" style="color: #1976d2; vertical-align: middle;">event</span>
                    開催日時
                </div>
                <div class="card-content">
                    <p>{{ site.data.event_info.dates }}</p>
                    <p>{{ site.data.event_info.time }}</p>
                </div>
            </div>
            <div class="card">
                <div class="card-title">
                    <span class="material-icons" style="color: #1976d2; vertical-align: middle;">location_on</span>
                    会場
                </div>
                <div class="card-content">
                    <p>愛知工業大学八草キャンパス14号館</p>
                    <p><a href="{{ '/venue' | relative_url }}">会場情報を見る</a></p>
                </div>
            </div>
            <div class="card">
                <div class="card-title">
                    <span class="material-icons" style="color: #1976d2; vertical-align: middle;">people</span>
                    参加対象
                </div>
                <div class="card-content">
                    <p>{{ site.data.event_info.target_audience[0] | split: "（" | first }}</p>
                    <p>参加費{{ site.data.event_info.fees.participation }}</p>
                </div>
            </div>
        </div>
    </div>
</section>

<section class="section">
    <div class="container">
        <h2 class="section-title">重要な日程</h2>
        <div class="card" style="max-width: 600px; margin: 0 auto;">
            <table style="width: 100%; border-collapse: collapse;">
                {% for item in site.data.important_dates.dates %}
                <tr>
                    <td style="padding: 1rem; {% unless forloop.last %}border-bottom: 1px solid #e0e0e0;{% endunless %}">
                        <strong>{{ item.title }}</strong>
                    </td>
                    <td style="padding: 1rem; {% unless forloop.last %}border-bottom: 1px solid #e0e0e0;{% endunless %} text-align: right;">
                        {{ item.date }}
                    </td>
                </tr>
                {% endfor %}
            </table>
        </div>
    </div>
</section>

<section class="section" style="background-color: #f5f5f5;">
    <div class="container">
        <h2 class="section-title">東海サマーワークショップとは</h2>
        <div class="card" style="max-width: 800px; margin: 0 auto;">
            <div class="card-content">
                {% capture workshop_content %}{% include_relative _content/about_workshop.md %}{% endcapture %}
                {{ workshop_content | markdownify }}
            </div>
        </div>
    </div>
</section>

<section class="section">
    <div class="container">
        <h2 class="section-title">お知らせ</h2>
        {% assign news = site.news | where_exp: "item", "item.draft != true" | sort: "date" | reverse %}
        {% for item in news limit: 3 %}
        <div class="card">
            <div class="card-title">{{ item.title }}</div>
            <div class="card-content">
                <p style="color: #757575; font-size: 0.9rem;">{{ item.date | date: "%Y年%-m月%-d日" }}</p>
                <p>{{ item.content | strip_html | truncate: 100 }}</p>
            </div>
        </div>
        {% endfor %}
    </div>
</section>