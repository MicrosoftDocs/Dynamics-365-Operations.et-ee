---
title: Human Resources'i parameetrite konfigureerimine
description: See artikkel selgitab, kuidas seadistada ettevõttespetsiifilisi parameetreid Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 13a25d3f1f72d8053ed3951b036522cfa3a15959
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065640"
---
# <a name="configure-human-resources-parameters"></a>Human Resources'i parameetrite konfigureerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Osa inimressursside parameetrite sätteid on ettevõtteülesed, samas kui teiste parameetrite sätted on ettevõttekohased. See artikkel selgitab, kuidas seadistada ettevõttepõhiseid inimressursside parameetreid.

Personali ehk inimressursside parameetrite määramiseks kasutatakse kahte lehte. Ettevõtetes ühiskasutatavate parameetrite puhul kasutate lehte **Inimressursside ühiskasutusega parameetrid**. Ettevõttele omaste parameetrite puhul kasutage lehte **Inimressursside parameetrid**.

![Avage inimressursside parameetrid.](./media/hr-employee-self-service-human-resources-parameters.png)

Lehel **Inimressursside parameetrid** jaotatakse sätted kuue vahekaardi vahel.

- **Üldine**
- **Värbamine** (Dynamics 365 Human Resources ei sisalda seda vahekaarti)
- **Hüvitus**
- **Numbriseeriad**
- **FMLA**
- **Töötaja iseteenindus**
- **Juhi iseteenindus**
- **Soodustuste haldus**
- **Puhkused ja puudumine**
- **Makseviisid**

Iga vahekaart sisaldab teavet, mis on seotud ühe ettevõttega.

## <a name="general"></a>Üldine

Sätted vahekaardil **Üldine** määratlevad puudumise, vigastuste ja haiguste ning uute värbamiste kohta käiva teabe ilmumise. Sellel vahekaardil olevad sätted määratlevad ka mõned vaikekirjed, mis ilmuvad töö tegemisel. Sellel vahekaardil saate:

- Valige värv avatud puudumiskannetele rakendatavaks värviks.
- Määrata aruannetes kasutatav laadileht.
- Lubada koolituskursuste ja puudumiste registreerimise vaheline integratsioon.
- valida selle integratsiooni juhtimiseks kasutatava puudumise koodi;
- näidata, kui kaua säilitada vigastus- ja haigusjuhtude juhtumeid;
- määrata uue töötaja palkamisel vaikimisi kuvatava ID-numbri.
- Määrata teenuseaastate arvutamiseks kasutatav kuupäev. 

![Vahekaart Üldine.](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Värbamine

Vahekaardi **Värbamine** sätted määratlevad dokumenditüübid, mida kasutatakse kandidaatidele automaatselt saadetavas kirjavahetuses. Samuti saate osutada soovimatute avalduste jaoks kasutatavale värbamisprojektile.

Värbamisprojekti aegumises määratletud periood määratleb **, millised värbamisprojektid kaasatakse** värbamishalduse **tööruumi** aegumisprojektide paanile **.** Perioodi, mis on määratud avalduse tähtaja hoiatuseks, kasutatakse selleks, et näidata värbamisprojekte, mis on **lähenemas nende avalduse tähtajale avalduse tähtajale läheneva** paani puhul värbamise **tööruumis**.

Värbamise kohta lisateabe saamiseks vt teemat [Kandidaatide värbamine](hr-personnel-recruit.md).

## <a name="compensation"></a>Hüvitus

Dynamics 365 Finance'is määravad **vahekaardi Tasu** sätted, kas kasutajad peavad kinnitama, et nad soovivad salvestada teavet fikseeritud või muutuva tasuplaani jaoks. Ruudu **Luba salvestamise kinnitamine** märkimise korral saavad kasutajad hüvitusega seotud lehe sulgemisel teate, mis küsib, kas nad soovivad kirje salvestada. Osa hüvituste halduse lehti ei luba kasutajatel teavet kustutada. Kui palute kasutajatel kinnitada, kas nad soovivad teabe salvestada, aitab see piirata sellise salvestatud teabe hulka, mida ei saa hiljem kustutada. Märkeruudu **Luba salvestamise kinnitamine** tühjendamisel salvestatakse kirjed alati kohe (võimalik, et enne seda, kui kasutaja on selleks valmis). Jõudlushalduse kasutamisel võimaldab vahekaart **Hüvitus** teil valida ka hindamismudeli, mida tööviljakuse ehk jõudluse hindamisel kompensatsiooniplaanidele määratud mudeli asemel kasutada.

Inimressursside moodulis saate vahekaardi **Hüvitus** kaudu soovi korral piirata juurdepääsu kompensatsiooniplaanidele ja häälestada vaikevaluuta.

> [!NOTE]
> Ühendatud infrastruktuuris on inimressursside parameetrite **lehe** **vahekaardil** Tasu vaikimisi **valuuta** parameeter eemaldatud. Edasi liikudes käsitseb valuutat **pearaamatu** valuuta parameeter, et tagada olemasolevate finantside ja operatsioonide funktsioonide vastuolud ja duplikaadid. Lisateavet pearaamatu valuutafunktsioonide kasutamise kohta vt pearaamatute [konfigureerimine](/general-ledger/configure-ledger#configuring-currencies-for-the-ledger.md). 

Lisateavet kompensatsiooni kohta leiate artiklist [Kompensatsiooniplaanide ülevaade](hr-compensation-overview.md).

## <a name="number-sequences"></a>Numbriseeriad

Vahekaardi **Numbriseeria** sätted määravad ära seeriad, mida kasutatakse inimressurssides üksustele ID-de automaatseks määramiseks, näiteks:

- Avaldused
- Puudumiste registreerimised
- Kompensatsiooniprotsessi tulemused
- Juhtuminumbrid
- Kursused
- Kursuste päevakord

Numbriseeriate viidete ja koodide säilitamiseks kasutage loendilehte **Numbriseeriad** (valige **Organisatsiooni haldus > Numbriseeriad > Numbriseeriad**).

Lisateabe saamiseks vt teemat [Numbriseeriate ülevaade](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Töötundide arv ei tohi ületada 1250 tundi ja töösuhte pikkus ei saa olla pikem kui 12 kuud. Need maksimumväärtused on kooskõlas USA föderaalseadustega.

![Numbriseeriad vahekaart.](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

FMLA vahekaardil saate määrata FMLA sobivuse nõuded ja FMLA õigustatud tunnid. Lisateabe saamiseks vt jaotist [Puhkuse ja puudumise parameetrite konfigureerimine](hr-leave-and-absence-parameters.md).

![FMLA vahekaart.](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Töövõtja iseteenindus

Töötaja iseteeninduse **vahekaardi sätted mõjutavad** töötaja **iseteeninduse kuvamist** töötajatele. Sellel vahekaardil saate lõpule viia järgmised ülesanded:

- Sisestage töötaja iseteeninduse **tööruumi nimi**.
- valida, millist teavet saab ülemus töötajate kohta sisestada;
- lisada töötajate jaoks kasulikke linke;
- piirata töötajatel ettevõtte kontaktteabe lisamist või redigeerimist. Lisateavet vt teemast [Isikuandmete redigeerimise piiramine](hr-employee-self-service-restrict-editing.md).

Lisateavet töötaja iseteeninduse häälestamise **kohta vt töötaja** ja [juhi iseteeninduse ülevaatest](hr-employee-manager-self-service-overview.md).

![Töötaja iseteeninduse vahekaart.](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Juhi iseteenindus

Vahekaardil Halduri iseteeninduse **sätted mõjutavad** seda, mida juhatajad haldurite **iseteeninduses näevad**. Sellel vahekaardil saate konfigureerida järgmisi valikuid:

- Aeguvate kirjete vahemik
- Teave, mida haldurid saavad aegumiskirjetes vaadata
- Kas ülemused saavad laiendatud aruannete jaoks vaadata vabu ametikohti?
- Lahkuvate töötajate vaated
- Ülemustele kasulikud lingid

Lisateavet halduri iseteeninduse häälestamise **kohta vt** töötaja [ja juhi iseteeninduse ülevaatest](hr-employee-manager-self-service-overview.md).

![Juhi iseteeninduse vahekaart.](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Soodustuste haldus

Vahekaardil Soodustuste **haldus saate** konfigureerida soodustuste halduse meilivalikud. Lisateavet soodustuste halduse häälestamise ja kasutamise kohta vt soodustuste [halduse ülevaadet](hr-benefits-management-overview.md).

![Soodustuste halduse vahekaart.](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Puhkused ja puudumine

Puhkuste ja puudumiste häälestamise ja kasutamise kohta teabe saamiseks vt teemat [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Makseviisid

Vahekaardil **Makseviisid** saate valida makseviisid, mida teie organisatsioon toetab. Lisateavet hüvituste konfigureerimise kohta leiate artiklist [Kompensatsiooniplaanide ülevaade](hr-compensation-overview.md).

![Makseviiside vahekaart.](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
