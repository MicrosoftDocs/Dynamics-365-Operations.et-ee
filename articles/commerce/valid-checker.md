---
title: Kaupluse kannete kinnitamine väljavõtte arvutamiseks
description: Selles artiklis kirjeldatakse kaupluse kannete kinnitamist Microsoft Dynamics 365 Commerce'is.
author: analpert
ms.date: 01/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4be40189777a37495f185467050b61af47b684d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890509"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Kaupluse kannete kinnitamine väljavõtte arvutamiseks

[!include [banner](includes/banner.md)]

Selles artiklis kirjeldatakse kaupluse kannete kinnitamist Microsoft Dynamics 365 Commerce'is. Kinnitamisprotsess tuvastab ja märgib kanded, mis põhjustavad sisestustõrkeid, enne kui väljavõtte sisestusprotsess need tuvastab.

Kui proovite väljavõtet sisestada, võib kinnitamisprotsess kaubanduse kannete tabelites olevate andmete vastuolu tõttu nurjuda. Järgnevalt on toodud mõned näidistegurid, mis võivad põhjustada neid vastuolusid.

- Päisetabelis olev kande kogusumma ei kattu kande ridade kogusummaga.
- Päisetabelis määratletud üksuste arv ei ühti kandetabelis olevate üksuste arvuga.
- Päisetabeli maksud ei kattu ridade maksusummaga. 

Kui väljavõtte sisestamisprotsess laadib vastuolulised kanded, võivad loodavad müügiarved ja maksetöölehed põhjustada väljavõtte sisestamise protsessi nurjumise. Protsess **Kinnita kaupluse kanded** ennetab neid probleeme, võimaldades kande väljavõtte arvutusprotsessi ainult kande kinnitamisreeglid läbinud kannete edastamist.

Järgmine näide kujutab korduvaid päevaseid toiminguid kannete üleslaadimiseks, kannete kinnitamiseks ning kandeväljavõtete arvutamiseks ja sisestamiseks ning päeva lõpu toiminguid finantsaruannete arvutamiseks ja sisestamiseks.

![Näites kujutatakse korduvaid päevaseid toiminguid kannete üleslaadimiseks, kannete kinnitamiseks ning kandeväljavõtete arvutamiseks ja sisestamiseks ning päeva lõpu toiminguid finantsaruannete arvutamiseks ja sisestamiseks](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Kaupluse kande kinnitusreeglid

Pakktöötluse funktsioon **Kinnita kaupluse kanded** kontrollib kaubanduse kandetabelite järjepidevust järgmiste kinnitusreeglite alusel.

> [!NOTE]
> Kinnitusreeglite lisamist jätkatakse järgnevates väljaannetes.

### <a name="transaction-header-validation-rules"></a>Kande päise kinnitusreeglid

Järgmises tabelis esitatakse kande päise kinnitusreeglite loend, mida kontrollitakse jaemüügikannete päise suhtes enne nende kannete edastamist väljavõtete sisestamiseks.

| Reegel | Kirjeldus |
|-------|-------------|
| Ärikuupäev | See reegel kontrollib, kas kande ärikuupäev seostatakse pearaamatus avatud rahandusperioodiga. |
| Valuuta ümardamine | See reegel kontrollib, kas kande summad ümardatakse valuuta ümardamisreegli põhjal. |
| Kliendi konto | See reegel kontrollib, kas kandes kasutatav klient on andmebaasis olemas. |
| Allahindluse summa | See reegel kontrollib, kas päises olev allahindluse summa vastab ridadel olevate allahindluse summade kogusummale. |
| Finantsdokumendi sisestamise olek (Brasiilia) | See reegel kontrollib, kas finantsdokumendi sisestamine on võimalik. |
| Brutosumma | See reegel kontrollib, kas kande päises olev brutosumma vastab kande ridadel olevale netosummale koos maksu ning tasudega. |
| Neto | See reegel kontrollib, kas kande päises olev netosumma vastab kande ridadel olevale netosummale ilma maksuta ning koos tasudega. |
| Neto + maks | See reegel kontrollib, kas kande päises olev brutosumma vastab kande ridadel olevale netosummale ilma maksuta ning koos kõigi maksude ja tasudega. |
| Kaupade arv | See reegel kontrollib, kas kande päises määratletud kaupade arv ühtib kanderidadel olevate koguste summaga. |
| Maksesumma | See reegel kontrollib, kas kande päise maksesumma ühtib kõigi maksekannete summaga. |
| Maksuvabastuse arvutamine | See reegel kontrollib, kas tasuridade arvutatud summa ja maksuvabastuse summa võrdub algse arvutatud summaga. |
| Maksu sisaldav hind | See reegel kontrollib, kas lipp **Maks sisaldub hinnas** on kande päises ja kõigis maksukannetes kooskõlas. |
| Kanne pole tühi | See reegel kontrollib, kas kanne sisaldab ridu ja et vähemalt üks rida poleks tühistatud. |
| Ala-/ülemakse | See reegel kontrollib, ega päises oleva brutosumma ja maksesumma vahe ei ületa üle-/alamakse konfiguratsiooni maksimumi. |

### <a name="transaction-line-validation-rules"></a>Kanderea kinnitusreeglid

Järgmises tabelis esitatakse kanderea kinnitusreeglite loend, mida kontrollitakse jaemüügikannete rea üksikasjade suhtes enne nende kannete edastamist väljavõtete sisestamiseks.

| Reegel | Kirjeldus |
|-------|-------------|
| Vöötkood | See reegel kinnitab, kas kõik kanderidadel kasutatavad kauba vöötkoodid on andmebaasis olemas. |
| Tasuread | See reegel kontrollib, kas tasuridade arvutatud summa ja maksuvabastuse summa võrdub algse arvutatud summaga. |
| Kinkekaardi tagastused | See reegel kontrollib, ega kandes pole kinkekaartide tagastusi. |
| Kaubavariant | See reegel kinnitab, kas kõik kanderidadel kasutatavad kaubad ja kõik variandid on andmebaasis olemas. |
| Rea allahindlus | See reegel kontrollib, kas rea allahindluse summa vastab allahindluse kannete summale. |
| Rea maks | See reegel kontrollib, kas rea maksu summa vastab maksu kannete summale. |
| Negatiivne hind | See reegel kontrollib, ega kanderidadel ei kasutata negatiivseid hindu. |
| Kontrollitud seerianumber | See reegel kontrollib, kas seerianumber on seerianumbriga kontrollitavate üksuste puhul kandereal olemas. |
| Seerianumbri dimensioon | See reegel kontrollib, et seerianumbrit ei sisestataks, kui kauba seerianumbri dimensioon on passiivne. |
| Märgi vastuolu | See reegel kontrollib, kas koguse ja netosumma märk on kõigil kanderidadel sama. |
| Maksuvabastus | See reegel kontrollib, kas reaüksuse hinna ja maksuvabastuse summa võrdub algse arvutatud hinnaga. |
| Maksugrupi määramine | See reegel kontrollib, kas käibemaksugrupi ja kauba maksugrupi kombinatsioon loob kehtiva maksu lõikumiskoha. |
| Mõõtühiku teisendamised | See reegel kontrollib, kas kõikide ridade mõõtühikutel on kehtiv teisendus varude mõõtühikuks. |

## <a name="enable-the-store-transaction-validation-process"></a>Kaupluse kande kinnitusprotsessi lubamine

Seadistage töö **Kontrolli kaupluse kandeid** Commerce'i peakontoris regulaarseks käitamiseks (**Retail ja Commerce \> Retaili ja Commerce'i IT \> Kassa sisestamine**). Pakett-töö ajastatakse kaupluse organisatsiooni hierarhia alusel. Soovitame teil konfigureerida selle pakktöötluse nii, et see töötaks teie pakett-töödega **P-töö** ja **Kandeväljavõtte arvutamine** samal sagedusel.

## <a name="results-of-the-validation-process"></a>Kontrollimisprotsessi tulemused

Pakktöötluse **Kinnita kaupluse kanded** tulemusi saab kuvada igal jaemüügikaupluse kandel. Kandekirje väli **Kinnitamise olek** olekuks on määratud **Õnnestunud**, **Tõrge** või **Puudub**. Väljal **Viimase kinnitamise aeg** kuvatakse viimase kinnitamise kuupäev.

Järgmises tabelis kirjeldatakse kõiki kinnitamise olekuid.

| Kinnitamise olek | Kirjeldus |
|-------------------|-------------|
| Õnnestunud | Kõik lubatud kinnitusreeglid on edastatud. |
| Tõrge | Lubatud kinnitusreegel tuvastas tõrke. Saate tõrke kohta rohkem üksikasju kuvada, valides toimingupaanil **Kinnitamistõrked**. |
| Pole | Kande tüüp ei nõua kinnitusreeglite rakendamist. |

![Kaupluse kannete leht, kus kuvatakse kinnitamise oleku välja ja kinnitamistõrgete nuppu.](./media/valid-checker-validation-status-errors.png)

Kandeväljavõtetesse võetakse ainult need kanded, mille kinnitamise olek on **Õnnestunud**. Olekuga **Tõrge** kannete kuvamiseks vaadake üle tööruumis **Kaupluse finantsandmed** paan **Selvehulgimüügi kinnitamistõrked**.

![Tööruumi Kaupluse finantsandmed paanid.](./media/valid-checker-cash-carry-validation-failures.png)

Lisateabe saamiseks selle kohta, kuidas parandada selvehulgimüügi kinnitamistõrkeid, vaadake teemat [Selvehulgimüügi- ja kassahalduskannete redigeerimine ning auditeerimine](edit-cash-trans.md).

## <a name="additional-resources"></a>Lisaressursid

[Selvehulgimüügi- ja kassahalduskannete redigeerimine ning auditeerimine](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
