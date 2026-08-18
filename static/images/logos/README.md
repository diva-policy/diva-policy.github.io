# Affiliation logos

Drop the four files here, keeping these exact names, and the logo strip in `index.html`
picks them up with no other change:

    uoft.svg        University of Toronto
    vector.svg      Vector Institute
    ac.svg          Acceleration Consortium
    nvidia.svg      NVIDIA          (present)

SVG is preferred so the strip stays sharp on any display; a PNG at roughly 600px wide
also works, in which case change the extension in `index.html`.

Only the NVIDIA wordmark is here. The other three are trademarked institutional marks
that free image hosts do not carry, so they have to come from each organisation's own
brand page rather than be scraped:

  * University of Toronto  https://brand.utoronto.ca
  * Vector Institute       https://vectorinstitute.ai (press / brand assets)
  * Acceleration Consortium https://acceleration.utoronto.ca

The strip is commented out in `index.html` until all four exist; publishing it with
missing files would render broken images on a public page.
