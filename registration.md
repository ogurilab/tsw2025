---
layout: page
title: 参加登録
---

<h1 class="section-title">参加・発表登録</h1>

<div class="grid grid-2">
    <div class="card" style="background-color: #f5f5f5; border-left: 4px solid #999;">
        <div class="card-title">
            <span class="material-icons" style="color: #999; vertical-align: middle;">check_circle</span>
            {{ site.data.registration_info.submission.title }}
        </div>
        <div class="card-content">
            <p><strong>締切：{{ site.data.registration_info.submission.deadline }} - <span style="color: #d32f2f;">締切済み</span></strong></p>
            <p>{{ site.data.registration_info.submission.description }}</p>
            <div style="margin-top: 1rem;">
                <button disabled class="btn" style="background-color: #999; color: #fff; cursor: not-allowed; opacity: 0.6;">発表申込フォーム（{{ site.data.registration_info.submission.form_status }}）</button>
            </div>
        </div>
    </div>

</div>