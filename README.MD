# Custom Liferay DDM Form Fields

Custom form fields for Liferay 7.3 built using React.

## Fields Included:

[Userdata Field](/modules/userdata-field/README.md)

[Character Limited Text Input](/modules/character-limited-text)

![example](/images/example.gif)

## Steps to Deploy

If you don't already have blade installed, you can find steps for that [here](https://help.liferay.com/hc/en-us/articles/360028833852-Installing-Blade-CLI).

1. Update the `liferay.workspace.home.dir=/path/to/liferay/home` property to point towards your liferay home directory.
2. From the root directory run `blade gw depoy`.

## Steps to Create

1. `$ blade init -v dxp-7.3-ga1 custom-liferay-ddm-form-fields`
2. `$ cd custom-liferay-ddm-form-fields`;
3.
```
$ blade create \
-t form-field \
-c CharacterLimitedText \
--js-framework react \
-p com.liferay.dynamic.data.mapping.form.field.type.internal.character.limited.text \
character-limited-text

```

At this point the field is ready to deploy.

To add custom settings for fields you will need to add additional files. This can be seen in the commit `Add logic for character limited text field`.