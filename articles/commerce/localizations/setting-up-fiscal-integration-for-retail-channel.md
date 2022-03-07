---
title: Commerce’i kanalite fiskaalüksuse integreerimise seadistamine
description: Sellest teemast leiate juhised kaubanduse kanalite fiskaalüksuse integratsiooni funktsiooni seadistamise kohta.
author: josaw
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: bc87972b1cd2e04d31a3d48132cd1de42353698d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801913"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Commerce’i kanalite fiskaalüksuse integreerimise seadistamine

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Sissejuhatus

Sellest teemast leiate juhised kaubanduse kanalite fiskaalüksuse integratsiooni funktsiooni seadistamise kohta. Lisateavet fiskaalüksuse integratsiooni kohta vt teemast [Kaubanduse kanalite fiskaalüksuse integratsiooni ülevaade](fiscal-integration-for-retail-channel.md).

Fiskaalüksuse integratsiooni seadistamise protsess hõlmab järgmisi ülesandeid.

1. Fiskaalüksuse registreerimiseks kasutatavaid fiskaalseadmeid või -teenuseid tähistavate fiskaalkonnektorite, nt fiskaalprinterid, konfigureerimine.
2. Fiskaalseadmetes või -teenustes fiskaalkonnektorite abil registreeritavaid fiskaaldokumente loovate dokumendipakkujate konfigureerimine.
3. Fiskaalüksuse registreerimise registreerimisetappide jada ning iga etapi puhul kasutatavate fiskaalkonnektoreid ja fiskaaldokumendi pakkujaid määratleva fiskaalüksuse registreerimisprotsessi konfigureerimine.
4. Fiskaalüksuse registreerimisprotsessi määramine kassa funktsiooniprofiilidele.
5. Konnektori tehniliste profiilide määramine riistvaraprofiilidele.

## <a name="set-up-a-fiscal-registration-process"></a>Fiskaalüksuse registreerimisprotsessi seadistamine

Enne fiskaalüksuse integreerimise funktsiooni kasutamist tuleb konfigureerida järgmised sätted.

1. Värskendage kaubanduse parameetreid.

    1. Valige lehel **Kaubanduse ühisparameetrid** vahekaardil **Üldine** suvandi **Luba fiskaalüksuse integratsioon** sätteks **Jah**. Määratlege vahekaardil **Numbriseeriad** järgmiste viidete jaoks numbriseeriad.

        - Fiskaalüksuse tehnilise profiili number
        - Fiskaalkonnektori grupi number
        - Registreerimisprotsessi number

    2. Määratlege lehel **Kaubanduse parameetrid** fiskaalüksuse funktsiooniprofiili numbri jaoks numbriseeria.

    > [!NOTE]
    > Numbriseeriad on valikulised. Kõigi fiskaalüksuse integratsiooniüksuste puhul saab numbrid luua kas numbriseeriate põhjal või käsitsi.

2. Laadige fiskaalkonnektorite ja fiskaaldokumendi pakkujate konfiguratsioonid üles.

    Fiskaaldokumendi pakkuja vastutab fiskaaldokumentide loomise eest, mis tähistavad kandeid ja sündmusi, mis on kassas registreeritud vormingus, mida kasutatakse ka fiskaalseadme või -teenusega suhtlemiseks. Näiteks võib fiskaaldokumendi pakkuja luua fiskaalsissetuleku esituse XML-vormingus.

    Fiskaalkonnektor vastutab fiskaalseadme või -teenusega suhtlemise eest. Näiteks võib fiskaalkonnektor saata fiskaalprinterile fiskaalsissetuleku, mille fiskaaldokumendi pakkuja lõi XML-vormingus. Lisateavet fiskaalüksuse integratsiooni komponentide kohta vt teemast [Fiskaalüksuse registreerimise protsess ja fiskaalüksuse integratsiooni näidised fiskaalseadmete puhul](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. Laadige lehel **Fiskaalkonnektorid** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Fiskaalkonnektorid**) üles XML-konfiguratsioon iga seadme või teenuse jaoks, mida kavatsete fiskaalüksuse integratsiooniks kasutada.

        > [!TIP]
        > Valides käsu **Kuva**, saate vaadata kõiki funktsiooni- ja tehnilisi profiile, mis on seotud praeguse fiskaalkonnektoriga.

    2. Laadige lehel **Fiskaaldokumendi pakkujad** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Fiskaaldokumendi pakkujad**) üles XML-konfiguratsioon iga seadme või teenuse jaoks, mida kavatsete kasutada.

        > [!TIP]
        > Valides käsu **Kuva**, saate vaadata kõiki funktsiooniprofiile, mis on seotud praeguse fiskaaldokumendi pakkujaga.

    Fiskaalkonnektorite ja fiskaaldokumendi pakkujate konfiguratsiooni näidised leiate teemast [Fiskaalüksuse integratsiooni näidised Retail SDK-s](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Andmetüüpide vastendamist käsitletakse fiskaaldokumendi pakkuja osana. Samale konnektorile erinevate vastenduste loomiseks (nt riigipõhised määrused), tuleb luua erinevad fiskaaldokumendi pakkujad.

3. Looge konnektori funktsiooniprofiilid ja konnektori tehnilised profiilid.

    1. Looge lehel **Konnektori funktsiooniprofiilid** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Konnektori funktsiooniprofiilid**) konnektori funktsiooniprofiil igale fiskaalkonnetori ja fiskaaldokumendi pakkuja kombinatsioonile, mis on fiskaalkonnektoriga seotud.

        1. Valige konnektori nimi.
        2. Valige dokumendipakkuja.

        Saate muuta andmetüüpide vastendamise parameetreid konnektori funktsiooniprofiilis. Vaikeparameetrite taastamiseks, mis on määratletud fiskaaldokumendi pakkuja konfiguratsioonis, valige käsk **Värskenda**.

        **Näited**

        |   | Vorming | Näide |
        |---|--------|---------|
        | **KM-määrade seadistamine** | väärtus: KM-määr | 1 : 2000, 2 : 1800 |
        | **KM-koodide vastendamine** | KM-kood: väärtus | KM20 : 1, KM18 : 2 |
        | **Maksevahendi tüüpide vastendamine** | TenderType: väärtus | Sularaha: 1 kaart: 2 |

        > [!NOTE]
        > Konnektori funktsiooniprofiilid on ettevõttekohased. Kui kavatsete kasutada sama fiskaalkonnektori ja fiskaaldokumendi pakkuja kombinatsiooni erinevates ettevõtetes, peate looma konnektori funktsiooniprofiili igale ettevõttele.

    2. Looge lehel **Konnektori tehnilised profiilid** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Konnektori tehnilised profiilid**) konnektori tehniline profiil igale fiskaalkonnektorile.

        1. Valige konnektori nimi.
        2. Valige konnektori tüüp. Riistvarajaamata ühendatud seadmete puhul valige suvand **Kohalik**.

            > [!NOTE]
            > Praegu toetatakse ainult kohalikke ühendusi.

        Parameetreid konnektori tehnilise profiili vahekaartidel **Seade** ja **Sätted** saab muuta. Vaikeparameetrite taastamiseks, mis on määratletud fiskaalkonnektori konfiguratsioonis, valige käsk **Värskenda**. Kui XML-konfiguratsiooni uus versioon on laaditud, saate teate, et praegune fiskaalkonnektor ja fiskaaldokumendi pakkuja on juba kasutusel. See protseduur ei kirjuta üle konnektori funktsiooni- ja tehnilistele profiilidele varem käsitsi tehtud muudatusi. Uue konfiguratsiooni parameetrite vaikekogumi rakendamiseks valige lehel **Konnektori funktsiooniprofiilid** või **Konnektori tehnilised profiilid** käsk **Värskenda**.

4. Looge fiskaalkonnektorite grupid.

    Fiskaalkonnektori grupp ühendab fiskaalkonnektorite, mis teostvad samu funktsioone ja mida kasutatakse fiskaalüksuse registreerimise protsessi samas etapis, funktsiooniprofiile. Näiteks kui kaupluses saab kasutada mitut fiskaalprinteri mudelit, saab nende fiskaalprinterite fiskaalkonnektorid koondada fiskaalkonnektorite gruppi.

    1. Looge lehel **Fiskaalkonnektorite grupp** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Fiskaalkonnektorite grupid**) uus fiskaalkonnektorite grupp.
    2. Konnektori grupile funktsiooniprofiilide lisamine. Valige vahekaardil **Funktsiooniprofiilid** suvand **Lisa** ja valige profiili number. Konnektorite grupis saab igal fiskaalkonnektoril olla ainult üks funktsiooniprofiil.
    3. Funktsiooniprofiili kasutamise peatamiseks valige suvandi **Keela** sätteks **Jah**. See muudatus mõjutab ainult praegust konnektorigruppi. Saate jätkata sama funktsiooniprofiili kasutamist teistes konnektorigruppides.

5. Looge fiskaalüksuse registreerimisprotsess.

    Fiskaalüksuse registreerimisprotsess määratletakse registreerimisetappide jada ja igas etapis kasutatava konnektorigrupi järgi.

    1. Looge lehel **Fiskaalüksuse registreerimisprotsess** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Fiskaalüksuse registreerimisprotsessid**) iga kordumatu fiskaalüksuse registreerimisprotsessi jaoks uus kirje.
    2. Registreerimisetappide protsessi lisamine.

        1. Valige **Lisa**.
        2. Valige fiskaalkonnektori tüüp.
        3. Valige väljal **Grupi number** sobiv fiskaalkonnektorite grupp.

6. Määrake fiskaalüksuse registreerimisprotsessi üksused kassaprofiilidele.

    1. Määrake lehel **Kassa funktsiooniprofiilid** (**Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa profiilid \> Funktsiooniprofiilid**) kassa funktsiooniprofiilile fiskaalüksuse registreerimisprotsess. Valige käsk **Redigeeri** ja seejärel valige vahekaardil **Fiskaalüksuse registreerimisprotsess** väljalt **Protsessi number** soovitud protsess.
    2. Määrake lehel **Kassa riistvaraprofiil** (**Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa profiilid \> Riistvaraprofiilid**) riistvaraprofiilile konnektori tehnilised profiilid. Valige käsk **Redigeeri**, lisage vahekaardile **Fiskaalvälisseadmed** uus rida ja seejärel valige väljalt **Profiili number** konnektori tehniline profiil.

    > [!NOTE]
    > Samale riistvaraprofiilile saab lisada mitu tehnilist profiili. Siiski peab riistvaraprofiilil või kassa funktsiooniprofiilil olema mis tahes fiskaalkonnektorite grupiga ainult üks ühisosa.

    Fiskaalüksuse registreerimise voog määratletakse fiskaalüksuse registreerimisprotsessi ja ka mõningate fiskaalüksuse integratsiooni komponentide parameetritega: Commerce’i käitusaja laiendus fiskaaldokumendi pakkuja puhul ja riistvarajaama laiendus fiskaalkonnektori puhul.

    - Sündmuste ja kannete tellimus fiskaalüksuse registreerimisele on eelmääratletud fiskaaldokumendi pakkujas.
    - Fiskaaldokumendi pakkuja vastutab ka fiskaalüksuse registreerimiseks kasutatava fiskaalkonnektori tuvastamise eest. See vastab konnektori funktsiooniprofiilidele, mis on kaasatud fiskaalüksuse registreerimise protsessi praeguse etapi jaoks määratud fiskaalkonnektorite gruppi koos konnektori tehnilise profiiliga, mis on määratud kassaga seotud riistvarajaama riistvaraprofiilile.
    - Fiskaaldokumendi pakkuja kasutab fiskaaldokumendi pakkuja konfiguratsiooni andmetüüpide vastenduse sätteid kannete/sündmuste andmete, nagu maksud ja maksed, teisendamiseks fiskaaldokumendi loomise ajal.
    - Kui fiskaaldokumendi pakkuja loob fiskaaldokumendi, võib fiskaalkonnektor saata selle samal kujul fiskaalseadmele või selle sõeluda ja teisendada seadme rakendusliidese (API) käskude jadaks olenevalt sellest, kuidas kommunikatsiooni käsitletakse.

7. Valige lehel **Fiskaalüksuse registreerimisprotsess** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Fiskaalüksuse registreerimisprotsessid**) käsk **Valideeri** fiskaalüksuse registreerimisprotsessi valideerimiseks.

    Soovitatav on seda tüüpi valideerimine käivitada järgmistel juhtudel.

    - Pärast kõigi uue registreerimisprotsessi sätete lõpuleviimist, sh registreerimisprotsesside määramisel kassa funktsiooniprofiilidele ja riistvaraprofiilidele.
    - Pärast olemasoleva fiskaalüksuse registreerimisprotsessi muutmist, mille puhul muudatused võivad põhjustada käitusajal teise fiskaalkonnektori valimise (näiteks kui muudate fiskaalüksuse registreerimisprotsessi etapi jaoks konnektorigruppi, lubate konnektorigrupis konnektori funktsiooniprofiili või lisate konnektorigrupile uue konnektori funktsiooniprofiili).
    - Pärast konnektori tehniliste profiilide riistvaraprofiilidele määramise muutmist.

8. Käivitage lehel **Jaotusgraafik** tööd **1070** ja **1090**, et edastada andmed kanali andmebaasile.

## <a name="set-up-fiscal-texts-for-discounts"></a>Fiskaaltekstide seadistamine allahindluste jaoks

Mõnel juhul tuleb allahindluse kohaldamisel printida fiskaalsissetulekule spetsiaalne tekst. Saate allahindluste fiskaaltekstid seadistada lehel **Fiskaalkonnektorite grupp** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Fiskaalkonnektorite grupid**).

- Kassas kohaldatavate käsitsi allahindluste puhul tuleb määrata fiskaaltekst teabekoodile või teabekoodigrupile, mis on määratud kassa funktsiooniprofiilis teabekoodina **Toote allahindlus**.

    1. Valige lehel **Fiskaalkonnektorite grupp** suvand **Fiskaalsissetuleku tekst**.
    2. Valige vahekaardil **Teabekoodid** käsk **Lisa** ja valige teabekood või teabekoodigrupp.
    3. Väljal **Teabekoodi number** valige soovitud väärtus.
    4. Väljal **Alamkoodi number** valige väärtus, kui valitud teabekoodi puhul on vajalik alamkood.
    5. Väljal **Fiskaalsissetuleku tekst** määrake fiskaaltekst, mis tuleb fiskaalsissetulekule printida.
    6. Valige suvandi **Prindi kasutaja sisend fiskaalsissetulekule** sätteks **Jah**, et asendada fiskaalsissetulekul olev tekst teabega, mille kasutaja kassas käsitsi sisestab. See suvand kehtib ainult teabekoodide puhul, mille sisendtüüp on **Tekst**.

    > [!NOTE]
    > Saate määrata fiskaalteksti mitmele teabekoodile, et toetada stsenaariume, milles kasutatakse teabekoodigruppe, lingitud teabekoode ja käivitatud teabekoode. Nende stsenaariumide puhul sisaldab fiskaalsissetulek fiskaaltekste kõigist teabekoodidest, mis on lingitud kandereaga, millele kohaldub allahindlus.

- Kanalipõhiste allahindluste puhul peate määratlema fiskaalteksti allahindluse ID-le.

    1. Valige lehel **Fiskaalkonnektorite grupp** suvand **Fiskaalsissetuleku tekst**.
    2. Valige lehel **Allahindluse** käsk **Lisa** ja valige allahindluse ID.
    3. Väljal **Fiskaalsissetuleku tekst** määrake fiskaaltekst, mis tuleb fiskaalsissetulekule printida.

    > [!NOTE]
    > Kui samale kandereale kohaldub mitu allahindlust, sisaldab fiskaalsissetulek fiskaaltekste kõigist selle kandereaga lingitud allahindlustest.

## <a name="set-error-handling-settings"></a>Tõrketöötluse sätete määramine

Fiskaalüksuse integratsioonis saadaolevad tõrketöötluse sätted määratakse fiskaalüksuse registreerimisprotsessis. Lisateavet tõrketöötluse kohta fiskaalüksuse integratsioonis vt teemast [Tõrketöötlus](fiscal-integration-for-retail-channel.md#error-handling).

1. Lehel **Fiskaalüksuse registreerimisprotsess** (**Jaemüük ja kaubandus \> Kanali seadistus \> Fiskaalüksuse integratsioon \> Fiskaalüksuse registreerimisprotsessid**) saate määrata fiskaalüksuse registreerimisprotsessi iga etapi kohta järgmised parameetrid.

    - **Luba vahelejätmine** – see parameeter lubab tõrketöötluse dialoogiboksis suvand **Jäta vahele**.
    - **Luba registreerituks märkimine** – see parameeter lubab tõrketöötluse dialoogiboksis suvandi **Märgi registreerituks**.
    - **Jätka tõrke korral** – kui see parameeter on lubatud, saab fiskaalüksuse registreerimise protsess kande või sündmuse fiskaalüksuse registreerimise nurjumise korral kassaregistris tegevust jätkata. Muidu peaks operaator järgmisel kandel või sündmusel fiskaalüksuse registreerimise käitamise jaoks nurjunud fiskaalüksuse registreerimist uuesti proovima, selle vahele jätma või märkima kande või sündmuse registreerituks. Lisateavet vaadake teemast [Valikuline fiskaalüksuse registreerimine](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Kui lubatud on parameeter **Jätka tõrke korral**, siis on parameetrid **Luba vahelejätmine** ja **Luba registreerituks märkimine** automaatselt keelatud.

2. Tõrketöötluse dialoogiboksi suvandid **Jäta vahele** ja **Märgi registreerituks** nõuavad luba **Registreerimise vahelejätmise või registreerituks märkimise lubamine**. Seetõttu lubage lehel **Lubade grupid** (**Jaemüük ja kaubandus \> Töövõtjad \> Lubade grupid**) luba **Registreerimise vahelejätmise või registreerituks märkimise lubamine**.
3. Suvandid **Jäta vahele** ja **Märgi registreerituks** võimaldavad operaatoritel sisestada lisateavet, kui fiskaalüksuse registreerimine nurjub. Selle funktsiooni kättesaadavaks tegemiseks peate määrama fiskaalkonnektorite grupis teabekoodid **Jäta vahele** ja **Märgi registreerituks**: Seejärel salvestatakse operaatorite sisestatav teave teabekoodi kandena, mis on lingitud fiskaalkandega. Lisateavet teabekoodide kohta vt teemast [Teabekoodid ja teabekoodigrupid](../info-codes-retail.md).

    > [!NOTE]
    > Käivitusfunktsiooni **Toode** ei toetata teabekoodide puhul, mida kasutatakse fiskaalkonnektorite gruppides suvandite **Jäta vahele** ja **Märgi registreerituks** puhul.

    - Valige lehel **Fiskaalkonnektorite grupp** vahekaardil **Teabekoodid** väljadel **Jäta vahele** ja **Märgi registreerituks** teabekoodid või teabekoodigrupid.

    > [!NOTE]
    > Fiskaalüksuse registreerimisprotsessi mis tahes etapis saab luua ühe fiskaaldokumendi ja ühe mittefiskaaldokumendi. Fiskaaldokumendi pakkuja laiendus tuvastab iga kande või sündmuse tüübi seose fiskaal- või mittefiskaaldokumentidega. Tõrketöötluse funktsioon kohaldub ainult fiskaaldokumentidele.
    >
    > - **Fiskaaldokument** – kohustuslik dokument, mis tuleb edukalt registreerida (nt fiskaalsissetulek).
    > - **Mittefiskaaldokument** – kande või sündmuse lisadokument (nt kinkekaardi sedel).

4. Kui operaator peab pärast seisundikontrolli tõrke esinemist olema võimeline jätkama praeguse operatsiooni (näiteks kande loomine või lõpetamine) protsessi, siis peaksite lubama loa **Luba seisundikontrolli tõrge vahele jätta**, mille leiate lehelt **Lubade grupid** (**Jaemüük ja kaubandus \> Töövõtjad \> Lubade grupid**). Lisateavet seisundikontrolli protseduuri kohta leiate teemast [Fiskaalüksuse registreerimise seisundikontroll](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Fiskaalüksuse x-/z-aruannete seadistamine kassast

Fiskaalüksuse x-/z-aruannete käitamise lubamiseks kassast peate lisama kassa ekraanipaigutusse uued nupud.

- Järgige lehel **Nupupaneelid** teemas [Kassatoimingute lisamine kassa paigutustele nupupaneeli koostaja abil](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) toodud juhiseid kujundaja installimiseks ja kassa ekraanipaigutuse värskendamiseks.

    1. Valige värskendatav paigutus. 
    2. Lisage uus nupp ja määrake nupu **Prindi fiskaalüksuse x** atribuut.
    3. Lisage uus nupp ja määrake nupu **Prindi fiskaalüksuse z** atribuut.
    4. Käivitage lehel **Jaotusgraafik** töö **1090**, et edastada muudatused kanali andmebaasile.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Edasi lükatud fiskaalüksuse registreerimise käsitsi käivitamise lubamine

Edasi lükatud fiskaalüksuse registreerimise käsitsi käivitamise lubamiseks peaksite kassa paigutusse lisama uue nupu.

- Järgige lehel **Nupupaneelid** teemas [Kassatoimingute lisamine kassa paigutustele nupupaneeli koostaja abil](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) toodud juhiseid kujundaja installimiseks ja kassa ekraanipaigutuse värskendamiseks.

    1. Valige värskendatav paigutus.
    2. Lisage uus nupp ja määrake nupu atribuut **Lõpeta fiskaalüksuse registreerimise protsess**.
    3. Käivitage lehel **Jaotusgraafik** töö **1090**, et edastada teie muudatused kanali andmebaasile.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]