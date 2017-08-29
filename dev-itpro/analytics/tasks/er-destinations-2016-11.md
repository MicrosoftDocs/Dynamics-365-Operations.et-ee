--- 
title: Elektroonilise aruandluse (ER) sihtkohtade konfigureerimine
description: "Selles protseduuris näidatakse, kuidas seadistada ja kasutada erinevaid sihtkohti elektroonilise aruandluse (ER) väljundi komponentide (nagu kaust või fail) jaoks."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 88927a220246d11e48b210eb5648d7e7c2a7cef8
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="configure-destinations-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) sihtkohtade konfigureerimine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris näidatakse, kuidas seadistada ja kasutada erinevaid sihtkohti elektroonilise aruandluse (ER) väljundi komponentide (nagu kaust või fail) jaoks. Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF. Saksamaa on juriidilise isiku emase aadressi riike\piirkond, kuid saate selles protseduuris kasutada mis tahes juriidilist isikut. 

Selles näites kasutatav vorming on ISO20022 kreeditiülekanne, kuid saate kasutada mis tahes vormingut, mis on juba imporditud. Arvestage sellega, et see protseduur on näide ühe faili ja ühe sihtkoha seadistusest. Lisateavet elektroonilise aruandluse sihtkoha halduse kohta leiate rakenduse Dynamics 365 for Finance and Operations spikrist.

1. Avage Organisatsiooni haldus > Elektrooniline aruandlus > Elektroonilise aruandluse sihtkoht.
2. Klõpsake nuppu Uus, et luua valemile uus sihtkohtade kogum.
3. Valige väljal Viide vorming, mille jaoks soovite sihtkohti konfigureerida.
    * Kui teil ei ole valitavat väärtust, tähendab see, et te ei ole importinud ühtki elektroonilise aruandluse vormingu konfiguratsiooni. Peate importima vormingu konfiguratsiooni enne sihtkohtade seadistamist.  
4. Klõpsake nuppu Uus, et luua uus faili sihtkoht.
    * Pange tähele, et saate luua ühe faili sihtkoha igale sama vormingu väljundi komponendile, nagu kaust või fail. Teil on võimalik sihtkohti sätetes eraldi lubada ja keelata.  
5. Sisestage väljale Nimi kasutajasõbralik väljundi komponendi nimi.
    * Soovitame kasutada tähendusega nimesid, nagu Maksefail või Kontrollaruanne. Need nimed on kasutajatele konfiguratsiooni käitusajal koos sihtkoha sätetega nähtavad.  
6. Valige väljal Faili nimi fail või kaust, mis on vormingule omane.
7. Klõpsake nuppu Sätted.
8. Tehke väljal Lubatud valik Jah.
    * Iga vahekaardi märkeruut Lubatud lubab ja keelab iga sihtkohta eraldi. Selles näites lubate saata faili loomisel väljundifaili e-posti adressaadile.  
9. Klõpsake nuppu Redigeeri meili adressaatide seadistamiseks.
10. Klõpsake vahekaarti Lisa.
11. Klõpsake valikut Prindihalduse meiliaadress.
12. Valige suvand väljal Meilisõnumi allikas.
    * Saate valida erinevaid meiliallika tüüpe, nt kliendi või hankija tüübi. See määratleb argumendi tüübi, mis meilisõnumi allika valemiga tagastatakse. Meilisõnumi allika konto valem, mida kirjeldatakse järgmises etapis, on koht, kus saate siduda meilisõnumi allika. Tehke valik Hankija, kui teie valem tagastab hankija konto. Kasutage hankijat, kui kasutate ISO 20022 kreeditkande konfigureerimise näidet.  
13. Klõpsake nuppu Meilisõnumi allika sidumine.
14. Sisestage väljale Valem dokumendipõhine viide varem valitud osapoole tüübile.
    * Tippimise asemel saate üles otsida andmeallika sõlme, mis tähistab osapoole kontot, ja klõpsata valemi värskendamiseks nuppu Lisa andmeallikas. Näiteks kui kasutate ISO 20022 krediidikande konfiguratsiooni, tähistab hankija kontot sõlm '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID. Vastasel korral sisestage valemi salvestamiseks stringi väärtus, nagu DE-001.  
15. Klõpsake nuppu Salvesta.
16. Sulgege leht.
17. Klõpsake nuppu Redigeeri osapoole kontaktandmete konfigureerimiseks.
18. Valige väljal Põhikontakt Jah.
    * Võite kasutada erinevaid valikuid näitamiseks, millist osapoole kontakti tüüpi tuleks selle sihtkoha puhul meiliaadressina kasutada. Selles näites kasutame põhikontakti.  
19. Klõpsake nuppu OK.
20. Klõpsake nuppu OK.
21. Sisestage väärtus väljale Teema.
22. Klõpsake nuppu OK.


