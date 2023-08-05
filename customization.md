# Customization

## Hide the EQ bar

Remove the `#` in front of `contentBar` in [line 116](https://github.com/metarex21/Showtify/blob/main/api/spotify.py#L116) of current master, then the EQ bar will be hidden when you're in not currently playing anything.

## Status String

Have a string saying either "Vibing to:" or "Last seen playing:".

* Change [`height` to `height + 40`](https://github.com/metarex21/Showtify/blob/main/api/templates/spotify.html.j2#L1-L2) (or whatever `margin-top` is set to)
* Uncomment [**.main**'s `margin-top`](https://github.com/metarex21/Showtify/blob/main/api/templates/spotify.html.j2#L10)
* Uncomment [currentStatus](https://github.com/metarex21/Showtify/blob/main/api/templates/spotify.html.j2#L93)

## Theme Templates

If you want to change the widget theme, you can do so by the changing the `current-theme` property in the `templates.json` file.

Themes:
* `light`
* `dark`

If you wish to customize farther, you can add your own customized `spotify.html.j2` file to the templates folder, and add the theme and file name to the `templates` dictionary in the `templates.json` file.

## Color

You can customize the appearance of your `Card` however you wish with URL params.

### Common Options:

- `background_color` - Card's background color _(hex color)_ without `#`
- `border_color` - Card border color _(hex color)_ without `#`

Use `/?background_color=8b0000&border_color=ffffff` parameter like so:  
&nbsp; <br> [![Spotify](https://showtify.vercel.app/api/spotify?background_color=0d1117&border_color=ffffff)]()
