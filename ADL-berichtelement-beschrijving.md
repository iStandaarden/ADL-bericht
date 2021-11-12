
# Beschrijving gegegevens ADL bericht

De beschrijving bevat de volgende onderdelen:
1. [Berichtelementen](#berichtelementen) : Beschrijving van de berichtelementen en opbouw
2. [Complexe-datatypen](#complexe-datatypen) : Beschrijvingen van de complexe datatypen
3. [Logisiche-datatypen](#logische-datatypen) : Beschrijvingen van de logische datatypen

## BERICHTELEMENTEN
|id|Complextype-name|documentation|verplicht|element-name|element-type|element-documentation|
|:---|:-------|:---|:---|:---|:---|:---|
|1|Root|Bericht met informatie over de geindiceerde Wlz-zorg (CIZ naar zorgkantoor).|ja|Header|adl:Header||
|1|Root|Bericht met informatie over de geindiceerde Wlz-zorg (CIZ naar zorgkantoor).|ja|Client|adl:Client||
|2|Header|De header bevat de identificerende gegevens van het bestand.|ja|BerichtVersie||Volgnummer van de formele uitgifte van een major release van een iStandaard.|
|2|Header|De header bevat de identificerende gegevens van het bestand.|ja|BerichtSubversie||Volgnummer van de formele uitgifte van een minor release van een iStandaard.|
|2|Header|De header bevat de identificerende gegevens van het bestand.|ja|Identificatie|adl:LDT_IdentificatieBericht|"Naam of nummer| die ter identificatie aan een totale aanlevering kan worden meegegeven."|
|2|Header|De header bevat de identificerende gegevens van het bestand.|ja|Dagtekening|adl:LDT_Datum|De datum van verzending van het bericht.|
|2|Header|De header bevat de identificerende gegevens van het bestand.|ja|Ontvanger|adl:LDT_AgbCode|"Identificatie van de zorginstelling| verantwoordelijk voor het leveren van ADL"|
|3|Client|Persoonsgegevens van de client.|ja|Bsn|adl:LDT_BurgerServicenummer|Een door de overheid toegekend identificerend nummer in het kader van het vereenvoudigen van het contact tussen overheid en burgers en het verminderen van de administratieve lasten.|
|3|Client|Persoonsgegevens van de client.|ja|GeheimeClient|adl:LDT_JaNee|Indicatie of er vanwege veiligheidsoverwegingen extra zorgvuldig omgegaan moet worden met de gegevens van een client.|
|3|Client|Persoonsgegevens van de client.|ja|Geboortedatum|adl:CDT_Geboortedatum|Geboortedatum van de client of relatie.|
|3|Client|Persoonsgegevens van de client.|ja|Geslacht|adl:LDT_Geslacht|"De sekse van een persoon| zoals bij geboorte formeel vastgesteld of nadien formeel gewijzigd."|
|3|Client|Persoonsgegevens van de client.|nee|BurgerlijkeStaat|adl:LDT_BurgerlijkeStaat|Unieke aanduiding die de rechtspositie van een client al dan niet in relatie tot een of meer personen beschrijft.|
|3|Client|Persoonsgegevens van de client.|ja|Naam|adl:CDT_VolledigeNaam|"Volledige naam van een natuurlijk persoon| aangeduid als Geslachtsnaam| eventueel Partnernaam| Voornamen en/of Voorletters en NaamGebruik."|
|3|Client|Persoonsgegevens van de client.|ja|Contactgegevens|adl:Contactgegevens||
|3|Client|Persoonsgegevens van de client.|ja|Indicatie|adl:Indicatie||
|4|Contact|Gegevens voor de aanduiding van het adres van de client of relatie.|ja|Soort|adl:LDT_AdresSoort|Nadere typering van het adres.|
|4|Contact|Gegevens voor de aanduiding van het adres van de client of relatie.|nee|Adres|adl:CDT_Adres|Adres van de client of relatie van de client.|
|4|Contact|Gegevens voor de aanduiding van het adres van de client of relatie.|nee|Telefoon|adl:CDT_Telefoonnummers|De telefoonnummers waarop de client of relatie van de client te bereiken is.|
|4|Contact|Gegevens voor de aanduiding van het adres van de client of relatie.|nee|Emailadres|adl:LDT_Emailadres|Het e-mailadres van de client of relatie van de client.|
|4|Contact|Gegevens voor de aanduiding van het adres van de client of relatie.|nee|Periode|adl:CDT_OpenPeriode|Begindatum en/of een einddatum van het verblijf van de client of relatie van de client op een tijdelijk adres.|
|5|Contactgegevens||ja|Contact|adl:Contact||
|6|Indicatie|De indicatie bevat de indicatiebesluitgegevens van de client.|ja|Besluitnummer|adl:LDT_Besluitnummer|Identificerend nummer van een indicatiebesluit.|
|6|Indicatie|De indicatie bevat de indicatiebesluitgegevens van de client.|nee|Grondslagen|adl:CDT_Grondslagen|De verzameling van gecodeerde aanduidingen die aangeven wat ten grondslag ligt aan het indicatiebesluit.|
|6|Indicatie|De indicatie bevat de indicatiebesluitgegevens van de client.|ja|Afgiftedatum|adl:LDT_Datum|De datum waarop het indicatiebesluit is afgegeven.|
|6|Indicatie|De indicatie bevat de indicatiebesluitgegevens van de client.|ja|Ingangsdatum|adl:LDT_Datum|De datum die aangeeft vanaf welke datum het indicatiebesluit rechtsgeldig is.|
|6|Indicatie|De indicatie bevat de indicatiebesluitgegevens van de client.|nee|Einddatum|adl:LDT_Datum|Datum die aangeeft tot en met welke datum het indicatiebesluit rechtsgeldig is.|
|6|Indicatie|De indicatie bevat de indicatiebesluitgegevens van de client.|nee|Commentaar|adl:LDT_Commentaar|Vrije tekst (bijvoorbeeld toelichting) in een bericht.|
|6|Indicatie|De indicatie bevat de indicatiebesluitgegevens van de client.|nee|GeindiceerdeFuncties|adl:GeindiceerdeFuncties||
|7|GeindiceerdeFuncties||ja|GeindiceerdeFunctie|adl:GeindiceerdeFunctie||
|8|GeindiceerdeFunctie|Gegevens over een geindiceerde functie.|ja|FunctieCode|adl:LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|
|8|GeindiceerdeFunctie|Gegevens over een geindiceerde functie.|ja|Ingangsdatum|adl:LDT_Datum|De datum die aangeeft vanaf welke datum de geindiceerde zorgeenheid rechtsgeldig is.|
|8|GeindiceerdeFunctie|Gegevens over een geindiceerde functie.|nee|Einddatum|adl:LDT_Datum|De datum die aangeeft tot en met welke datum de geindiceerde zorgeenheid rechtsgeldig is.|
|8|GeindiceerdeFunctie|Gegevens over een geindiceerde functie.|ja|Klasse|adl:LDT_Klasse|"Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid| uitgedrukt in een klasse."|
|8|GeindiceerdeFunctie|Gegevens over een geindiceerde functie.|nee|Opslag|adl:LDT_Opslag|De omvang van de opslag op de klasse van de functie.|
|8|GeindiceerdeFunctie|Gegevens over een geindiceerde functie.|ja|Leveringsvoorwaarde|adl:LDT_Leveringsvoorwaarde|Codering die aangeeft welke leveringsvoorwaarde van toepassing is op de zorg.|
|8|GeindiceerdeFunctie|Gegevens over een geindiceerde functie.|nee|Vervoer|adl:LDT_Vervoer|Gecodeerde aanduiding die aangeeft of vervoer van toepassing is.|
|8|GeindiceerdeFunctie|Gegevens over een geindiceerde functie.|ja|InstellingVoorkeur|adl:LDT_AgbCode|Identificerende code van de instelling die de voorkeur heeft van de client.|
|8|GeindiceerdeFunctie|Gegevens over een geindiceerde functie.|nee|Commentaar|adl:LDT_Commentaar|Vrije tekst (bijvoorbeeld toelichting) in een bericht.|

[terug naar TOC](#Beschrijving-gegegevens-ADL-bericht)
## Complexe-datatypen 
|id|Complextype name|Complextype documentation|verplicht|Element name|Element type|Element documentation|
|:---|:-------|:---|:---|:---|:---|:---|
|9|CDT_Achternaam|De achternaam van een natuurlijk persoon, aangeduid als Naam met Voorvoegsel.|ja|Achternaam|adl:LDT_Naam|De achternaam van een persoon, indien nodig verkort weergegeven.|
|9|CDT_Achternaam|De achternaam van een natuurlijk persoon, aangeduid als Naam met Voorvoegsel.|nee|Voorvoegsel|adl:LDT_Voorvoegsel|Verzameling van een of meer voorzetsels/lidwoorden, die aan het significante deel van de achternaam van een persoon vooraf gaat en daar een onderdeel van is.
|10|CDT_Adres|Gegevens voor de aanduiding van een adres.|nee|Huisnummer|adl:LDT_Huisnummer|De numerieke aanduiding zoals de gemeente die aan het object heeft toegekend.|
|10|CDT_Adres|Gegevens voor de aanduiding van een adres.|nee|Huisletter|adl:LDT_Huisletter|Een alfabetisch teken achter het huisnummer zoals dit door het gemeentebestuur is toegekend.
|10|CDT_Adres|Gegevens voor de aanduiding van een adres.|nee|HuisnummerToevoeging|adl:LDT_HuisnummerToevoeging|Die letters of tekens die noodzakelijk zijn om, naast huisnummer en -letter, de brievenbus te vinden.
|10|CDT_Adres|Gegevens voor de aanduiding van een adres.|nee|AanduidingWoonadres|adl:LDT_AanduidingWoonadres|De aanduiding die wordt gebruikt voor adressen die niet zijn voorzien van de gebruikelijke straatnaam en huisnummeraanduidingen.
|10|CDT_Adres|Gegevens voor de aanduiding van een adres.|nee|Postcode|adl:LDT_Postcode|Aanduiding van de (inter)nationale postcode. Dit veld is geschikt voor zowel de Nederlandse als niet-Nederlandse postcodes.
|10|CDT_Adres|Gegevens voor de aanduiding van een adres.|nee|Straatnaam|adl:LDT_Straatnaam|De officiele door de gemeente vastgestelde naam van een straat.
|10|CDT_Adres|Gegevens voor de aanduiding van een adres.|nee|Plaatsnaam|adl:LDT_Plaatsnaam|De door de gemeente vastgestelde naam van een woonplaats.
|11|CDT_Geboortedatum|Datum waarop een natuurlijk persoon geboren is.|ja|Datum|adl:LDT_Datum|Datum waarop een persoon geboren is.
|11|CDT_Geboortedatum|Datum waarop een natuurlijk persoon geboren is.|nee|DatumGebruik|adl:LDT_DatumGebruik|Indicator die aangeeft welk deel van de voorafgaande datum gebruikt mag worden.
|12|CDT_GeslotenPeriode|Tijdsperiode met zowel begin- als einddatum|ja|Begindatum|adl:LDT_Datum|De begindatum van de periode.|
|12|CDT_GeslotenPeriode|Tijdsperiode met zowel begin- als einddatum|ja|Einddatum|adl:LDT_Datum|De einddatum van de periode.|
|13|CDT_Grondslagen|De verzameling van gecodeerde aanduidingen die aangeven wat ten grondslag ligt aan het indicatiebesluit.|ja|Grondslag01|adl:LDT_Grondslag|Gecodeerde aanduiding van wat als eerste ten grondslag ligt aan het indicatiebesluit met betrekking tot de zorg voor een client.|
|13|CDT_Grondslagen|De verzameling van gecodeerde aanduidingen die aangeven wat ten grondslag ligt aan het indicatiebesluit.|nee|Grondslag02|adl:LDT_Grondslag|Gecodeerde aanduiding van wat als tweede ten grondslag ligt aan het indicatiebesluit met betrekking tot de zorg voor een client.|
|14|CDT_Telefoonnummers|De telefoonnummers waarop de client of relatie van de client te bereiken is.|ja|Telefoon01|adl:CDT_Telefoon|Het telefoonnummer waarop de client of relatie van de client te bereiken is.|
|14|CDT_Telefoonnummers|De telefoonnummers waarop de client of relatie van de client te bereiken is.|nee|Telefoon02|adl:CDT_Telefoon|Het telefoonnummer waarop de client of relatie van de client te bereiken is.|
|15|CDT_Telefoon|Het telefoonnummer waarop de client of relatie van de client te bereiken is.|ja|Telefoonnummer|adl:LDT_Telefoonnummer|Het telefoonnummer waarop de client of relatie van de client te bereiken is.|
|15|CDT_Telefoon|Het telefoonnummer waarop de client of relatie van de client te bereiken is.|nee|Landnummer|adl:LDT_Landnummer|Het telefoonnummer van een land, vanuit Nederland benaderd.|
|16|CDT_OpenPeriode|Aanduiding van een tijdsperiode met een Begindatum en/of een Einddatum.|nee|Begindatum|adl:LDT_Datum|De begindatum van de periode.|
|16|CDT_OpenPeriode|Aanduiding van een tijdsperiode met een Begindatum en/of een Einddatum.|nee|Einddatum|adl:LDT_Datum|De einddatum van de periode.|
|17|CDT_VolledigeNaam|Volledige naam van een natuurlijk persoon, aangeduid als Geslachtsnaam, eventueel Partnernaam, Voornamen en/of Voorletters en NaamGebruik.|ja|Geslachtsnaam|adl:CDT_Achternaam|Wettelijk vastgelegde achternaam die iemand bij de geboorte erft van de vader of moeder.|
|17|CDT_VolledigeNaam|Volledige naam van een natuurlijk persoon, aangeduid als Geslachtsnaam, eventueel Partnernaam, Voornamen en/of Voorletters en NaamGebruik.|nee|Partnernaam|adl:CDT_Achternaam|Na het voltrekken van een huwelijk of na een officiele partnerregistratie van de partner aangenomen familienaam.|
|17|CDT_VolledigeNaam|Volledige naam van een natuurlijk persoon, aangeduid als Geslachtsnaam, eventueel Partnernaam, Voornamen en/of Voorletters en NaamGebruik.|nee|Voorletters|adl:LDT_Voorletters|De verzameling van letters die wordt gevormd door de eerste letter van alle in volgorde voorkomende voornamen van een persoon.|
|17|CDT_VolledigeNaam|Volledige naam van een natuurlijk persoon, aangeduid als Geslachtsnaam, eventueel Partnernaam, Voornamen en/of Voorletters en NaamGebruik.|ja|Naamgebruik|adl:LDT_NaamGebruik|Aanduiding naamgebruik (gecodeerd).|

[terug naar TOC](#Beschrijving-gegegevens-ADL-bericht)

## Logische-datatypen
|id|Simpletype name|Simpletype documentation|base|Enumeratie value|Enumeratie documentation|maxInclusive|maxLength|minInclusive|minLength|pattern-regex|
|:---|:-------|:---|:---|:---|:---|:---|:---|:---|:---|:---|
|1|LDT_AanduidingWoonadres|De aanduiding die wordt gebruikt voor adressen die niet zijn voorzien van de gebruikelijke straatnaam en huisnummeraanduidingen.|xs:string|AB|Aan boord||2||||
|1|LDT_AanduidingWoonadres|De aanduiding die wordt gebruikt voor adressen die niet zijn voorzien van de gebruikelijke straatnaam en huisnummeraanduidingen.|xs:string|BY|Bij||2||||
|1|LDT_AanduidingWoonadres|De aanduiding die wordt gebruikt voor adressen die niet zijn voorzien van de gebruikelijke straatnaam en huisnummeraanduidingen.|xs:string|TO|Tegenover||2||||
|1|LDT_AanduidingWoonadres|De aanduiding die wordt gebruikt voor adressen die niet zijn voorzien van de gebruikelijke straatnaam en huisnummeraanduidingen.|xs:string|WW|Woonwagen||2||||
|2|LDT_AdresSoort|Nadere typering van het adres.|xs:string|1|BRP-adres||2||||
|2|LDT_AdresSoort|Nadere typering van het adres.|xs:string|2|Correspondentie-adres||2||||
|2|LDT_AdresSoort|Nadere typering van het adres.|xs:string|3|Verblijfadres||2||||
|2|LDT_AdresSoort|Nadere typering van het adres.|xs:string|4|Tijdelijk verblijfadres||2||||
|3|LDT_AgbCode|Identificerende code van een instelling of aanbieder van zorg of ondersteuning (zie https://www.agbcode.nl)|xs:string||||8||1|[0-9]{8}|
|4|LDT_Besluitnummer|Besluitnummer Indicatie|xs:integer|||999999999||1|||
|5|LDT_BurgerServicenummer|Een door de overheid toegekend identificerend nummer in het kader van het vereenvoudigen van het contact tussen overheid en burgers en het verminderen van de administratieve lasten.|xs:string||||9||1|[0-9]{9}|
|6|LDT_BurgerlijkeStaat|Unieke aanduiding die de rechtspositie van een client al dan niet in relatie tot een of meer personen beschrijft.|xs:string|1|Ongehuwd en geen geregistreerd partner en nooit gehuwd of geregistreerd partner geweest||1||||
|6|LDT_BurgerlijkeStaat|Unieke aanduiding die de rechtspositie van een client al dan niet in relatie tot een of meer personen beschrijft.|xs:string|2|Gehuwd||1||||
|6|LDT_BurgerlijkeStaat|Unieke aanduiding die de rechtspositie van een client al dan niet in relatie tot een of meer personen beschrijft.|xs:string|3|Gescheiden||1||||
|6|LDT_BurgerlijkeStaat|Unieke aanduiding die de rechtspositie van een client al dan niet in relatie tot een of meer personen beschrijft.|xs:string|4|Weduwe/weduwnaar||1||||
|6|LDT_BurgerlijkeStaat|Unieke aanduiding die de rechtspositie van een client al dan niet in relatie tot een of meer personen beschrijft.|xs:string|5|Geregistreerd partner||1||||
|6|LDT_BurgerlijkeStaat|Unieke aanduiding die de rechtspositie van een client al dan niet in relatie tot een of meer personen beschrijft.|xs:string|6|Gescheiden geregistreerd partner||1||||
|6|LDT_BurgerlijkeStaat|Unieke aanduiding die de rechtspositie van een client al dan niet in relatie tot een of meer personen beschrijft.|xs:string|7|Achtergebleven geregistreerd partner||1||||
|6|LDT_BurgerlijkeStaat|Unieke aanduiding die de rechtspositie van een client al dan niet in relatie tot een of meer personen beschrijft.|xs:string|9|Ongehuwd en geen geregistreerd partner, eventueel wel gehuwd of geregistreerd partner geweest||1||||
|7|LDT_Commentaar|Vrije tekst (bijvoorbeeld een toelichting) in een bericht.|xs:string||||||1|([.\s]*\S+[.\s]*)+|
|8|LDT_Datum|Datum|xs:date|||||||[^:Z]*|
|9|LDT_DatumGebruik|Indicator die aangeeft welk deel van de voorafgaande datum gebruikt mag worden.|xs:string|1|"dag onbekend| alleen maand en jaar gebruiken"||1||||
|9|LDT_DatumGebruik|Indicator die aangeeft welk deel van de voorafgaande datum gebruikt mag worden.|xs:string|2|"dag en maand onbekend| alleen jaar gebruiken"||1||||
|9|LDT_DatumGebruik|Indicator die aangeeft welk deel van de voorafgaande datum gebruikt mag worden.|xs:string|3|"dag, maand en jaar onbekend| onbekende datum"||1||||
|10|LDT_Emailadres|Emailadres van een client of relatie.|xs:string||||80||1|.*[^\s].*|
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|21|HV: Huishoudelijke Hulp||2||||
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|31|PV: Persoonlijke verzorging||2||||
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|41|VP: Verpleging||2||||
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|61|BHALG: Behandeling algemeen (buiten verblijf in Wlz-instelling)||2||||
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|62|BHVBF: Behandeling met verblijf||2||||
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|63|BH-IND: Behandeling individueel||2||||
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|64|BH-GRP: Behandeling in groepsverband||2||||
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|71|VBTYD: Verblijf tijdelijk||2||||
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|81|BG-IND: Begeleiding individueel||2||||
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|82|BG-GRP: Begeleiding in groepsverband||2||||
|11|LDT_FunctieCode|Gecodeerde aanduiding van een zorgfunctie.|xs:string|91|ADL: ADL-assistentie||2||||
|12|LDT_Geslacht|De sekse van een persoon, zoals bij geboorte formeel vastgesteld of nadien formeel gewijzigd.|xs:string|0|Onbekend||1||||
|12|LDT_Geslacht|De sekse van een persoon, zoals bij geboorte formeel vastgesteld of nadien formeel gewijzigd.|xs:string|1|Mannelijk||1||||
|12|LDT_Geslacht|De sekse van een persoon, zoals bij geboorte formeel vastgesteld of nadien formeel gewijzigd.|xs:string|2|Vrouwelijk||1||||
|13|LDT_Grondslag|Gecodeerde aanduiding die aangeeft wat ten grondslag ligt aan het indicatiebesluit.|xs:string|1|SOMATISCHE ZIEKTE/AANDOENING||2||||
|13|LDT_Grondslag|Gecodeerde aanduiding die aangeeft wat ten grondslag ligt aan het indicatiebesluit.|xs:string|2|PSYCHOGERIATRISCHE ZIEKTE/AANDOENING||2||||
|13|LDT_Grondslag|Gecodeerde aanduiding die aangeeft wat ten grondslag ligt aan het indicatiebesluit.|xs:string|3|PSYCHIATRISCHE AANDOENING, PSYCHISCHE STOORNIS||2||||
|13|LDT_Grondslag|Gecodeerde aanduiding die aangeeft wat ten grondslag ligt aan het indicatiebesluit.|xs:string|4|LICHAMELIJKE HANDICAP (FUNCTIESTOORNIS)||2||||
|13|LDT_Grondslag|Gecodeerde aanduiding die aangeeft wat ten grondslag ligt aan het indicatiebesluit.|xs:string|5|VERSTANDELIJKE HANDICAP (FUNCTIESTOORNIS)||2||||
|13|LDT_Grondslag|Gecodeerde aanduiding die aangeeft wat ten grondslag ligt aan het indicatiebesluit.|xs:string|6|ZINTUIGLIJKE HANDICAP (FUNCTIESTOORNIS)||2||||
|13|LDT_Grondslag|Gecodeerde aanduiding die aangeeft wat ten grondslag ligt aan het indicatiebesluit.|xs:string|7|PSYCHOSOCIALE PROBLEMEN||2||||
|14|LDT_Huisletter|Een alfabetisch teken achter het huisnummer zoals dit door het gemeentebestuur is toegekend.|xs:string||||1||1|.*[^\s].*|
|15|LDT_Huisnummer|De numerieke aanduiding zoals de gemeente die aan het object heeft toegekend.|xs:integer|||99999||0|||
|16|LDT_HuisnummerToevoeging|Die letters of tekens die noodzakelijk zijn om, naast huisnummer en -letter, de brievenbus te vinden.|xs:string||||4||1|.*[^\s].*|
|17|LDT_IdentificatieBericht|Naam of nummer, die ter identificatie aan een totale aanlevering kan worden meegegeven.|xs:string||||12||1|.*[^\s].*|
|18|LDT_JaNee|Codering voor ja of nee.|xs:string|1|Ja||1||||
|18|LDT_JaNee|Codering voor ja of nee.|xs:string|2|Nee||1||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|99|niet van toepassing||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|K0|0 tot 1 uur per week (intervalbegeleiding)||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|K1|0 tot 2 uur per week (intervalbegeleiding)||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|K2|2 tot 4 uur per week (intervalbegeleiding, doorgaans meerdere keren per week, gemiddeld 3 uur per week)||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|K3|4 tot 7 uur per week (min of meer dagelijkse begeleiding eventueel meerdere keren per dag, gemiddeld 5 uur/w)||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|K4|7 tot 10 uur per week (continue begeleiding, veelal in samenhang met geclusterd wonen, al dan niet verblijf)||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|K5|10 tot 13 uur per week (continue begeleiding plus toezicht, met geclusterd wonen, structuurbiedend klimaat)||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|K6|13 tot 16 uur per week (continue begeleiding plus toezicht, met geclusterd wonen, structuurbiedend klimaat met extra aandacht voor||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|K7|16 tot 20 uur per week (continue en intensieve begeleiding, individueel en structuurverlenend, permanent toezicht,||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|K8|20 tot 25 uur per week (continue begeleiding en bescherming, 24 uurs nabij, in therapeutisch leefklimaat,||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD01|Een dagdeel per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD02|Twee dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD03|Drie dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD04|Vier dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD05|Vijf dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD06|Zes dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD07|Zeven dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD08|Acht dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD09|Negen dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD10|Tien dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD11|Elf dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD12|Twaalf dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD13|Dertien dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD14|Veertien dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KD15|Vijftien dagdelen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KE1|Gemiddeld een etmaal per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KE2|Gemiddeld twee etmalen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KE3|Gemiddeld drie etmalen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KE4|Gemiddeld vier etmalen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KE5|Gemiddeld vijf etmalen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KE6|Gemiddeld zes etmalen per week||4||||
|19|LDT_Klasse|Gecodeerde aanduiding van de mate van zorg betreffende een zorgeenheid, uitgedrukt in een klasse.|xs:string|KE7|Zeven etmalen per week||4||||
|20|LDT_Landnummer|Het telefoonnummer van een land, vanuit Nederland benaderd.|xs:string||||4||1|.*[^\s].*|
|21|LDT_Leveringsvoorwaarde|Codering die aangeeft welke leveringsvoorwaarde van toepassing is op de zorg.|xs:string|1|Volgens afspraak op geplande tijden||1||||
|21|LDT_Leveringsvoorwaarde|Codering die aangeeft welke leveringsvoorwaarde van toepassing is op de zorg.|xs:string|2|Volgens afspraak + direct oproepbaar (toezicht op afstand)||1||||
|21|LDT_Leveringsvoorwaarde|Codering die aangeeft welke leveringsvoorwaarde van toepassing is op de zorg.|xs:string|3|Voortdurend in de nabijheid (toezicht in nabijheid)||1||||
|21|LDT_Leveringsvoorwaarde|Codering die aangeeft welke leveringsvoorwaarde van toepassing is op de zorg.|xs:string|4|24 uur per dag (toezicht steeds actief)||1||||
|21|LDT_Leveringsvoorwaarde|Codering die aangeeft welke leveringsvoorwaarde van toepassing is op de zorg.|xs:string|8|Onbekend||1||||
|22|LDT_Naam|De naam van een persoon, indien nodig verkort weergegeven.|xs:string||||200||1|.*[^\s].*|
|23|LDT_NaamGebruik|Aanduiding naamgebruik (gecodeerd).|xs:string|1|Eigen naam||1||||
|23|LDT_NaamGebruik|Aanduiding naamgebruik (gecodeerd).|xs:string|2|Naam echtgenoot of geregistreerd partner of alternatieve naam||1||||
|23|LDT_NaamGebruik|Aanduiding naamgebruik (gecodeerd).|xs:string|3|Naam echtgenoot of geregistreerd partner gevolgd door eigen naam||1||||
|23|LDT_NaamGebruik|Aanduiding naamgebruik (gecodeerd).|xs:string|4|Eigen naam gevolgd door naam echtgenoot of geregistreerd partner||1||||
|23|LDT_NaamGebruik|Aanduiding naamgebruik (gecodeerd).|xs:string|5|Pseudoniem||1||||
|23|LDT_NaamGebruik|Aanduiding naamgebruik (gecodeerd).|xs:string|6|Niet-natuurlijk persoon||1||||
|24|LDT_Opslag|De omvang van de opslag op de klasse van de functie.|xs:integer|||99||0|||
|25|LDT_Persoonsid|Identificerend nummer van een natuurlijk persoon.|xs:string||||20||1|.*[^\s].*|
|26|LDT_Plaatsnaam|De door de gemeente vastgestelde naam van een woonplaats.|xs:string||||80||1|.*[^\s].*|
|27|LDT_Postcode|Aanduiding van de (inter)nationale postcode. Dit veld is geschikt voor zowel de Nederlandse als niet-Nederlandse postcodes.|xs:string||||8||1|.*[^\s].*|
|28|LDT_Straatnaam|De officiele door de gemeente vastgestelde naam van een straat.|xs:string||||24||1|.*[^\s].*|
|29|LDT_Telefoonnummer|Het telefoonnummer waarop de client of relatie van de client te bereiken is.|xs:string||||15||1|[0-9]*|
|30|LDT_Vervoer|Gecodeerde aanduiding die aangeeft of vervoer van toepassing is.|xs:string|1|Vervoer nodig||1||||
|30|LDT_Vervoer|Gecodeerde aanduiding die aangeeft of vervoer van toepassing is.|xs:string|2|Vervoer niet nodig||1||||
|30|LDT_Vervoer|Gecodeerde aanduiding die aangeeft of vervoer van toepassing is.|xs:string|9|Onbekend||1||||
|31|LDT_Voorletters|De verzameling van letters die wordt gevormd door de eerste letter van alle in volgorde voorkomende voornamen van een persoon.|xs:string||||6||1|([a-zA-ZÀ-ỳ])+|
|32|LDT_Voorvoegsel|Verzameling van een of meer voorzetsels/lidwoorden, die aan het significante deel van de achternaam van een persoon vooraf gaat en daar een onderdeel van is.|xs:string||||10||1|.*[^\s].*|

[terug naar TOC](#Beschrijving-gegegevens-ADL-bericht)