---
title: "Náklady řízení mobilní pracovní prostor pro Microsoft Dynamics 365 pro provoz aplikace"
description: "S náklady řízení mobilní pracovní prostor, vedoucí centra nákladů můžete zobrazit výkon náklady center kdykoli a kdekoli."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Náklady řízení mobilní pracovní prostor pro Microsoft Dynamics 365 pro provoz aplikace

S náklady řízení mobilní pracovní prostor, vedoucí centra nákladů můžete zobrazit výkon náklady center kdykoli a kdekoli. 

<a name="prerequisites"></a>Předpoklady
-------------

| Předpoklad                                                         | popis                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Přečtěte si informace o Microsoft Dynamics 365 pro provoz mobilní platformu | [Dynamics 365 pro mobilní platformu operace](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 pro operace                                          | Ujistěte se, že používáte prostředí, které má Microsoft Dynamics 365 pro verzi operace 1611 a Microsoft Dynamics pro operace platformy aktualizace 3 (listopad 2016). |
| Opravy hotfix KB 3215650                                                    | Nainstalujte opravu hotfix Chcete-li povolit pracovní prostory, které jsou součástí Microsoft Dynamics 365 pro operace.                                                                       |
| Mobilní zařízení, které má 365 Dynamics pro operace aplikace nainstalována | Stáhněte 365 Dynamics pro operace aplikace z úložiště vaše mobilní aplikace.                                                                                                      |

## <a name="introduction"></a>Úvod
Náklady řízení mobilní pracovní prostor poskytuje okamžitý přehled o aktuálním výkonu nákladových středisek porovnáním skutečných nákladů s rozpočtovými náklady. Můžete přejít na stavy jednotlivých nákladových položek.

### <a name="example"></a>Příklad

Zaměstnanec obdrží pozvánku na mezinárodní konference. Organizace budou mít k pokrytí cestovních výdajů. Zaměstnanec požaduje jeho správce-li se zúčastnit konference. Vedoucí otevře rychle náklady řízení mobilní pracovní prostor na jeho mobilní telefon, chcete-li zjistit, zda má rozpočet pro zaměstnance k účasti na konferenci.

### <a name="data-security"></a>Zabezpečení dat

Data nákladů na řízení pracovního prostoru je zabezpečena pomocí pověření uživatele. Vedoucí centra nákladů je povoleno pouze zobrazit data pro své nákladové středisko. Úroveň zabezpečení přístupu jsou spravovány v modulu Nákladové účetnictví. Účetní náklady definovat náklady řízení konfigurace mobilního pracovního prostoru v modulu Nákladové účetnictví. Po publikování Centrum služeb Microsoft Dynamics 365 pro provoz aplikace je k dispozici v 365 Dynamics pro mobilní aplikace operace. Tím zajistíte, že všechny náklady center správce v organizaci Prohlédněte data ve stejném formátu.

### <a name="actions-views-and-links"></a>Akce, zobrazení a odkazy

Náklady řízení mobilní pracovní prostor pro Dynamics 365 pro operace app nabízí následující akce, zobrazení a propojení:

-   Akce 
    -   Vyberte **konfigurace** vybrat rozložení.
    -   Vyberte **nákladů objektů** vybrat nákladová střediska, na kterých chcete filtrovat data. **Poznámka:** se zobrazí v seznamu přístup udělen v modulu Nákladové účetnictví.

<!-- -->

-   Podle vybraného v seznamu **akcí** a co je nakonfigurován v modulu Nákladové účetnictví, můžete zobrazit následující informace v kartách. Všimněte si, že částka je zobrazena ve stejném formátu: % skutečné, rozpočet, odchylka a rozptyl. 
    -   Skutečnost a rozpočet (aktuální období)
    -   Skutečnost a revidovaný rozpočet (aktuální období)
    -   Skutečnost a rozpočet (předchozí období)
    -   Skutečnost a revidovaný rozpočet (předchozí období)
    -   Skutečnost a rozpočet (rok do dneška)
    -   Skutečnost a revidovaný rozpočet (rok do dneška)

<!-- -->

-   Odkazy
    -   Podrobnosti pro aktuální období.
    -   Údaje za předchozí období.
    -   Podrobnosti o rok do data.

Když vyberete jeden z odkazů, zobrazí se karta jeden element nákladů. Částka v kartách se zobrazí v následujícím formátu: odchylka skutečné, rozpočet, rozpočet, rozpočet odchylka %, revidovaný rozpočet, revidovaný rozpočet odchylka a % odchylky revidovaný rozpočet.  [![řízení nákladů](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Začínáme
Tento postup, abyste mohli začít používat mobilní aplikace řízení nákladů v mobilním zařízení.

1.  V úložišti mobilní aplikace stáhnout a nainstalovat 365 Microsoft Dynamics pro operace app.
2.  Spuštění aplikace v zařízení.
3.  Zadejte adresu URL aplikace Dynamics 365.
4.  Zadejte přihlášení do společnosti. Například zadejte **USMF**.
5.  Při prvním přihlášení, budete vyzváni pro uživatelské jméno a heslo pro vaše 365 Microsoft Dynamics pro účet operací. Zadejte svá pověření. Po přihlášení, zobrazí se dostupné pracovní prostory pro vaši firmu.

Zobrazení pracovní plochy na mobilní aplikace, musíte nejprve publikovat požadované pracovní prostory do 365 Dynamics pro operace app.

1.  Spusťte Dynamics 365 pro operace.
2.  Přejít na **Správa systému**&gt;**nastavení**&gt;**parametry systému**.
3.  Vyberte **Správa mobilní aplikace**.
4.  Vyberte pracovní prostor ** náklady řízení ** publikovat na mobilní platformy.
5.  Vyberte **publikovat pracovního prostoru**.
6.  Aktualizujte zařízení zobrazit publikované pracovní prostory.

## <a name="view-the-performance-of-your-cost-center"></a>Zobrazení výkonu nákladového střediska
1.  V mobilním zařízení, vyberte **nákladů řízení** prostoru.
2.  Vyberte **nákladů řízení objektu**.
3.  Klepněte na tlačítko **akcí**.
4.  Klepněte na tlačítko **Select configuration** vyberte náklady řízení rozložení.
5.  Click **Done**.
6.  Klepněte na tlačítko **akcí**.
7.  Klepněte na tlačítko **vyberte objekt** vyberte nákladová střediska, ke kterým vám byl udělen přístup.
8.  Click **Done**.
9.  Zobrazení celkového výkonu nákladového střediska.
10. Klepněte na tlačítko **podrobnosti pro aktuální období**.
11. Zobrazení výkonu jednotlivých nákladových položek.
12. Můžete také hledat konkrétní nákladových položek.



