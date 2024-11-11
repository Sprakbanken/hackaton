# Hackathon bildedata

[Her](simple-search.ipynb) er en liten eksempelnotebook som viser hvordan du kan laste inn datasettet og søker etter bilder.
Bildedatasettet er ganske stort (15 GiB) så kontakt Marie for en kopi.
Alternativt kan du basere deg på bildesøk-applikasjonen: https://dh.nb.no/bildesok/.

## Om datasettet

Datasettet består av 363061 bilder fra 16711 norske bøker i det fri fra før år 1900 med SigLIP embedding vektorer.
SigLIP embedding vektorene kommer fra `google/siglip-base-patch16-256-multilingual`.

I tillegg til bildene har vi følgende metadata hentet fra bøkene (der det er tilgjengelig):

 * access (streng)
 * authors (streng)
 * title (streng)
 * publisher (streng)
 * published_year (år)
 * tags (liste med strenger)
 * language (streng)
 * document_type (streng)
 * udc (streng)
 * license (streng)
 * page_urn (streng)
 * image_url (streng)
 * urn (streng)
 * file_name (streng)
 * public_domain (streng)
 * genres (streng)
 * issn (streng)
 * dewey (streng)
 * original_title (streng)
 * isbn (streng)

For å finne bildene har vi basert oss på tekstgjennkjenningsløypa til Nasjonalbiblioteket og hentet ut de områdene fra de digitaliserte bøkene som er klassifisert som grafiske elementer.
Derfor er det en del områder som er feilklassifisert og f.eks. inneholder deler av tabeller eller blanke ark.
