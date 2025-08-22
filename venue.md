---
layout: page
title: 会場
---

<h1 class="section-title">会場情報</h1>

<div class="card">
    <div class="card-title">会場</div>
    <div class="card-content">
        <h3 style="color: #1976d2; margin-bottom: 0.5rem;">{{ site.data.venue_info.venue_name }}</h3>
        <p style="margin-bottom: 1rem;">{{ site.data.venue_info.address }}</p>
        <p>{{ site.data.venue_info.description }}</p>
        <p><a href="https://www.ait.ac.jp/about/yakusa-campus/" target="_blank" rel="noopener">愛知工業大学 八草キャンパス 公式サイト</a></p>
    </div>
</div>

<div class="card" style="margin-top: 2rem;">
    <div class="card-title">会場マップ</div>
    <div class="card-content">
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d250.91405856535027!2d137.11080710343484!3d35.184324858394405!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6003670e1ea9d925%3A0x4b91fbaa2287b243!2z5oSb55-l5bel5qWt5aSn5a2m!5e0!3m2!1sja!2sjp!4v1755856441088!5m2!1sja!2sjp" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
</div>

<div class="card">
    <div class="card-title">アクセス</div>
    <div class="card-content">
        <h4>公共交通機関でお越しの方</h4>
        <table style="width: 100%; border-collapse: collapse; margin: 1rem 0;">
            <tbody>
                {% for train in site.data.venue_info.access.train %}
                <tr>
                    <th style="padding: 1rem; border: 1px solid #e0e0e0; background-color: #f5f5f5; width: 30%; text-align: left;">{{ train.route }}</th>
                    <td style="padding: 1rem; border: 1px solid #e0e0e0;">
                        {{ train.details }}
                    </td>
                </tr>
                {% endfor %}
            </tbody>
        </table>
        <div style="background-color: #e3f2fd; padding: 1rem; border-radius: 4px; margin: 1rem 0;">
            <p style="margin: 0;"><strong>シャトルバスについて：</strong><br>
            {{ site.data.venue_info.access.shuttle.info }}<br>
            シャトルバスは無料でご利用いただけます。</p>
            <img src="https://i.gyazo.com/1dd13d6441944e1693fa07fe54824138.png" alt="シャトルバス運行時刻表" style="width: 100%; max-width: 600px; margin-top: 1rem; border-radius: 4px;">
        </div>
        
        <h4>お車でお越しの方</h4>
        <p><strong>ルート：</strong>{{ site.data.venue_info.access.car.route }}</p>
        <p><strong>駐車場：</strong>{{ site.data.venue_info.access.car.parking }}</p>
    </div>
</div>

<div class="card" style="margin-top: 2rem;">
    <div class="card-title">お問い合わせ</div>
    <div class="card-content">
        <p>会場に関するご質問は、<a href="{{ '/contact' | relative_url }}">お問い合わせページ</a>からご連絡ください。</p>
    </div>
</div>