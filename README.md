TwoFactorAuth.org
=================

A list of popular sites and whether or not they accept two factor auth.

## The Goal

The goal is to have a website with a comprehensive list of sites that support
two factor auth as well as the methods that they support it.

This is to aid when deciding on alternative services based on the security they
offer for their customers.

This also is a way for consumers to see what sites still need to invest in
further security practices and which ones already do.

## Contributing

All the data is managed through a [Yaml][yaml] file so it may be useful to read
up on the Yaml syntax.

To add a new site, go to the [data file](_data/main.yml) and get familiar with
how it is setup. There is a section for each Category and they all follow this
syntax:

### New Sections

To add a new section, modify the `sections` value and follow the template below:

```yml
sections:
  - id: category-id
    title: Category Name
    icon: icon-class

    websites:
        # Sites go here...
```

### New Sites

The values should be pretty straight forward for adding a new website. The
`websites` array should already be defined, just add a new website to it like
this example:

```yml
    websites:
        - name: Site
          url: https://site.com
          img: site.png
          tfa: Yes
          goog: Yes
          authy: Yes
          sms: Yes
          doc: <url to the documentation>
          custom:
              - icon: android
                url: <url to a custom Android client>
              - icon: apple
                url: <url to a custom iOS client>
              # Any other custom clients...
```


## License

This code is distributed under the MIT license. For more info, read the
[LICENSE](/LICENSE) file distributed with the source code.

[yaml]: http://www.yaml.org/
