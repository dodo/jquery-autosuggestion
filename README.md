# jQuery plugin for auto suggestion

a simple plugin with which input fields can be extended so that they show a suggestion part

eg if you try to enter an email address it allows you to suggest the domain name

what you type in:

    [test           ]

what you can see and get from the input field:

    [test@domain.lit]

## usage

```javascript
$('input[type="email"]').autoSuggestion({suffix:"domain.lit"});
```

if you want to do more stuff with the input you can use a function:

```javascript
$('input[type="email"]').autoSuggestion({suffix:function (val) {
    if (val === "" || val.indexOf("@") !== -1) {
        return "";
    } else {
        return "@domain.lit";
    }
}});
```

if you want to have a more robust responsebility you can add the special input event plugin which uses the new `oninput` event and works for old browsers as well.

## depends on

* [copyCSS](http://plugins.jquery.com/project/copyCSS)
* [`input` special event](https://github.com/dodo/jquery-inputevent) (optional)

## todo

prefix, something better than keyup
