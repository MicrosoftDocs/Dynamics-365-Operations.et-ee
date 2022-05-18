---
title: Konteinerisse määramine
description: Teema kirjeldab koormakonteinerite koostamise automatiseerimist. Automaatne konteinerite koostamine loob saadetiste jaoks konteinerid ja komplekteerimistööd pärast voo töötlemist.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f738c0404a41ef862d4985a170a0eba991e4dd4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686622"
---
# <a name="containerization"></a>Konteinerisse määramine

[!include [banner](../includes/banner.md)]

Teema kirjeldab koormakonteinerite koostamise automatiseerimist. Automaatne konteinerite koostamine loob saadetiste jaoks konteinerid ja komplekteerimistööd pärast voo töötlemist.

Konteinerite koostamise häälestamiseks tuleb teil luua järgmised sätted.

- **Konteineri tüüp** ─ määratlege konteinerite füüsilised omadused. Konteineritüüpide alusel saate pakendada laokaubad kindla tüübi ja suurusega pakenditesse, näiteks kohtadesse või kaubaalustele.
- **Konteineri grupid** ─ looge sarnast tüüpi konteineritest gruppe. Näiteks võib konteinerigrupp sisaldada sarnaste mõõtudega konteinerite tüüpe. Konteinerigrupp määrab konteinerite pakkimise järjestuse ja iga konteineri täitmisprotsendi.
- **Konteineri koostemall** ─ looge mallid, mis määratlevad konteinerite loomise reeglid. See hõlmab näiteks varude segamise ja muude pakkimisstrateegiate reegleid.
- **Voomallid** – häälestage üks või mitu voomalli konteinerite koostamise komplekteerimistöö loomiseks.

## <a name="create-wave-templates-for-containerization"></a>Loomallide loomine konteinerite loomiseks

Teil tuleb häälestada üks või mitu tarnevoo malli konteinerite koostamise jaoks. Voomallid sisaldavad kriteeriume, mis määravad järgmise.

- Voogude töötlemise viis. Seda saab teha nii käsitsi kui ka automaatselt.
- Komplekteerimistöö loomise viis. Selle määravad voo meetodid. Voomall peab sisaldama **konteineri loomise** meetodit.
- Kaupade või eraldusridade vastendamine vooga.

Lisateabe saamiseks vaadake jaotist [Voomallid](wave-templates.md).

## <a name="create-container-types"></a>Konteineri tüüpide loomine

Konteinerite tüübid võimaldavad teil luua konteinerite kirjeldusi, sealhulgas füüsiliste mõõtmete ja massi maksimumväärtused. Konteineriks koostatud voo töötlemisel luuakse konteinerid tüübiteabe alusel.

Konteineri tüübi häälestamiseks tehke järgmist.

1. Avage **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteineri tüüp**.
1. Valige uue konteineri tüübi loomiseks **Uus**.
1. Sisestage konteineritüübi kordumatu ID ja kirjeldus.
1. Sisestage väljale **Nullkaal** konteineri tegelik või eeldatav kaal.
1. Sisestage väljale **Maksimaalne kaal** konteineri maksimaalne kandevõime.
1. Väljadel **Maksimaalne maht konteinerites**, **Konteinerite maksimaalne pikkus**, **Konteinerite maksimaalne laius** ja **Konteinerite maksimaalne kõrgus** määrake konteineri füüsilised dimensioonid.

    > [!NOTE]
    > Pikkuse ja laiuse väärtused on samaväärsed. See tähendab, et saate vajaduse korral pöörata kaupu külje suunas, st X-teljel. Näiteks kui pikkus on 2 jalga ja laius on 1 jalg, võite märkida pikkuseks 1 jala ja laiuseks 2 jalga. Pange tähele, et see ei kehti kõrguse puhul. Te ei saa muuta kõrguse väärtust, et pöörata kaupa vertikaalselt.

1. Valige atribuudiväljadel konteineri kohandatud atribuudiväärtused. Atribuudid on kohandatud väärtused, mida kasutatakse kaupade filtreerimiseks või sortimiseks väärtuse alusel, mis ei ole tavaliselt saadaval. Näiteks kui soovite pakkida kindla kliendi kaubad, saate luua kliendi nime atribuudi. Atribuuditüübid saate luua lehel **Konteineri atribuudid**.

## <a name="create-container-groups"></a>Konteinerigruppide loomine

Saate häälestada konteineritüüpide loogilised grupid. Iga grupi puhul saate määrata järjekorra, milles soovite konteinereid pakkuda, ja täidetavate konteinerite protsendi. Kauba suuruse mõõtude alusel tehakse kindlaks, kas see mahub konteinerisse. Kasutatakse konteinerit, mille mõõdud on kaubaga kõige sarnasemad. Kui grupis on mitu konteineritüüpi, soovitame korraldada järjestuse suuruse alusel, nii et suurim konteiner on esimene, järjekorras nr 1, ja väikseim konteiner viimane.

Konteinerigrupi häälestamiseks tehke järgmist.

1. Avage **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteinerigrupid**.
1. Valige uue konteineri grupi loomiseks **Uus**.
1. Sisestage konteinerigrupi kordumatu ID ja kirjeldus.
1. Klõpsake kiirkaardil **Üksikasjad** suvandit **Uus**, et lisada konteineritüüp gruppi.
1. Valige konteineri tüüp väljas **Konteineri tüübi kood**.
1. Konteineritüüpide pakkimise järjestuse määramiseks valige väärtus **Nihuta üles** või **Nihuta alla**.

## <a name="create-container-build-templates"></a>Looge uus konteineri koostemallid.

Saate häälestada konteineri koostamise protsessi reeglid, näiteks varude segamise reeglid ja muud pakkimisstrateegiad. Näiteks saate häälestada reegli, mis ei luba töötajatel pakkida samasse konteinerisse eraldusridu, mis põhinevad erinevate klientide müügitellimustel.

Konteineri koostemalli häälestamiseks tehke järgmist.

1. Avage **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteineri koostemall**.
1. Looge uus konteineri koostemall.
1. Sisestage väljadele **Konteineri nimi** ja **Seerianumber** konteineri koostamise malli nimi ja tellimus, mis on vastendatud eraldusreaga.

    > [!NOTE]
    > Süsteem rakendab esimese malli, mille päringukriteeriumitele eraldusrida vastab. Seetõttu paigutage kõige spetsiifilisemate kriteeriumitega mall loendi ülaossa. Mida üldisemad on kriteeriumid, seda tõenäolisemalt vastab eraldusrida kriteeriumitele. Seetõttu võidakse read määrata valesse konteinerisse. Vajadusel saate mallide järjestuse muutmiseks valida **Nihuta üles** või **Nihuta alla**.

1. Valige väljal **Konteineri grupi ID** konteinerigrupp, mille alusel konteinerid luua.
1. Valige väljal **Aluspäringu tüübid** päringu tüüp, mis määrab, mida pakkida ja millel põhineb filtripäring. Valikud on järgmised:

      - **Müügi eraldusread** ─ pakkige eraldusread, mis luuakse müügitellimuste jaoks.
      - **Ülekande eraldusread** ─ pakkige eraldusread, mis luuakse ülekandetellimuste jaoks.
      - **Konteiner** ─ pakkige konteiner, mis loodi juba konteineri koostamise protsessi ajal. Seda kasutatakse näiteks mitmetasemeliste konteinerite puhul.

        > [!NOTE]
        > Mitmetasemeliste konteinerite kasutamiseks peate määrama konteineri koostamise meetodi korratavaks. Lisateabe saamiseks vaadake jaotist [Voomallid](wave-templates.md).

1. Sisestage kiirkaardi **Üldine** väljale **Voo sammukood** kordumatu ID, mis on määratud vooprotsessi meetodile, mis lingib konteineri koostamise malli voomalli etappidega.
1. Märkige ruut **Luba vahevalikud**, et lubada töötajatel pakkida töötellimusest pärinevaid kaupu eraldi konteineritesse. Selleks peab terve kogus konteinerisse mahtuma. Seejuures kasutatakse alati eraldusrea suurimat mõõtühikut.
1. Valige väljal **Pakkige ühiku alusel** mõõtühik, mis kajastab konteinerit. Näiteks saate märkida, et ümbris on konteiner. Kui pakite mõõtühiku alusel, ei saa te määrata konteinerigruppi, kuna mõõtühik on konteiner.
1. Valige väljal **Konteineri pakkimise strateegia** pakkimisstrateegia, mida soovite kasutada. Valikud on järgmised:

    > [!NOTE]
    > Strateegia kehtib ainult müügi eralduse ja üleviimise eralduse ridadele.

      - **Pakenda kõikidesse avatud konteineritesse** – süsteem tuvastab, kas eraldusrida mahub mõnesse konteinerisse, mis loodi konteineri koostamise tsükli ajal.
      - **Pakenda ainult praegusesse konteinerisse** – süsteem tuvastab vaid seda, kas eraldusrida mahub viimati loodud konteinerisse.

    Lisateavet ja näiteid konteinerite pakkimise strateegiatega töötamise kohta leiate teemast [Konteinerite pakkimise strateegiad](container-packing-strategy-overview.md).

1. Eraldusridade konteinerisse pakkimise reeglite seadistamiseks valige **Koostamisloogika pausid**. Näiteks saate luua reegli, mis võimaldab töötajatel pakkida kahe erineva kauba eraldusread samasse konteinerisse. Koostamisreegli määratlemiseks tehke järgmist.

    1. Valige lehel **Koostamisloogika pausid** suvand **Uus**.
    1. Valige väljal **Tabel** tabel, mis sisaldab välja, mida kasutatakse koostamisloogika pausi kriteeriumina.
    1. Valige väljal **Välja valik** väli, mida kasutatakse koostamisloogika pausi kriteeriumina.
    1. Korrake neid etappe, kuni olete lisanud koostamisloogika pausi kõik kriteeriumid.

    > [!NOTE]
    > Kui kasutate koostamisloogikat, siis soovitame teil filtri kriteeriumite päringus sortida samade väljade alusel. See vähendab koostatavate konteinerite arvu.
