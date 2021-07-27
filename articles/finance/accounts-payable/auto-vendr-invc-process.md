---
title: Automatiseeritud hankijaarveldusprotsesside ülevaade
description: Selles teemas kirjeldatakse hankijaarveldusprotsesside automatiseerimise võimalust ja automatiseeritud protsessi kasutamise eeliseid.
author: abruer
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 778d00d777c44aa5cd19eced6d2d30e9b85500fd
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339056"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Automatiseeritud hankijaarveldusprotsesside ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse hankijaarveldusprotsesside automatiseerimise võimalust ja automatiseeritud protsessi kasutamise eeliseid. See võimalus koosneb funktsioonidest, mis lülitatakse sisse funktsioonihalduses. Need funktsioonid rakenduvad ainult hankija arvete korral, mitte arvete puhul, mida töödeldakse lehe **Arve tööleht** või **Arveregistri tööleht** kaudu.

Organisatsioonid töötavad tihti koos kolmandate osapooltega, et töödelda paberarveid optilise märgituvastuse (OCR) teenuse pakkuja kaudu. Teenusepakkuja tagastab masinloetavad arve metaandmed. Automatiseerimise hõlbustamiseks võimaldavad ostureskontro automatiseerimise funktsioonid teil tarbida neid artefakte ostureskontro funktsiooni kaudu.

Saate automatiseerida mõne ostureskontro hankijaarveldusprotsessi. Need protsessid hõlmavad imporditud hankija arvete edastamist töövoosüsteemile ja sisestatud toote sissetuleku ridade vastavusse viimist ootel hankija arve ridadega. Automatiseeritud protsess kuvab teavet hankija arve edenemise kohta protsesside läbimisel. See võimalus võib aidata ostureskontro ametnikel ja halduritel hankija arveid tõhusamalt töödelda. See aitab vähendada ka tõrkeid ja ebaefektiivsust, mis võivad tekkida, kui teave sisestatakse ja seda töödeldakse käsitsi.

Automatiseeritud protsesse saab kasutada järgmiste ülesannete täitmiseks.

- Imporditud arvete automaatne edastamine töövoosüsteemile.
- Toote sissetulekute vastavusseviimine hankija arve ridadega.
- Sisestamise jäljendamine enne hankija arve sisestamist.
- Töövoo ja automatiseerimise ajaloo kiire ja tõhus kuvamine.
- Hankija arvete töötlemise automatiseerimise tulemuste kuvamine ja analüüsimine.
- Mitme arve automatiseeritud töötluse jätkamine.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>Imporditud arvete automaatne edastamine töövoosüsteemile

Täiesti automaatse ostureskontro arveldusprotsessi osana saate lasta süsteemil automaatselt edastada imporditud arveid töövoosüsteemi. Protsess käivitub taustal sagedusel, mille määrate teie (kas iga tund või iga päev). Võimalus esitada imporditud arveid automaatselt töövoosüsteemile nõuab, et teie protsess algaks imporditud arvega. Tagamaks, et arvet saaks töödelda algusest lõpuni automaatselt, tuleb töövookonfiguratsiooni kaasata automatiseeritud sisestamisülesanne.


Töövoosüsteemile saab automaatselt edastada ostutellimustega seotud arveid ning arveid, mis sisaldavad ostutellimusega mitteseotud hankekategooriat ja mitteladustatavaid ridasid. Käsitsi sisestatud arved ja tööruumi **Hankija koostöö arveldus** kaudu loodud arved tuleb töövoosüsteemile käsitsi edastada. Ettemaksu avalduse töötlemine tuleb imporditud arvete puhul käsitsi läbi viia. Ettemakseid saate rakendada käsitsi enne või pärast imporditud arve sisestamist. Hankijaarvete lehte kasutades saate sisestamata standardarvetele **ettemakseid käsitsi** rakendada. Pärast sisestamist on tasakaalustatud ettemakse saadaval, et rakendada käsitsi teistele selle hankija arvetele leheküljel **Hankijad** lehel (**Ostureskontro \> Üld \> Hankijate \> hankijad vahekaart \> Arved \> Rakenda**).

Automatiseerimisfunktsioon pakub paindlikku raamistikku, mis võimaldab teil määratleda ettevõttespetsiifilisi reegleid imporditud hankija arvete edastamiseks töövoosüsteemile ja sisestatud toote sissetuleku ridade vastavusseviimiseks hankija arve ootel ridadega.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Toote sissetulekute vastavusseviimine arve ridadega, millel on kolmesuunaline vastavusse viimise poliitika

Süsteem saab sisestatud toote sissetulekuid viia automaatselt vastavusse arve ridadega, mille jaoks on määratletud kolmesuunaline vastavusse viimise poliitika. Protsess töötab seni, kuni vastavusse viidud toote sissetuleku kogus võrdub arve kogusega. Selle protsessi osana saate määrata, mitu korda peaks süsteem maksimaalset üritama viia toote sissetulekuid vastavusse arve ridadega, enne kui jõuab järeldusele, et protsess nurjus. Protsess töötab taustal, kas iga tund või iga päev. Saate käivitada automatiseeritud vastavusseviimise protsessi osana arvete edastamise protsessist töövoosüsteemi. Teise võimalusena saate selle käivitada eraldiseisva protsessina.

## <a name="pre-validate-vendor-invoice-posting"></a>Hankija arve sisestamise eelinstallimine

Sisestamise jäljendamise käigus viiakse lõpule kinnitamisetapid, mis tehakse hankija arvete puhul sisestamisprotsessi käigus, kuid ühtki kontot ei värskendata. Protsessi käivitamiseks saate valida kas ühe arve või mitu arvet lehel **Ootel hankija arved**.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Hankija arvete automatiseerimine – täiustatud kogemus töövoo ajaloolise teabe vaatamiseks hankija arvete puhul

Pakutakse hõlpsasti loetavat hankija arvete töövoo ajalugu. Hankija arvete töövoo ajaloo juurde pääseb otse hankija arvelt. Seetõttu on selle teabe leidmiseks vaja vähem klõpse. Kui teie organisatsioon on lubanud võimaluse edastada automaatselt imporditud hankija arveid töövoogu, pakutakse imporditud arvete jaoks automatiseerimise ajalugu. Automatiseerimise ajalugu aitab teil tuvastada praeguse protsessi etapi ja etapid, mis on juba lõpetatud. Kui etapp on ebaõnnestunud, pakub süsteem üksikasjalikku teavet, mis aitab teil mõista tõrke põhjuseid.

## <a name="analytics-and-metrics"></a>Telemeetria ja analüüs

Tööruum **Hankija arve sisestamine** võimaldab teil keskenduda hankija arvetele, mis ei jõudnud automatiseeritud protsessis lõpuni. Tööruumi paanidel on teave hankija arvete kohta, mida ei edastatud edukalt töövoosüsteemile, ei imporditud või ei viidud toote sissetulekutega vastavusse. Microsoft Power BI mõõdikud on samuti saadaval, et anda ostureskontro halduritele ülevaade hankija arvete automatiseerimise tõhususest.


## <a name="resume-automation-processing-for-multiple-invoices"></a>Mitme arve automatiseeritud töötluse jätkamine

Kui imporditud arve töövoogu edastamine automatiseeritud toimingu kaudu ei õnnestu, eemaldab süsteem selle edasisest automatiseeritud töötlusest. Ostureskontro ametnik saab arve läbi vaadata ja seda redigeerida, enne kui automatiseeritud protsess selle töövoogu uuesti esitab. Kui tõrke põhjuse saab lahendada mitme arve jaoks sama parandusega, saate taaskäivitada automatiseeritud protsessi lehel **Arve automatiseeritud töötluse jätkamine**. 

## <a name="tracking-the-invoice-received-date-value"></a>Arve saatmiskuupäeva väärtuse jälgimine

Arve **saatmiskuupäeva** väärtus näitab kuupäeva, mil ettevõte sai hankijalt arve. See pakub lähtepunkti arve edenemise jälgimiseks automatiseeritud protsesside kaudu. Selle väärtuse saab hankija arve imporditud andmetesse kaasata. Käsitsi loodud arvete jaoks saate määrata kuupäeva. Kui ühtegi väärtust ei sisestata, kasutatakse vaikimisi praegust kuupäeva.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>Imporditud arvesumma ja imporditud käibemaksusumma väärtuste jälgimine

Hankija arvete impordifailis saab esitada **imporditud arve summa** ja **imporditud käibemaksus** summa väärtused hankija arvete impordifailis. Tavaliselt on need väärtused pärit arvelt, mida skannis väline pakkuja ja mis kaasati impordifaili. Kuna arvet töödeldakse ostureskontros, arvutab süsteem väärtused arveandmete alusel. Arve saab sisestada ainult siis, kui imporditud väärtused ühtivad arvutatud väärtustega. Vastendamise väärtused tagavad, et arve kajastab täpselt summat, mille peab hankijale tagama. Kui teie organisatsioon lubab imporditud arveid töövoo süsteemile automaatselt esitada, saate valikuliselt nõuda, et imporditud kogusummad vastaksid arvutatud kogusummadele, enne kui arve saab töövoo süsteemile esitada.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Hankija arve automatiseerimine – mitme arve automatiseerimistoimingu jätkamine
Kui imporditud arve töövoogu edastamine automatiseeritud toimingu kaudu ei õnnestu, eemaldab süsteem selle edasisest automatiseeritud töötlusest. Ostureskontro ametnik saab arve läbi vaadata ja seda redigeerida, enne kui automatiseeritud protsess selle töövoogu uuesti esitab. Kui tõrke põhjuse saab lahendada mitme arve jaoks sama parandusega, saate taaskäivitada automatiseeritud protsessi lehel **Arve automatiseeritud töötluse jätkamine**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
