(plugins-for-napari-developers)=

# napari plugin architecture

```{admonition} Introducing npe2
:class: tip
We introduced a new plugin engine in December 2021. The new library [`npe2`][npe2]
is a re-imagining of how napari interacts with plugins. Plugins targeting
`napari-plugin-engine` will continue to work, but we recommend migrating to
`npe2` as soon as possible.  See the [](npe2-migration-guide).

To learn more about the architecture see the [](npe2-manifest-spec).
```

The napari plugin architecture is contained in an independent package called [napari-plugin-engine](https://github.com/napari/napari-plugin-engine), which
is a fork of [pluggy](https://github.com/pytest-dev/pluggy). The concept is
based around:

- **hook specifications**: function signatures that identify an API (argument
  names and types) that plugin developers must adhere to
- **hook implementations**: functions that plugin developers write to extend
  napari functionality, by providing the actual mechanism (implementation) for
  a specific hook specification.

The best place to get started with learning how plugins are incorporated into
napari is to look at the `napari-plugin-engine` [documentation](https://napari-plugin-engine.readthedocs.io/en/latest/). In particular,
look through the [Usage Overview](https://napari-plugin-engine.readthedocs.io/en/latest/usage.html) and the
[API Reference](https://napari-plugin-engine.readthedocs.io/en/latest/api.html).

The [documentation for pluggy](https://pluggy.readthedocs.io/en/latest/) is
also useful for understanding the concepts, but do note that a lot of the
attribute names and API is different in `napari-plugin-engine`.

[npe2]: https://github.com/napari/npe2
