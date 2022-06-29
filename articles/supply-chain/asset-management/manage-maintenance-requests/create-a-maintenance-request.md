---
title: Hooldusnõuete loomine
description: See artikkel selgitab, kuidas varahalduses hooldustaotlust luua.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 92f3a2bc3d2a4d5d1c3be0c6dda2674dc3e7d0bb
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016822"
---
# <a name="create-maintenance-requests"></a>Hooldustaotluste loomine

[!include [banner](../../includes/banner.md)]

 

Hooldustaotlusi saab kasutada juhul, kui hooldustöötajad või tootmistöötajad avastavad, et seadmed vajavad parandamist, kuid parandustööd ei saa kohe ära teha.

**Näide:** kui hooldustöötaja teeb remonti ja avastab, et samal aadressil peab hooldama ka teist vara. Hooldustöötajal ei ole aga aega ega vajalikke varuosi parandustöö jaoks. Seetõttu loob ta vara hooldustaotluse ja sisestab probleemi lühikirjelduse.

Paani **·** **Seotud** teave aktiivse hoolduse taotlused, mis **asub** **lehe** Kõik varad või Aktiivsed varad paremal pool (**Varade** \> **·** \> **·** **haldus Kõik varad või Aktiivsed** varad), kuvatakse valitud varale lisatud aktiivse hoolduse taotlused.

1. Valige **varahalduse hooldustaotlused** \> **·** \> **Kõik hooldustaotlused või** aktiivse hoolduse **taotlused.**
2. Valige suvand **Uus**.
3. Dialoogiboksis **Loo taotlus** väljal **Hoolduse taotluse tüüp** valige hooldustaotluse tüüp. Soovitatakse vaiketüüpi.
4. Väljale **Kirjeldus** sisestage nimi või pealkiri, mis kirjeldab lühidalt hooldustaotlust.
5. Väljadel **Funktsionaalne asukoht** ja **Vara** valige funktsionaalne asukoht või vara või funktsionaalse asukoha ja vara kombinatsioon, nii nagu soovite. Hooldustaotlust saate luua ilma vara valimata ja vara saab hooldustaotlusele hiljem lisada. Kui hooldustöötaja, kes on sisse logitud, on seotud varaga seotud ressursiga, sätestatakse väli **Vara** automaatselt.

    Kui hoolduspäring on valitud varale juba manustatud, kuvatakse dialoogiboksi **Loo taotlus** ülaosas teateriba, mis teavitab teid olemasoleva hooldustaotluse ID-st. Sõnumiriba teavitab teid ka sellest, kas varal on garantiileping.

6. Valige väljal **Hooldustase** teenuse tase, mis näitab taotluse kiireloomulisust.
7. Kui valisite vara 5. etapis, saate kasutada välju **Vea sümptom**, **Vea ala** ja **Vea tüüp**, et luua vea registreerimine.
8. Kui hooldustaotlus on põhjustanud hoolduse seisakuaja, sisestage seisakuaja alguskuupäev ja kellaaeg.

    Väljale **Alustaja** lisatakse automaatselt teie nimi.

10. Väljale **Päringu kuupäev** lisatakse automaatselt praegune kuupäev. Saate selle välja väärtust siiski muuta.
11. Sisestage väljale **Märkmed** kõik nõutavad täiendavad märkused.
12. Valige nupp **OK**.

![Hooldusnõude loomine.](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Hoolduse taotluste hilisem töötlemine

Kui hooldustaotlus on loodud, kuid see on enne teisendatud töötellimuseks, tuleks sellel värskendada mitmesuguseid andmeid. Tavaliselt täidab selle ülesande plaanija või mõni muu administratiivtöötaja.

- Lehel **Kõik hooldustaotlused** või **Aktiivsed hooldustaotlused** valige taotlus töötamiseks ja seejärel valige **Redigeeri**.

Üksikasjade vaates saate värskendada mitmesugust teavet. Järgmisena on toodud mõned näited.

- Vara valimine ja kinnitamine. Kui peate hiljem valima mõne muu vara, valige suvandi **Vara kinnitatud** väärtuseks **Ei**.
- Valige vastutustundlik hooldustöötajate rühm ja/või vastutustundlik hooldustöötaja. Nõutava seadistuse kohta lisateabe saamiseks vaadake teemat [Vastutustundlikud hooldustöötajaid](../setup-for-maintenance-requests/responsible-workers.md).
- Valige hooldustöö tüüp ja kui see teave on asjakohane, seotud hooldustöö variant ja töökaubandus.
- Väljadele **Laius** ja **Pikkus** sisestage geograafilised koordinaadid. Kõik hooldustaotlusele lisatud koordinaadid kantakse automaatselt üle seotud töötellimusele. 

![Hooldustaotluse uuendamine.](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Kui valite hooldustaotluse loomisel vara, saate sellele varale lisada ühe vea. Pärast hooldustaotluse loomist saate lisada rohkem vigu, kui vajate. Vigade lisamiseks valige **Vara viga** lehel **Kõik hoolduspäringud**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]