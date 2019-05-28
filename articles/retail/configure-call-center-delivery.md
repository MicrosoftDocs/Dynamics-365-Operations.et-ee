---
title: Kõnekeskuse tarneviiside ja -tasude konfigureerimine
description: Selles teemas kirjeldatakse, kuidas seadistada kõnekeskuse jaoks tarneviise ja -tasusid rakenduses Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 04/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2571b4ffd6c13dbf755ef2dfa93b757822890d96
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553595"
---
# <a name="configure-call-center-delivery-modes-and-charges"></a>Kõnekeskuse tarneviiside ja -tasude konfigureerimine

[!INCLUDE [banner](includes/banner.md)]

Kui rakenduses Microsoft Dynamics 365 for Retail tehakse müügitellimus ja müügitellimuse sisestanud isik on kõnekeskuse kanaliga seotud, siis kasutatakse tarneviisi kinnitamiseks ning tellimuse tasude arvutamiseks loogikaid ja reegleid.

Müügitellimuse loomisel saate valida tarneviisi müügitellimuse päisest ja müügitellimuse ridadest. Vaikimisi kasutatakse päisest valitud tarneviisi kõikidel müügitellimuse ridadel. Siiski saate vajaduse korral muuta vaike-tarneviisi igal müügireal eraldi. Saate määratleda tarneviisi ka kliendikirjel. Seejärel kasutatakse seda tarneviisi selle kliendi tellimuste loomisel müügitellimuse päises vaikimisi.

Rakendusel Retail on funktsioonid, mis võimaldavad kasutajatel piirata kanali kasutatavaid tarneviise, toote jaoks kasutatavaid tarneviise ja tarneviise, mis on sobivad vaid teatud tarne sihtkohtade jaoks. Tasusid saab määrata ka nii, et lisatasud lisatakse kliendi tellimusele olenevalt müügitellimuse jaoks valitud tarneviisidest ja tellimuse koguväärtusest.

## <a name="define-delivery-modes"></a>Tarneviiside määratlemine

Enne kui saate määratleda, milliseid tarneviise saab kõnekeskuse tellimuste jaoks kasutada, ja sätestada seotud reegleid ning tasusid, peate määratlema tarneviisid. Valige **Müük ja turundus \> Seadistamine \> Jaotus \> Tarneviisid**. Klõpsake valikut **Uus**, et luua uus tarneviis. Teine võimalus on valida loendist olemasolev tarneviis ja seejärel klõpsata käsku **Redigeeri**, et teha muutusi.

Väljale **Tarneviis** saate sisestada mis tahes tähe-või numbrimärkide kombinatsiooni teie ettevõtte nõuete kohaselt. Seejärel saate kasutada välja **Kirjeldus**, et sisestada täiendavat teavet. Väljad **Tasugrupp** ja **Kiirsaadetis** on valikulised ning neid kirjeldatakse hiljem selles teemas üksikasjalikult.

Lisage kiirkaardil **Jaemüügikanalid** ükskõik milline jaemüügi kanal, millele tuleks lubada tarneviisi kasutamist, kui selles kanalis luuakse müügikandeid.

Kiirkaardil **Tooted** saate määrata, milliste toodete ja/või tootekategooriate jaoks saab või ei saa tarneviisi kasutada. Näiteks kui toodet ei saa ohtlike materjalide piirangu tõttu õhu kaudu tarnida, siis eemaldage toode või tootekategooria kõikidelt tarneviisidelt, mis hõlmavad õhutransporti.

Kiirkaardil **Aadressid** saate määrata, milliste riikide, piirkondade või haldusüksuste jaoks saab või ei saa tarneviisi kasutada. Näiteks ei saa Hawaiile või Alaskale tarnitavate tellimuste puhul kasutada maatransporti. Seetõttu tuleb need osariigid välistada tarneviiside jaoks, milles kasutatakse maatransporti, kuid tuleb hõlmata tarneviiside jaoks, mis kasutavad õhutransporti.

## <a name="validate-delivery-modes-for-a-call-center-order"></a>Tarneviiside kinnitamine kõnekeskuse tellimuse jaoks

Pärast tarneviiside määratlemist peate käivitama pakett-töö **Tarneviiside töötlus**. See töö muudab tarneviisid saadavaks, nii et neid saab kasutada jaemüügikanalite müügitellimuste vormistamisel. Töö **Tarneviiside töötlus** käivitamiseks valige **Jaemüük \> Jaemüügi IT \> Tarneviiside töötlus**. See töö tuleb käivitada iga kord, kui jaemüügikanalile lisatakse uus tarneviis või muudetakse olemasolevaid tarneviiside/-kanalite seoseid.

Pärast pakett-töö **Tarneviiside töötlus** on lõpetanud, valige **Jaemüük \> Kanalid \> Kõnekeskused \> Kõik kõnekeskused**. Valige lehe **Kõik kõnekeskused** tegumiriba vahekaardil **Häälestamine** suvand **Tarneviisid**. Lehel **Tarneviisid** loetletakse kõik kehtivad tarneviisid valitud kõnekeskuse kanali jaoks. Olemasolevate tarneviiside redigeerimiseks või uute tarneviiside lisamiseks valige **Tarneviiside haldamine**. Pidage meeles, et töö **Tarneviiside töötlus** tuleb käivitada iga kord, kui on tehtud muudatusi.

## <a name="define-charges-for-delivery-services"></a>Tarneteenuste tasude määratlemine

Ettevõte võib soovida, et klientide müügitellimustele lisatakse vormistamisel tasud, mida arvutatakse tellimuse jaoks valitud tarneviisi põhjal automaatselt. Neid tasusid saab konfigureerida nii, et need oleksid ühesugused kõikide klientide ja tarneviiside jaoks. Või vastupidi – tasud võivad erineda olenevalt kliendist ja/või müügitellimuse jaoks valitud tarneviisidest.

Tasude määramiseks valige **Jaemüük \> Kanali häälestus \> Tasud \> Automaatsed tasud**. Uute tasude lisamiseks valige käsk **Uus**. Või valige olemasolev kirje ja seejärel käsk **Redigeeri**.

Tasusid saab määratleda nii, et need arvutatakse kas tellimuse päises või ridadel. Kasutage soovitud variandi valimiseks välja **Tase**.

Tasusid saab määratleda kindla kliendi, kliendigrupi või kõikide klientide jaoks. Valige väljalt **Konto kood** suvand **Tabel**, et määratleda tasusid, mida rakendatakse vaid teatud kliendile. Valige suvand **Grupp**, et määratleda tasud konkreetse kliendigrupi jaoks. Valige suvand **Kõik**, et rakendada tasud iga kliendi jaoks, kes vormistab müügitellimuse, mis kasutab seotud tarneviisi. Kui valisite väljal **Konto kood** suvandi **Tabel** või **Grupp**, siis valige klient või kliendigrupp väljalt **Konto seos**.

Tasusid saab konfigureerida nii, et neid rakendatakse kindla tarneviisi, tarneviiside grupi või kõikide tarneviiside jaoks. Kui valite väljal **Tarneviisi kood** suvandi **Tabel**, peate valima väljal **Tarneviisi seos** kindla tarneviisi. Kui valite suvandi **Grupp**, peate valima väljal **Tarneviisi seos** tarneviiside grupi. Tarneviiside gruppe saate määratleda, kui valite **Jaemüük \> Kanali häälestus \> Tasud \> Tarne lisakulude grupp**. Seejärel saab neid lehe **Tarneviisid** kaudu siduda ühe või enama tarneviisiga. Kui valite tasude määratlemisel grupi, siis kasutavad neid tasusid kõik tarnegrupiga seotud tarneviisid. Viimaseks, kui valite väljal **Tarneviisi kood** suvandi **Kõik**, siis kasutavad neid tasusid kõik tarneviisid. Seega ei vali te väärtust väljal **Tarneviisi seos**.

Jaotises **Read** saate vajaduse järgi määratleda ühe või mitu tasu valuuta järgi. Tasud peavad olema seotud tasude koodiga, mis määratleb tasule finantssisestusreeglid. Välja **Kategooria** kasutatakse tasude arvutamisviisi määratlemiseks. Näiteks kasutage kategooriat **Fikseeritud**, kui klientidelt tuleks tellimuse kindla tarneviisiga tarnimise eest küsida alati ühe suurusega tasu 9,95 dollarit. Kasutage kategooriat **Protsent**, kui ettevõte eelistab tarnetasude katmiseks klientidelt tellimuse koguväärtuselt teatud protsendimääraga tasu küsida. Tegelik kliendilt küsitav tasu määratletakse väljal **Tasude väärtus**.

Jaemüügiettevõtted kasutavad sageli mitmetasandilisi tasusid. Sellisel juhul sõltub summa, mille klient tarne eest maksab, tellimuse väärtusest. Mitmetasandiliste tasude konfigureerimiseks sisestage väärtused väljadele **Alates summast** ja **Summani** ning määratlege tasu ise väljal **Tasude väärtus**. Näiteks tellimuste puhul, mille väärtus on vähem kui 50 dollarit, küsib jaemüüja maatranspordi eest tasu 5,95 dollarit. Tellimuste puhul, mille väärtus on võrdne 50 dollariga või sellest suurem, kuid väiksem kui 100 dollarit, küsib jaemüüja tasu 7,95 dollarit. Tellimuste puhul, mille väärtus on võrdne 100 dollariga või sellest suurem, pakub jaemüüja tasuta tarnet. Järgmisel pildil on näidatud nende tasude konfiguratsioonid.

![Näide fikseeritud mitmetasandilistest tasudest](media/fixedtieredcharges.png)

Oma ettevõtte vajaduste kohaselt saate kasutada eri tasukategooriaid. Näiteks kõikide tellimuste puhul, mille väärtus on vähem kui 100 dollarit, küsitakse tarne eest fikseeritud tasu 9,95 dollarit. Seejärel arvutatakse tellimuste jaoks, mille väärtus on võrdne 100 dollariga või sellest suurem, tarnetasuks 5% tellimuse väärtusest. Järgmisel pildil on näidatud nende tasude konfiguratsioonid.

![Näide eri mitmetasandilistest tasudest](media/mixedtieredcharges.png)

## <a name="apply-delivery-modes-during-order-entry-in-a-call-center"></a>Tarneviiside rakendamine kõnekeskuses tellimuse sisestamise ajal

Uue müügitellimuse loomisel tuleb müügitellimuse päise kiirkaardi **Tarne** väljal **Tarneviis** määrata väärtus. See väli võib olla juba automaatselt täidetud kasutajakirje vaikeväärtuste põhjal.

Tellimuse päises määratletud tarneviis kopeeritakse müügitellimuse loomisel automaatselt selle ridadele. Siiski saate müügitellimuse lehe jaotise **Rea üksikasjad** vahekaardil **Tarne** muuta tarneviisi häälestust konkreetse rea kauba jaoks.

Kui valitud tarneviis ei sobi toote või tarneaadressi jaoks, mis on tellimusele või tellimuse reale sisestatud, kuvatakse veateade. Seejärel peate valima tarneviisi, mis on määratletud selle toote või aadressiga kokkusobivaks.

## <a name="calculation-of-delivery-charges-during-entry-of-order"></a>Tarnetasude arvutamine tellimuse sisestamisel

Kui teie kõnekeskuse kanali jaoks on säte **Tellimuse lõpetamise lubamine** sisse lülitatud, siis arvutatakse müügitellimuse tarnetasud automaatselt siis, kui kasutajad valivad käsu **Lõpeta**. Lehe **Müügitellimuse kokkuvõte** ülaosas kuvatakse järgmine teade „Mitmetasandilised tasud on arvutatud“. Arvutatud tasud lisatakse välja **Müügi kogusumma** väärtusele. Kiirkaardi **Summa** väli **Tasud** näitab tellimuse ja ridade jaoks arvutatud tasude kogusummat. Tasudest üksikasjalikuma ülevaate saamiseks valige lehelt **Müügitellimuse kokkuvõte** valik **Tellimus** ja seejärel suvand **Tasud**, et tasusid vaadata, lisada või redigeerida. Pange tähele, et tellimuse päises toimuv tarnetasude arvutamine põhineb päisega seotud tarneviisil. Rea tasemel arvutatud tarnetasud põhinevad tarneviisil, mis on konfigureeritud müügirea jaoks. Kui eri ridadel kasutatakse eri tarneviise, siis võidakse rakendada eri tasusid ja neid kokku liita. Kogusummat näidatakse seejärel lehe **Müügitellimuse kokkuvõte** väljal **Tasud**.

Kui säte **Tellimuse lõpetamise lubamine** on välja lülitatud, peavad kasutajad tasude arvutuse käsitsi käivitama. Valige lehe **Müügitellimus** tegumiriba vahekaardi **Müük** grupist **Arvuta** valik **Mitmetasandilised tasud**. Kuvatakse teade „Mitmetasandilised tasud on arvutatud“. Seejärel saate vahekaardilt **Müük** valida suvandi **Tasud**, et arvutatud tasusid vaadata, redigeerida või kustutada.

## <a name="use-expedited-delivery-modes-on-call-center-orders"></a>Kiirtarneviiside kasutamine kõnekeskuse tellimustel

Saate iga tarneviisiga, mida konfigureerite, valikuliselt siduda kiirsaadetise koodi. Seda koodi kasutatakse prioriteetse sortimise ja aruandluse tööriistana. Praegu ei rakendata sellega tellimusele lisatasusid. Kiirsaadetiste koodide seadistamiseks valige **Müük ja turundus \> Seadistus \> Jaotus \> Kiirsaadetise koodid**.

Näiteks tellimuste puhul, mis tarnitakse järgmisel päeval õhutranspordiga, peab komplekteerimine toimuma laos iga päev kell 13. Sellisel juhul saab luua kiirsaadetise koodi, mille saab siduda ükskõik millise järgmise päeva tarneviisiga, mis on süsteemis konfigureeritud. Kui laos koostatakse komplekteerimisvoog, siis saab väljal **Kiirsaadetis** olevat koodi kasutada filtrina, nii et komplekteeritakse vaid tellimusi, millel on selle koodiga seotud tarneviisid.

Peale selle, kui sisestatud on kõnekeskuse tellimus, saab müügitellimuse päisesse või üksikule müügitellimuse reale käsitsi sisestada kiirsaadetise koodi. Ka sellel puhul saab koodi kasutada sortimiseks ja aruandluseks. Mõnikord on vaja klienditeeninduse vea tõttu tellimust hoolikalt käsitleda. Sellisel juhul saab tellimuse päisesse või ridadele sisestada kiirsaadetise koodi, mis aitab tellimust täitmise käigus tuvastada ja prioriseerida.
