% name: Financials
% def: document="$(fzf)"
% def: event_date="$(grep startDate *.md | awk '{$1=""; print $0}' | xargs -I{} date '+%A, %B %d, %Y %I:%M %p' --date="{}")"
% def: title='Financials'
% def: subtitle="$(date '+%B %Y' -d "$event_date -1 months")"
% def: author="/roxie"
% def: post_date=$(date +%m/%d/%Y)
% def: summary="Financials for $(date '+%B %Y' -d "$event_date -1 months")"
---
template: article
title: ${title}
subtitle: ${subtitle}
date: ${post_date}
author: ${author}
content:
    title: Attachments
    items: '@self.children'
taxonomy:
    category: 
        - Documents
    tag: 
        - financials
---

${summary}

Download: [${title} - ${subtitle}](${document})

===


