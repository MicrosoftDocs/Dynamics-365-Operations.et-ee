---
title: Mobiilse seadme menüükäskude sammude ümbersuunamise konfigureerimine
description: See artikkel kirjeldab, kuidas konfigureerida menüükäske nii, et töötajad saavad praegust ülesannet parkida, teha muud ülesannet ja seejärel naasta algse ülesande juurde ilma teavet kaotamata.
author: Mirzaab
ms.date: 09/01/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: d8d3d434077fdb145291e2298055f692b78db3d6
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428059"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Mobiilse seadme menüükäskude sammude ümbersuunamise konfigureerimine

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Selles artiklis kirjeldatud funktsioonid kehtivad ainult uuele laohalduse mobiilirakendusele. Need ei mõjuta vana laorakendust, mis on nüüdseks iganenud.

See artikkel kirjeldab, kuidas konfigureerida menüükäske nii, et töötajad saavad "park" praeguse ülesande täita, teha muud ülesannet ja seejärel naasta algse ülesande juurde ilma teavet kaotamata.

Ümbersuunamine on eraldi menüüpunkt, mida saab avada põhiülesande etapist. Ümbersuunamise lõpus suunatakse töötaja tagasi kohta, kust ta põhiülesandelt lahkus. Seadistamise ajal määrate menüüelemendi, mis peaks toimima ümbersuunamisena. Lisaks saate valida, millised põhiülesande välja väärtused suunatakse (kopeeritakse) automaatselt ümbersuunamisele ja sisestatakse sinna. Seetõttu peate mõistma, millises toiminguvoos soovite, et ümbersuunamine oleks töötajatele kättesaadav. Samuti peate tagama, et ümbersuunamisele kopeeritav teave on ülesandevoo selle etapi jaoks saadaval.

## <a name="enable-detours-in-your-system"></a>Lubage oma süsteemis ümbersuunamised

Enne kui saate mobiilseadme menüü-üksustes sammude ümbersuunamisi konfigureerida, peate täitma järgmise protseduuri, et lubada vajalikud funktsioonid ja genereerida Warehouse Management mobiilirakenduses nõutavad väljanimed.

1. Avage **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.
1. Veenduge, et lao *rakenduse juhiste funktsioon* on teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon vaikimisi sisse lülitatud. Funktsiooni *Laorakenduse toimingujuhised* kohta lisateabe saamiseks vaadake jaotist [Warehouse Management mobiilirakenduse etappide pealkirjade ja juhiste kohandamine](mobile-app-titles-instructions.md). See funktsioon on *Warehouse management rakenduse ümbersuunamise* funktsiooni eeltingimus.
1. Lülitage sisse järgmised funktsioonid, mis pakuvad selles artiklis kirjeldatud funktsioone:
    - *Warehouse management appi kõrvalepõiked*<br>(Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon vaikimisi sisse lülitatud.)
    - *Mitmetasandilised kõrvalepõiked Warehouse Managementi mobiilirakenduses*
1. *Kui laohalduse rakenduse dekrüptimine ja/* või mitmetasemeliste dekutased laohalduse mobiilirakenduse funktsioonide jaoks ei ole veel sisse lülitatud, värskendage laohalduse mobiilirakenduse väljanimesid, *·* **\>\> liikudes laohalduse häälestuse \>** mobiilse seadme rakenduse väljanimedele ja valides suvandi **Loo vaikehäälestus.** Lisateavet vt [Mobiilirakenduse Warehouse Management väljade konfigureerimine](configure-app-field-names-priorities-warehouse.md).
1. Korrake eelmist sammu iga juriidilise isiku (ettevõtte) puhul, kus kasutate Warehouse Management mobiilirakendust.

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Konfigureerige menüüpõhisest ülekirjutamisest ümbersuunamine

Menüüspetsiifilise ülekirjutamise ümbersuunamise seadistamiseks kasutage järgmist protseduuri.

1. Looge vastava menüü ja sammu jaoks menüüpõhine ülekirjutamine, nagu on kirjeldatud jaotises [Warehouse Management mobiilirakenduse sammude pealkirjade ja juhiste kohandamine](mobile-app-titles-instructions.md).
1. Leidke **Etapi ID** ja **menüüelemendi nime** nende väärtuste kombinatsioon, mida soovite redigeerida, ja valige väärtus veerus **Etapi ID**.
1. Ilmuval lehel kiirkaardil **Saadaolevad ümbersuunamised (menüüelemendid)** saate määrata menüüelemendi, mis peaks toimima ümbersuunamisena. Lisaks saate valida, millised põhiülesande väljaväärtused kopeeritakse automaatselt ümbersuunamiselt ja sealt ümbersuunamisele. Näiteid, mis näitavad, kuidas neid sätteid kasutada, vaadake selles artiklis allpool stsenaariume.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a>Näidisstsenaarium 1: müügivalik, kus asukohapäring toimib ümbersuunamisena

See stsenaarium näitab, kuidas konfigureerida asukohapäring ümbersuunamisena töötaja juhitud müügikomplekti töövoos. See ümbersuunamine võimaldab töötajatel otsida üles kõik numbrimärgid kohas, kust nad valivad, ja valida numbrimärgi, mida nad soovivad valimise lõpetamiseks kasutada. Seda tüüpi ümbersuunamine võib olla kasulik, kui vöötkood on kahjustatud ja seetõttu skanneri jaoks loetamatu. Teise võimalusena võib olla kasulik, kui töötaja peab õppima, mis süsteemis tegelikult saadaval on. Pange tähele, et see stsenaarium töötab ainult siis, kui valite numbrimärgiga kontrollitavatest kohtadest.

### <a name="enable-sample-data"></a>Luba näidisandmed

Määratud näidiskirjete ja väärtuste kasutamiseks selle stsenaariumi läbimiseks peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/fin-ops/get-started/demo-data.md). Enne alustamist peate valima ka **USMF-i** juriidilise isiku.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Looge menüüpõhine ülekirjutamine ja konfigureerige 1. stsenaariumi jaoks ümbersuunamine

Selle protseduuri käigus konfigureerite numbrimärgi etapis menüüelemendi **Müügi komplekteerimine** jaoks ümbersuunamise.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme etapid**.
1. Otsige üles sammu ID, mille nimi on *LicensePlateId* ja valide see.
1. Valige toimingupaanilt suvand **Lisa etapi konfiguratsioon**.
1. Kasutage rippmenüü dialoogiboksis välja **Menüüüksus**, et leida ja valida *Müügiks valimine*.
1. Valige nupp **OK**.
1. Ilmub äsja loodud ülekirjutamise üksikasjade leht. Valige kiirkaardil **Saadaolevad ümbersuunamised (menüüelemendid)** tööriistaribal **Lisa**.
1. Dialoogiboksis **Lisa ümberuunamine** valige ümbersõiduks **Asukohapäring**, mis tehakse kättesaadavaks Warehouse Management mobiilirakenduses.
1. Valige nupp **OK**.
1. Valige kiirkaardil **Saadaolevad ümbersuunamised (menüüelemendid)** äsja lisatud ümbersuunamine ja seejärel valige tööriistaribal **Vali saatmiseks väljad**.
1. Dialoogiboksis **Vali saatmiseks väljad** määrake teave, mis tuleb ümbersuunamisele ja sealt tagasi saata. Selle stsenaariumi korral lubate töötajatel kasutada asukohapäringu ümbersuunamise sisendina asukohta, mille nad peaksid valima. Seetõttu jaotises **Saada komplekteerimisest** valige tööriistaribal **Lisa**, et lisada rida ruudustikule. Seejärel määrake uuel real järgmised väärtused.

    - **Saada müügkomplekteerimisest:** *Asukoht*
    - **Kleebi asukohapäringusse:** *Asukoht*

1. Kuna selle stsenaariumi korral on ümbersuunamine konfigureeritud numbrimärgi etapis, on kasulik, kui töötajad saavad numbrimärgi päringu juurest tagasi põhivoogu tuua. Seetõttu jaotises **Tooge asukohapäringust tagasi** valige tööriistaribal **Lisa**, et lisada rida ruudustikule. Seejärel määrake uuel real järgmised väärtused.

    - **Kopeeri asukohapäringust:** *Numbriplaat*
    - **Kleepige müügivalikusse:** *Numbriplaat*

1. Valige nupp **OK**.

Ümbersuunamine on nüüd täielikult konfigureeritud. Nupp **Asukohapäringu** ümbersuunamise alustamiseks kuvatakse nüüd menüüelemendi **Müügiks valimine** numbrimärgi etapil.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Tehke mobiilseadmes müügivalik ja kasutage ümbersuunamist

Selle protseduuri käigus lõpetate müügivaliku, kasutades Warehouse Management mobiilirakendust. Kasutate äsja seadistatud ümbersuunamist, et leida numbrimärk, mida kasutate valimisetapi lõpuleviimiseks.

1. Looge Microsoft Dynamics 365 Supply Chain Management rakenduses müügitellimus, mis nõuab numbrimärki jälgitavast asukohast valimiseks valimisetappi. Seejärel vabastage müügitellimus lattu. Märkige üles loodava töö ID.
1. Avage Warehouse Management mobiilirakendus ja logige sisse lattu 24. (Standardsete demoandmete korral logige sisse, kasutades kasutaja ID-na nr *24* ja paroolina nr *1*.)
1. Valige menüü **Väljaminev** ja seejärel menüüelement **Müükide komplekteerimine**.
1. Järgige ekraanil kuvatavaid andmesisestusjuhiseid, et sisestada 1. sammus loodud töö ID.
1. Sammul, mis sisaldab teksti **Skanni numbrimärki**, avage toimingute menüü. Peaksite nägema uut nuppu **Asukohapäring**. Nool vasakus ülanurgas näitab, et nupp alustab ümbersuunamist. Valige **Asukoha päring**.
1. Ümbersuunamine on alanud. Kinnitage põhivoost kopeeritud asukoht järgmisel lehel.
1. Puudutage asukohas saadaolevate numbrimärkide loendis numbrimärki, mille soovite põhivoogu tagasi kopeerida. Seejärel vajutage nuppu **Tagasi**.
1. Olete naasnud müügi kogumise põhivoogu ja numbrimärk on ümbersuunamiselt sinna tagasi kopeeritud. Järgmise sammuga jätkamiseks kinnitage väärtus.
1. Nüüd saate ülejäänud standardvoo lõpule viia, sisestades nõutud andmesisestusjuhised.

Laotööd on nüüdseks lõpetatud. Töötaja avas edukalt ümbersuunamise teise ülesande täitmiseks (asukohapäring), kaotamata oma kohta põhiülesandes, ja tõi tagasi põhiülesande täitmiseks vajaliku teabe.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>Näidisstsenaarium 2: kaubapäring koos liikumise ja reguleerimise ümbersuunamistega

See stsenaarium näitab, kuidas konfigureerida liikumist ja kohandusi mitme ümbersuunamisena asukohapäringu töövoos. See võimalus võib olla kasulik olukordades, kus töötaja saabub asukohta, leiab, et asukohas olev laovaru erineb süsteemis registreeritust ja peab seetõttu kaupu kohandama või teisaldama.

Asukohapäringu saate vastavalt vajadusele asendada numbrimärgi päringuga või kaubapäringuga.

### <a name="enable-sample-data"></a>Luba näidisandmed

Määratud näidiskirjete ja väärtuste kasutamiseks selle stsenaariumi läbimiseks peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/fin-ops/get-started/demo-data.md). Enne alustamist peate valima ka **USMF-i** juriidilise isiku.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Looge menüüpõhine ülekirjutamine ja konfigureerige 2. stsenaariumi jaoks ümbersuunamine

Selle protseduuri käigus konfigureerite numbrimärgi etapis menüüelemendi **Müügi komplekteerimine** jaoks ümbersuunamise.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme etapid**.
1. Otsige üles ja valige sammu ID, mille nimi on *LocationInquiryList*.

    > [!NOTE]
    > Kaubapäringu kasutamiseks asukohapäringu asemel valige rida, kus etapi ID on *ItemInquiryList*. Numbripäringu kasutamiseks valige rida, kus sammu ID on *LPInquiryList*.

1. Valige toimingupaanilt suvand **Lisa etapi konfiguratsioon**.
1. Kasutage rippmenüü dialoogiboksis välja **Menüüüksus**, et leida ja valida *Asukohapäring*.
1. Valige nupp **OK**.
1. Ilmub äsja loodud ülekirjutamise üksikasjade leht. Valige kiirkaardil **Saadaolevad ümbersuunamised (menüüelemendid)** tööriistaribal **Lisa**.
1. Dialoogiboksis **Lisa ümberuunamine** valige ümbersuunamiseks **Liikumine**, mis tehakse kättesaadavaks Warehouse Management mobiilirakenduses.
1. Valige nupp **OK**.
1. Valige kiirkaardil **Saadaolevad ümbersuunamised (menüüelemendid)** äsja lisatud ümbersuunamine ja seejärel valige tööriistaribal **Vali saatmiseks väljad**.
1. Dialoogis **Vali saatmiseks väljad** määrake teave, mis tuleb ümbersuunamisele ja sealt tagasi saata. Selle stsenaariumi korral eeldate, et töötajad otsivad numbrimärgiga kontrollitud asukohti. Seetõttu on abiks numbrimärgi kopeerimine päringust ümbersuunamisele **Liikumine**. Jaotises **Saada komplekteerimisest** valige tööriistaribal **Lisa**, et lisada rida ruudustikule. Seejärel määrake uuel real järgmised väärtused.

    - **Kopeeri asukohapäringust:** *Asukoht*
    - **Kleebi liikumises:** *Loc / LP*

    Sellel ümbersuunamisel ei eeldata, et teavet tagasi kopeeritakse, kuna põhivoog oli päring, mille puhul pole vaja täiendavaid samme teha.

1. Valige nupp **OK**.

Ümbersuunamine on nüüd täielikult konfigureeritud. Nupp **Liikumine** ümbersuunamise alustamiseks kuvatakse nüüd menüüelemendi **Asukohapäring** numbrimärgi etapil.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Tehke mobiilseadmes asukohapäring ja kasutage ümbersuunamist

Selle protseduuri käigus teete asukohapäringu, kasutades Warehouse Management mobiilirakendust. Seejärel kasutate kauba liikumise lõpetamiseks ümbersuunamist.

1. Avage Warehouse Management mobiilirakendus ja logige sisse lattu 24. (Standardsete demoandmete korral logige sisse, kasutades kasutaja ID-na nr *24* ja paroolina nr *1*.)
1. Valige menüü **Varud** ja seejärel uus menüükäsk **Asukohapäring**.
1. Sisestage asukoht, mille kohta pärida, nt *FL-001*.
1. Kui loend kuvatakse, puudutage ja hoidke mõnda selles olevat kaarti, et kuvada saadaolevad ümbersuunamised.
1. Valige **Liikumine**.
1. Pange tähele, et numbrimärk on teie valitud kaardilt kopeeritud. Kinnitage väärtus.
1. Nüüd saate liikumise lõpetamiseks järgida standardset ülesandevoogu. Pärast töö lõpetamist avage toimingute menüü ja valige **Tühista**.
1. Olete naasnud lehele **Asukohapäring**. Pange tähele, et väärtusi ei värskendata automaatselt. Seetõttu peate liikumise ümbersuunamisel tehtud muudatuste nägemiseks lehte käsitsi värskendama.

> [!NOTE]
> Laohalduse *mobiilirakenduse* mitmetasemelised dekrüptid võimaldab määratleda mitmetasemelised dekrüptid (de lisade piires), mis võimaldab töötajatel kohe teise võimalusena alustada olemasolevatelt dekubaasidelt ja seejärel uuesti tagasi. See funktsioon toetab kahest kastist väljamineku tasemeid ja vajadusel saate kohandada oma süsteemi, et toetada kolme või enama detsidi tasemeid, luues tabelile koodi laiendeid`WHSWorkUserSessionState`.
