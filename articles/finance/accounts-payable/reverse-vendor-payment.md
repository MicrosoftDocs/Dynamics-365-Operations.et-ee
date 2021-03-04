---
title: Hankija makse storneerimine
description: See artikkel kirjeldab makse tagasipööramise, kustutamise, tühistamise ja tagasilükkamise erinevusi. Lisaks selgitab see kahte hankija tšeki tagasipööramise meetodit.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db9208c8e76d963d5b8f6bee6b7c73268af68734
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442316"
---
# <a name="reverse-a-vendor-payment"></a>Hankija makse storneerimine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab makse tagasipööramise, kustutamise, tühistamise ja tagasilükkamise erinevusi. Lisaks selgitab see kahte hankija tšeki tagasipööramise meetodit. 

Mõnikord tuleb hankija makse pärast sisestamist storneerida. Storneerimine erineb makse kustutamisest, tühistamisest või tagasilükkamisest. Makse saate kustutada ainult siis, kui selle olek on **Loodud**. See olek näitab, et makse on loodud, kuid pole veel genereeritud. See piirang kehtib alati olenemata makseviisist. Saate sisestamata tšekid pärast nende loomist, kuid enne sisestamist tühistada. Kui loodud makse on tehtud elektroonilise ülekandena, saate makse enne sisestamist tagasi lükata. Makse tagasilükkamiseks muutke valiku **Makse olek** väärtust Tühistatud või tagasi lükatud makset ei saa uuesti luua, kui suvandi **Makse olek väärtus** on muudetud tagasi sättele **Puudub**. 

Kui makse on sisestatud, kasutatakse storneerimist. Elektrooniliselt tehtud makseid ei saa pärast sisestamist storneerida. Selle asemel tuleb luua uus kanne makse summale, et viia kohustus hankija kontole tagasi. Sisestatud tšekkide storneerimiseks on kaks meetodit. Esimese meetodi puhul sisestatakse storno kohe pärast lehel **Tšekk** suvandi **Makse storneerimine** klõpsamist. Teise meetodi puhul saadetakse storno pärast lehel **Tšekk** suvandi **Makse storneerimine** klõpsamist tšeki storneerimise töölehele jaotises Sularaha- ja pangahaldus, kus läbivaataja saab storneerimise sisestada või tagasi lükata. 

Oma organisatsioonis kasutatavat meetodit vaadake lehelt **Sularaha- ja pangahalduse parameetrid**. Kui suvandi **Kasuta maksete storneerimiseks läbivaatusprotsessi** sätteks on valitud **Jah**, saadetakse stornod läbivaatuseks tšeki storneerimise töölehele. Järgmine tabel kirjeldab tšeki tühistamise meetodite erinevust.

| Kui teie organisatsioon ei vaata tšekkide storneerimist enne sisestamist läbi                                                                                                                                  | Kui teie organisatsioon vaatab tšekkide storneerimise enne sisestamist läbi                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tšekk storneeritakse kohe, kui klõpsate lehel **Tšekk** nuppu **OK**.                                                                                                                      | Tšekki ei storneerita kohe. Luuakse tšeki tühistamise tööleht ülevaatamiseks. Tšeki tühistamise töölehe kustutamisel saab tšeki uuesti tühistada.                                                                                                                                                                                                                                                                |
| Algse tšeki raamatupidamiskirjed tühistatakse.                                                                                                                                         | Pearaamatukontot algse tšeki raamatupidamiskirjest ei pruugita sisestada. Algse tšeki töölehe finantsdimensioone kasutatakse tšeki storneerimise töölehel vaikefinantsdimensioonidena. Saate neid vaikeväärtusi muuta. Tšeki storneerimise töölehe sisestamisel sisestatakse ostureskontro põhikontod automaatselt sisestusreeglitest, mis võivad olla muutunud. |
| Tšeki tühistamisel kasutatakse algse tšeki sisestamisel kasutatud raamatupidamise struktuure, isegi kui konto struktuuri on muudetud. Konto kombinatsioon pole kinnitatud. | Kui konto struktuur pärast algse tšeki sisestamist muutus, võib tšeki tühistamiseks olla vajalik uus finantsdimensioon. Seda finantsdimensiooni ei pruugita algselt maksetöölehelt automaatselt sisestada. Tšeki tühistamise sisestamisel kontrollitakse konto kombinatsiooni.                                                                                                        |
| Fikseeritud dimensioone ei rakendata stornole, et tagada samade pearaamatukontode storneerimine.                                                                                      | Fikseeritud dimensioonid rakendatakse tšeki tühistamise töölehel sisestamise ajal. Algse tšeki finantsdimensiooni väärtust ei pruugi algse tšeki raamatupidamiskirjes olla, sõltuvalt sellest, millal fikseeritud dimensioon määratleti.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Sisestatud tšekkide tühistamine neid läbi vaatamata
Kui teie organisatsioon soovib sisestada tšekkide storneerimise kohe, kui klõpsate lehel **Tšekid** suvandit **Makse storneerimine**. Valige lehel **Sularaha- ja pangahalduse parameetrid** suvandi **Kasuta maksete storneerimiseks läbivaatusprotsessi** sätteks **Ei**. Lehel **Tšekid** saate valida tšeki storneerimise ja suvandi **Makse storneerimine**. Seejärel saate sisestada kuupäeva ja valida storneerimise põhjuse.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Sisestatud tšekkide storneerimine pärast nende läbivaatamist tšeki storneerimise töölehel
Kui teie organisatsioon soovib tšekkide storneerimised enne sisestamist läbi vaadata, looge tšeki storneerimise tööleht läbivaatuseks ja valige lehel **Sularaha- ja pangahalduse parameetrid** suvandi **Kasuta maksete storneerimiseks läbivaatusprotsessi** sätteks **Jah**. Lehel **Tšekid** saate valida storneeritava tšeki ja suvandi **Makse storneerimine**. Seejärel saate sisestada kuupäeva ja valida storneerimise põhjuse. Finantspõhjuse peab seadistama nii panga kui ka hankija tüüpide kohta. Töölehe loomiseks tšeki storneerimise töölehel tuleb valida ka töölehe nimi.

### <a name="review-a-reversal"></a>Tagasivõtmise ülevaatamine

Kui olete kasutaja, kes peab storneerimised läbi vaatama, saate töölehe kinnitada ja sisestada või storneerimise tagasi lükata, kustutades töölehe. Lehel **Tšeki storneerimiste tööleht** saate valida läbivaadatava storneerimistöölehe ja seejärel klõpsata suvandit **Read**. Saate storneeritud tšeki läbi vaadata ja seejärel valida ühe järgmistest kinnitussuvanditest.

-   Storneerimistöölehe kinnitamiseks ja sisestamiseks klõpsake suvandit **Sisesta** või **Sisesta ja kanna üle**.
-   Storneerimise tagasilükkamiseks kustutage tšeki storneerimise tööleht.

> [!NOTE]
> Töölehe kustutamisel eemaldatakse storno süsteemist, kuid algne tšekk jääb lehele **Tšekk** alles. Tšeki olek ei ole enam **Tühistamise ootel**.

## <a name="results-of-posting-a-reversal"></a>Tagasivõtmise sisestamise tulemused
Kui sisestate tšeki storneerimise, toimuvad järgmised sündmused.

-   Tšeki olek värskendatakse sättele **Tühistamine**.
-   Kui storneerimise ajal valiti storneerimislehel suvand **Vii vastavusse**, viiakse tšekk vastavusse (suvand **Vastavusse viidud** on valitud) ja seda ei kuvata lehel **Konto vastavusseviimine**.
-   Tagasivõtmise kanne sisestatakse pangakontole, millelt tšekk välja anti, et suurendada pangakonto saldot.
-   Kanne sisestatakse pearaamatusse.
-   Muudatuse üksikasju värskendatakse lehel **Tšekk** väljagrupis **Ajalugu**.

> [!NOTE] 
> Kui tühistate tšeki, mis anti välja kontsernisiseseks kaubanduskandeks, tulevad tasakaalustavad kirjed kontsernisisese kaubanduse raamatupidamise seadistusest, mitte algsest kandest. Kui storneeritud tšekk väljastati hankijamakseks, toimuvad ka järgmised sündmused.

-   Algset makset arvelt, millele see tasakaalustati, ei rakendata (tasakaalustus võetakse tagasi).
-   Makse tühistamiseks sisestatakse kanne hankija kontole ja tühistatud makse tasakaalustatakse algse maksega. Algse hankija väljamakse välja **Viimane tasakaalustuskanne** lehel **Hankija kanded** värskendatakse, et kajastada storneeritud kande kandenumbrit.

Kui storneeritud tšekk väljastati kliendi tagasimakseks, toimuvad ka järgmised sündmused.

-   Kanne sisestatakse makse tühistamise kliendikontole ja tasakaalustus algse makse ja dokumendi vahel, millele makse algselt tasakaalustati, tühistatakse (luuakse negatiivne makse).
-   Makse tagasivõtmist rakendatakse algsele maksele. Algse kliendimakse välja **Viimane tasakaalustuskanne** lehel **Kliendi kanded** värskendatakse, et kajastada storneeritud kande kandenumbrit.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]