---
title: Kupongid
description: See artikkel annab ülevaate kupongiga seotud võimalustest Microsoft Dynamics 365 Commerce.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 2594848948b141015adfaa4ec27e2c2b4cc4dcd2
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410468"
---
# <a name="coupons"></a>Kupongid

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

See artikkel annab ülevaate kupongiga seotud võimalustest Microsoft Dynamics 365 Commerce.

Kupongid on koodid ja vöötkoodid, mida kasutatakse allahindluste lisamiseks kannetele. Jaemüüjad jaotavad kuponge potentsiaalsetele või olemasolevatele klientidele, et aidata parandada nende kaubamärgituvastust, juhtida teisendamist, säilitada oma kliendibaasi, suurendada müüki ja lõpuks suurendada tulu. Kupongid on saanud üheks kõige populaarsemaks turundustööriistadest ja on e-kaubanduse müügis uueks normiks.

Kupongid Dynamics 365 Commerce on lingitud allahindlustega ja neid peetakse allahindluste peal täiendavaks kinnituseks. Iga kupong on seotud ühe allahindlusega ja sellega seotud allahindlus määratleb toodete komplekti, mille jaoks kupong kehtib.

Hinnagrupid, mis on seostatud allahindlusega määratlevad kõlblikke tingimusi, mille jaoks kupongi kasutada saab. Need tingimused hõlmavad kliendigruppe ja müüvad kanaleid. Kupongid pakuvad ka kasutuslimiiti **ja** kliendi **nõutavaid** atribuute, mida saab kasutada valikuliste kasutuspiirangute konfigureerimiseks.

Igal kupongil võib olla mitu kupongikoodi ja kupongi vöötkoodi ning igal koodil võib olla oma kehtivuse kuupäevade vahemik ja olek. Kui koodi olekuks on määratud **Passiivne**, ei saa koodi üheski kanalis kasutada.

## <a name="set-up-a-coupon"></a>Kupongi häälestamine

Enne kupongi seadistamist tuleb seadistada kupongi vöötkood ja kaks kupongi numbriseeriat.

Commerce Headquartersis kupongi häälestamiseks järgige neid samme.

1. Minge jaemüügi ja **äri varude halduse \> vöötkoodide \> ja siltide maski \> tähemärkidele**.
1. Valige **Lisa**, et luua kupongi koodi tüübi maski **tähemärk**. **Väljal Märk** saate valida mis tahes kasutamata märgi.
1. Minge jaemüügi ja **äri varude halduse vöötkoodide \>\> ja siltide vöötkoodi \> maski häälestusele**.
1. Valige **Kupongi** tüübi vöötkoodi maski loomiseks **uus**.
1. Minge jaemüügi ja **äri varude halduse \> vöötkoodide \> ja siltide vöötkoodi \> häälestusele**.
1. Valige **uus**, et luua vöötkood, mis kasutab teie loodud vöötkoodi maski.
1. Minge organisatsiooni **halduse \> numbriseeriate.**
1. Looge kaks numbriseeriat:

    1. Üks järjestus kuponginumbri **viite** jaoks. See järjestus määrab kupongi kordumatu IDENTIFIKAATORi.
    1. Üks järjestus Kupongi **koodi ID viite** jaoks. See järjestus määrab kupongi iga kupongikoodi kordumatu identifikaatori.

    Mõlema numbriseeria puhul tuleb määrata väljale **Ulatus** valik **Ettevõte**. Enamasti tuleks mõlemad järjekorranumbrid automaatselt luua.

1. Minge commerce’i **parameetritesse \> Hinnad ja allahindlused \> Kupongid**.
1. Seadke kupongi **vöötkoodi maski** väli varem loodud vöötkoodile.
1. Avage commerce’i **parameetrite \> numbriseeriad**.
1. Valige numbriseeriad, mille lõite varem kupongi numbri ja **kupongi koodi** **ID viidete** jaoks.

Kupongi häälestamiseks peate looma allahindluse ja kupongi eraldi ning need linkima, **valides** allahindluse konfiguratsiooni väljal Allahindlus. Kui kupong on lingitud allahindlusega, **·** **muutuvad** lingitud allahindluse oleku, **kehtivuse** kuupäevade ja aegumiskuupäeva väljad kirjutuskaitstuks, kuna väärtused määravad kupongi oleku ja kehtivuse perioodi. Kui kupongi olekuks on seatud **Aktiivne, uuendatakse lingitud allahindluse olek automaatselt olekusse Lubatud** **.** Kui kupongi olekuks on seatud **Passiivne**, uuendatakse lingitud allahindluse olek automaatselt olekusse **Keelatud**.

## <a name="use-a-coupon"></a>Kupongi kasutamine

Kupongi lisamiseks müügikandele Commerce Posis (POS), saate kasutada kupongikoodi või kupongi vöötkoodi. Kupongikoodi kasutamiseks valige toiming Kupongikoodi **lisamine** ja seejärel sisestage kood. Kupongi vöötkoodi kasutamiseks saate vöötkoodi skannida skannimisseadme abil või sisestada selle kande ekraanil numbriklaviatuuri **abil**.

Jaemüüjad soovivad mõnikord, et kassapidajad saavad määrata klientidele fikseeritud summaga allahindlusi jaotamise või tootedefektide tõttu, kuid nad ei soovi kupongikoode printida ja neid kassapidajatele jaotada. Sel juhul saate kupongi jaoks valida Rakenda **ilma kupongikoodita** valikule **Jah**. Kassapidajad saavad **seejärel** **kupongi** lisamiseks kandele kasutada kupongi funktsiooni Rakenda kupongi kuva saadaolevaid allahindlusi ilma koodi käsitsi sisestamata. Kui kupongi jaoks on mitu kupongikoodi, valib süsteem automaatselt esimese aktiivse koodi ja rakendab selle kandele.

Kupongi lisamiseks kõnekeskuse müügitellimusele peab **kõnekeskuse** **kasutaja** valima kupongid müügitellimuse lehe tegevuspaani vahekaardil Haldamine.

E-commerce’i tellimusele kupongi lisamiseks saab **ostukott sisestada kupongikoodi ostukorvi kampaaniakoodi** väljale.

Pärast kupongi lisamist müügitellimusele käivitab hinnakujundusmootor kohe kogu tellimuse ümberarvutuse, sõltumata sellest, kas edasilükatud arvutamine on lubatud.

> [!NOTE]
> Äriversioonis 10.0.30 ja varasemana pärast kõnekeskuse kasutajate kupongi lisamine kõnekeskuse müügitellimusele **tuleb** **·** **teil** kupongiga seostatud allahindluse rakendamiseks teha valik Arvuta uuesti tegevuspaani vahekaardil Müü.

## <a name="coupon-usage-limit"></a>Kupongi kasutuspiirang

Kuponge saab konfigureerida piiratud kasutamiseks. Kasutuslimiidi saab määratleda kliendi, kanali või globaalselt. Kasutuspiirang jõustatakse kupongikoodi alusel. Näiteks saab kaks kupongikoodiga ühekordselt kasutatavat kupongi kasutada kaks korda ja üks kord iga kupongikoodi kohta.

Kuponge saab kasutada kanalites. Kõnekeskuse puhul saab piiratud kasutusega kuponge **siiski** rakendada ainult siis, kui kõnekeskuse kanali tellimuse lõpetamise säte on lubatud. Kui säte **Luba tellimuse lõpetamine** on keelatud, saab rakendada vaid piiratud kasutusastmega kuponge.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
