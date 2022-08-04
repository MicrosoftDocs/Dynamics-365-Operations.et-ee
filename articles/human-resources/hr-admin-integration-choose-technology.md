---
title: Andme integratsioonitehnoloogia valimine
description: See artikkel annab teavet Inimressursside hallatavate andmetega integreerimise kohta.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2c542684642e4f6eda0f862623889a68f85b2b20
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068874"
---
# <a name="choose-a-data-integration-technology"></a>Andme integratsioonitehnoloogia valimine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



See artikkel annab teavet Dynamics 365 inimressursside hallatud andmetega integreerimiseks. Kirjeldatakse erinevaid integratsioonitehnoloogiaid, et aitata teil otsustada, millised tehnoloogiad teie vajadustele kõige paremini vastavad.

## <a name="data-integration-background"></a>Andmete integratsiooni taust

Äriandmed on oluline vara, mis muudab teie ettevõtte ainulaadseks. Teie ettevõtte andmed on väga väärtuslikud. Saate kasutada kogu oma ettevõttes kogutud andmete vahelisi seoseid äriprotsesside ja äriteabe parandamiseks kogu teie organisatsioonis. Püüame pakkuda lihtsat, turvalist ja stabiilset juurdepääsu teie äriandmetele olenemata sellest, millisest süsteemist see pärineb.

Ajalooliselt on teabe integreerimine mitme süsteemi vahel olnud raske. Microsoft astub samme, et muuta andmeintegratsioon lihtsamaks ja üks osa selle eesmärgi täideviimisest on platvorm [Dataverse](/powerapps/maker/common-data-service/data-platform-intro).

Human Resources on muutmas rakendust Dataverse rakenduse Human Resources andmete eelistatud avalikuks liideseks. Aja jooksul eeldame, et kõik kõige olulisemad rakendusega Human Resources hallatavad andmed jõuavad ka rakendusse Dataverse. Soovitame rakendust Dataverse kui tehnoloogilist valikut suurema osa integreeritavate rakenduste jaoks.

Saame aru, et Dataverse ei pruugi veel sisaldada kõiki andmeid, mida teie rakendus nõuab. Samuti saame aru, et teie projekti ajakava võib vajada alternatiivset tehnoloogiat. Andke meile kindlasti teada, kui Dataverse ei vasta teie integratsioonivajadustele.

## <a name="integration-technologies"></a>Integratsioonitehnoloogiad

Järgmised jaotised kirjeldavad erinevaid teabe integreerimise tehnoloogiaid, mis on saadaval rakendusega Human Resources kasutamiseks.

### <a name="dataverse-tables"></a>Dataverse'i tabelid

Dataverse on eelistatud avaliku teabe liides rakenduse Human Resources jaoks. See kasvas välja Dynamics 365 XRM-i platvormist, mida kasutavad [Dynamics 365 Customer Engagement](/dynamics365/?panel=customer-engagement#pivot=business-apps) lahendused.

Dataverse pakub andmetabelitele platvormi ja API-d. Human Reasourcesi juurutamisel ühendub see Dataverse'i eksemplariga. Human Resourcesi andmeüksused juurutatakse sellesse Dataverse'i eksemplari. Tabelid ja nende andmed on saadaval mis tahes rakendusele, mida saab Dataverse'i eksemplariga ühendada. Human Resources sünkroonib andmeid Dataverse'i tabelite vahel.

> [!NOTE]
> Human Resourcesi olemid vastavad Dataverse'i tabelitele. Lisateavet Dataverse'i (varem Common Data Service) ja terminoloogiavärskenduste kohta vaadake jaotisest [Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Kui teie integreerivate rakenduste jaoks nõutavad andmetabelid on olemas Dataverse'is, saate täielikult kasutada [Dataverse'it ja selle toetatud API-sid](/powerapps/?panel=developer#pivot=home). Toetatud API-de hulgas on [Dynamics 365 Web API](/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), mis pakub OData rakendamist Dataverse’i andmetele juurdepääsuks.

Dataverse’i tabelid ja nendega seotud API-d on parimad võimalused juurdepääsuks rakenduse Human Resources andmetele veebirakendustest, veebiteenustest/API-dest ja mis tahes muust OData vooge ühendavast rakendusest.

> [!NOTE]
> Kui otsustate teha Dataverse’ist eelistatud kasutajaliidese suhteliselt hiljutise rakenduse Human Resources jaoks, võite leida, et rakenduse Human Resources andmed, mida teie integreerimiseks vajate, pole veel rakenduses Dataverse saadaval.
> </br>
> Rakenduses Dataverse saadaolevate rakenduse Human Resources üksuste loendit vt teemast [Human Resources ja Dataverse](/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Kui teie integratsiooniks vajalikud rakenduse Human Resources üksused pole veel saadaval, peate ootama, kuni andmed on saadaval, või peate kasutama mõnda muud allpool kirjeldatud integratsioonitehnoloogiat.
> </br>
> Vaikimisi lülitatakse rakenduse Dataverse integratsioon välja uutes keskkondades, mis ei sisalda esitatud demoandmeid. Demoandmeid sisaldavates uutes keskkondades on see vaikimisi sisse lülitatud ja andmete sünkroonimine algab siis, kui keskkond on ette valmistatud. Pärast seda, kui teie keskkond on andmete sünkroonimiseks valmis, saate integratsiooni sisse lülitada.

### <a name="dmfdixf-entities"></a>DMF-/DIXF-i üksused

Inimressursid, mis on ehitatud peamiselt samale platvormile kui finantside ja toimingute rakendused, pakub andmehalduse [raamistikku (DMF)](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json). DMF on tuntud ka kui andmete importimise/eksportimise raamistik (DIXF). Human Resources pakub andmeüksuste kogumit, mida saate kasutada Human Resourcesi teabe importimiseks ja eksportimiseks. Kui Dataverse’i tabelid on rakenduses Human Resources eelistatud andmeintegratsiooni liideseks, on DMF-i üksused siiski mõnes olukorras kasulikud, näiteks järgmistes.

- Dataverse’i tabelid pole veel saadaval.

- Integratsioon vajab suuremahuliste andmete importimise/eksportimise võimalusi.

> [!NOTE]
> Human Resourcesi olemid vastavad Dataverse'i tabelitele. Lisateavet Dataverse'i (varem Common Data Service) ja terminoloogiavärskenduste kohta vaadake jaotisest [Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

DMF-i üksused pakuvad praegu kõige rohkem täielikke andmeid rakenduse Human Resources andmetele.

DMF ei sobi reaalajas integratsioonide jaoks, nt kui vajate kasutajaliideses kasutaja vahetut tagasisidet. Pakett-toimingud on ajastatud pakett-tööd ja sageli esineb 1–2-minutilist latentsust, enne kui partiiteenus võtab töö täitmiseks vastu, lisaks mis iganes aeg on importimise/eksportimise toimingu lõpuleviimiseks vajalik.

DMF võib olla parim valik, kui on vaja suurt läbilaskevõimet (nt tuhandete kirjete plaanitud import/eksport).

> [!NOTE]
> DMF ei ole saadaval Attracti ja Onboardi jaoks

### <a name="dmf-package-rest-api"></a>DMF-i pakett REST API

DMF pakub andmepakettidega manipuleerimiseks valikut [REST API](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api). Seda API-t saab kasutada programmiliselt DMF-iga suhtlemiseks, lubades selliseid tegevusi nagu järgmised.

- Andmepaketi importimine.

- Andmepaketi eksportimine.

- Impordi/ekspordi toimingu oleku kontrollimine.

DMF-paketi REST API on rakenduses Human Resources täielikult toetatud.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF pakub lisaks võimsat funktsiooni ( tuntud kui [Bring Your Own Database](/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) või BYOD), mis võimaldab rakendusel Human Resources andmeid eksportida oma Microsoft Azure SQL-i andmebaasi. See võimalus pakub tohutut paindlikkust. Kui andmed on olemas teie enda SQL-andmebaasis, saate kasutada kõiki rakendusi või vahevarasid, mida saab SQL DataStore’i ühendada.

BYOD on peamiselt kirjutuskaitstud lahendus. Samal ajal kui saate mis tahes soovitud andmeid Azure SQL-i andmebaasis manipuleerida ja salvestada (nt andmete koondamised), ei sünkroonita Azure SQL-i andmebaasi salvestatud andmeid rakendusega Human Resources.

BYOD on sobiv aruandluslahenduste, andmete integreerimise ja andmete koondamise, andmeallikana [Azure Data Factory](/azure/data-factory/) konveieri jaoks.

> [!NOTE]
> BYOD ei ole saadaval Attracti ja Onboardi jaoks.

### <a name="odata-enabled-entities"></a>OData-toega üksused

Enamikul DMF-üksustel on juurdepääs ka rakendusele Human Resources andmeside teenuse (OData) kaudu. Finantside ja toimingute [OData teenuse jaoks antud dokumentatsioon](/dynamics365/unified-operations/dev-itpro/data-entities/odata) kehtib inimressurssidele, v.a teie enda OData avatud üksuste loomisel.

Samal ajal kui Dataverse ja OData rakendamine, mida pakub Dataverse ([Dynamics 365 veebirakendusliidese](/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8)) kaudu), on eelistatud rakenduse Human Resources andmesideteenuse ees, on rakenduse Human Resources andmesideteenusel praegu suurem täielike üksuste katvus Human Resourcesi andmete jaoks.

### <a name="excel-add-in"></a>Exceli lisandmoodul

[Exceli lisandmoodul](/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) saab OData võimalusega üksustest kasu. See pakub tuttava Exceli kasutajaliidese kaudu lõppkasutajale rakenduse Human Resources andmete toomiseks ja muutmiseks mugavat viisi.

Exceli lisandmoodul sobib ad hoc-andmete importimiseks/eksportimiseks äridomeenide ekspertide poolt. Korduvaks andmeintegratsiooniks, mis nõuab programmilist automatiseerimist, on sobivam mõni muu integratsioonitehnoloogia.

### <a name="data-integrator"></a>Andmeintegraator

Saate kasutada [andmeintegraatori teenust](/powerapps/administrator/data-integrator) rakenduse Dataverse andmeitegratsiooniks. Andmeintegraator võimaldab integratsiooniprojektide määratlemist sageli varem määratletud mallide põhjal, mille rakenduse arendajad on kohandanud kindla integratsiooni jaoks. Saate ajastada integratsiooniprojekte korduva graafiku põhjal automaatselt käivituma või käivitada neid käsitsi.

Andmeintegraatori projektid sobivad rakenduse Dataverse pakktöötluse integreerimiseks. Need on suurepärane valik Dynamics 365 rakenduste pere vahelisteks integratsioonideks. Näiteks annab Microsoft andmeintegraatormalli Inimressurssidest Dynamics 365 Finance'i andmete integreerimiseks. Lisateavet malli kohta leiate integreerimisprotsessist [Dynamics 365 Human Resources Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Andmeintegraator toetab [Power Query](/power-query/power-query-what-is-power-query) seda täpsema päringu [funktsiooni kaudu](/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Power Query Pakub võimast, paindlikku andmete filtreerimist ja teisendamist, sh rikas M-i valemikeel. Power Query on ilmselt tutvunud, kui olete aruanded välja töötanud Power BI.

## <a name="deciding-on-an-integration-technology"></a>Integratsiooni tehnoloogia otsustamine

Saadaval on palju erinevaid integratsioonitehnoloogiaid, nii et otsustamine, millist integratsioonilähenemist kasutada, võib mõnikord olla üle jõu käiv. Kui andmekogumine rakenduses Dataverse täiustub, muutub otsuse tegemine lihtsamaks, nii et enamasti valitakse Dataverse’i andmeliides. Kuid seni võite leida, et Dataverse ei vasta veel teie vajadustele. Järgmine tabel võtab kokku integratsioonitehnoloogia suvandite peamisi omadusi.

| Tehnoloogia/tööriist/API    | Korduvad integreerimised                   | Sünkroonne/asünkroonne                    | Programmiline juurdepääs API kaudu        | Asjakohased andmemahud                                   | Andmete kaetus                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Dataverse'i tabelid           | Jah, kasutades andmeintegraatorit või vahevara | Asünkroonse sünkroonimine, partii (andmeintegraatori kaudu) | Jah, Dynamics 365 veebi API (OData) kaudu | Varieerub kasutusviisi puhul (toetab interaktiivseks kasutamiseks mõeldud kutsungit) | Parandamine<sup>2</sup>                       |
| DMF-i üksused           | Jah, plaanitud vahevara kaudu        | Asünkroonne, partii                                | Jah, DMF-paketi REST API kaudu         | Kõrge (sajad tuhanded kirjed)                    | Kõrge                                |
| DMF-pakett REST API   | Jah, plaanitud vahevara kaudu        | Asünkroonne, partii                                | Jah                                       | Kõrge (sajad tuhanded kirjed)                    | API toetab kõiki DMF-üksusi       |
| BYOD                   | Jah, administraatori plaanitud rakenduses Human Resources        | Asünkroonne, partii                                | Ei<sup>3</sup>                                    | Kõrge (sajad tuhanded kirjed)                    | Toetab kõiki DMF-üksusi           |
| OData-toega üksused | Jah, kasutades vahevara                    | Sünkroonimine                                        | Jah, Human Resourcesi andmeside teenuse kaudu (OData)  | Varieerub kasutusviisi puhul (toetab interaktiivseks kasutamiseks mõeldud kutsungit) | Kõrge                                |
| Exceli lisandmoodul           | Ei                                       | Sünkroonimine                                        | Ei                                        | Keskmine (kümned tuhanded kirjed)                      | Toetab kõiki OData toega üksusi |
| Andmeintegraator        | Jah, plaanitud andmeintegraatoris        | Asünkroonne, partii                                | Ei                                        | Varieerub kasutusviisist olenevalt                                       | Toetab kõiki Dataverse'i tabeleid           |

<sup>2</sup>Microsoft keskendub oluliselt Dataverse'i tabelite andmekogumise suurendamisele. Soovitame Dataverse'i kasutamist, kui andmekogumine on saadaval. Praegu on Dataverse’i andmekogumine väike DMF- ja OData toega üksustega võrreldes.

<sup>3</sup> SQL-i andmebaasil on programmiline juurdepääs.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

