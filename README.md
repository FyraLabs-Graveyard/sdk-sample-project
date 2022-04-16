# tauOS Sample Project

## Building

```sh
$ meson builddir --prefix=/usr/bin
$ cd builddir
$ ninja
$ ninja test
$ sudo ninja install
```

## Generating translations

```sh
$ meson builddir --prefix=/usr/bin
$ cd builddir
$ ninja my-project-pot
```

## Adding a new translation

1. Generate translations as listed above
2. Add the ISO 3166 language code to `po/LINGUAS`
3.
```sh
$ ninja my-project-update-po
```

## Packaging

```sh
$ flatpak-builder --user --install --force-clean flatpak com.example.MyProject.yml
```

Please visit the tauOS Developer Docs for more information, and happy hacking!
