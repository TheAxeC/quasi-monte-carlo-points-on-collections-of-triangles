# Quasi-Monte Carlo Points on Collections of Triangles

Honoursvoorstel voor Axel Faes onder begeleiding van Prof. Dirk Nuyens

## Inleiding 

Uniforme verdelingen van punten op driehoeken kennen veel toepassingen in de wiskundige modellering van allerlei toepassingen. Bijvoorbeeld in computer graphics waarbij driehoeken vaak gebruikt worden in de tesselatie van 3D figuren of bij eindige-elementen methoden voor het discretiseren van het domein van differentiaalvergelijkingen. In de meeste gevallen gaat het dan om een klein aantal punten per driehoek en vele kleine driehoeken. Het verfijnen van de discretisatie (het aantal driehoeken) wordt aangeduid met de parameter ​h (de mesh-diameter), terwijl de selectie van het aantal punten per driehoek wordt aangeduid met de parameter ​p (de orde van veelterminterpolatie). In dit voorstel zijn we voornamelijk geïnteresseerd in quasi-Monte Carlo punten (low-discrepancy punten) die in principe geen exacte orde van veelterminterpolatie hebben, maar asymptotisch wel met orde één (of hoger) convergeren. We sturen aan op een groter aantal punten per driehoek, maar wel zodanig dat het aan elkaar plakken van driehoeken nog steeds een goede puntenset oplevert. Het genereren van uniforme puntensets op driehoeken werd onlangs bestudeerd in Basu & Owen (2015). maar zonder rekening te houden met aansluitende driehoeken. 

## Methodologie

Het vertrekpunt zijn goede quasi-Monte Carlo puntensets voor periodieke permutatie-invariante functies gedefinieerd op een eenheidskubus, zie Nuyens, Suryanarayana & Weimar (2015, 2016). Deze functies zijn invariant onder het omwisselen van de argumenten. De restrictie van deze punten tot de eenheidssimplex, of de projectie (door het ordenen van de coördinaten per punt) tot de eenheidssimplex, levert dan intuïtief een goede puntenset op voor de eenheidssimplex (een driehoek in 2D). Een belangrijk startpunt is dan ook het bewijzen dat deze punten (restrictie of projectie) inderdaad een goede puntenset zijn voor functies op een driehoek, gelijkaardig aan Basu & Owen (2015). In 2D is het ook mogelijk om brute-force kwaliteitscriteria uit te rekenen en te bestuderen alvorens aan het bewijs te beginnen. In een volgende stap zijn we geïnteresseerd in de tesselatie van grotere 2D of 3D figuren en wordt het belangrijk om de kwaliteitscriteria te bestuderen op een tesselatie. Het lijkt het best om hiervoor eerst punten op gelijkzijdige driehoeken te genereren in plaats van de rechthoekige driehoeken die we via de eenvoudige restrictie of projectie verkrijgen. In dit hele verhaal is het ook telkens mogelijk om tijdens de constructie van deze puntensets rekening te houden met het gebruik van de punten op een driehoek (in plaats van op een vierkant).

## Stappenplan 
1. Literatuurstudie: Basu & Owen (2015), Nuyens, Suryanarayana & Weimar (2015, 2016), Dick, Kuo & Sloan (2013).
2. Bestuderen van kwaliteitscriteria voor getransformeerde punten: numeriek en wiskundig.
3. Aanpassing voor gelijkzijdige driehoeken.
4. Bestuderen van kwaliteitscriteria op een collectie van driehoeken en uitzoeken hoe de driehoeken in een tesselatie gebruikt kunnen worden.
5. Optioneel: aanpassen van constructiemethoden rekening houdend met het gebruik op collecties van driehoeken.

## Uitkomst 

Algoritme voor goede puntensets op collecties van driehoeken. Bewijs dat deze punten goed zijn. Voorbereiding van een mogelijke paper. Integratie in onderzoeksgroep en kennismaking met academische wereld. Mondeling en schriftelijk rapporteren van onderzoek.

## Referenties 

* Basu & Owen. Low discrepancy constructions in the triangle, SIAM Journal on Numerical Analysis, 53(2):743–761, 2015.
* Dick, Kuo & Sloan. High-dimensional integration: The quasi-Monte Carlo way, Acta Numerica 22:133–288, 2013.
* Nuyens, Suryanarayana & Weimar. Construction of quasi-Monte Carlo rules for multivariate integration in spaces of permutation-invariant functions, Constructive Approximation, 45(2):311–344, 2015.
* Nuyens, Suryanarayana & Weimar. Rank-1 lattice rules for multivariate integration in spaces of permutation-invariant functions, Advances in Computational Mathematics, 42(1):55–84, 2016.
* Transforming low-discrepancy sequences from a cube to a simplex

## Nog wat extra links:
* http://mathworld.wolfram.com/TrianglePointPicking.html
* http://www.joesfer.com/?p=84
* http://www.cse.cuhk.edu.hk/~ttwong/papers/udpoint/udpoints.html
* http://www.graphics.cornell.edu/pubs/1995/Arv95c.pdf


