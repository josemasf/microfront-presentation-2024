<template>
    <div class="diagram not-content astro-y4w3wuan">
        <div class="header app astro-y4w3wuan">Encabezado (isla interactiva)</div>
        <div class="sidebar astro-y4w3wuan">Barra Lateral (HTML estático)</div>
        <div class="main astro-y4w3wuan"><p>Contenido estático como texto, imágenes, etc.</p></div>
        <div class="carousel app astro-y4w3wuan">Carrusel de imágenes (isla interactiva)</div>
        <div class="footer astro-y4w3wuan"> Pie de página (HTML estático)</div>
    </div>
</template>

<style>
:root, :root:not([data-theme='dark']) .expressive-code[data-theme='dark'] {
    --ec-brdRad: 0px;
    --ec-brdWd: 1px;
    --ec-brdCol: 
color-mix(in srgb, var(--sl-color-gray-5), transparent 25%);
    --ec-codeFontFml: var(--__sl-font-mono);
    --ec-codeFontSize: var(--sl-text-code);
    --ec-codeFontWg: 400;
    --ec-codeLineHt: var(--sl-line-height);
    --ec-codePadBlk: 0.75rem;
    --ec-codePadInl: 1rem;
    --ec-codeBg: #011627;
    --ec-codeFg: #d6deeb;
    --ec-codeSelBg: #1d3b53;
    --ec-uiFontFml: var(--__sl-font);
    --ec-uiFontSize: 0.9rem;
    --ec-uiFontWg: 400;
    --ec-uiLineHt: 1.65;
    --ec-uiPadBlk: 0.25rem;
    --ec-uiPadInl: 1rem;
    --ec-uiSelBg: #234d708c;
    --ec-uiSelFg: #ffffff;
    --ec-focusBrd: #122d42;
    --ec-sbThumbCol: #ffffff17;
    --ec-sbThumbHoverCol: #ffffff49;
    --ec-tm-lineMarkerAccentMarg: 0rem;
    --ec-tm-lineMarkerAccentWd: 0.15rem;
    --ec-tm-lineMarkerLabelPadInl: 0.2rem;
    --ec-tm-lineMarkerLabelCol: white;
    --ec-tm-lineDiffIndMargLeft: 0.25rem;
    --ec-tm-inlMarkerBrdWd: 1.5px;
    --ec-tm-inlMarkerBrdRad: 0.2rem;
    --ec-tm-inlMarkerPad: 0.15rem;
    --ec-tm-insDiffIndContent: '+';
    --ec-tm-delDiffIndContent: '-';
    --ec-tm-markBg: #ffffff17;
    --ec-tm-markBrdCol: #ffffff40;
    --ec-tm-insBg: #1e571599;
    --ec-tm-insBrdCol: #487f3bd0;
    --ec-tm-insDiffIndCol: #79b169d0;
    --ec-tm-delBg: #862d2799;
    --ec-tm-delBrdCol: #b4554bd0;
    --ec-tm-delDiffIndCol: #ed8779d0;
    --ec-frm-shdCol: #011627;
    --ec-frm-frameBoxShdCssVal: none;
    --ec-frm-edActTabBg: var(--sl-color-gray-6);
    --ec-frm-edActTabFg: var(--sl-color-text);
    --ec-frm-edActTabBrdCol: transparent;
    --ec-frm-edActTabIndHt: 1px;
    --ec-frm-edActTabIndTopCol: var(--sl-color-accent-high);
    --ec-frm-edActTabIndBtmCol: transparent;
    --ec-frm-edTabsMargInlStart: 0;
    --ec-frm-edTabsMargBlkStart: 0;
    --ec-frm-edTabBrdRad: 0px;
    --ec-frm-edTabBarBg: var(--sl-color-black);
    --ec-frm-edTabBarBrdCol: 
color-mix(in srgb, var(--sl-color-gray-5), transparent 25%);
    --ec-frm-edTabBarBrdBtmCol: 
color-mix(in srgb, var(--sl-color-gray-5), transparent 25%);
    --ec-frm-edBg: var(--sl-color-gray-6);
    --ec-frm-trmTtbDotsFg: 
color-mix(in srgb, var(--sl-color-gray-5), transparent 25%);
    --ec-frm-trmTtbDotsOpa: 0.75;
    --ec-frm-trmTtbBg: var(--sl-color-black);
    --ec-frm-trmTtbFg: var(--sl-color-text);
    --ec-frm-trmTtbBrdBtmCol: 
color-mix(in srgb, var(--sl-color-gray-5), transparent 25%);
    --ec-frm-trmBg: var(--sl-color-gray-6);
    --ec-frm-inlBtnFg: var(--sl-color-text);
    --ec-frm-inlBtnBg: var(--sl-color-text);
    --ec-frm-inlBtnBgIdleOpa: 0;
    --ec-frm-inlBtnBgHoverOrFocusOpa: 0.2;
    --ec-frm-inlBtnBgActOpa: 0.3;
    --ec-frm-inlBtnBrd: var(--sl-color-text);
    --ec-frm-inlBtnBrdOpa: 0.4;
    --ec-frm-tooltipSuccessBg: #158744;
    --ec-frm-tooltipSuccessFg: white;
}
.diagram:where(.astro-y4w3wuan) {
    display: grid;
    grid-template-areas:
        "header header header"
        "sidebar main main"
        "sidebar carousel carousel"
        "footer footer footer";
    grid-gap: 0.75rem;
    padding: 0.75rem;
    overflow-x: auto;
}
.diagram:where(.astro-y4w3wuan) .header:where(.astro-y4w3wuan) {
    grid-area: header;
    background: hsla(100, 60%, 50%, .2);
    border-color: #50743ecc;
    color: var(--sl-color-gray-1);
}
.diagram:where(.astro-y4w3wuan) .app:where(.astro-y4w3wuan) {
    font-size: 1.05rem;
}
.diagram:where(.astro-y4w3wuan)>:where(.astro-y4w3wuan) {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 2rem;
    background: var(--sl-color-gray-6);
    border: 2px solid var(--sl-color-gray-5);
    color: var(--sl-color-gray-2);
}
.diagram:where(.astro-y4w3wuan) .sidebar:where(.astro-y4w3wuan) {
    grid-area: sidebar;
}
.diagram:where(.astro-y4w3wuan)>:where(.astro-y4w3wuan) {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 2rem;
    background: var(--sl-color-gray-6);
    border: 2px solid var(--sl-color-gray-5);
    color: var(--sl-color-gray-2);
}
.diagram:where(.astro-y4w3wuan) .main:where(.astro-y4w3wuan) {
    grid-area: main;
    height: 320px;
}
.diagram:where(.astro-y4w3wuan)>:where(.astro-y4w3wuan) {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 2rem;
    background: var(--sl-color-gray-6);
    border: 2px solid var(--sl-color-gray-5);
    color: var(--sl-color-gray-2);
}
.diagram:where(.astro-y4w3wuan) .carousel:where(.astro-y4w3wuan) {
    grid-area: carousel;
    background: hsla(320, 80%, 50%, .2);
    border-color: #743e62cc;
    color: var(--sl-color-gray-1);
}
.diagram:where(.astro-y4w3wuan) .app:where(.astro-y4w3wuan) {
    font-size: 1.05rem;
}
.diagram:where(.astro-y4w3wuan)>:where(.astro-y4w3wuan) {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 2rem;
    background: var(--sl-color-gray-6);
    border: 2px solid var(--sl-color-gray-5);
    color: var(--sl-color-gray-2);
}
.diagram:where(.astro-y4w3wuan) .footer:where(.astro-y4w3wuan) {
    grid-area: footer;
}
.diagram:where(.astro-y4w3wuan)>:where(.astro-y4w3wuan) {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 2rem;
    background: var(--sl-color-gray-6);
    border: 2px solid var(--sl-color-gray-5);
    color: var(--sl-color-gray-2);
}
</style>