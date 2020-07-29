% name: Agenda
% folder: date
% def: title='Agenda'
% def: subtitle="Regular Meeting of the Port of Alsea Board of Commissioners"
% def: author="/roxie"
% def: post_date=$(date +%Y-%m-%d)
% def: event_date="$(grep startDate *.md | awk '{$1=""; print $0}' | xargs -I{} date '+%A, %B %d, %Y %I:%m %p' --date="{}")"
% def: summary="$event_date at the Port Office"
---
title: ${title}
subtitle: ${subtitle}
template: article
author: ${author}
collection:
    name: Attachments
    showCount: true
    showMenu: true
content:
    items: '@self.children'
child_type: article
date: ${post_date}
taxonomy:
    category: 
        - Documents
    tag: 
        - agenda
---

${summary}

===


