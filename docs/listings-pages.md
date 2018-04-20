---
layout: default
colorspace: red
---

## Using Listing Pages

> Listing pages can be used as a central hub of a larger set of content that can then be navigated to through the listed links. These pages are benificial for simplifying navigation through your documentation.

[Preview](../samples/listings-page){: .button}

### Listing Hash Structure

```yaml
listings:
  "Featured":
    'React Dev Tools':
      link: '#example'
      icon: '/assets/images/candies.png'
    'Slack':
      link: '#example'
      icon: '/assets/images/candies.png'
    'Visual Studio Code':
      link: '#example'
      icon: '/assets/images/candies.png'
  "Code Editors":
    'Vim':
      link: '#example'
      icon: '/assets/images/candies.png'
```

As you can see, each Listings page has a page variable defined of `listings` with aa nested category hash with it's frontend name. These categories then have a final nested hash with the Listing items name and a link/icon pair inside.

This structure must be followed exactly for the layout to output the predefined structured listings page.

[Home](../){: .button}