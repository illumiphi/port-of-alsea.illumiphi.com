% name: Attachment
% def: document="$(fzf)"
% def: author="/roxie"
% def: post_date=$(date +%m/%d/%Y)
---
template: article
title: ${title}
subtitle: ${subtitle}
date: ${post_date}
author: ${author}
taxonomy:
    category:
        - Documents
    tag:
        - ${tag}
---

Download: [${title}](${document})

===


