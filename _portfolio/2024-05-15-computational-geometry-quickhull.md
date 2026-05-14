---
title: "Computational Geometry Independent Study - University of Virginia"
subtitle: "Independent Study (Supervisor: Prof. Sara Maloni)"
collection: portfolio
section: undergrad_research
permalink: /portfolio/computational-geometry-quickhull/
date: 2024-05-15
project_period: "Jan 2024 - May 2024"
header:
  teaser: projects/computational-geometry-quickhull.svg
excerpt: "Built Quickhull & Plane Sweep algorithms with BST optimization"

---

## Convex Hull — Quickhull Algorithm

- Implemented the **Quickhull algorithm** in Python using a divide-and-conquer approach: identifying extreme points, partitioning point sets recursively, and isolating outermost boundary points.
- Built interactive visualizations using **Matplotlib**, including randomized point generation, color-coded hull boundaries, and labeled segments for result verification.
- Compared Quickhull against the **Gift Wrapping algorithm**, analyzing trade-offs in computational complexity and implementation complexity.

## Line Segment Intersection — Sweep Line Algorithm

- Studied and implemented the **Plane Sweep algorithm** for detecting line segment intersections, utilizing a **Balanced Binary Search Tree** to maintain and query active segments efficiently.
- Refined the algorithm iteratively: from detecting existence of a single intersection → accurately identifying and outputting **all intersection points** with precise coordinates.
- Applied **NumPy** linear equation solving to compute exact intersection coordinates; enhanced graph output with automatic segment labeling via `matplotlib.pyplot.text`.

## Outreach & Presentation

- Presented Quickhull at an inter-lab session alongside **AWM and Math Club**, using visualized diagrams to explain the algorithm's step-by-step process.
- Introduced the Sweep Line algorithm and its real-world applications (e.g., bridge placement optimization for road-river intersections) at a **local Farmers Market**, engaging the public with interactive geometry activities.

## Links
- [Code (GitHub/GitLab)](https://github.com/AlecTraas/computational-geo-lab)
