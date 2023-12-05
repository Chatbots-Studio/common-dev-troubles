## Detecing "Enter" press on mobile
To manage to detect key "Enter" or 13 you have to add ```enterKeyHint='send'``` to your input component.

Then you can easily detect this event with ```onKeyDown``` etc.


Visit: https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/enterkeyhint)

## Ignore switching between inputs with "Tab" or "Enter"
You can face problem when user press "Enter" key on android / ios and it's switches to next input WITHOUT firing focus & blur event. The same behavior is noticed when you pressing "Tab" between inputs.

To solve this add ```tabIndex={-1}``` to your component.
