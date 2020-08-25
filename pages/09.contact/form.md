---
published: false
title: Contact
subtitle: send us a message
taxonomy:
    photon:
        - header
form:
    name: contact-form
    fields:
        -
            name: name
            label: Name
            placeholder: 'Enter your name'
            autofocus: 'on'
            autocomplete: 'on'
            type: text
            validate:
                required: true
        -
            name: email
            label: Email
            placeholder: 'Enter your email address'
            type: email
            validate:
                required: true
        -
            name: message
            label: Message
            placeholder: 'Enter your message'
            type: textarea
            validate:
                required: true
    buttons:
        -
            type: submit
            value: Submit
        -
            type: reset
            value: Reset
    process:
        -
            email:
                from: '{{ config.plugins.email.from }}'
                to:
                    - '{{ config.plugins.email.from }}'
                    - '{{ form.value.email }}'
                subject: '[CONTACT] {{ form.value.name|e }}'
                body: '{% include ''forms/data.html.twig'' %}'
        -
            save:
                fileprefix: feedback-
                dateformat: Ymd-His-u
                extension: txt
                body: '{% include ''forms/data.txt.twig'' %}'
        -
            message: 'Thank you for your feedback!'
        -
            display: thankyou
---

We look forward to hearing from you

===


# Port of Alsea, Marina and Office

[map-leaflet lat=44.434464 lng=-124.059657 zoom=13 mapname=transd style=transport-dark ]
[a-markers markerColor="lightred"
iconColor="white"
]
[{ "lat": 44.434464, "lng": -124.059657, "icon": "home", "title": "Port of Alsea Marina and Office" } ]
[/a-markers]
[a-markers icon=""]
[  { "lat": 37.775,  "lng": -122.48 , "text": 1, "draggable": true  },
{ "lat":  37.77,  "lng": -122.414 , "text": 2, "markerColor": "pink" },
{ "lat":   37.765,  "lng": -122.409, "text": 3, "spin": true },
{ "lat":   37.76,  "lng": -122.3995, "text": 4, "spin": false },
{ "lat":   37.755,  "lng": -122.499, "icon": "coffee", "markerColor": "lightred", "title": "Lovely bistro"}
]
[/a-markers]
[/map-leaflet]
