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

<div class="card" style="margin-top: 2rem; background-color: #e3f2fd; border-left: 4px solid #2196f3;">
    <div class="card-title">
        <span class="material-icons" style="color: #2196f3; vertical-align: middle;">info</span>
        聴講参加について
    </div>
    <div class="card-content">
        <p><strong>事前参加登録をお忘れの方へ</strong></p>
        <p>聴講のみの参加をご希望の方は、<strong>当日会場での参加登録も可能</strong>です。<br>
        受付にてお名前・ご所属等をお伝えください</p>
        <div style="background-color: #fff3e0; padding: 1rem; border-radius: 4px; margin-top: 1rem;">
            <p style="margin: 0; font-size: 0.95rem;">
                <span class="material-icons" style="font-size: 1rem; vertical-align: text-bottom;">schedule</span>
                当日受付時間：9:15〜9:50（1日目）/ 9:30〜9:50（2日目）
            </p>
        </div>
    </div>
</div>