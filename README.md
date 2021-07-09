# TerminoloGit Template

This IG template is used to display further information regarding Code Systems and Value Sets. The template is based on [HL7 Austria's IG template](https://github.com/gabriel0316/hl7at_template).

For Code Systems the display of the following additional file formats is possible:
- FSH v1
- ClaML v3
- PropCSV v1

## Getting Started

Follow these instructions for using this template in your IG.

### Prerequisites

In order to use the template you have to have set up an IG Publisher project - see [https://build.fhir.org/ig/FHIR/ig-guidance/index.html](https://build.fhir.org/ig/FHIR/ig-guidance/index.html) for more details.

### Installing

Use this template by cloning this repository into a local directory and configuring IG's `ig.ini` as follows:

```
[IG]
template = <path_to_directory>/terminologit_template
```

### Additional File Formats

Currently, the following additional file formats (and file extensions) for Code Systems are **supported and required**, if this template is being used:
- FSH v1 (`.fsh`)
- ClaML v3 (`.claml.xml`)
- PropCSV v1 (`.csv`)

The source files for these formats have to be placed into the following directory of the IG:

```
input/additionalFormats
```

For displaying the source file's content in HTML a `.xhtml` file has to be created for each of the supported additional file formats and placed into IG's

```
input/includes
```

The file's content has to be structured as follows. Make sure to escape `"` with `&quot;`, `<` with `&lt;`, and `>` with `&gt;`.

```
{% raw %}<pre class="xml"><code>

<!-- source file's content goes here -->

</code></pre>{% endraw %}
```
## Versioning

TODO
We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

## Authors

* **Gabriel Kleinoscheg** - *Initial work*

## License

TODO
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
