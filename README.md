This repository holds diagrams for an assignment from the course WA3064.102 at ITESM GDA.

This is not an active project.

The diagrams can be found under the [diagrams](diagrams) folder.

This uses mermaid as tool to generate the diagrams based on a markdown file. Please install mermaid CLI.

```
npm install -g @mermaid-js/mermaid-cli
```

To generate the diagrams, run the following command:

```bash
$ mkdir out
$ mmdc -i diagrams/<diagram>.md -o out/<diagram>.png
```