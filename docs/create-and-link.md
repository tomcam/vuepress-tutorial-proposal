# Create and link to more pages

A VuePress documentation site consists of one or more directories.
Each directory requires at least a single file named `README.md`.
Filenames are considered to be case sensitive and the uppercase
naming is expected for this, the main file of each directory. 
`README.md` is a filename with special significance. It
will be translated to `index.html` ultimately, but naming it
`README.md` helps avoid name collisions with other readme files.

Files ending in `.md` use a simplified formatting scheme called
[Markdown](https://guides.github.com/features/mastering-markdown/).
These files are translated by VuePress into HTML.

Normally there will be other files in the directory, of course.

Here's a minimal Markdown file that links to another one.
You can append this text to bottom the `README.md` file in the
root (in this case, `/docs/`) directory of your
VuePress project if you like, because the `/guide/`
directory has already been created for demonstration purposes.

```markdown
# Markdown demo page

If you want specifics, try the 
[using vue](/guide/using-vue.md) section. 
Otherwise, get an overview by visiting 
the [guide](/guide/).
```

This shows pretty much everything you need to link to
pages or directories. `# Markdown demo page` will
be converted to an `<h1>` tag in HTML. VuePress
automatically creates an anchor to that part of the
page. If you had written `## Markdown demo page`
you'd end up with an `<h2>` tag, and so on.

The Markdown `[using vue](/guide/using-vue.md)`
will be rendered into an HTML link to a document called `using-vue.html`
in the `/guide` directory, with `using vue` as the anchor text.
The plain text surrounding it becomes a standard `<p>` paragraph.

The Markdown `get an overview by visiting 
the [guide](/guide/)` contains a link to the `/guide` directory, where
it expects to find at least one file named `README.md`.

You can learn more about how this works where the
VuePress [directory structure](https://vuepress.vuejs.org/guide/directory-structure.html#default-page-routing)
is documented.

It's slightly odd but helpful that links to files are by convention targeted
at the Markdown file, not the generated HTML file. For
example, `using-vue.md` generates the target that you really want to link
to, which is `using-vue.html`. You can of course link directly to any 
file on the web.

How about images? That's discussed in [Handling graphic assets](graphic-assets.md)
