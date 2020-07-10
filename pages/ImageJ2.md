---
autogenerated: true
title: ImageJ2
breadcrumb: ImageJ2
layout: page
author: test author
categories: Software,ImageJ2,SciJava,Citable
description: test description
---

{% include project content='ImageJ' %}

<div style="clear: right; float: right">

{% include sidebox-right float='right' text='

<h2>

ImageJ2"s Mission

</h2>

  - """Design""" the next generation of ImageJ, driven by the needs of
    the community.
  - """Collaborate""" across organizations, fostering open development
    through sharing and reuse.
  - """Broaden""" ImageJ"s usefulness and relevance across many
    disciplines of the scientific community.
  - """Maintain""" backwards compatibility with existing ImageJ
    functionality.
  - """Unify""" online resources to a central location for the ImageJ
    community.
  - """Lead""" ImageJ development with a clear vision.

See also [these presentation slides about
ImageJ](https://imagej.github.io/presentations/2015-09-03-imagej2-and-fiji/#/4).'
%}

</div>

ImageJ2 is a new version of [ImageJ](ImageJ "wikilink") for the next
generation of multidimensional image data, with a focus on scientific
imaging. Its central goal is to broaden the paradigm of ImageJ beyond
the limitations of ImageJ 1.x, to support the next generation of
multidimensional scientific imaging.

To ensure backwards compatibility, ImageJ2 has been designed to fully
integrate into the existing ImageJ user interface. This allows users to
keep using ImageJ in familiar ways, while providing the ability to
migrate toward more powerful new features as needed.

The [Fiji](Fiji "wikilink") distribution of ImageJ has shipped with beta
versions of ImageJ2 for quite some time, so you may already be familiar
with some of ImageJ2's features—some of which, such as the
[Updater](Updater "wikilink") and [Launcher](Launcher "wikilink"), were
originally developed as part of Fiji. {% include toc %}

## Features of ImageJ2

ImageJ2 provides a wealth of new features and capabilities:

  - The [ImageJ Updater](ImageJ_Updater "wikilink") makes it simple to
    keep your ImageJ up to date, and to add new plugins by enabling
    additional [Update Sites](Update_Sites "wikilink").
  - New and enhanced file format support via the
    [SCIFIO](SCIFIO "wikilink") library ([see
    below](#Improved_image_I.2FO_with_the_SCIFIO_library "wikilink")).
  - More powerful [Script Editor](Script_Editor "wikilink") with support
    for several scripting languages.
  - New commands:
      - {% include bc content='Plugins | Debug | Dump Stack'%} for
        debugging when things
        [hang](wikipedia:Hang_\(computing\) "wikilink").
      - {% include bc content='Plugins | Debug | System Information'%}
        for reporting on versions of installed plugins and libraries.
  - Use ImageJ2's N-dimensional [ImgLib2](ImgLib2 "wikilink")-based data
    structures (still in beta).
  - Write parameterized commands and scripts:
      - Typed inputs and outputs with no dependence on AWT user
        interface.
      - Mix and match ImageJ 1.x and ImageJ2 data structures.
      - Plugins appear in the menu automatically without plugins.config
        files.
      - Reusable in many contexts: [KNIME](KNIME "wikilink"),
        [CellProfiler](CellProfiler "wikilink"),
        [OMERO](OMERO "wikilink"), [headless](headless "wikilink")...

### Integrated search bar

![Search-bar.png](/images/pages/Search-bar.png "Search-bar.png")"

The search bar finds commands, and can search the ImageJ wiki as well as
the [ImageJ Forum](http://forum.imagej.net/) if you check those
respective checkboxes.

For power users and developers, the search bar supports execution of
"code snippets"—single lines of code for performing tasks—by starting
the query with `!`. Any code that works in the [Script
Interpreter](Script_Interpreter "wikilink") should be usable as a code
snippet.

Developers can extend the capabilities of the search bar by writing
[Searcher](https://github.com/scijava/scijava-search/blob/scijava-search-0.3.1/src/main/java/org/scijava/search/Searcher.java#L36-L46)
plugins.

### Improved image I/O with the SCIFIO library

ImageJ2 uses the [SCIFIO](SCIFIO "wikilink") library (SCientific Image
Format Input and Output) by default for most image input tasks. You can
change this behavior at any time by running {% include bc content='Edit
| Options | ImageJ2'%} and modifying the *Use SCIFIO when opening files*
option.

For further details, see the [SCIFIO](SCIFIO "wikilink") page.

### ImageJ2 is more than just an application

ImageJ2 is also a collection of reusable software libraries built on
[SciJava](SciJava "wikilink"), using a powerful plugin framework to
facilitate rapid development and painless user customization.

The following software component libraries form the core of ImageJ2:

  - [ImageJ Common](ImageJ_Common "wikilink") - The core image data
    model, using ImgLib2.
  - [ImageJ Ops](ImageJ_Ops "wikilink") - An extensible framework for
    reusable image processing algorithms.
  - [ImageJ Updater](ImageJ_Updater "wikilink") - A mechanism to update
    individual plugins and libraries within ImageJ.
  - [ImageJ Legacy](ImageJ_Legacy "wikilink") - Provides complete
    backwards compatibility with ImageJ 1.x.
  - [SciJava Common](SciJava_Common "wikilink") - The core frameworks
    for plugins, modules and the application itself.

See the [Architecture](Architecture "wikilink") page for further
details.

## Rationale

In recent years a segment of the ImageJ developer community has
repeatedly inquired as to ImageJ's future. The program has been
successful enough that it would greatly benefit from modern open source
software best practices: a publicly accessible source code repository, a
suite of unit tests with a continuous build integration system, a
central repository of extensions, clear guidelines on how external
developers can contribute to both those extensions and to the core
program when warranted, and a development roadmap addressing feature
requests and tasks from the community.

Listening to the ImageJ community, it is clear that:

1.  There is substantial demand from developers for a next-generation
    version of ImageJ with a cleaner, more modular API, so that ImageJ
    can be leveraged not just as a standalone analysis program, but as a
    **robust, extensible library** in a variety of contexts.
2.  The ImageJ user community has invested a lot of time and energy to
    develop complex workflows within ImageJ, and they oppose any change
    that would break them. Thus, any effort to improve the software must
    **maintain compatibility with existing code**.
3.  Further, any next-generation version of ImageJ must maintain
    community unity, and **not fork the project**. All components of
    this project will be developed as upgrades to core ImageJ.
4.  The ImageJ community as a whole would substantially benefit from a
    **central effort to organize** and serve program code (both the core
    application and its plugins), keep track of bugs and feature
    requests, and better leverage external developer contributions.

For more details, see the [presentation from the 2010 ImageJ
Conference](http://developer.imagej.net/2010/10/29/imagejdev-presentation-imagejconf-2010).

## Funding

ImageJ2 is funded from a variety of sources. See the
[Funding](Funding "wikilink") page for details.

## Publications

  - {% include publication content='ImageJ2' %}
  - {% include publication content='Ecosystem' %}

For the moment, we suggest using "The ImageJ ecosystem" paper for
citations. But we recommend both of the above for learning about ImageJ2
in depth.

## Presentations

  - 2017-Feb-16 "What's New in ImageJ2?" \[
    [slides](http://imagej.github.io/presentations/2017-02-16-imagej2-neubias/)
    \]
  - 2015-Sep-03 "The ImageJ2 platform, and the Fiji distribution of
    ImageJ" \[ [video](https://vimeo.com/140929687),
    [slides](https://imagej.github.io/presentations/2015-09-03-imagej2-and-fiji/)
    \]
  - 2012-Oct-24 "ImageJ2: Current Status and Future Directions" \[
    [slides](http://conference.imagej.net/2012/curtis-rueden/2012-10-24-imagej-conference.odp)
    \]
  - 2010-Oct-27 "ImageJDev: Next Generation ImageJ" \[
    [slides](http://conference.imagej.net/2010/curtis-rueden/2010-10-27-ImageJDev.pdf)
    \]

## See also

  - [ImageJ1-ImageJ2 cheat
    sheet](ImageJ1-ImageJ2_cheat_sheet "wikilink")

[Category:Software](Category:Software "wikilink")
[Category:ImageJ2](Category:ImageJ2 "wikilink")
[Category:SciJava](Category:SciJava "wikilink")
[Category:Citable](Category:Citable "wikilink")