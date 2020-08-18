% name: Board Meeting Event
% folder: event
% def: title='Board of Commissioners'
% def: subtitle='Regular Monthly Meeting'
% def: author='/roxie'
% def: post_date=$(date +%m/%d/%Y)
% def: start_dt="$(date +%Y-%m-%d) 14:00"
% def: place_name='Port Office'
% def: place_street='365 Port St #A'
% def: place_city='Waldport'
% def: place_state='OR'
% def: place_zip='97394'
% def: place_country='US'
% def: place_lat='44.4343779'
% def: place_long='-124.0593175'
---
template: event
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
        - Meetings
    tag: 
        - Commissioners
show_gallery: false
data:
    event:
        '@type': Event
        startDate: ${start_dt}
        location:
            '@type': Place
            name: ${place_name}
            addcdss:
                streetAddress: ${place_street}
                addressLocality: ${place_city}
                addressRegion: ${place_state}
                postalCode: ${place_zip}
                addressCountry: ${place_country}
            geo:
                '@type': GeoCoordinates
                latitude: ${place_lat}
                longitude:  ${place_long} 
---

- The regular monthly meeting of the Port of Alsea Board of Commissioners will be held on ${start_dt_long} via teleconference

===



## Related Documents
The agenda and related documents will be posted on the [Port of Alsea Calendar](http://www.portofalsea.com/calendar) entry for this meeting. Contact the Port Office to request hard copies.

## To Join the Teleconference
- dial-in to 1-848-220-3300. (toll-free)
- after the prompt, enter Conference ID number 1216-1947.

## To Provide Comments
- instructions will be given at the start of the teleconference on how and when the public can provide comments.
- written comments can be delivered to the Port Office up to 30 minutes prior to the start of the meeting for inclusion into the record.

## Regular Meetings
Regular meetings of the Port of Alsea Board of Commissioners are usually scheduled on the third Thursday of every month at 2:00 PM. Due to Covid-19 restrictions, the Board will be inviting the public to participate on the teleconference until further notice.

Those who wish to attend the meeting but cannot do so by phone or require other accommodations should contact the Port Manager within 48 hours of the meeting. 

## Contact
Contact us with any questions, comments, or requests. 

>> Roxie Cuellar, Port Manager
    rcuellar@portofalsea.com
    541-563-3872 

