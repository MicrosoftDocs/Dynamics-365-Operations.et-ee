---
title: TDS-i arvutamine arvetel vabas vormis arve lehelt
description: See teema kirjeldab, kuidas arvutada arvetel allika järgi mahaarvatud maks (TDS), kasutades vabas vormis arvelehte.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: c543876c48eca55eaaa6fd67585ec357dfea276ffbf8abad3c28c6f4cf29f782
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750360"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>TDS-i arvutamine arvetel vabas vormis arve lehelt

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas arvutada arvetel allika järgi mahaarvatud maks (TDS), kasutades **vabas vormis arvelehe** lehte.

1. Avage **Müügireskontro \> Arved \> Kõik vabas vormis arved**.

    [![Vabas tekstis arve leht.](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Tehke valik **Uus**, et luua maksetööleht, ja sisestage seejärel nõutavad üksikasjad.
3. Vaadake hankija või kliendi hinnalepete kategooria olemust **Arve** vahekaardil, **Kinnipeetava maksu** väljagrupis ja **Hinna hindamise** väljal.
4. Väljal **TDS grupp** vaadake või muutke hankijale või kliendile määratud vaikimisi TDS-i gruppi.

    > [!NOTE]
    > Väli **TCS-grupp** ei ole saadaval, kui valite TDS-grupi väärtuse **TDS-grupp** väljal. TDS arvutatakse ainult siis, kui on märgitud **Arvuta kinnipeetav maks** valik **Jah** klientide jaoks **Kõik kliendid** lehel.

5. Vahekaardil **Maksuteave**, **Ettevõtte teave** jaotises **Nimi** väljal valige ettevõtte nimi, mis on seadistatud alternatiivse aadressi jaoks.

    **Kinnipeetava maksu** jaotises kuvatakse väljal **Maksukonto number (TAN)** väljal kuvatakse valitud ettevõtte maksukonto number (TAN).

6. Looge kaubaread vahekaardil **Arve read** ja sisestage nõutavad üksikasjad.

    **Kinnipeetava maksu grupi** jaotises näitab väli **Maksukonto number (TAN)** väljal näitab TANi ja **TDS-grupp** väli TDS-gruppi.

7. Valige **Kinnipeetav maks**, et avada **Kinnipeetava maksu kannete** leht. Selle lehekülje ülemisel osal on järgmised väljad:

    - **Kinnipeetava maksu summa kokku** - TDS-grupi kande jaoks arvutatud TDS-i kogusumma.
    - Väljal **Väärtus** - Kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent. Koguprotsent põhineb valemil, mis on määratud TDS-grupiga seotud TDS-i maksukoodide jaoks.
    - **Korrigeeritud kinnipeetava maksu summa kokku** - TDS-i grupi kõikide maksukoodide korrigeeritud TDS-i kogusumma.
    - **TDS** – valitud märkeruut näitab, et TDS-grupp on kandega seotud.

    Välja **Ülevaade**, **Üldine**, ja **Summa** vahekaardil kinnipeetava maksu kannete lehel kuvatakse TDS-summa ja korrigeeritud TDS-i summa TDS-i grupiga seotud TDS-i maksukoodi kohta.

8. Valige **Lävi** et avada leht **Lävi** kus saate üle vaadata läve piirmäära, mis on määratud konkreetse TDS-maksukoodiga seotud TDS-i maksukomponendile.
9. Valige **Valemikoostur** et avada **Valemikoosturi leht** kus saate üle vaadata TDS-i maksukoodi jaoks määratud valemi.
10. Vabas vormis arve sisestamine. Müügiarvetel arvutatud TDS-summa sisestatakse tasumisele kuuluvale kontole, mis on määratud igale TDS-i maksukoodile TDS-grupis. TDS-i maksukoodide ostureskontro või müügireskontrod määratletakse **Kinnipeetava maksu koodide** lehel.
11. Valige **Sisestatud kinnipeetav maks**, et avada **Kinnipeetava maksu kannete** leht. Väljal **Väärtus** kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent.

    Vahekaartide **Ülevaade** **Üldine** ja **Summa** väljadel kuvatakse arveridadel arvutatud TDS-summad.

12. Vaadake TDS-i kalkulatsiooniteavet iga TDS-grupiga seotud TDS-i maksukoodi kohta.
