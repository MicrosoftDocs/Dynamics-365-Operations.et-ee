---
title: ER Sihtkohade konfigureerimine
description: Selles protseduuris näidatakse, kuidas seadistada ja kasutada erinevaid sihtkohti elektroonilise aruandluse (ER) väljundi komponentide (nagu kaust või fail) jaoks.
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
ms.openlocfilehash: 3c8d03e9783013183fbe76cb36014fa9e1e1cbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291050"
---
# <a name="er-configure-destinations"></a>ER Sihtkohade konfigureerimine

[!include [banner](../../includes/banner.md)]

Selles protseduuris näidatakse, kuidas seadistada ja kasutada erinevaid sihtkohti elektroonilise aruandluse (ER) väljundi komponentide (nagu kaust või fail) jaoks. Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF. Saksamaa on juriidilise isiku emase aadressi riik\piirkond, kuid saate selles protseduuris kasutada mis tahes juriidilist isikut. 

Selles näites kasutatav vorming on ISO20022 kreeditiülekanne, kuid saate kasutada mis tahes vormingut, mis on juba imporditud. Arvestage sellega, et see protseduur on näide ühe faili ja ühe sihtkoha seadistusest. Lisateavet elektroonilise aruandluse sihtkohahalduse kohta leiate Dynamics 365 finantss spikrist.

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
