# GOAL

This is a demo to show-case how to implement an easy date picker in rails using the `simple form` gem.

[You can also check my other demos](https://github.com/andrerferrer/dedemos/blob/master/README.md#ded%C3%A9mos).

## TLDR
```erb
<%= f.input :a_date, as: :date, html5: true %>
<%= f.input :a_date, as: :datetime, html5: true %>
```

## What needs to be done?

- `yarn add flatpickr`

- have a model with the date / date-time

eg.: `rails g model booking restaurant:references booked_at:datetime`

- create the form:

```erb
  <h2>Create a new booking</h2>
  <%= simple_form_for Booking.new do |f| %>
    <%= f.input :booked_at, as: :datetime, html5: true %>

    <%# It would work as date as well! %>
    <%# f.input :booked_at, as: :date %>
    
    <%= f.association :restaurant %>
    <%= f.submit %>
  <% end %>
```



And we're good to go

Good Luck 🍀 and Have Fun 🤓
