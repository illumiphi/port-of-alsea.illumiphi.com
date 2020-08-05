% name: Minutes
% def: title='Minutes'
% def: subtitle="Regular Meeting of the Port of Alsea Board of Commissioners"
% def: author="/roxie"
% def: post_date=$(date +%m/%d/%Y)
% def: event_date="$(grep startDate *.md | awk '{$1=""; print $0}' | xargs -I{} date '+%A, %B %d, %Y %I:%M %p' --date="{}")"
% def: summary="$event_date at the Port Office"
---
template: article
title: ${title}
subtitle: ${subtitle}
date: ${post_date}
author: ${author}
sets:
    default:
        name: Attachments
        showCount: true
        showMenu: true
content:
    items: '@self.children'
taxonomy:
    category: 
        - Documents
    tag: 
        - minutes
---

${summary}

===


