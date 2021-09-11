# Compact_Nord_Firefox
Compact Firefox with Nord theme.

![screen-1630671932](https://user-images.githubusercontent.com/52444457/132004845-03f1a36d-9d30-4f30-999f-b432be4774d7.png)

Install Firefox Nord Polar theme: https://addons.mozilla.org/en-GB/firefox/addon/nord-polar-night-theme/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search

Read this rep: https://github.com/ranmaru22/firefox-vertical-tabs

My addon config:
```
/* Overwrite some colours */
:root {
    --tab-separator: transparent;
    --tab-selected-line: transparent;
    --tablist-separator: #5b6278;
}

@media (prefers-color-scheme: dark) {
    :root {
        --background: #333333;
        --icons: rgb(251,251,254);
        --tab-separator: transparent;
        --tab-active-background: rgb(66,65,77);
        --tab-active-text: rgb(251,251,254);
        --tab-text: #fbfbfe;
        --toolbar-background: #383c4a;
        --toolbar-text: rgb(251, 251, 254);
        --input-background: rgb(28,27,34);
        --input-border: transparent;
        --input-background-focus: rgb(66,65,77);
        --input-selected-text: rgb(251,251,254);
        --input-text: rgb(251,251,254);
        --input-text-focus: rgb(251,251,254);
        --identity-color-toolbar: rgb(251,251,254);
        --tablist-separator: #333333;
    }
}


body {
  --icons: white;
  --toolbar-text: white;
  --input-text: white;
  --input-text-focus: white;
  --tab-text: white;
  --background: #3b4252;
  --tab-active-background: #5b6278;

}

/* Move topmenu to bottom */
#topmenu {
    order: 2;
    background: transparent;
    border: none;
}

#newtab {
    margin-left: 6px;
}

#settings {
    margin-right: 2px;
}

/* Hide filterbox */
#filterbox-icon,
#filterbox-input {
    display: none;
}

/* Right-align settings icon */
#settings {
    margin-left: auto;
}

#tablist-wrapper {
    height: auto;
    margin: 0 6px;
}

#tablist-wrapper::after {
    content: "";
    max-width: 34px;
    margin: 2px 0;
    border: 1px solid var(--tablist-separator);
    transition: all 0.2s ease;
    transition-delay: 200ms;
}

#tablist-wrapper .tab-title-wrapper {
    visibility: hidden;
    transition: all 0.2s ease;
    transition-delay: 200ms;
}

#newtab {
    flex-grow: 1;
    margin-right: 4px;
    margin-left: 3px;
    padding-left: 9px;
}


.tab,
.tab.active {
    max-width: 36px;
    border-radius: 0px;
    margin: 0px 0px 2px 1px;
    transition: max-width 12s ease;
}

#pinnedtablist:not(.compact) .tab,
#tablist .tab {
    padding: 0;
}

#pinnedtablist:not(.compact) .tab {
    padding-left: 6px;
}

/* Show more when hovering over the sidebar */
body:hover #tablist-wrapper .tab-title-wrapper {
    visibility: visible;
}

body #newtab::after {
    content: "New tab";
    visibility: hidden;
    margin-left: 10px;
    transition: all 0.2s ease;
    transition-delay: 200ms;
}

body:hover #newtab::after {
    visibility: visible;
}

body:hover #tablist-wrapper::after,
body:hover .tab {
    max-width: 100%;
}

body:hover #pinnedtablist:not(.compact) .tab {
    padding-left: 0;
}

/* Move close button to left side */
/*.tab-close {
    left: 0;
    margin-left: 3px;
}*/

/* Fix title gradient */
/*#tablist .tab:hover > .tab-title-wrapper {
    mask-image: linear-gradient(to left, transparent 0, black 2em);
}*/

/* Move tab text to right when hovering to accomodate for the close button */
/*#tablist .tab:hover > .tab-title-wrapper {
    margin-left: 28px;
    transition: all 0.2s ease;
}*/

/* Move favicon to right when hovering to accomodate for the close button */
/*#tablist .tab:hover > .tab-meta-image {
    padding-left: 25px;
    transition: all 0.2s ease;
}*/


/*** Move container indicators to left ***/
#tablist-wrapper {
    margin-left: 0px;
    padding-left: 6px;
}
#tablist {
    margin-left: -6px;
    padding-left: 6px;
}
.tab {
    overflow: visible;
}
#tablist .tab[data-identity-color] .tab-context {
    box-shadow: none !important;
}
#tablist .tab[data-identity-color] .tab-context::before {
    content: "";
    position: absolute;
    top: 6px;
    left: -6px;
    bottom: 6px;
    width: 3px;
    border-radius: 0 5px 5px 0;
    background: var(--identity-color);
    transition: inset .1s;
}
#tablist .tab.active[data-identity-color] .tab-context::before {
    top: 1px;
    bottom: 1px;
}
```
