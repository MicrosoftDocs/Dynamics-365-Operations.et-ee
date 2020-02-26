---
title: Andmete integreerimise tehnoloogia valimine
description: Selles artiklis antakse juhtnööre selle kohta, kuidas rakenduse Human Resources hallatavate andmetega on võimalik integreerida, ning kirjeldatakse erinevate integratsiooni tehnoloogiate omadusi, et integreerijad saaksid teha teadlikke otsuseid selle kohta, millised tehnoloogiad nende vajadustele kõige rohkem sobivad.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029884"
---
# <a name="choose-a-data-integration-technology"></a>Andmete integreerimise tehnoloogia valimine

Dynamics 365 Human Resources haldab mitmesuguste äriprotsesside jaoks kasulikke äriandmeid. Selles artiklis antakse juhtnööre selle kohta, kuidas rakenduse Human Resources hallatavate andmetega on võimalik integreerida, ning kirjeldatakse erinevate integratsiooni tehnoloogiate omadusi, et integreerijad saaksid teha teadlikke otsuseid selle kohta, millised tehnoloogiad nende vajadustele kõige rohkem sobivad.

## <a name="data-integration-vision"></a>Andmeintegratsiooni visioon

Microsoft näeb äriandmeid kui olulist vara, mis muudab teie ettevõtte ainulaadseks. Teie ettevõtte andmed on väga väärtuslikud. Äritegevuse ühe poole kogutud ja hallatavad andmed on seotud äritegevuse teise poole kogutud andmetega ning neid suhteid saab kasutada äriprotsesside ja äriteabe parandamiseks kogu teie organisatsioonis. Lihtne, turvaline, stabiilne juurdepääs teie äriandmetele, olenemata sellest, milline süsteem „omab” andmed, mis on meie jaoks rakenduse Human Resources andmeintegratsiooni visiooni võtmeosaline.

Ajalooliselt on teabe integreerimine mitme süsteemi vahel olnud raske.
Microsoft astub samme, et muuta andmeintegratsioon lihtsamaks ja üks osa selle eesmärgi täideviimisest on platvorm [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Human Resources on muutmas rakendust Common Data Service rakenduse Human Resources andmete eelistatud avalikuks liideseks. Aja jooksul eeldame, et kõik kõige olulisemad rakendusega Human Resources hallatavad andmed jõuavad ka rakendusse Common Data Service. Soovitame rakendust Common Data Service kui tehnoloogilist valikut suurema osa integreeritavate rakenduste jaoks. Mõistame, et mitte kõik teie rakenduse andmed ei ole praegu rakenduses Common Data Service esindatud, ja et teie projekti ajakavad võivad vajada alternatiivset tehnoloogiat. Seetõttu andke teada, kui rakendus Common Data Service ei vasta teie integratsioonivajadustele.

## <a name="integration-technologies"></a>Integratsioonitehnoloogiad

Järgmised jaotised kirjeldavad erinevaid teabe integreerimise tehnoloogiaid, mis on saadaval rakendusega Human Resources kasutamiseks.

### <a name="common-data-service-entities"></a>Common Data Service’i üksused

Common Data Service on eelistatud avaliku teabe liides rakenduse Human Resources jaoks. Common Data Service on ehitatud valmis platvormile, mis on välja kasvanud Dynamics 365 XRM-i platvormist, millele rakenduse [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement) lahendused on ehitatud.

Common Data Service pakub nendele üksustele juurdepääsuks andmeüksuste platvorme ja API-sid. Kui rakendus Human Resources on teie organisatsioonis kasutusele võetud, on Human Resources ühendatud rakenduse Common Data Service eksemplariga ja rakenduse Human Resources andmeid haldavad üksused viiakse sellesse Common Data Serviceֹ’i eksemplari, muutes üksused ja nende andmed kättesaadavaks mis tahes rakendusele, mis saab Common Data Service’i eksemplariga ühendust luua. Olenevalt kasutatavatest Human Resourcesi rakendustest teeb Human Resources andmetoiminuid otse Common Data Service’i (nii Attract kui ka Onboard) või sünkroonib andmed Common Data Service’i üksustega.

Kui teie integreeritavatele rakendustele esitatavad andmeüksused on rakenduses Common Data Service olemas, saate täielikult kasutada rakendust [Common Data Service ja selle toetatud API-sid](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Toetatud API-de hulgas on [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), mis pakub OData rakendamist Common Data Service’i andmetele juurdepääsuks.

Common Data Service’i üksused ja seotud API-d on parimad võimalused juurdepääsuks rakenduse Human Resources andmetele veebirakendustest, veebiteenustest/API-dest ja mis tahes muust OData vooge ühendavast rakendusest.

> [!NOTE]
> Kui otsustate teha Common Data Service’ist eelistatud kasutajaliidese suhteliselt hiljutise rakenduse Human Resources jaoks, võite leida, et rakenduse Human Resources andmed, mida teie integreerimiseks vajate, pole veel rakenduses Common Data Service<sup>1</sup> saadaval. Kui teie integratsiooniks vajalikud rakenduse Human Resources üksused pole veel saadaval, peate ootama, kuni andmed on saadaval, või peate kasutama mõnda muud allpool kirjeldatud integratsiooni tehnoloogiat.
> 
> Vaikimisi lülitatakse rakenduse Common Data Service integratsioon välja uutes keskkondades, mis ei sisalda esitatud demoandmeid. Demoandmeid sisaldavates uutes keskkondades on see vaikimisi sisse lülitatud ja andmete sünkroonimine algab siis, kui keskkond on ette valmistatud. Pärast seda, kui teie keskkond on andmete sünkroonimiseks valmis, saate integratsiooni sisse lülitada.

<sup>1</sup>Rakenduses Common Data Service saadaolevate rakenduse Human Resources üksuste loendit vt teemast [Human Resources ja Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). Attracti ja Onboardi jaoks on kõik üksused rakenduses Common Data Service saadaval.

### <a name="dmfdixf-entities"></a>DMF-/DIXF-i üksused

Human Resources, mis on ehitatud peamiselt samale platvormile kui Finance and Operationsi rakendused, pakub [dokumendihalduse raamistiku (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json), mida nimetatakse ka andmete impordi/ekspordi raamistik või DIXF, ja andmed üksuste kogumit, mida saab kasutada teabe importimiseks/importimiseks rakendusse Human Resources. Kui Common Data Service’i hankeüksused on rakenduses Human Resources eelistatud andmeallikate liideseks, on DMF-i üksused siiski mõnes olukorras kasulikud, näiteks järgmistes.

- Common Data Service’i üksused pole veel saadaval.

- Integratsioon vajab suuremahuliste andmete importimise/eksportimise võimalusi.

DMF-i üksused pakuvad praegu kõige rohkem täielikke andmeid rakenduse Human Resources andmetele.

DMF ei sobi reaalajas integreerimiseks (nt kui kasutaja kasutajaliideses on nõutav vahetu kasutaja tagasiside), sest pakett-toimingud on ajastatud pakett-töödeks, ja sageli esineb 1-2-minutilist latentsust, enne kui partiiteenus võtab töö täitmiseks vastu, lisaks mis iganes aeg on importimise/eksportimise toimingu lõpuleviimiseks vajalik.

DMF võib olla parim valik, kui on vaja suurt läbilaskevõimet (nt tuhandete kirjete plaanitud import/eksport).

> [!NOTE]
> DMF ei ole saadaval Attracti ja Onboardi jaoks

### <a name="dmf-package-rest-api"></a>DMF-i pakett REST API

DMF pakub andmepakettidega manipuleerimiseks valikut [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api). Seda API-t saab kasutada programmiliselt DMF-iga suhtlemiseks, lubades selliseid tegevusi nagu järgmised.

- Andmepaketi importimine.

- Andmepaketi eksportimine.

- Impordi/ekspordi toimingu oleku kontrollimine.

DMF-paketi REST API on rakenduses Human Resources täielikult toetatud: Core HR.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF pakub lisaks võimsat funktsiooni (üldiselt tuntud kui [Bring Your Own Database](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) või BYOD), mis võimaldab rakendusel Human Resources andmeid eksportida oma Microsoft Azure SQL-i andmebaasi. See annab tohutu paindlikkuse, sest kui andmed on olemas teie enda SQL-andmebaasis, saate kasutada kõiki rakendusi või vahevarasid, mida saab SQL DataStore’i ühendada.

BYOD-d tuleks üldiselt lugeda kirjutuskaitstud lahenduseks. Samal ajal kui saate mis tahes soovitud andmeid Azure SQL-i andmebaasis manipuleerida ja salvestada (nt andmete koondamised), ei sünkroonita Azure SQL-i andmebaasi salvestatud andmeid rakendusega Human Resources.

BYOD on sobiv aruandluslahenduste, andmete integreerimise ja andmete koondamise, andmeallikana [Azure Data Factory](https://docs.microsoft.com/azure/data-factory/) konveieri jaoks.

> [!NOTE]
> BYOD ei ole saadaval Attracti ja Onboardi jaoks.

### <a name="odata-enabled-entities"></a>OData-toega üksused

Enamikul DMF-üksustel on juurdepääs ka rakendusele Human Resources andmeside teenuse (OData) kaudu. [Finance and Operationsi Odata teenuse](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) kohta esitatud dokumentatsiooni rakendatakse üldiselt ka rakendusele Human Resources, kuigi teie enda OData üksuste loomise dokumentatsiooni ei rakendata.

Samal ajal kui Common Data Service ja OData rakendamine, mida pakub Common Data Service ([Dynamics 365 veebirakendusliidese](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) kaudu), on eelistatud rakenduse Human Resources andmesideteenuse ees, on rakenduse Human Resources andmesideteenusel praegu suurem täielike üksuste katvus Human Resourcesi andmete jaoks.

### <a name="excel-add-in"></a>Exceli lisandmoodul

[Exceli lisandmoodul](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) saab OData võimalusega üksustest kasu. See pakub tuttava Exceli kasutajaliidese kaudu lõppkasutajale rakenduse Human Resources andmete toomiseks ja muutmiseks mugavat viisi.

Exceli lisandmoodul sobib ad hoc-andmete importimiseks/eksportimiseks äridomeenide ekspertide poolt. Korduvaks andmeintegratsiooniks, mis nõuab programmilist automatiseerimist, on sobivam mõni muu integratsioonitehnoloogia.

### <a name="data-integrator"></a>Andmeintegraator

Common Data Service’i administraatori kogemus pakub [andmeintegraatori teenust](https://docs.microsoft.com/powerapps/administrator/data-integrator), mida saab kasutada rakenduse Common Data Service andmeintegratsiooniks. Andmeintegraatorit saab kasutada integratsiooniprojektide määratlemiseks (sageli varem määratletud mallide põhjal, mille rakenduse arendajad on kohandanud kindla integratsiooni jaoks). Integratsiooniprojekte saab korduva graafiku põhjal kavandada automaatselt käivituma või käivitada neid käsitsi.

Andmeintegraatori projektid sobivad rakenduse Common Data Service pakktöötluse integreerimiseks ja need on suurepärane valik integratsiooniks Dynamics 365 perekonna rakenduste vahel. Näiteks pakub Microsoft valmiskujul andmeintegraatori malli, mida saab kasutada rakendusest Human Resources pärinevate andmetega integreerimiseks Dynamics 365 Finance’i. Lisateavet vt teemast [Integratsioon rakendusest Dynamics 365 Human Resources rakendusse Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Andmeintegraator toetab ka [võimsuse päringut](https://docs.microsoft.com/power-query/power-query-what-is-power-query) (selle [täpsema päringu funktsiooni](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering) kaudu).
Võimsuse päring pakub võimsat, paindlikku filtreerimist ja teisendust, sh rikkaliku M-valemi keelt, ja tõenäoliselt on see tuttav neile, kel on Power BI aruannete väljatöötamise kogemus.

## <a name="deciding-on-an-integration-technology"></a>Integratsiooni tehnoloogia otsustamine

Saadaval on palju erinevaid integratsioonitehnoloogiaid, nii et otsustamine, millist integratsioonilähenemist kasutada, võib mõnikord olla üle jõu käiv. Aja jooksul ja eriti kui andmekogumine rakenduses Common Data Service täiustub, muutub otsuse tegemine lihtsamaks, nii et enamasti valitakse Common Data Service’i andmeliides. Kuid seni võite leida, et Common Data Service ei vasta veel teie vajadustele. Järgmine tabel aitab kokku võtta erinevate integratsioonitehnoloogia suvandite peamisi omadusi.

| Tehnoloogia/tööriist/API    | Korduvad integreerimised                   | Sünkroonne/asünkroonne                    | Programmiline juurdepääs API kaudu        | Asjakohased andmemahud                                   | Andmete kaetus                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Common Data Service’i üksused           | Jah, kasutades andmeintegraatorit või vahevara | Asünkroonse sünkroonimine, partii (andmeintegraatori kaudu) | Jah, Dynamics 365 veebi API (OData) kaudu | Varieerub kasutusviisi puhul (toetab interaktiivseks kasutamiseks mõeldud kutsungit) | Parandamine<sup>2</sup>                       |
| DMF-i üksused           | Jah, plaanitud vahevara kaudu        | Asünkroonne, partii                                | Jah, DMF-paketi REST API kaudu         | Kõrge (sajad tuhanded kirjed)                    | Kõrge                                |
| DMF-pakett REST API   | Jah, plaanitud vahevara kaudu        | Asünkroonne, partii                                | Jah                                       | Kõrge (sajad tuhanded kirjed)                    | API toetab kõiki DMF-üksusi       |
| BYOD                   | Jah, administraatori plaanitud rakenduses Human Resources        | Asünkroonne, partii                                | Ei<sup>3</sup>                                    | Kõrge (sajad tuhanded kirjed)                    | Toetab kõiki DMF-üksusi           |
| OData-toega üksused | Jah, kasutades vahevara                    | Sünkroonimine                                        | Jah, Human Resourcesi andmeside teenuse kaudu (OData)  | Varieerub kasutusviisi puhul (toetab interaktiivseks kasutamiseks mõeldud kutsungit) | Kõrge                                |
| Exceli lisandmoodul           | Ei                                       | Sünkroonimine                                        | Ei                                        | Keskmine (kümned tuhanded kirjed)                      | Toetab kõiki OData toega üksusi |
| Andmeintegraator        | Jah, plaanitud andmeintegraatoris        | Asünkroonne, partii                                | Ei                                        | Varieerub kasutusviisist olenevalt                                       | Toetab kõiki Common Data Service’i üksusi           |

<sup>2</sup> Microsoft investeerib oluliselt, et suurendada Common Data Service’i üksuste andmete kaetust, ja soovitab katvuse olemasolul Common Data Service’it eelistatud andmevahetusviisiks. Praegu on Common Data Service’i DMF- ja OData toega üksuste andmete kaetus väike.

<sup>3</sup> SQL-i andmebaasil on programmiline juurdepääs.

## <a name="summary"></a>Kokkuvõte

Teie äriandmed on väärtuslikud varad, kuid nende väärtus väheneb, kui teil on raskusi andmete kasutamiseks kindlal eesmärgil (nt aruandlus, andmete koondamised või kohandatud rakendused). Dynamics 365 Human Resources pakub mitut tehnoloogiat teie andmetega töötamiseks väljaspool Human Resourcesi rakenduse kasutajaliidest (UI), mis võimaldab integreerida rakendustele andmejuurdepääsu. Selles teemas on kirjeldatud olemasolevaid integratsioonitehnoloogiaid ja mõningaid nende peamisi omadusi. See teave peaks aitama teil teha paremaid otsuseid selle kohta, milliseid lähenemisi teie integratsiooniprojektide puhul võimendada.

