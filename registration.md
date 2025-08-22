---
layout: page
title: 参加登録
---

<h1 class="section-title">参加・発表登録</h1>

<div class="grid grid-2">
    <div class="card">
        <div class="card-title">
            <span class="material-icons" style="color: #ff6f00; vertical-align: middle;">campaign</span>
            {{ site.data.registration_info.submission.title }}
        </div>
        <div class="card-content">
            <p><strong>締切：{{ site.data.registration_info.submission.deadline }}</strong></p>
            <p>{{ site.data.registration_info.submission.description }}</p>
            <div style="margin-top: 1rem;">
                <a href="{{ site.data.registration_info.submission.form_url }}" class="btn btn-accent">発表申込フォーム（{{ site.data.registration_info.submission.form_status }}）</a>
            </div>
        </div>
    </div>

</div>

<!-- <div class="card">
    <div class="card-title">登録の流れ</div>
    <div class="card-content">
        <ol style="line-height: 2;">
            <li><strong>発表申込</strong>（発表者のみ）- {{ site.data.registration_info.submission.deadline | split: "（" | first }}まで</li>
            <li><strong>発表採択通知</strong> - 8月上旬</li>
            <li><strong>参加登録</strong>（全参加者）- {{ site.data.registration_info.registration.deadline | split: "（" | first }}まで</li>
            <li><strong>予稿提出</strong>（発表者のみ）- {{ site.data.registration_info.proceedings.deadline }}まで</li>
        </ol>
    </div>
</div> -->

<!-- <div class="card">
    <div class="card-title">発表申込について</div>
    <div class="card-content">
        <h4>申込に必要な情報</h4>
        <ul>
            {% for req in site.data.registration_info.submission_requirements %}
            <li>{{ req }}</li>
            {% endfor %}
        </ul>
        
        <h4>発表形式</h4>
        <p><strong>{{ site.data.event_info.presentation_formats.oral.name }}：</strong>{{ site.data.event_info.presentation_formats.oral.duration }}</p>
        <p><strong>{{ site.data.event_info.presentation_formats.poster.name }}：</strong>{{ site.data.event_info.presentation_formats.poster.format }}、コアタイム{{ site.data.event_info.presentation_formats.poster.core_time }}</p>
    </div>
</div>

<div class="card">
    <div class="card-title">予稿について</div>
    <div class="card-content">
        <p>発表が採択された方は、以下の形式で予稿を提出してください：</p>
        <ul>
            <li>{{ site.data.registration_info.proceedings.page_limit }}</li>
            <li>{{ site.data.registration_info.proceedings.format }}</li>
            <li>{{ site.data.registration_info.proceedings.template }}</li>
        </ul>
    </div>
</div>

<div class="card" style="background-color: #e3f2fd;">
    <div class="card-title">注意事項</div>
    <div class="card-content">
        <ul>
            {% for note in site.data.registration_info.notes %}
            <li>{{ note }}</li>
            {% endfor %}
        </ul>
    </div>
</div> -->
