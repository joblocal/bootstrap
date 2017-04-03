---
layout: docs
title: Cards
description: Bootstrap's cards provide a flexible and extensible content container with multiple variants and options.
group: components
---

A **card** is a flexible and extensible content container. It includes options for headers and footers, a wide variety of content, contextual background colors, and powerful display options.

If you're familiar with Bootstrap 3, cards replace our old panels, wells, and thumbnails. Similar functionality to those components is available as modifier classes for cards.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Example

Cards are built with as little markup and styles as possible, but still manage to deliver a ton of control and customization. Built with flexbox, they offer easy alignment and mix well with other Bootstrap components.

Below is an example of a basic card with mixed content and a fixed width. Cards have no fixed width to start, so they'll naturally fill the full width of its parent element. This is easily customized with our various [sizing options](#sizing).

{% example html %}
<div class="card" style="width: 20rem;">
  <div class="card-img">
    <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
  </div>
  <div class="card-block">
    <h4 class="card-title">Card title</h4>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
{% endexample %}

## Content types

Cards support a wide variety of content, including images, text, list groups, links, and more. Below are examples of what's supported.

### Blocks

The building block of a card is the `.card-block`. Use it whenever you need a padded section within a card.

{% example html %}
<div class="card">
  <div class="card-block">
    This is some text within a card block.
  </div>
</div>
{% endexample %}

### Titles, text, and links

Card titles are used by adding `.card-title` to a `<h*>` tag. In the same way, links are added and placed next to each other by adding `.card-link` to  a `<a>` tag.

Subtitles are used by adding a `.card-subtitle` to a `<h*>` tag. If the `.card-title` and the `.card-subtitle` items are placed in a `.card-block` item, the card title and subtitle are aligned nicely.

{% example html %}
<div class="card">
  <div class="card-block">
    <h4 class="card-title">Card title</h4>
    <h6 class="card-subtitle mb-2 text-muted">Card subtitle</h6>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="card-link">Card link</a>
    <a href="#" class="card-link">Another link</a>
  </div>
</div>
{% endexample %}

### Images

`.card-img-top` places an image to the top of the card. With `.card-text`, text can be added to the card. Text within `.card-text` can also be styled with the standard HTML tags.

{% example html %}
<div class="card">
  <div class="card-img">
    <img class="card-img-top" data-src="holder.js/100px180/?text=Image cap" alt="Card image cap">
  </div>
  <div class="card-block">
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
</div>
{% endexample %}

`.card-img` adds the top border. It is a **wrapper class**, because the applied paddings would result in image distortions when an image has defined width and height (due to used box-sizing). We might use a more general class in the future. For the sake of simplicity we decided to use `p-X` utility for the padding, as discussed.

{% example html %}
<div class="card">
  <div class="card-block">
    <p class="card-text">Default <code>card-img</code> has no padding</p>
  </div>
  <div class="card-img">
    <img data-src="holder.js/100px180/?text=Image cap" alt="Card image cap">
  </div>
  <div class="card-block">
    <p class="card-text"><code>p-1</code> adds padding</p>
  </div>
  <div class="card-img p-1">
    <img data-src="holder.js/100px180/?text=Image cap" alt="Card image cap">
  </div>
  <div class="card-block">
    <p class="card-text"><code>p-2</code> padding</p>
  </div>
  <div class="card-img p-2">
    <img data-src="holder.js/100px180/?text=Image cap" alt="Card image cap">
  </div>
  <div class="card-block">
    <p class="card-text"><code>p-3</code> padding</p>
  </div>
  <div class="card-img p-3">
    <img data-src="holder.js/100px180/?text=Image cap" alt="Card image cap">
  </div>
  <div class="card-block">
    <p class="card-text"><code>p-5</code> padding</p>
  </div>
  <div class="card-img p-5">
    <img data-src="holder.js/100px180/?text=Image cap" alt="Card image cap">
  </div>
</div>
{% endexample %}

### Buttons

`.card-btn` creates a full block button. Use it for collapse toggles or other full-width-buttons

{% example html %}
<div class="card">
  <div class="card-img">
    <img class="card-img-top" data-src="holder.js/100px180/?text=Image cap" alt="Card image cap">
  </div>
  <div class="card-block">
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
  <button class="card-btn btn btn-link">Show more</button>
</div>
{% endexample %}

### List groups

Create lists of content in a card with a flush list group.

{% example html %}
<div class="card">
  <ul class="list-group list-group-flush">
    <li class="list-group-item">Cras justo odio</li>
    <li class="list-group-item">Dapibus ac facilisis in</li>
    <li class="list-group-item">Vestibulum at eros</li>
  </ul>
</div>
{% endexample %}

### Tables

Shows a table inside a card.

{% example html %}
<div class="card">
  <table class="table table-flush">
    <tbody>
      <tr>
        <th>Company</th>
        <td>Delos Destinations</td>
      </tr>
      <tr>
        <th>Employees</th>
        <td>5000</td>
      </tr>
      <tr>
        <th>Website</th>
        <td><a href="https://muenchenerjobs.de/">http://muenchenerjobs.de</a></td>
      </tr>
    </tbody>
  </table>
</div>
{% endexample %}

### Kitchen sink

Mix and match multiple content types to create the card you need, or throw everything in there. Shown below are image styles, blocks, text styles, and a list group—all wrapped in a fixed-width card.

{% example html %}
<div class="card" style="width: 20rem;">
  <div class="card-img">
    <img class="card-img-top" data-src="holder.js/100px180/?text=Image cap" alt="Card image cap">
  </div>
  <div class="card-block">
    <h4 class="card-title">Card title</h4>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
  <ul class="list-group list-group-flush">
    <li class="list-group-item">Cras justo odio</li>
    <li class="list-group-item">Dapibus ac facilisis in</li>
    <li class="list-group-item">Vestibulum at eros</li>
  </ul>
  <table class="table table-flush table-responsive">
    <tbody>
      <tr>
        <th>Company</th>
        <td>Delos Destinations</td>
      </tr>
      <tr>
        <th>Employees</th>
        <td>5000</td>
      </tr>
      <tr>
        <th>Website</th>
        <td><a href="https://muenchenerjobs.de/">http://muenchenerjobs.de</a></td>
      </tr>
    </tbody>
  </table>
  <div class="card-block">
    <a href="#" class="card-link">Card link</a>
    <a href="#" class="card-link">Another link</a>
  </div>
  <button class="card-btn btn btn-link">Show more</button>
</div>
{% endexample %}

### Header and footer

Add an optional header and/or footer within a card.

{% example html %}
<div class="card">
  <div class="card-header">
    Featured
  </div>
  <div class="card-block">
    <h4 class="card-title">Special title treatment</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
{% endexample %}

Card headers can be styled by adding `.card-header` to `<h*>` elements.

{% example html %}
<div class="card">
  <h3 class="card-header">Featured</h3>
  <div class="card-block">
    <h4 class="card-title">Special title treatment</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
{% endexample %}

{% example html %}
<div class="card">
  <div class="card-header">
    Quote
  </div>
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
{% endexample %}

{% example html %}
<div class="card text-center">
  <div class="card-header">
    Featured
  </div>
  <div class="card-block">
    <h4 class="card-title">Special title treatment</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
  <div class="card-footer text-muted">
    2 days ago
  </div>
</div>
{% endexample %}

#### Footer Table

{% example html %}
<div class="card text-center">
  <div class="card-header">
    Featured
  </div>
  <div class="card-block">
    <h4 class="card-title">Special title treatment</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
  <div class="card-footer p-0">
    <table class="table table-flush table-sm">
      <tbody>
        <tr>
          <th>Label</th>
          <td>Value</td>
        </tr>
        <tr>
          <th>Label</th>
          <td>Value</td>
        </tr>
        <tr>
          <th>Label</th>
          <td>Value</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>
{% endexample %}

## Sizing

Cards assume no specific `width` to start, so they'll be 100% wide unless otherwise stated. You can change this as needed with custom CSS, grid classes, grid Sass mixins, or utilities.

### Using grid markup

Using the grid, wrap cards in columns and rows as needed.

{% example html %}
<div class="row">
  <div class="col-sm-6">
    <div class="card">
      <div class="card-block">
        <h3 class="card-title">Special title treatment</h3>
        <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
      </div>
    </div>
  </div>
  <div class="col-sm-6">
    <div class="card">
      <div class="card-block">
        <h3 class="card-title">Special title treatment</h3>
        <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
      </div>
    </div>
  </div>
</div>
{% endexample %}

### Using utilities

Use our handful of [available sizing utilities]({{ site.baseurl }}/utilities/sizing/) to quickly set a card's width.

{% example html %}
<div class="card w-75">
  <div class="card-block">
    <h3 class="card-title">Card title</h3>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Button</a>
  </div>
</div>

<div class="card w-50">
  <div class="card-block">
    <h3 class="card-title">Card title</h3>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Button</a>
  </div>
</div>
{% endexample %}

### Using custom CSS

Use custom CSS in your stylesheets or as inline styles to set a width.

{% example html %}
<div class="card" style="width: 20rem;">
  <div class="card-block">
    <h3 class="card-title">Special title treatment</h3>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
{% endexample %}

### Using shadows

Shadow utility classes overwrite the default shadow on the card

{% example html %}
<div class="card shadow-soft">
  <div class="card-block">
    <h3 class="card-title">Soft shadow</h3>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
  </div>
  <a href="#" class="card-btn btn btn-link">Go somewhere</a>
</div>
{% endexample %}

{% example html %}
<div class="card shadow-large">
  <div class="card-block">
    <h3 class="card-title">Large Shadow</h3>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
  </div>
  <a href="#" class="card-btn btn btn-primary">Go somewhere</a>
</div>
{% endexample %}

## Text alignment

You can quickly change the text alignment of any card—in its entirety or specific parts—with our [text align classes]({{ site.baseurl }}/utilities/typography/#text-alignment).

{% example html %}
<div class="card" style="width: 20rem;">
  <div class="card-block">
    <h4 class="card-title">Special title treatment</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>

<div class="card text-center" style="width: 20rem;">
  <div class="card-block">
    <h4 class="card-title">Special title treatment</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>

<div class="card text-right" style="width: 20rem;">
  <div class="card-block">
    <h4 class="card-title">Special title treatment</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
{% endexample %}

## Navigation

Add some navigation to a card's header (or block) with Bootstrap's [nav components]({{ site.baseurl }}/components/navs/).

{% example html %}
<div class="card text-center">
  <div class="card-header">
    <ul class="nav nav-tabs card-header-tabs">
      <li class="nav-item">
        <a class="nav-link active" href="#">Active</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Link</a>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled" href="#">Disabled</a>
      </li>
    </ul>
  </div>
  <div class="card-block">
    <h4 class="card-title">Special title treatment</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
{% endexample %}

{% example html %}
<div class="card text-center">
  <div class="card-header">
    <ul class="nav nav-pills card-header-pills">
      <li class="nav-item">
        <a class="nav-link active" href="#">Active</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Link</a>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled" href="#">Disabled</a>
      </li>
    </ul>
  </div>
  <div class="card-block">
    <h4 class="card-title">Special title treatment</h4>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
{% endexample %}

### Card Nav
Special Component, that adds the correct padding and top border without using the `card-header` class.

<div class="card">
  <div class="card-block px-3 py-3 px-sm-4 py-sm-3 px-md-5 py-md-4 px-lg-6 py-lg-5">
    <h1 class="card-title">Ausbildung zum Drogist (w/m) mit der Möglichkeit der Zusatzqualifikation zum Handelsfachwirt 2017 <small>in München</small></h1>
    <p class="card-text small"><span class="badge badge-primary">Top Job</span> <a href="#">dm-drogerie markt GmbH + Co. KG</a></p>
  </div>
  <div class="card-nav bg-faded">
    <ul class="nav nav-buttons card-buttons card-buttons">
      <li class="nav-item">
        <button type="button" class="btn btn-secondary">Job merken</button>
      </li>
      <li class="nav-item">
        <div class="btn-group">
          <button type="button" data-toggle="dropdown" class="btn btn-secondary dropdown-toggle">Teilen</button>
          <div class="dropdown-menu">
            <a href="mailto:" class="dropdown-item">Per E-Mail</a>
            <div class="dropdown-divider"></div>
            <h6 class="dropdown-header">Soziale Netzwerke</h6>
            <a href="#" class="dropdown-item">Facebook</a>
            <a href="#" class="dropdown-item">Twitter</a>
            <a href="#" class="dropdown-item">Google Plus</a>
            <a href="#" class="dropdown-item">LinkedIn</a>
          </div>
        </div>
      </li>
      <li class="nav-item">
        <button type="button" class="btn btn-secondary">Drucken</button>
      </li>
      <li class="ml-auto">
        <a href="#" class="btn btn-cta btn-primary">Jetzt bewerben</a>
      </li>
    </ul>
  </div>
  <div class="card-block px-3 py-3 px-sm-4 py-sm-3 px-md-5 py-md-4 px-lg-6 py-lg-5">
    <h2 class="card-title">Stellenbeschreibung</h2>
    <p>AmRest Holdings SE is the largest independent restaurant operator in Central and Eastern Europe with a growing international presence. Since 1993 we have been building a portfolio of well recognized, power brands such as KFC, Pizza Hut, Burger King and Starbucks based on solid franchise and joint venture partnerships. AmRest owns the La Tagliatella brand which is being developed internationally as both Company operated restaurants and franchised stores. In 2012 AmRest acquired two unique brands operating in China- Blue Frog and Kabb.</p>
    <p>AmRest Coffee Deutschland Sp. z o.o. &amp; Co. KG is a sub company of AmRest Holdings SE, which operates almost 150 Starbucks Stores in Germany as licensee.</p>
  </div>
</div>

## Images

Cards include a few options for working with images. Choose from appending "image caps" at either end of a card, overlaying images with card content, or simply embedding the image in a card.

### Image caps

Similar to headers and footers, cards can include top and bottom "image caps"—images at the top or bottom of a card.

{% example html %}
<div class="card mb-3">
  <div class="card-img">
    <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
  </div>
  <div class="card-block">
    <h4 class="card-title">Card title</h4>
    <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
  </div>
</div>
<div class="card">
  <div class="card-block">
    <h4 class="card-title">Card title</h4>
    <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
  </div>
  <div class="card-img">
    <img class="card-img-bottom" data-src="holder.js/100px180/" alt="Card image cap">
  </div>
</div>
{% endexample %}

### Image overlays

Turn an image into a card background and overlay your card's text. Depending on the image, you may or may not need `.card-inverse` (see below).

{% example html %}
<div class="card card-inverse">
  <div class="card-img">
    <img data-src="holder.js/100px270/#55595c:#373a3c/text:Card image" alt="Card image">
  </div>
  <div class="card-img-overlay">
    <h4 class="card-title">Card title</h4>
    <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
  </div>
</div>
{% endexample %}

## Card styles

Cards include various options for customizing their backgrounds, borders, and color.

### Interactive / Arrow

{% example html %}
<div class="card">
  <a href="#" class="card-block has-arrow">
    <h3 class="card-title">Special title treatment</h3>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
  </a>
</div>
{% endexample %}

{% example html %}
<div class="card">
  <div class="list-group list-group-flush">
    <a href="#" class="list-group-item list-group-item-action has-arrow">Cras justo odio</a>
    <a href="#" class="list-group-item list-group-item-action has-arrow">Dapibus ac facilisis in</a>
    <a href="#" class="list-group-item list-group-item-action has-arrow">Vestibulum at eros</a>
  </div>
</div>
{% endexample %}

### Card Block Action
Introduces the same concept as list-group action and its variables. We don't use list-groups here, because we want to inherit colors etc. from card block elements as we know it.

{% example html %}
<div class="card">
  <a href="#" class="card-block card-block-action has-arrow">
    <h3 class="card-title">Job</h3>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
  </a>
  <a href="#" class="card-block card-block-action has-arrow">
    <h3 class="card-title">Special title treatment</h3>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
  </a>
  <a href="#" class="card-block card-block-action has-arrow">
    <h3 class="card-title">Special title treatment</h3>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
  </a>
</div>
{% endexample %}

### Inverted text

By default, cards use dark text and assume a light background. You can reverse that by toggling the `color` of text within, as well as that of the card's subcomponents, with `.card-inverse`. Then, specify a dark `background-color` and `border-color` to go with it.

You can also use `.card-inverse` with the [contextual backgrounds variants](#background-variants).

{% example html %}
<div class="card card-inverse" style="background-color: #333; border-color: #333;">
  <div class="card-block">
    <h3 class="card-title">Special title treatment</h3>
    <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
{% endexample %}

### Background variants

Cards include their own variant classes for quickly changing the `background-color` and `border-color` of a card. **Darker colors require the use of `.card-inverse`.**

{% example html %}
<div class="card card-inverse card-primary mb-3 text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
<div class="card card-inverse card-success mb-3 text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
<div class="card card-inverse card-info mb-3 text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
<div class="card card-inverse card-warning mb-3 text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
<div class="card card-inverse card-danger text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
{% endexample %}

{% capture callout-include %}{% include callout-warning-color-assistive-technologies.md %}{% endcapture %}
{{ callout-include | markdownify }}

### Outline cards

In need of a colored card, but not the hefty background colors they bring? Replace the default modifier classes with the `.card-outline-*` ones to style just the `border-color` of a card.

{% example html %}
<div class="card card-outline-primary mb-3 text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
<div class="card card-outline-secondary mb-3 text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
<div class="card card-outline-success mb-3 text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
<div class="card card-outline-info mb-3 text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
<div class="card card-outline-warning mb-3 text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
<div class="card card-outline-danger text-center">
  <div class="card-block">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>Someone famous in <cite title="Source Title">Source Title</cite></footer>
    </blockquote>
  </div>
</div>
{% endexample %}

## Card layout

In addition to styling the content within cards, Bootstrap includes a few options for laying out series of cards. For the time being, **these layout options are not yet responsive**.

### Card groups

Use card groups to render cards as a single, attached element with equal width and height columns. Card groups use `display: flex;` to achieve their uniform sizing.

{% example html %}
<div class="card-group">
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This card has supporting text below as a natural lead-in to additional content.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
</div>
{% endexample %}

When using card groups with footers, their content will automatically line up.

{% example html %}
<div class="card-group">
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    </div>
    <div class="card-footer">
      <small class="text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This card has supporting text below as a natural lead-in to additional content.</p>
    </div>
    <div class="card-footer">
      <small class="text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
    </div>
    <div class="card-footer">
      <small class="text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
</div>
{% endexample %}

### Card decks

Need a set of equal width and height cards that aren't attached to one another? Use card decks.

{% example html %}
<div class="card-deck">
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px200/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px200/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This card has supporting text below as a natural lead-in to additional content.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px200/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
</div>
{% endexample %}

Just like with card groups, card footers in decks will automatically line up.

{% example html %}
<div class="card-deck">
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    </div>
    <div class="card-footer">
      <small class="text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This card has supporting text below as a natural lead-in to additional content.</p>
    </div>
    <div class="card-footer">
      <small class="text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
  <div class="card">
    <div class="card-img">
      <img class="card-img-top" data-src="holder.js/100px180/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
    </div>
    <div class="card-footer">
      <small class="text-muted">Last updated 3 mins ago</small>
    </div>
  </div>
</div>
{% endexample %}

### Card columns

Cards can be organized into [Masonry](http://masonry.desandro.com)-like columns with just CSS by wrapping them in `.card-columns`. Cards are built with CSS `column` properties instead of flexbox for easier alignment. Cards are ordered from top to bottom and left to right.

**Heads up!** Your mileage with card columns may vary. To prevent cards breaking across columns, we must set them to `display: inline-block` as `column-break-inside: avoid` isn't a bulletproof solution yet.

{% example html %}
<div class="card-columns">
  <div class="card">
    <div class="card-img">
      <img class="card-img-top img-fluid" data-src="holder.js/100px160/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title that wraps to a new line</h4>
      <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
    </div>
  </div>
  <div class="card p-3">
    <blockquote class="card-block card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>
        <small class="text-muted">
          Someone famous in <cite title="Source Title">Source Title</cite>
        </small>
      </footer>
    </blockquote>
  </div>
  <div class="card">
    <div class="card-img">
      <img class="card-img-top img-fluid" data-src="holder.js/100px160/" alt="Card image cap">
    </div>
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This card has supporting text below as a natural lead-in to additional content.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  <div class="card card-inverse card-primary p-3 text-center">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat.</p>
      <footer>
        <small>
          Someone famous in <cite title="Source Title">Source Title</cite>
        </small>
      </footer>
    </blockquote>
  </div>
  <div class="card text-center">
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This card has supporting text below as a natural lead-in to additional content.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
  <div class="card">
    <div class="card-img">
      <img class="img-fluid" data-src="holder.js/100px260/" alt="Card image">
    </div>
  </div>
  <div class="card p-3 text-right">
    <blockquote class="card-blockquote">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
      <footer>
        <small class="text-muted">
          Someone famous in <cite title="Source Title">Source Title</cite>
        </small>
      </footer>
    </blockquote>
  </div>
  <div class="card">
    <div class="card-block">
      <h4 class="card-title">Card title</h4>
      <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content than the first to show that equal height action.</p>
      <p class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p>
    </div>
  </div>
</div>
{% endexample %}

Card columns can also be extended and customized with some additional code. Shown below is an extension of the `.card-columns` class using the same CSS we use—CSS columns— to generate a set of responsive tiers for changing the number of columns.

{% highlight scss %}
.card-columns {
  @include media-breakpoint-only(lg) {
    column-count: 4;
  }
  @include media-breakpoint-only(xl) {
    column-count: 5;
  }
}
{% endhighlight %}
