---
title: Hoolduslepete ja projektide integreerimine
description: Hoolduslepete ja hooldusleppe ridadega töötamisel saate kasutada jaotise Projektihaldus ja raamatupidamine osades seadistatud andmeid.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77b61c0b9d48557e25ec5aec43dd6546605d35b6fa2ac810d55b3333a8f00289
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720153"
---
# <a name="integration-for-service-agreements-and-projects"></a>Hoolduslepete ja projektide integreerimine 

[!include [banner](../includes/banner.md)]


Hoolduslepete ja hooldusleppe ridadega töötamisel saate kasutada jaotise **Projektihaldus ja raamatupidamine** järgmistes osades seadistatud andmeid.

## <a name="project-prices"></a>Projekti hinnad

Hooldusleppe kande omahind ja müügihind saadakse omahinna seadistusest, mis rakendub hooldusleppega seotud projektile. Omahinna ja müügihinna saab seadistada projekti, töötaja või kategooria alusel. 

## <a name="project-validation"></a>Projekti kontrollimine

Hooldusleppe real valimiseks saadaval olevaid projekte, töötajaid ja kategooriaid saab limiteerida kontrolli seadistamisega jaotises **Projektihaldus ja raamatupidamine**. Kontrolli seadistamise abil saate juurdepääsu juhtimiseks kombineerida töötajaid, projekte ja kategooriaid. 

## <a name="project-line-properties"></a>Projektirea atribuudid

Rea atribuut sisestatakse automaatselt hooldusleppe reale.

Rea atribuudid luuakse **Projektihalduse ja raamatupidamise** vormil **Rea atribuudid**. Hooldusleppesse sisestatud rea atribuut seotakse hooldusleppe jaoks valitud projektiga ja seejärel tuletatakse hooldusleppe realt. 

## <a name="default-offset-accounts"></a>Vaikevastaskontod

Kui sisestate kulukande, valitakse selle kande jaoks automaatselt kulu vaikevastaskonto. Kulu vaikevastaskonto seadistatakse praeguse hooldusleppega seotud projekti kohta.

## <a name="project-categories"></a>Projekti kategooriad

Hooldusleppe ridade jaoks saadaval olevad kategooriad saate seadistada **Projektihalduse ja raamatupidamise** vormil **Projekti kategooriad**. 

> [!NOTE]
> <P>Valimiseks on saadaval kategooriad, mille puhul on valitud märkeruut <STRONG>Aktiivne töölehtedel</STRONG> vahekaardil <STRONG>Projekt</STRONG> vormil <STRONG>Projekti kategooriad</STRONG>. Ent kui on valitud märkeruut <STRONG>Passiivsed kategooriad</STRONG> vahekaardil <STRONG>Töölehed</STRONG> vormil <STRONG>Projektihalduse ja raamatupidamise parameetrid</STRONG>, on kõik kategooriad valimiseks saadaval.</P>

## <a name="project-parameters"></a>Projekti parameetrid

Kui valitud on märkeruut **Töötajad, kellega on leping lõpetatud** vahekaardil **Töölehed** vormil **Projektihalduse ja raamatupidamise parameetrid**, saate passiivseid ja aktiivseid töötajaid valida vormidel **Hoolduslepped** ja **Hooldustellimused**.

Samuti saate lubada väljad **Algusaeg** ja **Lõppaeg** vahekaardil **Projekt** vormil **Hooldustellimused**, et sisestada hooldustellimuse ridadele algus- ja lõppaeg.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>Hooldustellimuste algus- ja lõppaja funktsiooni lubamine

1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Projektihalduse ja raamatupidamise parameetrid**.

2.  Klõpsake vahekaarti **Töölehed** ja seejärel valige märkeruut **Näita algus-/lõppaegu**.

3.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Töölehed** \> **Töölehenimed**.

4.  Valige hooldustellimusega seotud töölehe nimi.

5.  Klõpsake vahekaarti **Üldine** ja seejärel valige märkeruut **Näita algus-/lõppaegu**.


> [!NOTE]
> <P>Valige hooldustellimuse töölehe nimi väljal <STRONG>Tund</STRONG> vahekaardil <STRONG>Töölehed</STRONG> vormil <STRONG>Teenuste halduse parameetrid</STRONG>.</P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]