# Simple Preloading Screen

## Step-by-Step Video:

[YouTube-Link => Loading Spinner until Ready: Simple Preloading Screen](https://youtu.be/xUma9U4Ekto)

## Source Code:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Preloading Spinner</title>
        <style>
            body {
                margin: 0;
                background: #191919;
                text-align: center;
                color: #ffffff;
            }

            .preloader {
                display: flex;
                justify-content: center;
                align-items: center;
                background-color: #191919;
                position: absolute;
                top: 0;
                left: 0;
                height: 100%;
                width: 100%;
                z-index: 99999999;
            }

            .preloader img {
                width: 200px;
            }
        </style>
    </head>
    <body>
        <div class="preloader">
            <img src="loader.svg" />
        </div>
        <div class="main-content">
            <h1>Welcome!</h1>
            <h2>
                This content is not visible until loading of page content is
                complete
            </h2>
            <p>
                Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed
                diam nonumy eirmod tempor invidunt ut labore et dolore magna
                aliquyam erat, sed diam voluptua. At vero eos et accusam et
                justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea
                takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum
                dolor sit amet, consetetur sadipscing elitr, sed diam nonumy
                eirmod tempor invidunt ut labore et dolore magna aliquyam erat,
                sed diam voluptua. At vero eos et accusam et justo duo dolores
                et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus
                est Lorem ipsum dolor sit amet.
            </p>
        </div>
        <script>
            window.onload = function() {
                // Small delay to see the effect, most often you would wait for api request here
                setTimeout(() => {
                    document.getElementsByClassName(
                        'preloader'
                    )[0].style.display = 'none';
                }, 1000);
            };
        </script>
    </body>
</html>
```
