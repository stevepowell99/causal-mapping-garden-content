  
  
Remember that whatever you do, Causal Map always knows where the claims come **from**, so you can always do things like "[show me only sources and links](https://app.causalmap.app/help-docs#source-groups-sub-panel) from group B" or "[show me only links](https://app.causalmap.app/help-docs#source-groups-filter) with information from group B".  


Different ways you could differentiate the groups which the information applies **to**: 

- Use different labels for each group, like "Professionals give training" vs "Beneficiaries have improved confidence". This makes most sense if you think the causal maps for each group are basically quite different with different contents.   

- If you think the material overlaps for each group like "Professionals have improved confidence" vs "Beneficiaries have improved confidence", you could:

  - Keep the labels separate

  - Use hierarchical labels like "Improved confidence; professionals" so you can show/hide the group by zooming in or out

  - Use tags in square brackets like "Improved confidence [professionals]" so you can temporarily remove the tags when required   

  - Use [tags on the links](https://app.causalmap.app/help-docs#link-editor) (rather than on the factor labels) to show the group which the information refers to so you can show or [hide](https://app.causalmap.app/help-docs#exclude-link-tag-filter) those groups.

## Transformation and interpretation rules {.banner}

### Transformation rule {.rounded}

- **Input:** links/factors where claims apply to different target groups.
- **Transformation:** encode group distinction using one of these syntax choices: separate labels, hierarchical suffixes, factor tags, or link tags.
- **Output:** a links table/map where group-targeted claims can be compared, merged, or filtered depending on chosen encoding.

### Interpretation rule {.rounded}

- This encoding captures who/what the claim applies to (`about`), while source filters capture who made the claim (`from`).
- Choose syntax based on whether you want strict separation or roll-up comparability across groups.