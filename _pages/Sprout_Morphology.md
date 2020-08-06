---
autogenerated: true
title: Sprout Morphology
breadcrumb: Sprout Morphology
layout: page
categories: 
description: test description
---


{% capture author%}
{% include person content='Eglinger' %}
{% endcapture %}

{% capture maintainer%}
{% include person content='Eglinger' %}
{% endcapture %}

{% capture source%}
{% include github org='angiogenesis ' repo='Sprout\_Analysis ' %}
{% endcapture %}
{% include info-box software='Fiji ' name='Sprout Morphology ' author=author maintainer=maintainer source=source released=' ' latest-version=' ' status='stable ' category='[Analysis](Category_Analysis ) ' %} The **Sprout Morphology** plugin measures sprout *number*, *length*, *width* and *cell density* of endothelial cell (EC) sprouts grown in a bead sprouting assay. It optionally includes measuring the coverage of these sprouts with pericytes included in the assay, as well as the endothelial cell/pericyte ratio.

## Installation

To install the plugin, activate the **Angiogenesis** [update site](How_to_follow_a_3rd_party_update_site ) and restart Fiji.

## Usage

Open a maximum intensity projection of the multi-channel image to be analyzed, then start the plugin via {% include bc content='Analyze|Sprout Morphology'%}. The process consists of up to six dialogs:

### General configuration

![Configuration dialog](/images/pages/SproutAnalyzer Configuration.png "Configuration dialog")

### Bead detection

![Bead detection](/images/pages/SproutAnalyzer BeadDetection.png "Bead detection")

### Sprout detection

![Sprout detection](/images/pages/SproutAnalyzer SproutDetection.png "Sprout detection")

### Nucleus segmentation

![Nucleus segmentation](/images/pages/SproutAnalyzer NucleusSegmentation.png "Nucleus segmentation")

### Endothelial cell/Pericyte classification

![Cell classification of ECs and pericytes](/images/pages/SproutAnalyzer CellClassification.png "Cell classification of ECs and pericytes")

### Pericyte coverage

![Pericyte coverage measurement](/images/pages/SproutAnalyzer PericyteCoverage.png "Pericyte coverage measurement")

## Publication

  - {% include citation last='Eglinger ' first='J. ' last2='Karsjens ' first2='H. ' last3='Lammert ' first3='E. ' year='2017 ' journal='Inflammation and Regeneration ' url='http://inflammregen.biomedcentral.com/articles/10.1186/s41232-016-0033-2 ' title='Quantitative assessment of angiogenesis and pericyte coverage in human cell-derived vascular sprouts ' volume='37(2) ' pmid=' ' doi='10.1186/s41232-016-0033-2 ' %}