---
layout: page
title: プログラム
---

<h1 class="section-title">プログラム</h1>

<!-- <div class="card" style="text-align: center; background-color: #fff3e0; border-left: 4px solid #ff6f00;">
    <div class="card-content">
        <p><strong>プログラムの詳細は現在準備中です</strong></p>
    </div>
</div> -->

<!-- <h2 style="margin-top: 3rem;">タイムスケジュール</h2> -->

<!-- <div class="card">
    <div class="card-title">
        <span class="material-icons" style="color: #1976d2; vertical-align: middle;">schedule</span>
        開催時間について
    </div>
    <div class="card-content">
        <table style="width: 100%; border-collapse: collapse;">
            <tr style="background-color: #f5f5f5;">
                <th style="padding: 0.75rem; border: 1px solid #e0e0e0; width: 150px;">時間</th>
                <th style="padding: 0.75rem; border: 1px solid #e0e0e0;">内容</th>
            </tr>
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">9:30～</td>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">受付開始</td>
            </tr>
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">10:00</td>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">開会</td>
            </tr>
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0; text-align: center;" colspan="2">
                    <em style="color: #666;">詳細なプログラムは後日公開予定</em>
                </td>
            </tr>
        </table>
    </div>
</div> -->

<h2 style="margin-top: 3rem;">発表について</h2>

<div class="card" style="background-color: #e3f2fd; border-left: 4px solid #2196f3;">
    <div class="card-title">
        <span class="material-icons" style="color: #2196f3; vertical-align: middle;">info</span>
        口頭発表者の皆様へ
    </div>
    <div class="card-content">
        <p><strong>発表時間について</strong></p>
        <ul style="margin-top: 1rem; margin-bottom: 1.5rem;">
            <li>口頭発表は発表者によって発表時間が異なる場合があります</li>
            <li>プログラムに記載の発表開始時間はおおよその目安となります</li>
        </ul>
        <p style="color: #555; font-size: 0.95rem;">
            <span class="material-icons" style="font-size: 1rem; vertical-align: text-bottom;">tips_and_updates</span>
            詳細な発表時間については事前にご確認いただきますようお願いいたします
        </p>
    </div>
</div>

<div class="card" style="background-color: #e8f5e9; border-left: 4px solid #4caf50; margin-top: 1rem;">
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

<h2 style="margin-top: 3rem;">プログラム</h2>

<div class="card">
    <div class="card-title">1日目：{{ site.data.schedule.day1.date }}</div>
    <div class="card-content">
        <table style="width: 100%; border-collapse: collapse;">
            <tr style="background-color: #f5f5f5;">
                <th style="padding: 0.75rem; border: 1px solid #e0e0e0; width: 150px;">時間</th>
                <th style="padding: 0.75rem; border: 1px solid #e0e0e0;">内容</th>
            </tr>
            {% for session in site.data.schedule.day1.sessions %}
            {% if session.type == "break" %}
            <tr style="background-color: #f0f8ff;">
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0; text-align: center;" colspan="2">
                    <strong>{{ session.time }}</strong> - {{ session.title }}
                </td>
            </tr>
            {% elsif session.presentations %}
            {% if session.type == "poster" %}
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">{{ session.time }}</td>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">
                    <strong>{{ session.title }}</strong><br>
                    <ul style="margin: 0.5rem 0; padding-left: 1.5rem;">
                    {% for presentation in session.presentations %}
                        <li style="margin: 0.25rem 0;">{{ presentation.speaker }}: {{ presentation.title }}</li>
                    {% endfor %}
                    </ul>
                </td>
            </tr>
            {% else %}
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;" rowspan="{{ session.presentations.size | plus: 1 }}">
                    {{ session.time }}
                </td>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0; background-color: #fafafa;">
                    <strong>{{ session.title }}</strong>
                </td>
            </tr>
            {% for presentation in session.presentations %}
            <tr>
                <td style="padding: 0.5rem 0.75rem; border: 1px solid #e0e0e0;">
                    <span style="color: #666;">{{ presentation.time }}</span><br>
                    {{ presentation.speaker }}: {{ presentation.title }}
                </td>
            </tr>
            {% endfor %}
            {% endif %}
            {% else %}
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">{{ session.time }}</td>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">
                    {{ session.title }}
                    {% if session.speaker %}（{{ session.speaker }}）{% endif %}
                    {% if session.presentation_title %}<br>「{{ session.presentation_title }}」{% endif %}
                </td>
            </tr>
            {% endif %}
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
            {% if session.type == "break" %}
            <tr style="background-color: #f0f8ff;">
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0; text-align: center;" colspan="2">
                    <strong>{{ session.time }}</strong> - {{ session.title }}
                </td>
            </tr>
            {% elsif session.presentations %}
            {% if session.type == "poster" %}
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">{{ session.time }}</td>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">
                    <strong>{{ session.title }}</strong><br>
                    <ul style="margin: 0.5rem 0; padding-left: 1.5rem;">
                    {% for presentation in session.presentations %}
                        <li style="margin: 0.25rem 0;">{{ presentation.speaker }}: {{ presentation.title }}</li>
                    {% endfor %}
                    </ul>
                </td>
            </tr>
            {% else %}
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;" rowspan="{{ session.presentations.size | plus: 1 }}">
                    {{ session.time }}
                </td>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0; background-color: #fafafa;">
                    <strong>{{ session.title }}</strong>
                </td>
            </tr>
            {% for presentation in session.presentations %}
            <tr>
                <td style="padding: 0.5rem 0.75rem; border: 1px solid #e0e0e0;">
                    <span style="color: #666;">{{ presentation.time }}</span><br>
                    {{ presentation.speaker }}: {{ presentation.title }}
                </td>
            </tr>
            {% endfor %}
            {% endif %}
            {% else %}
            <tr>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">{{ session.time }}</td>
                <td style="padding: 0.75rem; border: 1px solid #e0e0e0;">
                    {{ session.title }}
                    {% if session.speaker %}（{{ session.speaker }}）{% endif %}
                    {% if session.presentation_title %}<br>「{{ session.presentation_title }}」{% endif %}
                    {% if session.topic %}「{{ session.topic }}」{% endif %}
                </td>
            </tr>
            {% endif %}
            {% endfor %}
        </table>
    </div>
</div>