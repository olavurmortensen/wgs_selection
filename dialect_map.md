# Genealogy registry and dialect regions

It is well known that differences in language is closely connected to genetic differentiation [**citation**]. Usually, geographic barriers lead to stratification in populations that lead to both genetic and linguistic differences [**citation**].

We will create a discriminatory map of the Faroe Islands that define strict regions based on dialect. This map will then be the basis to examine geographical stratification of the Faroese population, both in terms of population structure seen in sequencing data, and familial clustering seen in the Faroese genealogy registry.

Why use language as a proxy for geography? This may seem like a somewhat circular process. But it is not directly obvious how one should define the regions. We could apply the principle of isolation by distance, but we would need to include the topology of the landscape. For example, two near villages that have a tall mountain chain between them could not be as connected as one might think. Similarly, while the sea might seem like a barrier, in most cases it connects villages. For example, if two relatively distant villages are in a long sound, travelling between the villages by boat will be relatively easy, increasing the connectivity between them. Therefore, *in the absence of a complicated model of isolation by distance* (which would be prone to overfitting), *it is ideal to divide the regions by dialect*.

The map below shows isoglosses that define boundries that descriminate some of the main dialect differences in the Faroe Islands. All the main differences in dialect in the Faroes, shown in the map, are differences in how certain vowels are pronounced.

![Dialect map](https://upload.wikimedia.org/wikipedia/commons/7/7e/Faroe_islands_isoglosses.png =300x)

This map was drawn in a book by Thráinsson et al. (see below), based on work by Faroese linguist Eivind Weyhe.

> *Faroese. An Overview and Reference Grammar Tórshavn*: Føroya Fróðskaparfelag 2004, ISBN 99918-41-85-7
> 
> Höskuldur Thráinsson, Hjalmar P. Petersen, Jógvan í Lon Jacobsen, Zakaris Svabo Hansen

With the help of Faroese linguist Eivind Weyhe, we generated a list of six regions and the villages therein. I've illustrated this on a map below, and the names of the region(s) and the corresponding color are listed below.

![Dialect Map](/home/olavur/Documents/sync/workstuff/ilegusavnid/aebs/dialect_regions/dialect_map/dialect_map.png)

Region number | Region name(s) | Color
-----|-----|----
1 | Norðoyggjar | <span style="color:#157EBF">Blue #157EBF</span>
2 | Eysturoy og Norðstreymoy | <span style="color:#78B430">Green #78B430</span>
3 | Suðurstreymoy | <span style="color:#FAA530">Orange #FAA530</span>
4 | Vágar og Mykines | <span style="color:#00E9E8">Teal #00E9E8</span>
5 | Sandoy, Skúvoy, Stóra Dímun | <span style="color:#FFF73F">Yellow #FFF73F</span>
6 | Suðuroy | <span style="color:#974C93">Purple #974C93</span>

Note that there are some differences between the isoglosses in the first map and the regions in the second map. For example Gjógv, the northernmost village in Eysturoy, is placed together with the other villages in Eystoroy, despite being in the same "á" isoglossal group as Norðoyggjar.

In appendix 1, there is a list of place names (village names), their postcodes, and corresponding regions (using the region number from the list above). Using this list, we can easily translate the postcodes in the genealogy registry to region IDs.

## Appendix 1: postcodes and regions

Place name | Postcode | Region ID
---|---|---
Tórshavn | 100 | 3
Argir | 160 | 3
Kirkjubøur | 175 | 3
Velbastaður | 176 | 3
Syðradalur(Str.) | 177 | 3
Norðradalur | 178 | 2
Kaldbak | 180 | 2
Kaldbaksbotnur | 185 | 2
Sund | 186 | 2
Hvítanes | 187 | 3
Hoyvík | 188 | 3
Sandur | 210 | 5
Skálavík | 220 | 5
Húsavík | 230 | 5
Dalur | 235 | 5
Skarvanes | 236 | 5
Skopun | 240 | 5
Skúvoy | 260 | 5
Nólsoy | 270 | 3
Hestur | 280 | 3
Koltur | 285 | 3
StóraDímun | 286 | 5
Stykkið | 330 | 2
Leynar | 335 | 2
Skælingur | 336 | 2
Kvívík | 340 | 2
Vestmanna | 350 | 2
Válur | 358 | 2
Sandavágur | 360 | 4
Miðvágur | 370 | 4
Sørvágur | 380 | 4
Vatnsoyrar | 385 | 4
Bøur | 386 | 4
Gásadalur | 387 | 4
Mykines | 388 | 4
Oyrarbakki | 400 | 2
Kollafjørður | 410 | 2
Oyrareingir | 415 | 2
Signabøur | 416 | 2
Hósvík | 420 | 2
Hvalvík | 430 | 2
Streymnes | 435 | 2
Saksun | 436 | 2
Nesvík | 437 | 2
Langasandur | 438 | 2
Haldarsvík | 440 | 2
Tjørnuvík | 445 | 2
Oyri | 450 | 2
Norðskáli | 460 | 2
Svínáir | 465 | 2
Ljósá | 466 | 2
Eiði | 470 | 2
Funningur | 475 | 2
Gjógv | 476 | 2
Funningsfjørður | 477 | 2
Elduvík | 478 | 2
Skáli | 480 | 2
Skálabotnur | 485 | 2
Strendur | 490 | 2
InnanGlyvur | 494 | 2
Kolbanargjógv | 495 | 2
Morskranes | 496 | 2
Selatrað | 497 | 2
Gøta | 510 | 2
Gøtugjógv | 511 | 2
Norðragøta | 512 | 2
Syðrugøta | 513 | 2
Leirvík | 520 | 2
Fuglafjørður | 530 | 2
Saltangará | 600 | 2
Runavík | 620 | 2
Glyvrar | 625 | 2
Lambareiði | 626 | 2
Lambi | 627 | 2
Rituvík | 640 | 2
Æðuvík | 645 | 2
Toftir | 650 | 2
Nes(Eysturoy) | 655 | 2
Saltnes | 656 | 2
Søldarfjørður | 660 | 2
Skipanes | 665 | 2
Gøtueiði | 666 | 2
Oyndarfjørður | 690 | 2
Hellur | 695 | 2
Klaksvík | 700 | 1
Norðoyri | 725 | 1
Ánir | 726 | 1
Árnafjørður | 727 | 1
Norðdepil | 730 | 1
Depil | 735 | 1
Norðtoftir | 736 | 1
Múli | 737 | 1
Hvannasund | 740 | 1
Viðareiði | 750 | 1
Svínoy | 765 | 1
Kirkja | 766 | 1
Hattarvík | 767 | 1
Kunoy | 780 | 1
Haraldssund | 785 | 1
Syðradalur(Kal.) | 795 | 1
Húsar | 796 | 1
Mikladalur | 797 | 1
Trøllanes | 798 | 1
Tvøroyri | 800 | 6
Froðba | 825 | 6
Trongisvágur | 826 | 6
Øravík | 827 | 6
Hvalba | 850 | 6
Sandvík | 860 | 6
Fámjin | 870 | 6
Vágur | 900 | 6
Nes(Vágur) | 925 | 6
Lopra | 926 | 6
Akrar | 927 | 6
Víkarbyrgi | 928 | 6
Porkeri | 950 | 6
Hov | 960 | 6
Sumba | 970 | 6






