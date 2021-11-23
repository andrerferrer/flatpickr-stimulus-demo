# GOAL

This is a demo to show-case how to implement an easy date picker in rails using the `simple form` gem and the `flatpickr` plugin using `stimulus`.

This demo was created from [this](https://github.com/andrerferrer/flatpickr-demo#goal) one

[You can also check my other demos](https://github.com/andrerferrer/dedemos/blob/master/README.md#ded%C3%A9mos).

## What needs to be done?

- install stimulus
```sh
rails webpacker:install:stimulus
```

- create a new controller with the flatpickr logic
```js
// app/javascript/controllers/flatpickr_controller.js
import { Controller } from "stimulus"
import flatpickr from "flatpickr";

export default class extends Controller {
  connect() {
    flatpickr(".datepicker", {});

  }
}
```

- add the data-controller to the input
```erb
  <!-- app/views/bookings/index.html.erb -->
  <%= f.input :booked_at, as: :string, input_html: {class: "datepicker", data: { controller: 'flatpickr' } } %>
```

- [refactor removing the need for a class if you want](https://github.com/andrerferrer/flatpickr-stimulus-demo/commit/22c68606999e4fb7c564b9b940ecfa21f7f4efd2)

And we're good to go

Good Luck 🍀 and Have Fun 🤓
