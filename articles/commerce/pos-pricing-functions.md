---
title: Hinnakujunduse funktsioonid kassas
description: See artikkel kirjeldab erinevaid hinna ja allahindluse funktsioone Microsoft Dynamics 365 Commerce kassa rakenduse puhul.
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 92bbc3b81b889f106dc113528afbdc37d1106ff3
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2022
ms.locfileid: "9293651"
---
# <a name="pricing-functions-in-pos"></a>Hinnakujunduse funktsioonid kassas

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See artikkel kirjeldab erinevaid hinna ja allahindluse funktsioone Microsoft Dynamics 365 Commerce kassa rakenduse puhul.

Müügikoha Dynamics 365 Commerce rakendus pakub võimalusi, mis võimaldavad esimese rea töötajatel kauplusetoiminguid sooritada. Järgmine tabel näitab hinna ja allahindluse funktsioone, mis on hetkel rakenduses saadaval.

| Funktsioon                       | Kassatoimingud |
|--------------------------------|----------------|
| Kuva hinnad                    | [Hinnakontroll](#price-check) |
| Allahindluste kuvamine                 | [Kuva kõik allahindlused](#view-all-discounts)<br>[Kuva pakutavad allahindlused](#view-available-discounts) |
| Alista hinnad                | [Hinnaerand](#price-override) |
| Allahindluste rakendamine või eemaldamine      | [Rea allahindluse summa](#line-discount-amount)<br>[Rea allahindluse protsent](#line-discount-percent)<br>[Lõppallahindluse summa](#total-discount-amount)<br>[Lõppallahindluse protsent](#total-discount-percent)<br>[Eemalda kandest süsteemi allahindlused](#remove-system-discounts-from-transaction)<br>[Rakenda süsteemi allahindlused uuesti](#reapply-system-discounts) |
| Kupongide rakendamine või eemaldamine        | [Lisa kupongikood](#add-coupon-code)<br>[Kupongikoodi eemaldamine](#remove-coupon-code) |
| Hindade ja allahindluste arvutamine | [Arvuta uuesti](#recalculate) |

Teavet selle kohta, kuidas eelnevaid toiminguid kassarakenduses konfigureerida ja kas need toetavad võrguühenduseta režiimi, [vaadake võrgu ja võrguühenduseta kassatoimingutest](pos-operations.md).

## <a name="price-check"></a>Hinnakontroll

Hinnakontrolli **toiming** võimaldab müügikoha kasutajatel otsida konkreetse toote eelkonfigureeritud hindu.

## <a name="view-all-discounts"></a>Kuva kõik allahindlused

Toiming **Kuva kõik allahindlused võimaldab kassa kasutajatel otsida kõiki kanaleid, mis hetkel kaupluse kanalis** töötavad. See toiming loetleb kõik allahindlused, mis vastavad järgmistele tingimustele:

- Allahindluse rühm ühtib kaupluse hinnarühmaga.
- Allahindlusrühm on vastendatud kuuluvuse- või püsikliendiprogrammiga.
- Allahindlusrühm on vastendatud kauplusega seotud kataloogiga.

Kõigi **allahindluste kuvamise toiming** näitab ainult allahindlusi, mis ei konkureeri juba rakendatud allahindlusega. Selline käitumine aitab tagada, et kui müügiesindaja teavitab klienti allahindlusest ja klient võtab vajalikud meetmed (nt klient ostab veel ühe üksuse, et saada 10 protsenti allahindlust), rakendatakse allahindlus kandele. Kupongipõhised allahindlused kuvatakse ainult juhul, kui kupongikoodita **rakendumise** parameeter on sisse lülitatud.

Kõikide allahindluste **kuvamise toimingu sees** saavad müügikoha kasutajad otsida allahindlusi nime ja kirjelduse järgi ning nad saavad allahindlusi filtreerida selle põhjal, kas nad vajavad kupongi.

## <a name="view-available-discounts"></a>Kuva pakutavad allahindlused

Toiming **Kuva saadaolevad allahindlused** võimaldab kassa kasutajatel vaadata kõiki allahindlusi, mis kehtivad kande valitud real või kogu kandel. Valitud reale rakendatavad allahindlused sisaldavad allahindlusi, mida on juba rakendatud ja allahindlusi, mida pole veel rakendatud, kuid mida ei saa rakendada (nt segamise ja sobitamise allahindlusi, mis nõuavad täiendavaid kaupu). **Kui** rakenduv allahindlus on lingitud kupongiga, kus kupongikoodita parameetrid on sisse lülitatud, **saab** müügikoha kasutaja kasutada toimingu sees kupongi rakendamisfunktsiooni, et kupongi otse lunastada, ilma et oleks vaja sisestada või skannida kupongikoode või kupongi vöötkoode.

## <a name="price-override"></a>Hinnaerand

Hinna **alistamise** toiming võimaldab müügikoha kasutajatel kandes toote müügihinna alistada. See toiming töötab ainult toodete puhul, mis on konfigureeritud lubama hinnaesimesi.

## <a name="line-discount-amount"></a>Rea allahindluse summa

Rea **allahindluse summa** toiming võimaldab kassa kasutajatel kandes rea kaubale allahindluse summa sisestada. See toiming rakendub ainult allahinnatavatele kaupadele ja see peab arvesse maksimaalset rea allahindluse **summa väärtust, mis on määratud kasutajale kassa loagrupis**.

## <a name="line-discount-percent"></a>Rea allahindluse protsent

Rea **allahindluse protsendi toiming** võimaldab müügikoha kasutajatel kandes rea kaubale allahindluse protsendi sisestada. See toiming rakendub ainult allahinnatavatele kaupadele ja see peab arvesse maksimaalse rea allahindluse protsendi väärtust, mis on määratud kasutajale kassa **loagrupis**.

## <a name="total-discount-amount"></a>Lõppallahindluse summa

Lõppallahindluse **summa** toiming võimaldab müügikoha kasutajatel sisestada kandele allahindluse summa. See toiming rakendub ainult allahinnatavatele kaupadele ja see peab arvesse maksimaalset lõppallahindluse summa väärtust, mis on määratud kasutajale kassa **loagrupis**. Kui sisestatud allahindluse summa ületab maksimaalse lõppallahindluse summa, siis toiming on blokeeritud ja õiguse alistamise voogu ei käivitata. Praegu ei saa lõppallahindluse summat rakendada ostukorvile, kus on müügiüksuste ja tagastatud kaupade segamine.

## <a name="total-discount-percent"></a>Lõppallahindluse protsent

Lõppallahindluse **protsendi** toiming võimaldab müügikoha kasutajatel kandele allahindluse protsendi sisestada. See toiming rakendub ainult allahinnatavatele kaupadele ja see peab arvesse maksimaalset lõppallahindluse protsendi väärtust, mis on määratud kasutajale kassa **loagrupis**. Kui sisestatud allahindluse protsent ületab maksimaalse lõppallahindluse protsendi, siis toiming on blokeeritud ja õiguse alistamise voogu ei käivitata. Praegu ei saa lõppallahindluse protsenti rakendada ostukorvile, kus on müügiüksuste ja tagastatud kaupade segamine.

## <a name="remove-system-discounts-from-transaction"></a>Eemalda kandest süsteemi allahindlused

Kandetoimingust **süsteemi allahindluste** eemaldamine võimaldab kassa kasutajatel kandest kustutada kõik rakendatud süsteemi allahindlused (sh kupongipõhised allahindlused). Pärast selle toimingu sooritamist hakkab hinnakujundusmootor välistama süsteemi allahindlused allahindluse arvutamise ulatusest. Kandetoimingust **süsteemi allahindluste** eemaldamine ei eemalda käsitsi allahindlusi.

## <a name="reapply-system-discounts"></a>Rakenda süsteemi allahindlused uuesti

Süsteemi **allahindluste** **uuesti rakenduse toiming võimaldab kassa kasutajatel süsteemi arvutatud allahindlused kandele uuesti kõrvaldada, kui allahindlused eemaldati, kasutades selleks funktsiooni Eemalda süsteemi allahindlused kande toimingust**. Pärast selle toimingu sooritamist hakkab hinnakujundusmootor kaasama allahindlusarvutuse ulatusesse kõik süsteemi allahindlused.

## <a name="add-coupon-code"></a>Lisa kupongikood

Kupongikoodi **lisamise** toiming võimaldab müügikoha kasutajatel lisada kandele kupongi, sisestades kupongikoodi. Teise võimalusena saavad müügikoha kasutajad skannida kupongi vöötkoodi või sisestada selle, kasutades numbriklaviatuuri tehingute **ekraanil**.

## <a name="remove-coupon-code"></a>Kupongikoodi eemaldamine

Kupongikoodi **eemaldamise toiming** võimaldab kassa kasutajatel valida ja eemaldada ühe või mitu kupongi, mida praegu kandele rakendatakse.

## <a name="recalculate"></a>Arvuta uuesti

Ümberarvutamise **toiming võimaldab** kassa kasutajatel käivitada nõudmisel hinnakujunduse arvutuse. See toiming on vajalik, kui hinnalukk ja/või hilinenud hinnakalkulatsioon on lubatud ning müügikoha kasutaja soovib hinnad ja allahindlused pärast ostukorvi või tellimuse muudatusi uuesti arvutada. Ümberarvutamistoiming **arvutab** alati kogu tellimuse ümber. Seda ei saa kasutada valitud müügiridade ümberarvutamiseks. Käsitsi allahindluste rakendamiseks lukustatud müügireale kassas peavad **müügikoha** kasutajad esmalt kasutama toimingut Arvuta uuesti, et vabastada kõik müügiread.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
