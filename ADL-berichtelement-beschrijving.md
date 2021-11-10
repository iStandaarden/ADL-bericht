## BERICHTELEMENTEN
|id|/Complextype-name|/documentation|verplicht|xs:element/@name|xs:element/@type|xs:element/xs:annotation/xs:documentation|
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
