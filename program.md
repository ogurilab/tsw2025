---
layout: page
title: プログラム
---

<h1 class="section-title">プログラム</h1>

<div class="card" style="text-align: center; background-color: #fff3e0; border-left: 4px solid #ff6f00;">
    <div class="card-content">
        <p><strong>プログラムは現在準備中です</strong></p>
    </div>
</div>

<h2 style="margin-top: 3rem;">ポスター発表について</h2>

<div class="card" style="background-color: #e8f5e9; border-left: 4px solid #4caf50;">
    <div class="card-title">
        <span class="material-icons" style="color: #4caf50; vertical-align: middle;">info</span>
        ポスター発表者の皆様へ
    </div>
    <div class="card-content">
        <p><strong>ポスターサイズについて</strong></p>
        <ul style="margin-top: 1rem; margin-bottom: 1.5rem;">
            <li>A0サイズまたはA1サイズのポスターをご持参ください</li>
            <li>会場のポスターボードにはA0サイズ（841mm × 1189mm）まで貼り付け可能です</li>
        </ul>
        <p style="color: #555; font-size: 0.95rem;">
            <span class="material-icons" style="font-size: 1rem; vertical-align: text-bottom;">tips_and_updates</span>
            ポスターは各自で印刷してご持参いただきますようお願いいたします
        </p>
    </div>
</div>

<!-- <h2 style="margin-top: 3rem;">プログラム概要（予定）</h2>

<div class="card">
    <div class="card-title">1日目：{{ site.data.schedule.day1.date }}</div>
    <div class="card-content">
        <table style="width: 100%; border-collapse: collapse;">
            <tr style="background-color: #f5f5f5;">
                <th style="padding: 0.75rem; border: 1px solid #e0e0e0; width: 150px;">時間</th>
                <th style="padding: 0.75rem; border: 1px solid #e0e0e0;">内容</th>
            </tr>
            {% for session in site.data.schedule.day1.sessions %}
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">{{ session.time }}</td>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">
                    {{ session.title }}
                    {% if session.speaker %}（{{ session.speaker }}）{% endif %}
                </td>
            </tr>
            {% endfor %}
        </table>
    </div>
</div>

<div class="card">
    <div class="card-title">2日目：{{ site.data.schedule.day2.date }}</div>
    <div class="card-content">
        <table style="width: 100%; border-collapse: collapse;">
            <tr style="background-color: #f5f5f5;">
                <th style="padding: 0.75rem; border: 1px solid #e0e0e0; width: 150px;">時間</th>
                <th style="padding: 0.75rem; border: 1px solid #e0e0e0;">内容</th>
            </tr>
            {% for session in site.data.schedule.day2.sessions %}
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">{{ session.time }}</td>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">
                    {{ session.title }}
                    {% if session.speaker %}（{{ session.speaker }}）{% endif %}
                    {% if session.topic %}「{{ session.topic }}」{% endif %}
                </td>
            </tr>
            {% endfor %}
        </table>
    </div>
</div>

<div class="card">
    <div class="card-title">発表分野（予定）</div>
    <div class="card-content">
        <ul>
            {% for field in site.data.event_info.research_fields %}
            <li>{{ field }}</li>
            {% endfor %}
        </ul>
    </div>
</div> -->
