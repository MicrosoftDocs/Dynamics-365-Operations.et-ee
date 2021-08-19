---
title: Standardkuludega koosluse kalkulatsioonides kasutatud teave
description: Koosluse kalkulatsioonid kasutavad toodetud kauba standardkulu kalkuleerimiseks erinevate allikate andmeid. Allikad hõlmavad teavet kaupade, protsesside, kaudsete kulukalkulatsioonide valemite ja kuluversiooni kohta.
author: AndersGirke
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26d5590943ece1480e11a17a684cd7ec8cbaae451ddd5e0407bc72576ae53055
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731861"
---
# <a name="information-used-in-bom-calculations-with-standard-costs"></a>Standardkuludega koosluse kalkulatsioonides kasutatud teave

[!include [banner](../includes/banner.md)]

Koosluse kalkulatsioonid kasutavad toodetud kauba standardkulu kalkuleerimiseks erinevate allikate andmeid. Allikad hõlmavad teavet kaupade, protsesside, kaudsete kulukalkulatsioonide valemite ja kuluversiooni kohta.

Standardkulu koosluse kalkulatsioonis kasutatav ostetud kauba teave sisaldab järgmist:
-   Kulu – ostetud kauba kulud salvestatakse standardkulude kuluversioonis tegevuskohapõhiste kulukirjetena. Igal kulukirjel on kehtiv kuupäev ja koosluse kalkulatsiooni kuupäev määratleb kasutatavad kulukirjed. Näiteks võib tulevase kuupäevaga koosluse kalkulatsioon kasutada ootel oleku ja tulevase kuupäevaga kulukirjet.
-   Kulugrupp ? ostetud kaubale määratud kulugrupp sisaldab kulu segmenteerimise alustaset toodetud kauba kalkuleeritud kuludes.
-   Kauba koosluse kalkulatsioonigrupile manustatud hoiatustingimused võimaldavad koosluse kalkulatsioonil tuvastada võimalikke probleeme. Sellised olukorrad on näiteks, kui ostetud kaubal on nullkulu, koosluses on nullkogus või kulukirje on aegunud. Kohanduvad hoiatustingimused saab koosluse kalkulatsiooni algatamisel tühistada.

Standardkulu koosluse kalkulatsioonis kasutatav toodetud kauba teave hõlmab järgmist:
-   Varude standardtellimuse kogus – kauba standardtellimuse kogus varude puhul toimib kui amortiseerivate püsikuludele saatepartii suuruse vaikearvestus koosluse kalkulatsioonis. Saatepartii suuruse arvestus kajastab ka tellimuse koguse kordsust, kui see on määratud.
-   Kauba koosluse kalkulatsioonigrupile manustatud hoiatustingimused võimaldavad koosluse kalkulatsioonil tuvastada võimalikke probleeme. Näide: toodetud kaubal ei ole kooslust või protsessi. Kohanduvad hoiatustingimused saab koosluse kalkulatsiooni algatamisel tühistada.

Standardkulu koosluse kalkulatsioonis kasutatav koosluse teave hõlmab järgmist:
-   Koosluse versioon ? toodetud kaubaga seotud koosluse versioonil on kehtivad algus- ja lõppkuupäevad ning kinnitatud ja aktiivne olek. Kooslus võib olla ettevõtet hõlmav või laoalapõhine ning see võib valikuliselt kajastada koguse katkestuspunkte.
-   Koosluse rea kauba kogus ? komponendil on nõutav kogus tavaliselt erinev, kuid see võib olla ka konstantne. Komponendi kogus väljendatakse tavalist ühe emaühiku tootmiseks, kuid see võidakse kuvada ka 100 või 1000 kohta kümnendarvu täpsusega käsitlemiseks. Komponendi kogust saab kalkuleerida ka mõõtühikutel põhinevalt.
-   Koosluse rea kauba praak ? komponendil võib planeeritud praagi jaoks olla erinev või konstantne kogus.
-   Koosluse rea kauba kehtiv kuupäev ? komponendil võivad olla kehtivad algus- ja lõppkuupäevad.
-   Koosluse rea kauba tootmistüüp – amortiseerivate püsikulude saatepartii suuruse omahinna arvutamine kajastab koosluse kalkulatsiooni kogust ja tellimise koosnevusrežiimi, sest koosluse kalkulatsioon eeldab, et komponente toodetakse täpses koguses.
-   Toodetud komponendi alamkooslus ? alamkomponendil võib valikuliselt olla määratud koosluse versioon, mida kasutatakse kauba praeguse aktiivkoosluse versiooni asemel koosluse versioonis.
-   Toodetud komponendi alamprotsess ? toodetud komponendil võib valikuliselt olla määratud protsessi versioon, mida kasutatakse kauba praeguse aktiivprotsessi versiooni asemel koosluse versioonis.
-   Operatsiooni number ja operatsiooni praagi protsendimäära mõju ? operatsiooni number lingib komponendi määratud operatsioonile ja operatsioonidel võib olla praagi protsendimäär. Linkimine võimaldab koosluse kalkulatsioonidel arvestada komponendi nõutud koguse praagi protsendimäärasid ja kumulatiivseid praagi protsendimäärasid mitmes operatsioonis.
-   Koosluse rea kauba eiramine kulukalkulatsioonides ? komponenti saab koosluse kalkulatsiooni eesmärkidel eirata.

Standardkulu koosluse kalkulatsioonis kasutatav operatsiooniressursi teave hõlmab järgmist.
-   Tunnikulud – operatsiooniressursiga seotud tunnikulusid väljendatakse kulukategooriatena, mis on määratud kellaaja ja käitusaja seadistamiseks. Need kulukategooriad peavad olema ressursigruppide ja operatsiooniressursside jaoks identifitseeritud. Kulukategooriaga seostatud tunnikulud võivad olla tegevuskohapõhised või ettevõtteülesed.
-   Kulud ühiku kohta – mõni tootmiskeskkond määrab operatsooniressursi kulud väljundi ühiku kohta, mida väljendatakse koguse puhul erineva kulukategooriana. Näiteks võivad kogusepõhised kulud kajastada tükipalga määra või võib värvitootja määrata operatsiooniressursi kulud väljundi galloni kohta.
-   Operatsiooniressursi teabe tühistamine protsessi operatsioonides – ressursiteave kulukategooriate kohta tuletatakse operatsioonidega, kus selle saab tühistada. Koosluse kalkulatsioonid kasutavad kulukategooria teavet, mis on määratud protsessi operatsioonides.
-   Kulugrupp kulukategooriale ? kulukategooriale määratud kulugrupp sisaldab kulu segmenteerimist toodetud kauba kalkuleeritud kuludes. Näiteks võib erinevaid kulugruppe kasutada kalkuleeritud kulude (mis on seotud masinate ja tööga või häälestuse ja käitusajaga) segmentimiseks.

Standardkulu koosluse kalkulatsioonis kasutatav protsessi teave hõlmab:
-   Protsessi versioon ? toodetud kaubaga seotud protsessi versioonil on kehtivad algus- ja lõppkuupäevad ning kinnitatud või aktiivne olek. Protsessi versioon peab olema laoalapõhine ja see võib valikuliselt kajastada koguse katkestuspunkte.
-   Protsessi operatsiooni aeg ? aja saab määrata nii käitusajale kui häälestuse ajale. Tunniaega väljendatakse tavaliselt ühe emaühiku tootmiseks, kuid seda võib väljendada ka 100 või 1000 kohta kümnendarvu täpsusega käsitlemiseks.
-   Protsessi operatsiooniaeg teiseste ressursside puhul – teisesel ressursil on sama operatsiooninumber, mis peamisel ressursil ning sama protsessi operatsiooniaeg. Näiteks võib operatsioon nõuda peamiseks ressursiks masinat ning teisesteks ressurssideks tööjõudu ja tööriistu.
-   Protsessi operatsiooni praagi protsendimäär – koosluse kalkulatsioonid arvestavad praagi protsendimäärasid ja kumulatiivseid praagi protsendimäärasid mitmes operatsioonis. See kehtib protsessi operatsioonide jaoks nõutavale ajale ja operatsiooninumbritega lingitud komponentide nõutavale kogusele.
-   Kulukategooriad protsessi operatsiooni kohta – operatsiooniressursi teave kulukategooriate kohta tuletatakse operatsioonidega, kus selle saab tühistada. Koosluse kalkulatsioonid kasutavad kulukategooria teavet, mis on määratud protsessi operatsioonides.

Standardkulu koosluse kalkulatsioonis kasutatav üldkulude teave hõlmab:
-   Lisatasu ? lisatasu kalkuleerimise valem kajastab protsendi väärtust, nt 100 protsenti, mis on seotud määratud kulugrupiga (nt tööjõud).
-   Määr ? määra kalkuleerimise valem kajastab ühiku summat, nt 10,00 USA dollarit tunni kohta, mis on seotud määratud kulugrupiga (nt tööjõud).
-   Ajapõhine vs materjalipõhine üldkulu ? tootmise üldkulu võib olla seotud protsessi operatsioonidega või materjali komponentidega.

Standardkulu koosluse kalkulatsioonis kasutatav kulu versiooni teave hõlmab:
-   Kulu tüüp ? kulu versioon peab sisaldama standardkulusid. Mitmed piirangud kohanduvad koosluse kalkulatsioonides, mis kasutavad standardkulusid. Näiteks määravad need piirangud lisakulude kaasamise ühiku kuludesse ja koosluse kalkulatsiooni tormilise arengu režiimi olemise ühetasemelisena.
-   Kohustuslik taande põhimõte ? kuluversioon võib taande põhimõtte kasutamise kohustuslikuks muuta, nt määratud kuluversiooni või aktiivse kulukirje kasutamine. Kohustuslik taande põhimõte rakendub tavaliselt kuluversioonile, mis esindab järk-järgulisi uuendusi kaheversioonilises lähenemises kulu uuendustele.
-   Ootel kulude blokeeriv lipp ? blokeeriv lipp võib ennetada toodetud kaupade ootel kulude koosluse kalkulatsioone.
-   Määratud alguskuupäev ? määratud alguskuupäev toimib vaikimisi kalkulatsiooni kuupäevana kõikidele koosluse kalkulatsioonidele, mis hõlmavad kuluversiooni.
-   Määratud laoala ? määratud laoala piirab koosluse kalkulatsioone ühele laoalale.
-   Kuluversiooni sisu peab sisaldama kulusid ? sisu peab sisaldama kulusid. Valikuliselt võib see sisaldada ka müügihindasid soovitatud müügihindade kalkuleerimiseks toodetud kaupadele.

Mitmed teabeallikaid saab määrata koosluse kalkulatsiooni algatamisel. See sisaldab laoala, kalkulatsiooni kuupäeva ja kuluversiooni.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]