---
tags:
  - mapcat_methods
---

**What are the main causal pathways from an intervention to an outcome?** We can trace **chains of influence** from a starting point like an intervention to a key outcome, revealing the step-by-step or branching logic described by the sources. We can even compare the strength of evidence for different pathways. 

Path tracing is similar to [Looking upstream](113.6 Looking upstream. What are the direct and indirect influences on one or more-factors qq) and [Looking downstream](113.5 Looking downstream. What are the direct and indirect consequences of one or more factors qq),: you can specify the number of steps, and you can apply the more conservative source tracing approach. The difference is just that you can specify both the source and the target factors.


![[100 Task 3 -- Answering questions -- Individual questions/img/screenshot-116-path-tracing-how-do-one-or-more-causes-affect-one-or-more-effects.jpg]]
[[116 Source tracing -- What are the consequences of one or more factors, looking  only at stories told in their entirety by individual sources qq ((source-tracing))]]

**How to use**

**🔍 Start path tracing:** Select the 'trace paths' filter.

**➡️ Define your path:** Specify the starting and ending factors for the path you want to trace. You can leave the `end` field blank to show all paths leading _from_ a factor, or leave the `start` field blank to show all paths leading _to_ a factor.

**🔢 Set the steps:** Choose the number of steps (or links) to include in your traced path. Increasing this number will _broaden_ the results by including _longer paths_. But keep in mind that, when you’re analysing interviews, **people usually don’t report causal chains longer than 4 steps.**

The factors which match the filter are shown with **coloured borders.**

When you have several starting and/or ending factors, the **From × To matrix** can summarise the traced paths in a way that is hard to see on the map. It puts From factors in the rows and To factors in the columns, with each cell showing the number of sources or citations involved in direct or indirect paths up to the selected number of steps. This is especially useful for noticing **zeros**: cases where you might have expected a path from some X to some Y, but no such path is found in the current filtered data. Maps are good for seeing what is present; these tables also make absence easier to inspect.

**Tips for Success💡:**

**🗺️ Simplify your map:** Consider applying other filters beforehand to format and simplify your map before tracing paths.

**⛓️ Avoid the** **[transitivity trap](https://guide.causalmap.app/transitivity-trap/)****:** Be careful when drawing conclusions. The presence of links from A to B and B to C does not automatically mean that all respondents indirectly connect A to C: some may have mentioned only A to B and others only mentioned B to C. To avoid this trap, you can trace individual respondents’ _threads_ within the paths, which filters to show only continuous chains of links from the same source to avoid the transitivity trap issue.

In most cases, we should always trace threads **before** any filter which changes labels: zooming, removing brackets, combining opposites and autoclustering. See [this page](https://guide.causalmap.app/transforms-filters/) for more information.  
  

Remember that [**order matters**](https://guide.causalmap.app/transforms-filters/): the order in which the filters are applied makes a difference.

<!-- xrefs-v1 -->

## Related

- [[010 Individual questions -- introduction ((questions-introduction))|chapter intro]]
- [[250 Formatting your map for what you want to show ((howto-map-formatting))|Formatting your map (recipe)]]
