---
title: Lehekülje mudeli sõnastik
description: See teema kirjeldab erinevaid elemente, mida kasutatakse rakenduse Microsoft Dynamics 365 Commerce saidi lehtedel.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2225bdca654e164d97feec7848f077f54054b37f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257095"
---
# <a name="page-model-glossary"></a>Lehemudeli sõnastik


[!include [banner](includes/banner.md)]

See teema kirjeldab erinevaid elemente, mida kasutatakse rakenduse Microsoft Dynamics 365 Commerce saidi lehtedel.

## <a name="page-element-definitions"></a>Lehekülje elemendi definitsioonid

Järgmine tabel näitab kokkuvõtet tingimustest, mida peaksite tundma, kui muudate oma saidi välimust, olemust ja sisu. Põhjalikumate selgituste ja protseduuride jaoks järgige linke.

| Mõiste | Kirjeldus ja märkmed |
|------|-----------------------|
| [Moodul](work-with-modules.md) | <p>**Definitsioon:** moodulid on koosteüksus, mida saab luua ja mis moodustavad veebilehe raamistiku. Näidete hulka kuuluvad päise, põhiväärtuse ja karusselli moodulid.</p><p>**Kus see on valitud:** juurutatud mooduleid on võimalik valida ja konfigureerida saidi loomise töövoo erinevatel etappidel, nagu mall, küljendus, lehekülg ja fragmendi loomise etapid.</p><p>**Kui see on redigeeritud:** kohandatud moodulid luuakse koodiga, kasutades tarkvara arenduse komplekti (SDK). Seejärel laaditakse need üles saidile, kus need muutuvad valikuks kättesaadavaks.</p> |
| Mooduli atribuut | <p>**Definitsioon:** mooduli atribuudid on konkreetsed sätted, mis on moodulis määratletud. Neid saab redigeerida e-kaubanduse autorluse tööriistade abil. Näiteks mooduli atribuute kasutatakse ribareklaami mooduli pealkirja ja taustpildi määramiseks.</p><p>**Kus see on konfigureeritud:** mooduli atribuudid on valitud ja konfigureeritud atribuutide paanil, mis kuvatakse mallide, paigutuste, lehtede, fragmentide ja rakenduse sätete loomise keskkonnas (redaktorid).</p> |
| [Mall](templates-layouts-overview.md) | <p>**Definitsioon:** mallid määratlevad mooduli kombinatsioonid ja valikud, mida tuleks kasutada lehtede kategooria puhul (nt turunduse lehed, kategooria lehed ja toote lehed).</p><p>**Kus see on valitud:** malle saab valida lehe või paigutuse loomise töövoogude ajal.</p><p>**Kus seda redigeeritakse:** malle luuakse malli redaktoris. Nende loomiseks või muutmiseks pole vaja koodi.</p> |
| [Paigutus](templates-layouts-overview.md) | <p>**Definitsioon:** paigutused määratlevad põhimalli valikute kogumite lõpliku valiku ja paigutuse. Paigutust saab konfigureerida ühele lehekülje jaoks (*kohandatud paigutus*) või seda saab jagada mitme leheküljega (*eelhäälestatud paigutus*).</p><p>**Kus see on valitud:** paigutusi saab valida uue lehekülje loomise ajal või kui olemasoleva lehe jaoks on vaja teistsugust paigutust.</p><p>**Kus seda redigeeritakse:** paigutusi luuakse paigutuse redigeerijas. Nende loomiseks või muutmiseks pole vaja koodi.</p> |
| [Lehekülge eksemplar](modify-existing-page.md) | <p>**Definitsioon:** lehekülje eksemplarid määratlevad ühe lehekülje lõpliku, leheküljele vastava lokaliseeritud sisu. See sisu tuletatakse mooduli atribuutide väärtustest.</p><p>**Kus see on valitud:** leheküljed valitakse URL-ide määramisel.</p><p>**Kus seda redigeeritakse:** lehekülgi redigeeritakse lehekülje redigeerijas. Nende loomiseks või muutmiseks pole vaja koodi.</p> |
| [Kujundus](select-site-theme.md) | <p>**Definitsioon:** teemad määratlevad kaskaadlaadilehe (CSS) ja määratlevad lehel renderdatud moodulite ilme ja olemuse.</p><p>**Kui see on valitud:** pärast teema üleslaadimist saidile, kasutades rakenduse Microsoft Dynamics Lifecycle Services (LCS), saab seda valida lehe konteineri mooduli atribuudina.</p><p>**Kus seda redigeeritakse:** teemasid luuakse ja redigeeritakse praegu SDK abil. Seejärel laaditakse need LCS-i abil saidile üles.</p> |
| [Fragment](work-with-fragments.md) | <p>**Definitsioon:** fragmendid on täielikult konfigureeritud moodulid, millel on lokaliseeritud sisu, mida saab taaskasutada ja mida saab keskselt värskendada mitmel leheküljel. Näiteks saab päise moodulist loodud fragmenti kasutada kõigil mallidel ja kõigil teie saidil olevatel lehekülgedel ja ühes kohas keskselt uuendada.</p><p>**Kus see on valitud:** fragmente saab valida seal, kus saab valida mooduleid. Neid saab asendada mooduliga, mis aitab suurendada tõhusust korduvkasutatavate ja tsentraliseeritud autorluse kaudu.</p><p>**Kus seda redigeeritakse:** fragmente redigeeritakse fragmendi redaktoris. Nende loomiseks või muutmiseks pole vaja koodi.</p> |
| [URL](create-page-URL.md) | <p>**Definitsioon:** universaalsed ressursilokaatorid (URL-id) on aadressid, mis viitavad veebilehtedele või teistele URL-idele.</p><p>**Kus see on valitud:** URL-id valitakse, kui nõutud on lingid lehekülgede vahel.</p><p>**Kus seda redigeeritakse:** URL-e redigeeritakse URL-i redaktoris. Nende loomiseks või muutmiseks pole vaja koodi.</p> |
| Vara | <p>**Definitsioon:** varad on faili kahendfailid, millel on laiend, nagu .jpg, .docx, .PDF või .mpg.</p><p>**Kus see on valitud:** varad valitakse mooduli atribuutidena moodulite jaoks, mis neid nõuavad.</p><p>**Kus seda redigeeritakse:** varad laaditakse üles ja seotud metaandmeid redigeeritakse vara halduris.</p> |

## <a name="additional-resources"></a>Lisaressursid

[Sisu lisamise viisid](add-manage-content.md)

[Dokumendi olekud ja töötsükkel](document-states-overview.md)

[Avaldamisrühmadega töötamine](publish-groups.md)

[Kanaliülese ühiskasutuse lubamine ja kasutamine](cross-channel-sharing.md)

[Moodulitega töötamine](work-with-modules.md)

[Fragmentidega töötamine](work-with-fragments.md)

[Mallide ja paigutuste ülevaade](templates-layouts-overview.md)

[Saidil navigeerimise kohandamine](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]