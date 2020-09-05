---
title: 'Property Line Adjustment'
body_classes: application
form:
    name: property-line-adjustment
    fields:
        -
            name: applicant
            type: fieldset
            id: applicant
            legend: 'Applicant Information'
            fields:
                -
                    name: name
                    label: Name
                    placeholder: 'Enter your name'
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
            name: application-type
            type: radio
            label: 'Select Application Type'
            default: conditional_use
            options:
                conditional_use: 'Conditional Use $250'
                nonconforming_use: 'Nonconforming Use $250'
                variance: 'Variance $250'
                zone_change: 'Zone Change $500'
                comp_plan_change: 'Comprehensive Plan Change $500'
                urban_growth_change: 'Urban Growth Boundary Change $1000'
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
                subject: '[Site Contact Form] {{ form.value.name|e }}'
                body: '{% include ''forms/data.html.twig'' %}'
        -
            save:
                fileprefix: land-use-app-
                dateformat: Ymd-His-u
                extension: txt
                body: '{% include ''forms/data.txt.twig'' %}'
        -
            message: 'Thank you for getting in touch!'
        -
            display: thankyou
---

Application for Conditional Use, Nonconforming Use, Variance, Zone Chang, Comprehensive Plan Change, Urban Growth Boundary Change

===

[Original PDF](land_use_app.pdf)

City of Yachats

441 Hwy 101 N
PO Box 345
Yachats OR 97498

(541) 547-3565
