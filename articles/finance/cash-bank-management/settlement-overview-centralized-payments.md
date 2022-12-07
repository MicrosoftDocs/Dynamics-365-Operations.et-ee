---
title: Tasakaalustuse ülevaade tsentraliseeritud maksete puhul
description: See artikkel kirjeldab 365 finantsi puhul Microsoft Dynamics tsentraliseeritud maksete tasakaalustamist.
author: angelad116
ms.date: 11/22/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "222414"
- intro-internal
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42c359edbe49af151ac76c9873c0d429bbe1ca12
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804222"
---
# <a name="settlement-overview-for-centralized-payments"></a>Tasakaalustuse ülevaade tsentraliseeritud maksete puhul

[!include [banner](../includes/banner.md)]

Organisatsioonid, mis sisaldavad mitut juriidilist isikut, saavad luua ja hallata makseid, kasutades kõigi maksetega tegelevat juriidilist isikut. See kõrvaldab vajaduse sisestada sama kannet mitmes juriidilises isikus ja säästab aega, korrastades maksesoovituse protsessi, tasakaalustusprotsessi, avatud kande redigeerimist ja suletud kande redigeerimist tsentraliseeritud maksete jaoks. 

Kui ühes juriidilises isikus sisestatakse kliendi- või hankijamakse ja tasakaalustatakse teises juriidilises isikus sisestatud arvega, genereeritakse kummagi juriidilise isiku kohta automaatselt sobiv tasakaalustus ning algus- ja lõputähtaegade kanded. Igale arve- ja maksekombinatsioonile kandes luuakse tasakaalustuskanne. Igale tasakaalustuskirjele määratakse uus kandenumber, mis põhineb makse kande numbriseerial, mis on määratud klientide puhul lehel **Müügireskontro parameetrid** ja hankijate puhul lehel **Ostureskontro parameetrid**. 

Kui lisatasakaalustuskirjed luuakse skontodele, välisvaluuta ümberarvutamistele, sendierinevustele, üle- või alamaksetele, määratakse neile makse või arvekande hilisem kuupäev. Kui tasakaalustus toimub pärast makse sisestamist, kasutavad tasakaalustuskirjed tasakaalustuse sisestuskuupäevi, mis on määratud lehel **Tasakaalusta avatud kanded**.

## <a name="posting-types-transaction-types-and-default-descriptions"></a>Sisestustüübid, kandetüübid ja vaikekirjeldused

Kontsernisisesed tasakaalustuskanded kasutavad kontsernisisese tasakaalustuse sisestustüüpi, kontsernisisese kliendi tasakaalustuse ja kontsernisisene hankija tasakaalustuse kandetüüpe. Kandetüübi teavet saate seadistada lehel **Vaikekirjeldused**. 

Järgnevad kandetüübid on saadaval nii ühe ettevõtte kui ka kontsernisiseseks tasakaalustuseks:

-   Tasakaalustus
-   Skonto
-   Välisvaluuta ümberarvutamised (hõlmab realiseeritud ja realiseerimata välisvaluuta ümberarvutamisi)
-   Sendierinevus
-   Üle- või alamakse

Saate ka määrata vaikekirjeldused kontsernisisestele tasakaalustuskannetele.

## <a name="currency-exchange-gains-or-losses"></a>Valuutavahetuse kasumid ja kahjumid

Valuutakurssi, mida kasutatakse kliendi- või hankijakanneteks, talletatakse koos kandega. Valuutavahetusega seotud realiseeritud kasumid või kahjumid sisestatakse kas arve juriidilisse isikusse või makse juriidilisse isikusse, olenevalt makse juriidilise isiku lehel **Kontsernisisene raamatupidamine** väljal **Sisesta valuutavahetusega seotud kasum või kahjum** tehtud valikust. Järgnevad näited kasutavad neid valuutasid:
-   Makse arvestusvaluuta: EUR
-   Arve arvestusvaluuta: USD
-   Makse kandevaluuta: DKK
-   Arve kandevaluuta: CAD

### <a name="currency-calculations"></a>Valuutaarvutused

Ühes juriidilises isikus sisestatud arve tasakaalustamisel teises juriidilises isikus sisestatud arvega teisendatakse makse kandevaluutat (DKK) kolmes etapis:
1.  Teisendatakse makse arvestusvaluutaks (EUR), kasutades makse juriidilise isiku vahetuskurssi alates makse kuupäevast.
2.  Teisendatakse arve arvestusvaluutaks (USD).
3.  Teisendatakse arve kandevaluutaks (CAD), kasutades arve juriidilise isiku vahetuskurssi.

Teisendusprotsess kasutab vahetuskursse alates makse kuupäevast. Kui tulemuseks olev maksesumma arvekande valuutas (CAD) on võrdne arve summaga (CAD), loetakse arve täielikult makstuks. 

Kui leht **Avatud kannete tasakaalustamine** avatakse maksetöölehelt, kuhu maksesummat pole sisestatud, arvutatakse tasakaalustatav summa lehel **Avatud kannete tasakaalustamine** tasakaalustamiseks valitud vormide põhjal. Tasakaalustatav summa teisendatakse kolmes astmes:
1.  Teisendatakse arve arvestusvaluutaks (USD), kasutades arve juriidilise isiku vahetuskurssi makse kuupäeval.
2.  Teisendatakse makse arvestusvaluutaks (EUR), kasutades arve juriidilise isiku vahetuskurssi makse kuupäeval.
3.  Teisendatakse makse kandevaluutaks (DKK).

Tulemuseks olev maksesumma kantakse üle maksetöölehe reale, kui sulete lehe **Avatud kannete tasakaalustamine**.

### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Erinevate arvestusvaluutade tõttu tekkinud kasumi või kahjumi sisestamine

Valuutavahetusega seotud kasumi või kahjumi korral sisestatakse kasum või kahjum juriidilisse isikusse, kes on määratud makse juriidilise isiku lehel **Kontsernisisene raamatupidamine** väljal **Sisesta valuutavahetusega seotud kasum või kahjum**. Kasumi või kahjumi summa teisendatakse juriidilise isiku, kus kasum või kahjum sisestati, arvestusvaluutaks, kasutades selle juriidilise isiku puhul määratletud vahetuskurssi.

## <a name="cash-discounts"></a>Skontod

Kontsernisisese tasakaalustusprotsessi käigus loodud skontod sisestatakse kas arve juriidilisse isikusse või makse juriidilisse isikusse, olenevalt makse juriidilise isiku lehel **Kontsernisisene raamatupidamine** väljal **Sularaha allahindluse sisestamine** tehtud valikust. Vastav seadistuskanne luuakse arve juriidilises isikus.

## <a name="overpayments-and-underpayments"></a>Ülemaksed ja alamaksed

Ülemaksete, alamaksete ja sendierinevuse kõikumised määratakse ülemaksete makse juriidilise isiku põhjal ja alamaksete arve juriidilise isiku põhjal. Kasutatav sisestuskonto määratakse klientide puhul väljaga **Skonto haldamine** lehel **Müügireskontro parameetrid** ja hankijate puhul väljaga **Skonto haldamine** lehel **Ostureskontro parameetrid**.

-    **Kui** skonto administratsiooni säte on Konkreetne või **kui** säte on Määramata ja rakendatav skonto on sisestatud ülemaksest erinevale juriidilisele isikule, kasutatakse automaatset kontot Kliendi skonto, Hankija skonto või Sendierinevuse jaoks arvestusvaluutas. Saate määrata need kontod lehel **Automaatsete kannete kontod**.
-    **Kui** skonto administratsiooni säte on Määramata ja skonto sisestatakse ülemaksega samasse juriidilisse isikusse (makse juriidiline isik ja arve juriidiline isik on samad), korrigeeritakse skonto kontot. Nt kui arve 100,00-le koos saadaoleva skontoga 3,00 tasakaalustatakse maksega 98,00, korrigeeritakse skontot 1,00 võrra. Netoallahindlussumma on 2,00.
-    **Kui** skonto administratsiooni säte on Määramata, sisestatakse skonto ülemaksega samasse juriidilisse isikusse ja üle- või alamakse tasakaalustatakse mitme arvega skontoga, korrigeeritakse viimase arve skontokontot.

Kui skonto administreerimisvalik **on Määramata**, kehtivad määramata makse tasakaalustusreeglid ainult järgmistes olukordades:
-   Ülemakse.
-   Ülemakse tasakaalustatakse ühe või rohkema arvega, millel on skonto.
-   Skonto sisestatakse ülemaksega samasse juriidilisse isikusse.

Muudel juhtudel sisestatakse ülemaksed või alamaksed kliendi skonto, hankija skonto või arvestusvaluuta sendierinevuse automaatsele kontole.

## <a name="sales-tax"></a>Käibemaks
Käibemaksukanded jäävad juriidilisse isikusse, kuhu need algselt sisestati. 

Kui käibemaks sisestati ettemaksena, tühistab kontsernisisene tasakaalustus käibemaksu ettemakse ettemakse juriidilises isikus. Arve juriidilise isiku maksud jäävad arve juriidilisse isikusse.

## <a name="financial-dimensions"></a>Finantsdimensioonid
Kliendimaksete puhul kasutavad makse juriidilise isiku algus- ja lõputähtaja kanded tasakaalustatava makse müügireskontro koondkontole määratud finantsdimensioone. Arve juriidilises isikus kasutavad algus- ja lõputähtaja kanded tasakaalustatava arve müügireskontro koondkontole määratud finantsdimensioone. 

Hankijamaksete puhul kasutavad makse juriidilise isiku algus- ja lõputähtaja kanded tasakaalustatava makse ostureskontro koondkontole määratud finantsdimensioone. Arve juriidilises isikus kasutavad algus- ja lõputähtaja kanded tasakaalustatava arve ostureskontro koondkontole määratud finantsdimensioone.

## <a name="withholding-tax"></a>Maksu kinnipidamine
Arvega seostatud hankijakontot kasutatakse määramiseks, kas kinnipeetav maks tuleb arvutada. Kinnipeetava maksu rakendumisel arvutatakse see juriidilises isikus, mis on arvega seostatud. Kui juriidilised isikud kasutavad erinevaid valuutasid, kasutatakse arvega seostatud juriidilise isiku vahetuskurssi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
