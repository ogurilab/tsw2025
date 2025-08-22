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