---
title: Müügitellimuste tulu tuvastamine
description: Selles teemas kirjeldatakse müügitellimuste ja arvete tulu tuvastamise põhifunktsioone. Tulu tuvastamine on saadaval müügitellimuse ja selle müügitellimuse alusel loodud arve jaoks.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 6212ecbf1883405d7ca8cb1dba752b778e4d901c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995538"
---
# <a name="revenue-recognition-on-sales-orders"></a>Müügitellimuste tulu tuvastamine

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tulu tuvastamise funktsiooni ei saa funktsioonihalduse kaudu sisse lülitada. Praegu peate selle sisselülitamiseks kasutama konfiguratsioonivõtmeid.

Selles teemas kirjeldatakse müügitellimuste ja arvete tulu tuvastamise põhifunktsioone. Tulu tuvastamine on saadaval müügitellimuse ja selle müügitellimuse alusel loodud arve jaoks. Müügitellimuse saab luua ka aja- ja materjalikulu projekti kaudu.

> [!NOTE]
> Selle teema joonistel on veerud peidetud või lisatud ruudustikele, et mõistete näitlikustamist hõlbustada. Seetõttu võivad jooniste lehed ja andmed erineda sellest, mida teie tootes näete.

## <a name="enter-a-sales-order"></a>Müügitellimuse sisestamine

Sisestatakse järgmine müügitellimus, mis hõlmab kolme kaupa, mis on seadistatud tulu tuvastamiseks.

[![Müügitellimuse sisestamine](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Tulu tuvastamiseks on kaks mõistet:

- **Tulu hinna määratlemine** Tulu hind arvutatakse väljastatud toodete seadistuse põhjal. Tulu hinda ei näidata kunagi kliendile, vaid seda kasutatakse ainult müügitellimuse arve raamatupidamises. Müügitellimuse read ja müügi osana prinditavad dokumendid näitavad jätkuvalt ühiku/hinnakirja hinda.
- **Tulu tuvastamise toimumisaja määratlemine.** Tulu tuvastamise aja määratlemiseks kasutatakse tulugraafikut.

    Selles näites määratakse esimene kaup (S0001) tulugraafikule **1O** (üks esinemine). See rida kajastab vahe-eesmärgi tüüpi stsenaariumi, kus tulu tuvastatakse pärast installi toimumist tulevikus. Seetõttu lükatakse tulu edasi, kuni installimine on lõpule viidud.

    Teine kaup (S0008) on teenusüksus, mis seadistatakse lepingujärgse toe (PCS) kaubana. Püsivaid projekteerimisteenuseid pakutakse kliendile 12-kuulise perioodi jooksul. Seetõttu määratakse tootele vaikimisi tulugraafik **12 k**. Kuna see kaup on PCS-i kaup, tuleb määratleda lepingu algus- ja lõppkuupäevad. Vaikimisi leitakse lepingu algus- ja lõppkuupäevad vahekaardilt Kauba üksikasjad – Seadistus. Tulugraafikul määratakse **12 k** seadistus nii, et lepingutingimused lisatakse automaatselt, nagu näidatud järgmisel joonisel.

    [![Tulugraafikud](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Kolmas kaup (S0012) on riistvara ja tulugraafikut vaikimisi ei määrata. Riistvara tulu tuvastatakse kohe, kui kaup on arveldatud.

## <a name="confirm-the-sales-order"></a>Müügitellimuse kinnitamine

Tulu hinna ja tulugraafiku kohta lisateabe vaatamiseks kasutage müügitellimuse tegumiriba vahekaardi **Halda** grupi **Tulu tuvastamine** nuppe. Kuna müügitellimus ei ole selles etapis kinnitatud, ei ole tulu tuvastamiseks kasutatavad nupud saadaval. Need nupud muutuvad kättesaadavaks või mittekättesaadavaks vastavalt müügitellimuse edenemisele läbi eri etappide kuni täitmiseni.

[![Müügitellimuse päis](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

Esimesed kolm nuppu annavad teavet tulu tuvastamise müügitellimuse seadistuse kaupade tulu hinna kohta.

- **Tulu hinna eraldamine** – see nupp muutub kättesaadavaks pärast müügitellimuse kinnitamist või arve sisestamist. Nii müügitellimuse kinnitus kui ka arve sisestamine arvutavad tulu, et tuvastada hind, mis raamatupidamise kandes tuvastatakse või edasi lükatakse. Sõltuvalt seadistusest võib arvutatud tulu hind erineda kliendile kuvatavast ühiku hinnast.
- **Hinna ümberjaotamine uute tellimuse ridadega** – see nupp muutub kättesaadavaks pärast müügitellimuse kinnitamist või arve sisestamist. Ümberjaotamise protsessi kasutatakse selleks, at arvutada uuesti tulu, mis tuleb tuvastada pärast uue rea lisamist kas praegusele müügitellimusele, pärast selle arveldamist, või uuele müügitellimusele. Mõlema stsenaariumi korral põhjustab uue kauba lisamine lepingu muudatuse. Seetõttu tuleb tulu hind ümber jaotada.
- **Tulu hinna eraldamise uuendamine** – see nupp muutub kättesaadavaks pärast müügitellimuse kinnitamist ja mittekättesaadavaks pärast müügitellimuse arveldamist. Uuendamist kasutatakse tulu hinna eraldamise uuesti käitamiseks, ilma et oleks vaja müügitellimust kinnitada. Pärast müügitellimuse arveldamist ei saa tulu hinda uuesti arvutada.

Kaks viimast nuppu annavad üksikasjalikku teavet nende müügitellimusel olevate kaupade tulugraafiku kohta, millel on tulugraafik.

- **Eeldatav tulu tuvastamise graafik** – see nupp muutub kättesaadavaks pärast müügitellimuse kinnitamist ja mittekättesaadavaks pärast müügitellimuse arveldamist. See avab lehe, millel kuvatakse eeldatav tulugraafik. Lõplik graafik võib muutuda, kuna eeldatav graafik kasutab taotletud lähetuskuupäeva, kuid lõplik graafik kasutab tegelikku lähetuskuupäeva.
- **Tulu tuvastamise graafik** – see nupp muutub kättesaadavaks pärast müügitellimuse arveldamist. Lõplikku tulu tuvastamise graafikut ei looda, kui toimub kinnitamine või luuakse saateleht. See luuakse ainult siis, kui müügitellimus arveldatakse.

Järgmises näites toimus tulu hinna eraldamine müügitellimuse kinnitamisel. Arvestage, et ehkki tulu hinnad eraldatakse erinevalt, peab välja **Tuvastatav tulu** kogusumma siiski võrduma kliendile arveldatavate müügitellimuse ridade summaga. Näiteks on müügitellimuse ridade summa (v.a maks) 1499 $. Seetõttu peab väärtuste **Tuvastatav tulu** summa olema samuti 1499 $.

[![Tulu hinna eraldamine](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Luuakse ka eeldatav tulu tuvastamise graafik. Tulugraafik kasutab edasilükatava summana väärtust **Tuvastatav tulu**. Kaubal S0001 lükatakse 300 $ asemel edasi 321,21 $ ja kaubal S0008 lükatakse 100 $ asemel edasi 160,61 $. Kaupa S0012 ei kuvata eeldatavas graafikus, kuna tulu ei lükata edasi. Sisestamisel sisestatakse kauba S0012 kohta 1017,18 $ otse tulu pearaamatukontole.

[![Eeldatav tulu tuvastamise graafik](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>Saatelehe loomine

Järgmiseks saab müügitellimuse jaoks luua saatelehe. Saatelehe sisestamisel tulu ei tuvastata. Kui müügitellimust ei kinnitatud, ei käivita saatelehe sisestamine tulu hinna arvutamist. Samuti ei käivita see eeldatava või lõpliku tulu tuvastamise graafiku loomist. Kui kauba mudeligrupp on seadistatud saatelehel tulu edasi lükkama, jätkab see sisestamist praeguse sisestusprofiili pearaamatukontode abil, mitte arve sisestamisel kasutatavate uute edasilükatud tulu kontode abil.

## <a name="create-the-invoice"></a>Arve loomine

Viimaseks etapiks on müügitellimuse arveldamine. Kui vaatate arve kannet, siis näete, et kaupade S0001 ja S0008 tulu on edasi lükatud (321,21 + 160,61 = 481,82 $) ja kauba S0012 allesjäänud summa sisestati tulusse (1017,18). Need väärtused annavad kokku 1499 $, mis kattub müügitellimuse ridade summaga.

[![Kande kanded](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Pärast arve loomist muutuvad kättesaadavaks tulu tuvastamise nupud **Tulu hinna eraldamine**, **Hinna ümberjaotamine uute tellimuse ridadega** ja **Tulu tuvastamise graafik**, kuid nupud **Tulu hinna eraldamise uuendamine** ja **Eeldatav tulu tuvastamise graafik** pole kättesaadavad.

[![Saadaoleva tulu tuvastamise nupu kättesaadavus](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

Nupp **Tulu hinna eraldamine** on endiselt kättesaadav, et saaksite vaadata tulu hinna arvutust. Kui müügitellimusel ei ole pärast kinnitamist midagi muudetud, ei muuda arve sisestamine arvutatud summat väljal **Tuvastatav tulu**.

Eeldatav tulu tuvastamise graafik eemaldatakse ja asendatakse lõpliku tulu tuvastamise graafikuga. Tulugraafiku üksikasjad säilitatakse iga müügitellimuse rea kohta ja neid kasutatakse edasilükatud tulu vabastamiseks tegelikule tulule, kui lepingujärgsed kohustused on täidetud.

[![Lõplik tulu tuvastamise graafik](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]