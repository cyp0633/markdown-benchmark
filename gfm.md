# GitHub flavored markdown extensions

This document is derived from [GitHub Flavored Markdown Spec](https://github.github.com/gfm/) and GitHub docs. CC BY-SA

## Tables

| foo | bar |
| --- | --- |
| baz | bim |
| abc | defghi |
:-: | -----------:
bar | baz

> a table, the second is delimiter row

| f\|oo  |
| ------ |
| b `\|` az |
| b **\|** im |

> escape `|`

| abc | def |
| --- | --- |
| bar |
| bar | baz | boo |

> empty cell and ignored boo

## Task list items

- [x] foo
  - [ ] bar
  - [x] baz
- [ ] bim

## Strikethrough

~~Hi~~ Hello, world!

## Autolinks

www.commonmark.org

www.commonmark.org/help<lp

foo@bar.baz

## Graphs

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

> a simple flow chart

```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "id": 1,
      "properties": {
        "ID": 0
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
              [-90,35],
              [-90,30],
              [-85,30],
              [-85,35],
              [-90,35]
          ]
        ]
      }
    }
  ]
}
```

> geojson map with Alabama selected

```topojson
{
  "type": "Topology",
  "transform": {
    "scale": [0.0005000500050005, 0.00010001000100010001],
    "translate": [100, 0]
  },
  "objects": {
    "example": {
      "type": "GeometryCollection",
      "geometries": [
        {
          "type": "Point",
          "properties": {"prop0": "value0"},
          "coordinates": [4000, 5000]
        },
        {
          "type": "LineString",
          "properties": {"prop0": "value0", "prop1": 0},
          "arcs": [0]
        },
        {
          "type": "Polygon",
          "properties": {"prop0": "value0",
            "prop1": {"this": "that"}
          },
          "arcs": [[1]]
        }
      ]
    }
  },
  "arcs": [[[4000, 0], [1999, 9999], [2000, -9999], [2000, 9999]],[[0, 0], [0, 9999], [2000, 0], [0, -9999], [-2000, 0]]]
}
```

> topojson map with Malaysia

```stl
solid cube_corner
  facet normal 0.0 -1.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 1.0 0.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
  facet normal 0.0 0.0 -1.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 1.0 0.0 0.0
    endloop
  endfacet
  facet normal -1.0 0.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 0.0 1.0
      vertex 0.0 1.0 0.0
    endloop
  endfacet
  facet normal 0.577 0.577 0.577
    outer loop
      vertex 1.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
endsolid
```

> STL 3D model

## LaTeX (MathJax/KaTeX)

$\sqrt{3x-1}+(1+x)^2$

$$
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
$$

```math
\sqrt{3}
```

> Inline math, math block, math block as code

$\{n\in\mathbb{N}:\: n \text{even}\}$

$`U`$

$x = \text{my $y$}$

&dollar;\frac{f}{a}&dollar;

> Some tricky math formula, from [Math on GitHub: The Good, the Bad and the Ugly](https://nschloe.github.io/2022/05/20/math-on-github.html). Have curly brackets, have colon, math text, no math