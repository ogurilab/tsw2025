---
layout: page
title: お問い合わせ
---

<h1 class="section-title">お問い合わせ</h1>

<div class="card" style="max-width: 600px; margin: 0 auto;">
    <div class="card-title">お問い合わせ先</div>
    <div class="card-content">
        <p>東海サマーワークショップ2025に関するお問い合わせは、下記までお願いいたします。</p>
        
        <div style="margin: 2rem 0; padding: 1.5rem; background-color: #f5f5f5; border-radius: 4px;">
            <p style="margin: 0;"><strong>{{ site.data.contact_info.committee_name }}</strong></p>
            <p style="margin: 0.5rem 0;">
                <span class="material-icons" style="vertical-align: middle; font-size: 1.2rem;">email</span>
                {{ site.data.contact_info.email }}
            </p>
            <p style="margin: 0; font-size: 0.9rem; color: #757575;">{{ site.data.contact_info.email_note }}</p>
        </div>
    </div>
</div>

<!-- <div class="grid grid-2" style="margin-top: 2rem;">
    <!-- <div class="card">
        <div class="card-title">よくあるご質問</div>
        <div class="card-content">
            {% for item in site.data.contact_info.faq %}
            <h4>Q: {{ item.question }}</h4>
            <p>A: {{ item.answer }}</p>
            {% endfor %}
        </div>
    </div>
    
    <div class="card">
        <div class="card-title">お問い合わせ内容例</div>
        <div class="card-content">
            <ul>
                {% for example in site.data.contact_info.inquiry_examples %}
                <li>{{ example }}</li>
                {% endfor %}
            </ul>
        </div>
    </div> -->
<!-- </div> --> 

<!-- <div class="card">
    <div class="card-title">最新情報</div>
    <div class="card-content">
        <p>{{ site.data.contact_info.social_media.description }}</p>
    </div>
</div> -->
