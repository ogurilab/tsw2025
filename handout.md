---
layout: none
---
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{{ site.data.event_info.title }} - 当日配布資料</title>
    <style>
        @page {
            size: A4;
            margin: 15mm 10mm;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: "游ゴシック", "Yu Gothic", "ヒラギノ角ゴ ProN W3", "Hiragino Kaku Gothic ProN", "メイリオ", Meiryo, sans-serif;
            font-size: 9pt;
            line-height: 1.3;
            color: #333;
        }
        
        .page {
            page-break-after: always;
            min-height: 100vh;
        }
        
        .page:last-child {
            page-break-after: auto;
        }
        
        h1 {
            font-size: 16pt;
            text-align: center;
            margin-bottom: 6mm;
            padding-bottom: 2mm;
            border-bottom: 2px solid #333;
        }
        
        h2 {
            font-size: 12pt;
            margin-top: 4mm;
            margin-bottom: 3mm;
            padding: 1.5mm 2mm;
            background-color: #f0f0f0;
            border-left: 3px solid #333;
        }
        
        .event-info {
            text-align: center;
            margin-bottom: 8mm;
        }
        
        .event-info p {
            margin: 1mm 0;
        }
        
        .session {
            margin-bottom: 3mm;
        }
        
        .session-header {
            font-weight: bold;
            background-color: #f8f8f8;
            padding: 1.5mm 2mm;
            border: 1px solid #ddd;
            font-size: 9pt;
        }
        
        .presentation {
            border: 1px solid #ddd;
            border-top: none;
            padding: 1.5mm 2mm;
            display: flex;
            gap: 2mm;
            page-break-inside: avoid;
        }
        
        .presentation-info {
            flex: 1;
        }
        
        .presentation-time {
            color: #666;
            font-size: 8pt;
            display: inline;
        }
        
        .presentation-speaker {
            font-weight: bold;
            display: inline;
            font-size: 8.5pt;
        }
        
        .presentation-affiliation {
            color: #666;
            font-size: 8pt;
        }
        
        .presentation-title {
            margin-top: 0.5mm;
            font-size: 8pt;
            line-height: 1.2;
        }
        
        .memo-space {
            width: 30mm;
            border-left: 1px dashed #ccc;
            padding-left: 2mm;
            position: relative;
            min-height: 10mm;
        }
        
        .memo-label {
            position: absolute;
            top: 0;
            right: 0;
            font-size: 6pt;
            color: #999;
        }
        
        .break-session {
            text-align: center;
            padding: 1.5mm;
            background-color: #e8f4ff;
            border: 1px solid #b3d9ff;
            margin: 2mm 0;
            font-size: 8.5pt;
        }
        
        .poster-session {
            margin-bottom: 3mm;
        }
        
        .poster-list {
            border: 1px solid #ddd;
            border-top: none;
        }
        
        .poster-item {
            padding: 1.5mm 2mm;
            border-bottom: 1px dashed #ddd;
            display: flex;
            gap: 2mm;
            page-break-inside: avoid;
        }
        
        .poster-item:last-child {
            border-bottom: none;
        }
        
        .poster-info {
            flex: 1;
        }
        
        .poster-info .presentation-speaker {
            font-size: 8pt;
        }
        
        .poster-info .presentation-title {
            font-size: 7.5pt;
        }
        
        .page-number {
            text-align: center;
            margin-top: 10mm;
            font-size: 8pt;
            color: #666;
        }
        
        @media print {
            body {
                width: 210mm;
                height: 297mm;
            }
            
            .no-break {
                page-break-inside: avoid;
            }
        }
        
        .venue-info {
            margin: 5mm 0;
            padding: 3mm;
            border: 1px solid #ddd;
            background-color: #f9f9f9;
        }
        
        .venue-info h4 {
            font-size: 10pt;
            margin-bottom: 2mm;
        }
        
        .venue-info p {
            margin: 1mm 0;
            font-size: 8.5pt;
        }
        
        @media screen {
            body {
                max-width: 210mm;
                margin: 0 auto;
                background: #f5f5f5;
            }
            
            .page {
                background: white;
                margin: 10mm auto;
                padding: 15mm 10mm;
                box-shadow: 0 0 10px rgba(0,0,0,0.1);
            }
        }
    </style>
</head>
<body>
    <!-- 表紙ページ -->
    <div class="page">
        <div style="margin-top: 50mm;">
            <h1 style="font-size: 24pt; border: none;">{{ site.data.event_info.title }}</h1>
            <div class="event-info" style="margin-top: 20mm;">
                <p style="font-size: 14pt;">当日配布資料</p>
                <p style="font-size: 12pt; margin-top: 10mm;">{{ site.data.event_info.dates }}</p>
                <p style="font-size: 11pt; margin-top: 5mm;">{{ site.data.venue_info.venue_name }}</p>
            </div>
        </div>
        
        <div class="venue-info" style="margin-top: 40mm;">
            <h4>会場案内</h4>
            <p>◆ 口頭発表会場：14号館 202教室</p>
            <p>◆ ポスター会場A：14号館 204-205教室</p>
            <p>◆ ポスター会場B：14号館 206-207教室</p>
        </div>
        
        <div style="margin-top: 30mm; padding: 5mm; border: 1px solid #999;">
            <p style="font-size: 10pt;">氏名 / Name:</p>
            <div style="height: 10mm; border-bottom: 1px solid #ccc; margin-top: 3mm;"></div>
            <p style="font-size: 10pt; margin-top: 5mm;">所属 / Affiliation:</p>
            <div style="height: 10mm; border-bottom: 1px solid #ccc; margin-top: 3mm;"></div>
        </div>
    </div>
    
    <!-- 1日目 -->
    <div class="page">
        <h1>1日目：{{ site.data.schedule.day1.date }}</h1>
        
        {% for session in site.data.schedule.day1.sessions %}
        {% if session.type == "break" %}
        <div class="break-session">
            {{ session.time }} - {{ session.title }}
        </div>
        {% elsif session.presentations %}
            {% if session.type == "poster" %}
            <div class="poster-session no-break">
                <div class="session-header">{{ session.time }} - {{ session.title }}</div>
                <div class="poster-list">
                    {% for presentation in session.presentations %}
                    <div class="poster-item">
                        <div class="poster-info">
                            <div>
                                <span class="presentation-speaker">{{ presentation.speaker }}</span>
                                {% if presentation.affiliation and presentation.affiliation != "" %}
                                <span class="presentation-affiliation">（{{ presentation.affiliation }}）</span>
                                {% endif %}
                            </div>
                            <div class="presentation-title">{{ presentation.title }}</div>
                        </div>
                        <div class="memo-space" style="width: 25mm;">
                            <span class="memo-label">メモ</span>
                        </div>
                    </div>
                    {% endfor %}
                </div>
            </div>
            {% else %}
            <div class="session no-break">
                <div class="session-header">{{ session.time }} - {{ session.title }}</div>
                {% for presentation in session.presentations %}
                <div class="presentation">
                    <div class="presentation-info">
                        <div>
                            <span class="presentation-time">{{ presentation.time }}</span>
                            <span class="presentation-speaker">{{ presentation.speaker }}</span>
                            {% if presentation.affiliation and presentation.affiliation != "" %}
                            <span class="presentation-affiliation">（{{ presentation.affiliation }}）</span>
                            {% endif %}
                        </div>
                        <div class="presentation-title">{{ presentation.title }}</div>
                    </div>
                    <div class="memo-space">
                        <span class="memo-label">メモ</span>
                    </div>
                </div>
                {% endfor %}
            </div>
            {% endif %}
        {% else %}
        <div class="session">
            <div class="session-header">{{ session.time }} - {{ session.title }}</div>
            {% if session.speaker or session.presentation_title %}
            <div class="presentation">
                <div class="presentation-info">
                    {% if session.speaker %}
                    <div class="presentation-speaker">{{ session.speaker }}</div>
                    {% endif %}
                    {% if session.presentation_title %}
                    <div class="presentation-title">「{{ session.presentation_title }}」</div>
                    {% endif %}
                </div>
                <div class="memo-space">
                    <span class="memo-label">メモ</span>
                </div>
            </div>
            {% endif %}
        </div>
        {% endif %}
        {% endfor %}
    </div>
    
    <!-- 2日目 -->
    <div class="page">
        <h1>2日目：{{ site.data.schedule.day2.date }}</h1>
        
        {% for session in site.data.schedule.day2.sessions %}
        {% if session.type == "break" %}
        <div class="break-session">
            {{ session.time }} - {{ session.title }}
        </div>
        {% elsif session.presentations %}
            {% if session.type == "poster" %}
            <div class="poster-session no-break">
                <div class="session-header">{{ session.time }} - {{ session.title }}</div>
                <div class="poster-list">
                    {% for presentation in session.presentations %}
                    <div class="poster-item">
                        <div class="poster-info">
                            <div>
                                <span class="presentation-speaker">{{ presentation.speaker }}</span>
                                {% if presentation.affiliation and presentation.affiliation != "" %}
                                <span class="presentation-affiliation">（{{ presentation.affiliation }}）</span>
                                {% endif %}
                            </div>
                            <div class="presentation-title">{{ presentation.title }}</div>
                        </div>
                        <div class="memo-space" style="width: 25mm;">
                            <span class="memo-label">メモ</span>
                        </div>
                    </div>
                    {% endfor %}
                </div>
            </div>
            {% else %}
            <div class="session no-break">
                <div class="session-header">{{ session.time }} - {{ session.title }}</div>
                {% for presentation in session.presentations %}
                <div class="presentation">
                    <div class="presentation-info">
                        <div>
                            <span class="presentation-time">{{ presentation.time }}</span>
                            <span class="presentation-speaker">{{ presentation.speaker }}</span>
                            {% if presentation.affiliation and presentation.affiliation != "" %}
                            <span class="presentation-affiliation">（{{ presentation.affiliation }}）</span>
                            {% endif %}
                        </div>
                        <div class="presentation-title">{{ presentation.title }}</div>
                    </div>
                    <div class="memo-space">
                        <span class="memo-label">メモ</span>
                    </div>
                </div>
                {% endfor %}
            </div>
            {% endif %}
        {% else %}
        <div class="session">
            <div class="session-header">{{ session.time }} - {{ session.title }}</div>
            {% if session.speaker or session.presentation_title or session.topic %}
            <div class="presentation">
                <div class="presentation-info">
                    {% if session.speaker %}
                    <div class="presentation-speaker">{{ session.speaker }}</div>
                    {% endif %}
                    {% if session.presentation_title %}
                    <div class="presentation-title">「{{ session.presentation_title }}」</div>
                    {% endif %}
                    {% if session.topic %}
                    <div class="presentation-title">「{{ session.topic }}」</div>
                    {% endif %}
                </div>
                <div class="memo-space">
                    <span class="memo-label">メモ</span>
                </div>
            </div>
            {% endif %}
        </div>
        {% endif %}
        {% endfor %}
    </div>
    
    <!-- メモページ -->
    <div class="page">
        <h1>メモ</h1>
        <div style="height: 240mm;">
            <div style="height: 100%; background: repeating-linear-gradient(white, white 7mm, #f0f0f0 7mm, #f0f0f0 7.5mm);"></div>
        </div>
    </div>
</body>
</html>