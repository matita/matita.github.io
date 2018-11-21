---
layout: post
published: false
title: Link to create events on Google Calendar
---
This is something I periodically search for, so I decided to finally write it down somewhere.

Is there a way to construct a link that opens a prefilled Google Calendar form to create an event?  
Yes, there is.

And that's it:

```
https://www.google.com/calendar/render?
  action=TEMPLATE&
  text=Your+Event+Name&
  dates=20140127T224000Z/20140320T221500Z&
  details=For+details,+link+here:+http://www.example.com&
  location=Waldorf+Astoria,+301+Park+Ave+,+New+York,+NY+10022&
  sf=true&
  output=xml
```
[Try it!](https://www.google.com/calendar/render?action=TEMPLATE&text=Your+Event+Name&dates=20140127T224000Z/20140320T221500Z&details=For+details,+link+here:+http://www.example.com&location=Waldorf+Astoria,+301+Park+Ave+,+New+York,+NY+10022&sf=true&output=xml)

As per 2018/11/21 this URL is redirected to:

```
https://calendar.google.com/calendar/r/eventedit?
  text=Your+Event+Name&
  dates=20140127T224000Z/20140320T221500Z&
  details=For+details,+link+here:+http://www.example.com
  &location=Waldorf+Astoria,+301+Park+Ave+,+New+York,+NY+10022&
  sf=true&
  output=xml
```
[Try it!](https://calendar.google.com/calendar/r/eventedit?text=Your+Event+Name&dates=20140127T224000Z/20140320T221500Z&details=For+details,+link+here:+http://www.example.com&location=Waldorf+Astoria,+301+Park+Ave+,+New+York,+NY+10022&sf=true&output=xml)