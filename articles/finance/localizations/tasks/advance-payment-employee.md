---
title: EEU-00047 Töötajale avansi maksmine
description: See protseduur näitab, kuidas seadistada ja registreerida avansisaaja kandeid.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCashTable, LedgerJournalSetup, HcmWorkerGroup_RU, EmplPosting_RU, VendParameters, RCashPosting, BankParameters, PaymTerm, HcmWorker, HcmWorkerNewWorker, HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU, PurchTable, PurchCreateOrder, HcmAdvHolderLookup_RU, InventItemIdLookupPurchase, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, EmplTrans_RU, EmplBalance_RU
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fe975f802a8d8080a306d9ac1cedb377f280690
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407849"
---
# <a name="eeu-00047-advance-payment-to-employee"></a>EEU-00047 Töötajale avansi maksmine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas seadistada ja registreerida avansisaaja kandeid. Selle protseduuri loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Leedu, andmeid. Selle toiming sobib ainule juriidilistele isikutele esmase aadressiga Poolas, Leedus, Lätis, Eestis, Tšehhi Vabariigis või Ungaris. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="create-a-new-cash-account"></a>Uue sularahakonto loomine
1. Minge jaotisse Sularaha- ja pangahaldus > Pangakontod > Sularahakontod.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Sularaha.
4. Sisestage väärtus väljale Nimi.
5. Sisestage või valige väärtus väljal Numbriseeria grupp.
6. Laiendage jaotist Kinnitamine.
7. Valige või sisestage väärtus väljal Valuuta.
8. Tehke väljal Negatiivne kassa valik Jah.
9. Klõpsake nuppu Salvesta.

## <a name="create-a-new-journal"></a>Uue töölehe loomine
1. Minge jaotisesse Pearaamat > Töölehe seadistamine > Töölehtede nimed.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Sisestage või valige väärtus väljal Kande seeria.
5. Klõpsake nuppu Salvesta.
6. Klõpsake valikut Uus.
7. Sisestage väärtus väljale Nimi.
8. Valige suvand väljal Töölehe tüüp.
9. Sisestage või valige väärtus väljal Kande seeria.
10. Klõpsake nuppu Salvesta.

## <a name="create-an-advance-holder-group"></a>Avansisaajate grupi loomine
1. Avage Ostureskonto > Seadistus > Avansisaajad > Avansisaajate rühmad.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Grupp.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake nuppu Salvesta.

## <a name="create-an-employee-posting-profile"></a>Töötaja sisestusreeglite loomine
1. Avage Ostureskontro > Seadistus > Avansisaajad > Töötaja sisestusreeglid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Sisestusreeglid.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Märkige loendis valitud rida.
6. Valige suvand väljal Kehtiv.
7. Määrake väljal Summakonto soovitud väärtused.
8. Klõpsake nuppu Salvesta.

## <a name="set-up-advance-holder-parameters"></a>Avansisaaja parameetrite seadistamine
1. Avage Ostureskontro > Seadistus > Ostureskontro parameetrid.
2. Klõpsake vahekaarti Avansisaajad.
3. Sisestage või valige väärtus väljal Sisestusreeglid.
4. Sisestage või valige väärtus väljal Nimi.
5. Valige või sisestage väärtus väljal Sularaha.
6. Sisestage või valige väärtus väljal Nimi.
7. Valige suvand väljal Konto tüüp.
8. Täpsustage soovitud väärtusi väljal Põhikonto.
9. Klõpsake vahekaarti Numbriseeriad.
10. Klõpsake nuppu Salvesta.

## <a name="set-up-a-cash-posting-profile"></a>Kassa sisestusprofiili seadistamine
1. Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha sisestusreeglid.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Kassaseisu sisestamine.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Märkige loendis valitud rida.
6. Valige suvand väljal Kehtiv.
7. Täpsustage soovitud väärtusi väljal Põhikonto.
8. Klõpsake nuppu Salvesta.

## <a name="set-up-cash-and-bank-parameters"></a>Sularaha- ja pangahalduse parameetrite seadistamine
1. Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.
2. Klõpsake vahekaarti Sularaha.
3. Valige või sisestage väärtus väljal Sularaha.
4. Valige või sisestage väärtus väljal Kassaseisu sisestamine.
5. Klõpsake nuppu Salvesta.
6. Klõpsake vahekaarti Numbriseeriad.
7. Otsige loendist ja valige soovitud kirje.
8. Sisestage või valige väärtus väljal Numbriseeria kood.
9. Otsige loendist ja valige soovitud kirje.
10. Sisestage või valige väärtus väljal Numbriseeria kood.
11. Klõpsake nuppu Salvesta.

## <a name="set-up-terms-of-payment"></a>Maksetingimuste häälestamine
1. Avage Ostureskontro > Makse seadistus > Maksetingimused.
2. Klõpsake nuppu Redigeeri.
3. Tehke väljal Avansisaajalt valik Jah.
4. Klõpsake nuppu Salvesta.

## <a name="create-a-new-worker"></a>Uue töötaja loomine
1. Avage Personaliarvestus > Töötajad > Töötajad.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Eesnimi.
4. Sisestage väärtus väljale Perekonnanimi.
5. Tippige väärtus väljale Töötaja ID.
6. Klõpsake suvandit Uue töötaja värbamine.
7. Klõpsake nuppu Salvesta.

## <a name="set-up-a-worker-as-an-advance-holder"></a>Töötaja seadistamine avansisaajaks
1. Avage Ostureskonto > Avansisaajad > Avansisaajad.
2. Klõpsake nuppu Redigeeri.
3. Sisestage või valige väärtus väljal Grupp.
4. Tehke väljal Avansisaaja valik Jah.
5. Klõpsake nuppu Salvesta.

## <a name="create-and-post-a-purchase-order-invoice"></a>Ostutellimuse arve loomine ja sisestamine
1. Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Hankija konto või valige see.
4. Klõpsake nuppu OK.
5. Valige üks suvand väljalt Read või päis.
6. Laiendage jaotist Hind ja allahindlus.
7. Valige või sisestage väärtus väljal Terms of payment (Makse tingimused).
8. Valige või sisestage väärtus väljal Avansisaaja.
9. Valige üks suvand väljalt Read või päis.
10. Märkige loendis valitud rida.
11. Sisestage või valige väärtus väljal Kaubakood.
12. Sisestage arv väljale Kogus.
13. Sisestage arv väljale Ühiku hind.
14. Klõpsake nuppu Salvesta.
15. Klõpsake toimingupaanil valikut Ost.
16. Klõpsake käsku Kinnita.
17. Klõpsake toimingupaanil valikut Arve.
18. Klõpsake valikut Arve.
19. Rippdialoogi avamiseks klõpsake valikut Vaikimisi asukohast: toote sissetuleku kogus.
20. Valige suvand väljal Ridade vaikekogus.
21. Klõpsake nuppu OK.
22. Sisestage väärtus väljale Arv.
23. Sisestage väljale Arve kirjeldus soovitud väärtus.
24. Sisestage kuupäev väljale Arve kuupäev.
25. Sisestage kuupäev väljale KM-registri kuupäev.
26. Sisestage kuupäev väljale Vastuvõtudokumendi kuupäev.
27. Klõpsake valikut Sisesta.

## <a name="balance-and-close-advance-holders-transactions"></a>Avansisaajate kannete tasakaalustamine ja sulgemine
1. Avage Ostureskonto > Avansisaajad > Avansisaajad.
2. Klõpsake suvandit Kanded.
3. Sulgege leht.
4. Klõpsake valikut Saldo.
5. Klõpsake valikut Sule panga kaudu.
6. Tehke väljal Automaatne valik Jah.
7. Sisestage väljale Ülekantav summa number.
8. Klõpsake nuppu OK.
9. Klõpsake valikut Sule kassa kaudu.
10. Tehke väljal Automaatne valik Jah.
11. Klõpsake nuppu OK.
12. Sulgege leht.
13. Klõpsake suvandit Kanded.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]