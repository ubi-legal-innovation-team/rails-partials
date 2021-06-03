First of all make sure you've created a rails app

```bash
rails new APP_NAME
```

## Setup

Add Rails' default partials:

```
curl -L https://raw.githubusercontent.com/ubi-legal-innovation-team/rails-partials/master/partials/_flashes.html.erb > app/views/shared/_flashes.html.erb
curl -L https://raw.githubusercontent.com/ubi-legal-innovation-team/rails-partials/master/partials/_footer.html.erb > app/views/shared/_footer.html.erb
curl -L https://raw.githubusercontent.com/ubi-legal-innovation-team/rails-partials/master/partials/_navbar.html.erb > app/views/shared/_navbar.html.erb
curl -L https://raw.githubusercontent.com/ubi-legal-innovation-team/rails-partials/master/partials/navbar_components/_menu.html.erb > app/views/shared/navbar_components/_menu.html.erb
curl -L https://raw.githubusercontent.com/ubi-legal-innovation-team/rails-partials/master/partials/navbar_components/_notifications.html.erb > app/views/shared/navbar_components/_notifications.html.erb
curl -L https://raw.githubusercontent.com/ubi-legal-innovation-team/rails-partials/master/partials/navbar_components/_user_nav.html.erb > app/views/shared/navbar_components/_user_nav.html.erb
curl -L https://raw.githubusercontent.com/ubi-legal-innovation-team/rails-partials/master/partials/ajax/ajax_calls/_user_nav.html.erb > app/views/ajax/ajax_calls/_user_nav.html.erb
curl -L https://raw.githubusercontent.com/ubi-legal-innovation-team/rails-partials/master/partials/ajax/ajax_calls/_notifications.html.erb > app/views/ajax/ajax_calls/_notifications.html.erb
curl -L https://raw.githubusercontent.com/ubi-legal-innovation-team/rails-partials/master/partials/ajax/ajax_calls/modals/_example.html.erb > app/views/ajax/ajax_calls/modals/_example.html.erb
```

**On Ubuntu/Windows**: if the `unzip` command returns an error, please install it first by running `sudo apt install unzip`.

Then add partials to your application's layout as below and the viewport :

```html
<!-- app/views/layouts/application.html.erb -->
<head>
  <!-- Add these line for detecting device width -->
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">

  <!-- [...] -->
</head>

<body>
    <%= render "shared/navbar" %>

    <!-- [...] -->

    <%= yield %>

    <!-- [...] -->

    <%= render "shared/flashes" %>
    <%= render "shared/footer" %>
</body>
```
